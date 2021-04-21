# Business Fundamentals Proposal

## Question:

New York's MoMa is struggling to recoup its financial losses from Covid-19. The Art Newspaper reports that museums saw a vistor drop of 77% worldwide; MoMa saw a drop of 65% to 706,000 visitors for 2020. In attempt to stay afloat as maintenance costs rise and visitorship is still on the decline, MoMa is looking into selling some art. Looking at their collection of almost 200,000 works, MoMA would like to know what should they sell and what they should retain. 

## Data:
MoMA provides 2 datasets -- one compromised of ~140,000 artworks with 21 different features and another compromised of ~15,000 artists with 5 features. These two datasets will be my primary sets where I will be completing most of my analysis and visualization. 

The main goal is determining how to balance potential profit of work, # of similar pieces of the genre/era/artist, popularity of the artist or work itself into an equation to measure "success." As there are a lot of different angles to analyze this dataset and with the wide breadth of information provided, it is important to figure our how to balance the right ratio of amount of money generated via sales/# of works sold while maintaining instutitional integrity and vistitor retention. Is it better to sell a lot of smaller works or one big blockbuster piece? Museums on average only show 2-10% of their total holdings, how will visitors even notice when that sketch by Matisse or Dali is sold when they've never seen it in the first place? While selling Van Gogh's _Starry Night_ might generate the most revenue, is it smart to let go of one of the most popular pieces in the world?

Time allowing, I would like to scrape data from Artprice.com that compiles annual lists of the most expensive pieces of art sold at auction and top artists by auction turnover (total amount of money generated at auction, total amount of works sold.) As MoMA wants to know how to maximize their profits, the addition of art market data will be extremely valuable -- we can see what is trending, what isn't, what typically sells above starting bid price, artists or mediums that have a lower unsold lot rate. Ideally, as we want to provide MoMA with a prediction, the auction results could be a train-valiation set of a model that is applied to MoMA's holdings. 

## Tools:
- Google Sheets, Python for EDA
- Tableau for data visualization
- BeautifulSoup for web scraping 

## MVP Goal:
I hope to have MoMA data cleaned with some EDA and visualizations finished as my MVP. 
If I choose to scrape an additional dataset, I hope to have that cleaned and formatted as well. 