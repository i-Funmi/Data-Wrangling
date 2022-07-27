# Data-Wrangling
Most data in the real world hardly come clean and to bring out meaningful insights from data, the data needs to be clean. To get a data clean, some wrangling processes need to be carried out on the data. In this project, different wrangling processes would be carried out using Python's Libraries. The project involves querying data from different data sources, cleaning and documenting the processes involved in each step, then bringing out meaningful insights from the data and communicating the insights using visualzations.
## Description:
The dataset to be wrangled, analyzed and visualized is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs.
WeRateDogsis a Twitter account that rates people's dogs with humorous comments about the dog. These ratings usually have a denominator of 10. The numerators though are almost always greater than 10. 11/10, 12/10, 13/10, etc.
In this project, the following datasets would be worked with: 
1. Enhanced Twitter Archive: 
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, though not everything. The archive did contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make the Twitter archive "enhanced" (according to Udacity's instructor). Of the 5000+ tweets, tweets with ratings only have been filtered for (there were 2356).

2. Additional Data via the Twitter API:
Of the columns omitted in the above dataset, retweet counts and favorite counts were two of the notable columns. These additional data would hence be gathered using Twitter's API.

3. Image Prediction File:
Every image in the WeRateDogs Twitter archive were ran through a neural network that can classify breeds of dogs by Udacity. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets could have up to four images).
The columns in the text files are:
* tweet_id which was the last part of the tweet URL after "status/" → [https://twitter.com/dog_rates/status/889531135344209921](https://twitter.com/dog_rates/status/889531135344209921)
* p1 was the algorithm's #1 prediction for the image in the tweet → **golden retriever**
* p1_conf meant how confident the algorithm was in its #1 prediction → **95%**
* p1_dog was whether or not the #1 prediction was a breed of dog → **TRUE**
* p2 was the algorithm's second most likely prediction → **Labrador retriever**
* p2_conf meant how confident the algorithm was in its #2 prediction → **1%**
* p2_dog meant whether or not the #2 prediction was a breed of dog → **TRUE**
etc.
### Section 1: Gathering Data
In this section, the three pieces of data as mentioned above were gathered using different methods. The first file 'twitter_archive_enhanced.csv' was provided at hand and was read into dataframe using `pandas.read_csv`.
The second file 'image_predictions.tsv' was read from Udacity's server using the `Requests` Library.
The third file 'tweet_json.txt' was gathered through querying Twitter API with the use of Python's `Tweepy Library`. Each tweet set of JSON (retweet counts and favorite counts) was then read and saved in the file.
### Section 2: Assessing Data
After gathering all the three pieces of data, the data were then assessed visually (using Microsoft Excel) and programmatically (using Pandas' functions and methods). Through the assessments, issues detected about the data were dutifully documented; grouping them into quality issues and tidiness issues depending on the rule of clean data the issue violated.
### Section 3: Cleaning Data
After assessing the data and documenting the issues, the dataset was then copied before cleaning started for easy future referencing. Then, using the `Define-Code-Test` method, the issues detected were cleaned; where 'Define' meant defining the issue detected, 'Code' meant writing codes to solve the detected issue and 'Test' meant testing to ensure the issue has been solved accordingly.
The gathering, assessing and cleaning acts were then saved in the `wrangle_act.ipynb` file attached, while the cleaned dataset was also saved('twitter_archive_master.csv') in preparation for analyses and visualizations.
### Section 4: Analyzing and Visualizing Data
In this section, the final part of the project was carried out- analyzing and visualizing the cleaned data. Here, clear insights were derived from the data and the insights dutifully communicated and explained with the aid of visuals using simple Python's Matplotlib and Seaborn's functions.
### Section 5: Reporting
Reports about the wrangling processes were then reported, separating the reports into 'wrangling report' entailing summaries of the wrangling processes, and 'visualization report'- entailing insights gotten from the data and visualizations used to communicate the insights. The reports `wrangle_report.html`; the wrangling report and `act_report.html`; the insights report were attached.
### Conclusion:
Wrangling processes- gathering, assessing, cleaning, analyzing and visualizing are processes carried out in order to derive meanings from data. 

Data gathered in any form can be tweaked to give out meaningful insights through the help of DATA WRANGLING.
