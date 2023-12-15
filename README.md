# asueppel.github.io

# Final Project Report
Analysis of Specific Goals:
1. I was able to identify a simple trading algorithm based on various price momentum over varying intervals of time. There were helpful videos to follow along with and guide me through the implementation process.
2. I successfully implemented the trading strategy in Python. Python was a great language to implement the algorithm in, as it is especially adept at data processing.
3. The most difficult aspect of the project was the importation of data. The initial source of data (IEX) for stock price information ended up shutting down their sandbox mode. This meant I had to find another data source. I identified a service called Polygon. While they did not offer the breadth of data available through IEX, it provided the information I needed for a cheap price. It took a while to learn a new API standard, but Polygon provides in depth documentation, which helped greatly. Once I had established the API calls, I needed to convert the data into a usable format. I used a pandas DataFrame, which made handle the data very straightforward.
4. I used Anaconda Navigator, which made importing the necessary libraries very easy. I had no issues with the libraries.
5. I was able to setup the algorithm so that the last column of the DataFrame provided the recommended number of shares to buy for each stock.
6. I struggled with this aspect. I was able to setup a simple back testing system. I calculated the recommended buy signals for the period November 2021 to November 2022. I then compared the performance of this recommended portfolio of stocks to the overall average return of stocks in the S&P 500 for the period November 2022 to November 2023. The recommended basket of stocks underperformed the S&P 500 as a whole, which demonstrates why it is so difficult to consistently beat the market. For proper evaluation of the trading strategy, I would need to setup a system to test the recommended portfolio to the overall performance of the S&P 500 over many varying periods of time.

Analysis of Risks:
1. As the trading algorithm was simple, my finance domain knowledge was more than enough to complete this project.
2. As stated above, Anaconda Navigator made it extremely easy to import the required libraries for this project.
3. Finding the required data proved to be more challenging than I expected for the reasons explained above. However, once I identified an alternative data source, importing the data was straightforward.
4. The data was pulled from a service specifically designed for uses like mine, so there was very little data cleaning required.

Final Project Assessment:
1. I was able to import and clean the necessary data for use in my trading algorithm.
2. My trading algorithm provided trading signals in the form of number of shares to buy of each stock in our end basket.
3. While not robust, I was able to setup a simple back testing system.

Overall, I am pleased with the outcome of my project. There were some hurdles along the way but I was able to overcome them and produce a working trading algorithm. This project sharpened my Python skills, API knowledge, and data processing skills.

GitHub Link: https://github.com/asueppel/CSPB3112_Project
Relevant Files: https://github.com/asueppel/CSPB3112_Project/blob/main/quantitative_momentum_strategy.ipynb; https://github.com/asueppel/CSPB3112_Project/blob/main/backtesting.ipynb


# Week 15 Status Update
1. This past week was spent finalizing the trading algorithm, working out any kinks on the API calls, and creating a simple back testing system to evaluate the performance of the trading algorithm.
2. N/A
3. As I looped through the S&P 500 tickers, I found that certain stocks were not on the index a year ago. This caused an error to be thrown and I had to manually remove those tickers. (Same issue as last week)
4. I was able to set aside quite a bit of time over the last week to finalize everything for this project. I feel pretty good with the final output.

# Week 14 Status Update
1. This past week was focused on creating and populating the dataframe via a loop, so that I did not need to manually enter each S&P 500 stock. Setting up the loop was slightly tedious, as I had to do two API calls each loop, which is a slow process.
2. This coming week, I will be focused on writing the actual quantitative momentum algorithm.
3. As I looped through the S&P 500 tickers, I found that certain stocks were not on the index a year ago. This caused an error to be thrown and I had to manually remove those tickers.
4. This past week, I would only work on the project for bits at a time, which meant when I came back to the project I had to remember where I had left off. This weekend I will set aside a large chunk of time to finish this project.

# Week 13 Status Update
No update

