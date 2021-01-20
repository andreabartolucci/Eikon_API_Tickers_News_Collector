# Eikon_API_Tickers_News_Collector
This repository contains the two scripts that make possible to collect from Eikon the news headlines for a list of tickers input and a specific time windows

The scripts consists in a wrapper for the Eikon API. The main advantage of these two scripts is to easily retrieve the text of news related to a list of Tickers selected by the user and a time windows. The Eikon API at each request must have a ticker and a date time range. There is a limit on the number of news retrieved on each request (usually 100), the scripts automatically solve the problem by bisecting the date time range of the single API request untill the news collected in the response are less than the limit (100).

main_download_storyID_auto.ipynb is used to retrieve the storyID and save them in your local folder. Story ID are just identification number, they do not contain the actual news text.

main_download_news_text.ipynb is used to retrieve the news text of the news which storyIDs have been previously dowloaded.
The scrip save the news in a csv file

The ticker list can be passed as a csv or hardcoed in the script main_download_storyID_auto.ipynb itslef.

More comment and instructions are present within the lines of code of the script.

In order to use the script, generally according to your Eikon license, you have to authenticate on Eikon passing a key with the API.
The key is read by main_download_storyID_auto.ipynb or it can be hardcoded.


Some reference about Python Eikon API can be found here (you have to register for free therefore I cannot distribute them here but trust me, they are really clear, so just register and have a look at them):
https://pypi.org/project/eikon/
https://www.refinitiv.com/en/products/eikon-trading-software/eikon-app-api-innovation/eikon-data-api
https://developers.refinitiv.com/en/api-catalog/eikon/eikon-data-api/documentation
https://github.com/Refinitiv-API-Samples/Tutorial.EikonDAPI.Python.BankingBalance
