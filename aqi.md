## Air Quality Advertising

![](aqi_gif.gif)

#### Summary:
This algorithm was built for a small business for the purpose of finding low air quality zip codes in the US for targeted advertising. The algorithm scrapes the airnow.gov website, maps low air quality locations to their corresponding zip codes and returns the zip codes, state, city and AQI values in a csv file. [VIEW CODE HERE](https://github.com/tesseract314/tesseract314.github.io/blob/master/AQI_Zip_Codes.ipynb)

#### Technical Overview:
The goal of this project was to retrieve regions in the US with low air quality and convert those regions to zip codes. This algorithm was used by a polution mask company to help with targeted advertising. Some code and data was redacted to not give away the client's competitive advantage.

Pandas' read_html function was used to pull the air quality data into a dataframe. The resulting dataframe was messy and required a bit of logic to match each region to the correct air quality. There was also an issue reading zip codes from an Excel spreadsheet. When a number in an Excel column starts with zero, Excel truncates the zero. And, because many zip codes legitimately start with zero, the algorithm was missing those zip codes at first. I simply had to change the format within the Excel file to correct the issue.

As of now, the script runs a little slow. To speed things up, I will use thread pools for the website requests.

#### Technology Used:
- Requests
- Numpy
- Pandas
- Datetime
- Excel