# Week 12 Status Update
1. This past week was spent getting acquainted with the API of the new datasource I will use for stock market data (Polygon). The amount of data available through Polygon is significantly less than through IEX but it will be enough for this project. I also was able to pull the required data into a Pandas data frame for a single stock (AAPL).
2. This coming week, I will create a loop to automatically loop through the stocks in the S&P 500 and append the needed data into a Pandas data frame.
3. Fortunately this week did not involve any impediments. I ironed those out last week by finding an alternative data source and getting acquainted with the API.
4. I have been particularly busy with work and my other class. This coming week, I should be able to focus on this project for significant chunks of time.

# Week 11 Status Update
1. This past week was mostly focused on attempting to troubleshoot access to IEX. I then focused on finding an alternative (Polygon) and familiarizing myself with the API. I was able to successfully pull the closing price for various stocks.
2. This coming week, I will continue to familiarize myself with the API and update my current code to fit the data structure of Polygon. I will work to consolidate the data into a dataframe for easy manipulation.
3. Unfortunately, I encountered additional hurdles this week as it relates to my initial data source. IEX removed their "sandbox" mode and access to their real data is price prohibitive. I found an alternative called Polygon, that should give me access to the data I need for free.
4. This week reinforced the importance of a back up plan. I am once again glad the "sandbox" mode was removed now, rather than at the very end of the semester. Unfortunately, there was not anything I could do about the changes made by IEX but it created a learning opportunity for how to adjust code on the fly.

# Week 10 Status Update
No update

# Week 09 Status Update
1. This week I resolved the API calls and imported the full JSON data into a data frame. This will be used as the basis for data manipulation and analysis moving forward.
2. Next week I will begin building the actual algorithm to digest the data and produce the signals. I planned to get to that this week but did not get as far as I would have hoped.
3. The only impediment this week was a time crunch. I did not encounter any technical hurdles, which was refreshing after last week.
4. This past week reinforced the importance of time management. I would have liked to have gotten farther in building the algorithm. I will need to catchup over the weekend.

# Mid-Semester Project Report
Thus far, I am feeling pretty confident I will be able to build something close to what I initially set out to. I may have to make the trading algorithm simpler than my original idea due to some hurdles along the way. For example, I had to spend a substantial amount of time over the last week reestablishing API calls because a previous API "sandbox mode" was discontinued on 10/17/2023. This set me back a bit but I believe I have found the solution. I also have my environment set up in the way needed, in terms of libraries. With these two items (API and local environment) solved, I should be able to focus the remainder of the semester on learning about various algorithmic trading strategies and tweaking them for my own use.

# Week 08 Status Update
1. This past week was very frustrating. I discovered that the "sandbox mode" I had been using at the beginning of my project to access stock market data has been discontinued. This meant I had to setup an actual account and reconfigure my API calls, instead of making "fake" calls to the sandbox data. However, I got the API calls working again and have added the JSON data to a Pandas DataFrame.
2. This next week I will do batch API calls, so that I can import data on every stock in the S&P 500, rather than adding stocks information manually. Once the DataFrame is fully populated this way, I will start making calculations for the basic algorithms.
3. In addition to the discontinued sandbox mode mentioned above, I also spent some time setting up my environment on my local machine. Initially I had been using the CU JupyterLab but ran into some hurdles with libraries. I have my environment setup in a way now that seems to be fully functional for this project.
4. This past week was really important. There will always be unexpected challenges and this week was a major one. However, I worked through it using IEX's documentation and some other online resources.

# Week 07 Status Update
No update

# Week 06 Status Update
1. This past week I continued to work through the educational material I have found online. This primarily consisted of getting familiar with API calls to IEX cloud, where I will be pulling stock data from to use within my trading algorithms. IEX is stock exchange founded in 2012. I will likely be using the free "sandbox" version of the IEX cloud, as they charge for actual data. For the purpose of this project, dated or random data will be okay.
2. This next week will be focused on becoming more familiar with API calls to IEX, as mastering these calls is integral to the overall success of the project. I will also begin building my pandas data frame to store the information from the numerous API calls I will be required to do.
3. I have had issues importing some libraries (e.g., xlsxwriter) that I do not need right now but will likely need as I proceed deeper into this project. At some point over the next few weeks, I will need to spend time getting all of these libraries and dependencies setup on my local machine.
4. This past week, I had a clearer focus on what aspect of the learning process I want to focus (API calls). This helped me to use my time more efficiently. I will continue to structure my weeks like this, with a certain educational area as the focus of the week, until I have all the necessary tools in place.

