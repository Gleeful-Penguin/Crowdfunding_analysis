# Analysis of Kickstarter projects
Before introducing this project, I want to explain two terms that might be new to you:

**Crowdfunding**: funding a project by raising money from a large number of people. (AKA crowd)

**Kickstarter**: platform which showcases projects people can back up. (Mitigating the process)

I analyzed data containing 370,000 projects and found that **project target goal**, **category** and **launch date** impacts their success.

## Initial idea
It is clear to everyone that some characteristics have a direct impact on the success of a project. For example, successful projects usually:
 1. Solve a problem for the buyer, or stimulate a great desire (want) in them to purchase
 2. Have a great explaination and presentation of the project
 3. Showcase the story behind the creation, making people care
 4. Explain how the funds will be spent, building trust with the backers

All of those things determine how successful a project is to reach its goal, however, those factors also can't be placed in a dataset and be analyzed.
Focusing strictly on the trends like the project target goal, category, launch date does not take into consideration the abovementioned factors and could have a big margin of error.

## Dataset
I used a dataset provided by Kaggle: https://www.kaggle.com/kemical/kickstarter-projects. More specifically the table containing the latest data (ks-projects-201801.csv)

## Database
I mainly worked with the dataset as a whole, however, to gather more insights I split the dataset based on categories and states of the projects

## Workflow

I started by cleaning the data list:

1.1 Exclude live, suspended and undefined statuses

1.2 Add name length column

1.3 Add fundraising period

1.4 Drop usd pledged column

1.5 Rename usd pledged_real colimn

1.6 Add avg money per backer column

1.7 Add percentage funded

1.8 Fix contry values

1.9 Fix order of columns

Then I performed quick analysis:

2.0 General correlation analysis

2.1 (turn "success" to 1 and "fail" + "cancelled" to 0)

2.2 Create new Dataframes with only "failed", "successful", "cancelled" states

2.3 Do individual corr

2.4 Group by main_category % of success = ?

2.5 Compare project duration with project success

2.6 Is there seasonal effect on amount of money spent in Kickstarter

2.7 What are the most used words in successful projects

2.8 Funding goal negatively corr with campaign success

2.9 Length of the campaign title negatively corr with campaign success

Finally, I used Tableau to observe and visualize the data

## Organization

Day 1-2 - Choosing a topic, cleaning and understanding the data.

Day 3-4 - Analyzing the data, testing various visualizations, hypothesis, correlations, and behaviours.

Day 4-5 - Summarizing valuable insights, simplifying the findings and prepering my slides. Practise and Present.

Weekend - Finalized the documentation.

## File structure:
The repo contains the original dataset, EDA notebook and a folder with the split and cleaned dataset for Tableau visualization and analysis.

## Links
Repository: https://github.com/Gleeful-Penguin/Crowdfunding_analysis

Slides: https://docs.google.com/presentation/d/1BGfrtauKcnzUcGKj_j0iUJkCf0AgWxBNdtxvbylL4Fw/edit?usp=sharing

Tableau: https://public.tableau.com/profile/kostadin.mitkov#!/vizhome/Kickstater-EDA/Sheet273
