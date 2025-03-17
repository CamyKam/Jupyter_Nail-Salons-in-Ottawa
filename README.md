# Evaluating Top Nail Salons Near Me in Ottawa
For the R-Ladies' 2025 IWD Code Challenge, the main theme was to find a passion project to round out one's portfolio and develop their professional story. Upon review of my Github and previous projects completed in the past, I decided to use this challenge to learn how to present visuals with the Python language. I primarily use Excel and Power BI as a Business/Data Analyst for presenting visuals, and although I have experience with Python, this was my first time learning to work with various Python libraries to present graphs.

**All the information below can also be found in the NailSalonsOttawa.ipynb file where you can follow along with my code. Otherwise this document will just show the graphical results.**

Living downtown in the city of Ottawa, I find a lot of nail salons pop up around my neighbourhood which got me wondering, 'just how many are there in my area and which ones are the best based on ratings and reviews?'
![nailSalon1](https://github.com/user-attachments/assets/86cc5875-a580-4596-92af-bc1b094d7b9c)

## Gathering the Data
To find the best nail salon, I could have opened up and checked for all nail salons in my area on Google maps, but that would have involved scrolling through countless businesses. I needed an easier way to gather all the data in one place for data analysis and so I looked for tools to assist.

For this personal project, I ended up using this open sourced tool to help me find all nail salons near me in Ottawa on Google Maps and exported the information into an .xlsx file: https://github.com/omkarcloud/google-maps-scraper/tree/master

This file contained information such as the number of reviews each nail salon had, the ratings, the opening hours, location, etc. After having all the data conveniently in a file, it was time to start working on examining the data.

## Examining the Data
I imported the main libraries I needed for this project which were the popular and common 'numpy', 'pandas', and 'matplotlib' libraries for graphs. After reading my excel file I took a look to see what the data and columns were like:
![data_info](https://github.com/user-attachments/assets/cfaaa67e-35b1-4ee6-b601-70ba51beb493)

The data had 28 columns, though I will only require some of them and will select the ones I want to look at throughout this project.

## Examining the Data
The first information I wanted to find out was which nail salons in Ottawa had the greatest number of reviews in total. I only wanted to see the top 5, so I filtered to only have the top highest review numbers and set up my horizontal bar chart.

In Ottawa, Rose & Rebel Salon have the highest number of reviews at 1053, with the rest being above 500! However, this doesn't paint the full picture yet. Upon external research, Rose & Rebel have been around for 5-6 years and are primarily a hair salon who ALSO provide nail services. This also applies to #2: Flawless Hair Salon. The rest of the top 5 provide other spa related services which means that despite the high number of reviews, **not all those reviews are related directly to nail services.**

Seeing as how this project aimed to look at the best 'nail salons' I had to keep this information in mind when searching for the best 'nail' salons.

![horizontal_graph](https://github.com/user-attachments/assets/9b872232-060d-429d-a15c-3ed9f574803f)

## Examining Salons with the Highest Star Rating
The next step after looking at the greatest number of reviews was to see which nail salons had the highest star rating on Google. To look at the relationship between number of reviews versus ratings, I first plotted a scatterplot graph.

The graph below indicates that most Google ratings of nail salons near me are 4 stars and higher. There are quite a fair amount around 4.5 stars and approximately 6 salons have the highest rating of 5 stars. 
![Scatterplot](https://github.com/user-attachments/assets/d3ebd0c6-54f2-459a-ad53-a01bdc987718)


Now looking back at the top 5 salons with highest # of reviews, I wanted to see what their ratings were and which neighbourhood/city ward they were located in. Rose & Rebel Salon had the highest reviews and also had very high ratings of 4.8 stars, which is the same as Moony Beauty Nails and Spa (which ranked 3rd in number of reviews).


![top_salon_numofReviews](https://github.com/user-attachments/assets/09077c9f-8480-42b3-8c85-3cf410c1c044)

Now what about those top star salons that we saw from the scatterplot? We'll be taking a look at them below. The top 'rated' salons have 4.9 or 5 stars, but you can see that 11/15 (73.33%) of these salons have less than a hundred reviews, with LJ Nails only having 2 in total! It is very likely they are new nail salons that may have opened up recently and haven't had a lot of customers yet.

By looking at the data so far, it seems that relying only on star ratings may not provide a big enough customer experience pool for me to judge how good the nail salon is. On the other hand, if I only look at the volume of reviews I can't tell how many reviews are related to nail services or even if those reviews may be negative or positive.

The information so far has provided me good starting points however, on nail salons I can start looking into for more details.

![top_salon_ratings](https://github.com/user-attachments/assets/92d9cdcb-917d-4c38-8cf1-aa777be1c6ff)

## Location of the Nail Salons
Apart from reviews and ratings, I wanted to see which areas the nail salons in my dataset were actually located in. The dataset contained Google maps information on the latitude and longitude points, address, and city ward of the salons to aide in my analysis. Firstly, I went with a pie graph to show the breakdown of the locations of the salons by city ward.

![pieChart](https://github.com/user-attachments/assets/6dca9fe1-b1e1-4a57-9f42-9f93e432060f)

Then, to visualize the locations of the salons in more graphic details I used a 3rd party library to plot the locations on a map. To interact with the map, please view it through this link and scroll down: https://nbviewer.org/github/CamyKam/Jupyter_Nail-Salons-in-Ottawa/blob/main/NailSalonsOttawa.ipynb

![map](https://github.com/user-attachments/assets/4ca62328-9a75-4761-b326-77d196e16577)

Since I live in downtown Ottawa, the breakdown of locations matched my assumptions on how the data would look when I scraped it; with a higher cluster of points around Centertown and Vanier in Ottawa, and 23.3% (close to 1/4) of the 109 salons in my dataset being in the area of Byward Market- Parliament.

It was interesting to see just how many nail salons were so close to home! I am truly spoiled for choices in this regard.

## Salon Closed Days

Now that I was aware of the number of salons close to me, I wanted to see how many were closed on Sundays or other days of the week. As I usually have a busy week, Sunday is my relaxation day and if I wanted to get my nails done that day, how many and which nail salons would actually be opened?

![salonClosedDaysBarChart](https://github.com/user-attachments/assets/e7547922-e704-4997-9b18-3f4dfe30d4cb)

Looking at the bar graph, it seems like 33 (30%) of the Nail Salons would be closed on Sunday, but 55 (50%) of the nail salons were actually opened every day of the week! So if I wanted to have my nails done on Sunday, I would not need to worry about the lack of remaining options of where to go.

Finally, to end my data analysis I wanted to take a look at the list of the salons that were opened 7 days a week. Here's hoping the owners and employees take enough breaks!

![salonsOpened24_7_1](https://github.com/user-attachments/assets/32484dd3-ccdb-479e-a38a-7c2ebaf83b87)
![salonsOpened24_7_2](https://github.com/user-attachments/assets/3b8c91e4-efbf-49cd-a6d3-b8a3a8e12f91)

## Conclusions
Trying to determine the best nail salons close to my home was not simply a matter of finding the highest number of reviews for a business or the top rated ones. As I've uncovered, nail salon businesses with the highest volume of reviews also offer other types of services, making it difficult to determine how many positive or negative reviews were related to just nail services alone.

As for ratings, most nail salons scored 4 stars or above but most of the '5 star' businesses had less than 100 customer reviews, making it difficult to know if they were truly better than salons that may have scored 4.8 for example, but with 500+ reviews. A next step for this project would be to start evaluating the Google comments for these businesses to weigh the positive/negative reviews and to research how long some of these businesses have been operating for, as that would influence the number of reviews. However, that is beyond the current scope of this project.

The results I've seen so far provide a good enough starting point for me with a list of businesses I would look into. I would personally examine the salons with greatest number of reviews first and then research for futher details such as the type of nail services provided and pricing.

Overall this project was a good way for me to learn and present Python graphs and visuals while exploring a fun topic. Now I can plan for my next manicure and pedicure.
