# html_challenge

Part 1: Scrape Titles and Preview Text from Mars News

The link to the website was "https://static.bc-edx.com/data/web/mars_news/index.html"

I used browser from splinter to automatically open chrome and visit the url above.

I used BaeutifulSoup to parse the html for further scraping

After inspecting the entire website, the text content was in html element div and class list_text. I used find all on these parameters to get all the text elements.

The text elements contained the title and preview. The title has element div and class content_title while preview has element div and class article_teaser_body.

Since the text element was a list, I used a for loop to access each element and used find method to get the title and preview based on  their classes. I used text and strip function to get only the text without any '/n' symbols

I created an empty list called news_article_list to which I appended the whole dictionary news_article_dict.

The keys of the this dictionary are title and preview and their values were added each time from the for loop.

----------------------------------------

Part 2: Scrape and Analyze Mars Weather Data

The link for part 2 is "https://static.bc-edx.com/data/web/mars_facts/temperature.html"

tr distinguishes the rows upon inspection of the table. Hence, to extract rows, I used find method on tr with class data-row.

Each element of the list from tr, had contents as td. Using a for loop, I extrated each item from the td and used text to get only the correspondign text.

I appended each row as a list to the row_list I created.

After putting it in a dataframe, I convrted the datatypes using astype function.

Using the max function on the column month, there are 12 months on Mars.

Using count function on the column sol, there are 1867 Martian days in the data

Using groupby and then sort values function, I plotted the bar charts. March is the coldest month while August was the hottest.

Lowest atmospheric pressure was experienced in June (month 6) and highest atmospheric pressure was measured in September.

By looking at the length of the cycles ftom the graph, there are approximately 700 days in a Martian year.




