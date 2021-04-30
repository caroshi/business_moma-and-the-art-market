# MoMA and the Art Market -- What's Popular at Auction and Finding It in MoMA's Collection

Caroline Shi

## Abstract
The purpose of this project is to deliver a well-scoped project proposal to MoMA and present some preliminary data analysis on their collection. In particular, in correlation with current art market data, determine what parts of their collection will sell well at auction and what is the best way to recoup financial losses incurred due to COVID-19. 

## Design
The Art Newspaper reports that museums saw a vistor drop of 77% worldwide; MoMa saw a drop of 65% to 706,000 visitors for 2020. Visitorship is still on the decline and maintenance costs are on the rise. With a $45 million budget cut, layoffs, and exhibition cuts, MoMA would like to explore the option of selling some selections from their collection. Looking at their collection of almost 200,000 works, they would like to know what is the best way to recoup losses and what will sell well at auction. 

By better understanding patterns of the art market as reflected in MoMA's collection, they can make a better informed decision about what to sell and what not to sell. While I am presenting some preliminary EDA about the art market and MoMA's collection, I ultimately would like to build a predictive model that will accurately estimate how much MoMA's holdings will sell for at auction. If successful, MoMA will ideally be able to sell a work, or works, of art for its maximum potential price. As a result, the annual budget will be fuller, exhibitions can be organized without restrictive budgets, and no more layoffs will have to occur. 

With all said, there are some risks and assumptions that come along with this project proposal. Often the price of an artwork can be driven up exponentially at auction due to the competitive nature of bidding. How do we account for that in our model? How do we predict the price of artwork when it is something that hinges on human interest and subjective taste? The art market plays hot and cold; an artist that might be a hot commodity now might be forgotten in a few years. The smart choice in picking a piece to go to auction might be selecting an artist with provenance and substantial auction history. 

## Data
I scraped and compiled 4 datasets: two pertaining to MoMA's artworks and artists and the other two to the most expensive works sold at auction and total amount of money made at auction per artist for 2017-19. In regards to MoMA's datasets, I filtered out and only looked at their paintings and sculptures holdings as that is what typically sells for the most amount of money at auction. 

## Algorithms
* _Importing and Cleaning Data_
	* Used BeautifulSoup to scrap 6 tables from Artprice.com pertaining to art auction data and merged them together in Python
	* Looked for duplicates, missing values, dropped unnecessary columns
	* Made sure all artist names, dates were consistent across the board for easy data visualization and analysis

* _Analyzing Data_
	* Created pivot tables and grouped data into relevant tables in Google Sheets
	* Looked for patterns or meaningful ways to analyze my data:
		* Grouping MoMA's collection by artist, acquistion year, type of medium, nationality, gender
		* Grouping art auction data set by auction house, artist
		* Filtering art auction data by # of lots sold, total amount of money generated at auction, top expensive work sold
		
* _Visualizing Data_
	* Used Tableau to create a series of visualizations based on my pivot tables and data analysis

## Tools
* BeautifulSoup and Requests for web scraping and wrangling
* Numpy and Pandas for data cleaning and manipulation
* Google Sheets for data analysis
* Tableau for plotting and visualization
* Statsmodels and Scikit-learn for some very rudimentary modelling and analysis

## Insights
Based on my preliminary data analysis, I focused on a handful of artists that MoMA had a larger amount of paintings and sculptures by. There seems to be a relationship between the number of lots sold at auction, unsold rate at auction, and total artist turnover that indicated whether or not an artist would sell at a high price and whether or not they would be a guaranteed sale. 

Looking at Rothko's works, the rarity of his lots appearing at auction due to the lower volume of work produced during his career is reflected in his low unsold rate. Perhaps it would be a good idea to focus on his work when my model is complete. On the other hand, Picasso proves to be a more complex example of whether or not he is a good market sell. Due to his enormous breadth of work, there is an abnormally large amount of his work available as he accounts for $1.5 billion of the art market for the past three years. This also accounts for a higher unsold rate. When delving deeper into his work, one can see how a seven decade career can draw significant difference in the demand for his work -- his earlier Rose period works, a brief two year period, is more sought after due to its rarity while his Cubism and Surrealism work seen later in his career does not garner nine digit prices. While a model is feasible, I need to do more research in how to encompass all the nuances of an artist and their oeuvre as features. 