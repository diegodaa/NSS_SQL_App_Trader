## Project Summary:

This was one of the projects I worked on as part of the Data Analytics program at NSS.

In a group of 4, we used SQL queries combine two different sets of data provided and pull the right information needed for the business scenario described below.  Excel was also used to create some charts used in the presentation. 

Some of my personal contributions to the team:
- Project planning:  vision of what info we will need for our analysis, and how to get it
- Main query to combine and format data: Set up our "main database", using naming conventions a team-member came up with, so that we were then able to easily create smaller queries to explore specific questions, as opposed to having to write complicated queries from the start every time. 
- I also had a big part in the presentation and story-telling, as I've had more industry experience presenting analytical data to different audiences.


## App Trader

You have been hired by a new company called App Trader to help them explore and gain insights from apps that are made available through the Apple App Store and Android Play Store. App Trader will serve as a broker buying rights to apps from developers then deploying and marketing them. App developers retain **all** money from users purchasing the app, and they retain _half_ of the money made from in-app advertising and in-app purchases. App Trader will be solely responsible for marketing apps they purchase rights to.  

Unfortunately, the data for Apple App Store apps and Android Play Store Apps is located in separate tables with no referential integrity.

#### 1. Loading the data
a. Launch PgAdmin and create a new database called app_trader.  

b. Right-click on the app_trader database and choose `Restore...`  

c. Use the default values under the `Restore Options` tab. 

d. In the `Filename` section, browse to the backup file `app_store_backup.backup` in the data folder of this repository.  

e. Click `Restore` to load the database.  

f. Verify that you have two tables:  
    - `app_store_apps` with 7197 rows  
    - `play_store_apps` with 10840 rows


#### 2. Assumptions
Based on research completed prior to launching App Trader as a company, you can assume the following:  

a. App Trader will purchase apps for 10,000 times the price of the app. For apps that are priced from free up to $1.00, the purchase price is $10,000.  

b. Apps earn $5000 per month on average from in-app advertising and in-app purchases _regardless_ of the price of the app.  

c. App Trader will spend an average of $1000 per month to market an app _regardless_ of the price of the app. If App Trader owns rights to the app in both stores, it can market the app for both stores for $1000 per month.  

d. For every half point that an app gains in rating, its projected lifespan increases by one year, in other words, an app with a rating of 0 can be expected to be in use for 1 year, an app with a rating of 1.0 can be expected to last 3 years, and an app with a rating of 4.0 can be expected to last 9 years. Ratings should be rounded to the nearest 0.5 to evaluate its likely longevity.  

e. App Trader would prefer to work with apps that are available in both the App Store and the Play Store since they can market both for the same $1000 per month. 

#### 3. Deliverables
a. Develop some general recommendations as to price range, genre, content rating, or anything else for apps that the company should target.  

b. Develop a Top 10 List of the apps that App Trader should buy next week for its **Memorial Day** debut.  

c. Prepare a 5-10 minute presentation for the leadership team of App Trader to inform them of your recommendations.



### All analysis work must be done in PostgreSQL, however you may export query results if you want to create charts in Excel for your presentations.