# Week 05 Status Update
1. I continued to work my way through the educational materials I found for creating a trading algorithm in Python.
2. Next week I will continue to go through these materials to create the basis of knowledge I need to implement my own algorithm.
3. To date, there have not been any impediments.
4. Figuring out how to spruce up my personal website is taking longer than I originally anticipated. I will likely need to set aside more time for this aspect of the project.

# Week 04 Status Update
1. This past week I finalized my project proposal (below) and began to setup my coding environment.
2. Next week I will continue to setup the coding environment (download all the dependencies and libraries) and get my personal website looking more professional.
3. To date, there have not been any impediments in my way.
4. Taking a note from Lindsay Kriz's post, it would be good for me to setup a formalized schedule for each week to ensure I stay on track.

# Week 03 Status Update
1. Last week I mainly focused on gathering resources that will help me set the educational foundation for my project, which is to build a simple algorithmic trading model.
https://www.youtube.com/watch?v=xfzGZB4HhEE <br>
https://quantra.quantinsti.com/course/python-for-trading?utm_source=harshit_tyagi&utm_medium=affiliate&utm_campaign=python_finance_article <br>
https://www.freecodecamp.org/news/how-to-get-started-with-algorithmic-trading-in-python/ <br>
2. This week I began going through the materials listed above and researching what to base the algorithm on (e.g., moving averages).
3. I have not hit any impediments as of yet.
4. I did not focus on any coding this past week. Next week I will begin to build up the code base, such as getting the environment set up and importing data.

# Project Proposal
Vision Statement: I have worked in finance for my entire working career. Finance has becoming increasing reliant on big data and being able to process the data to gain actionable business insights. My project will focus on building a simple trading algorithm, which will require importing historical data, processing the data, and extracting trading signals from the processed data. This project will develop skills in sourcing and processing data, specifically as it relates to the financial world. <br><br>

Motivation Statement: Beyond just working in finance, I have a particular interest in economics, as it was my original area of study. I am fascinated how prices in the stock market theoretically capture all publicly available information related to that stock. For example, supply chain disruptions or a drop in the price of silicon could potentially have a very meaningful impact on the price movement of Apple stock. While the algorithm I develop will not be advanced enough to quantify and process these types of information, even a simple trading algorithm will expand my knowledge as to how modern algorithmic trading models are designed and applied.

Specific Goals: Given the limited time allocated to this project (45 hours), my specific and measurable goals are as follows.<br>
1. Identify a simple algorithm based on either technical analysis (e.g., using stock price and trading volume data) or a select input variables (e.g., high yield interest rates and a chosen stock market index).<br>
2. Implement the chosen trading strategy in Python.
3. Be able to import and scrub data from external sources for processing by the implemented algorithm.
4. Be able to properly setup the Python environment and import the necessary libraries for the algorithm to function and potentially visualize the output.
5. Output trading signals to act on (trading actions).
6. Be able to back test the trading strategy from historical data.

Risks:
1. While I have a finance background, I do not have experience in building a trading algorithm.
2. I have experience in Python; however, the project may require the use of libraries or aspects of Python I do not have experience with.
3. It may be difficult to find the data I need to analyze for free.
4. The data needed for the project may be available but require a lot of cleaning for it to be useful for this project.

Mitigation Strategy: I did a fair amount of research on developing trading algorithms when choosing a topic for this project. There are a lot of resources in this area, specifically for using Python to create trading algorithms. For access to data, Kaggle has been a tremendous resource for free data that I have used in the past.


Project Assessment:
1. I am able to import and clean the necessary data.
2. The trading algorithm successfully processes the data and outputs actionable trading signals.
3. I am able to back test the performance of the algorithm using historical data.
