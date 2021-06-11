# Reddit_Sentiment_Trader

An algo that scans the most popular trading sub-reddits and logs the tickers mentioned in due-diligence or discussion-styled posts. As well as scanning for how many times each ticker was mentioned in a comment, it logs how popular the post was among the sub-reddit. Essentially if it makes it to the 'hot' page, regardless of the subreddit, then it will most likely be on this list.

## How is sentiment calculated?

This uses VADER (Valence Aware Dictionary for Sentiment Reasoning), which is a model used for text sentiment analysis that is sensitive to both polarity (positive/negative) and intensity (strength) of emotion. The way it works is by relying on a dictionary that maps lexical (aka word-based) features to emotion intensities -- these are known as sentiment scores. The overall sentiment score of a comment/post is achieved by summing up the intensity of each word in the text. In some ways, it's easy: words like ‘love’, ‘enjoy’, ‘happy’, ‘like’ all convey a positive sentiment. Also VADER is smart enough to understand the basic context of these words, such as “didn’t really like” as a rather negative statement. It also understands the emphasis of capitalization and punctuation, such as “I LOVED”. Phrases like “The turkey was great, but I wasn’t a huge fan of the sides” have sentiments in both polarities, which makes this kind of analysis tricky -- essentially with VADER you would analyze which part of the sentiment here is more intense. There’s still room for more fine-tuning here for forkers, but make sure to not be doing too much. There’s a similar phenomenon with trying to hard to fit existing data in stats called overfitting, and you don’t want to be doing that.


## Some stats

Note: Based only on a backtest to January 2020 (not enough data prior), so take these numbers really with a grain of salt, and take the algorithm as a fun novelty more than a reliable alpha-generator

### Annualized return of 35% (compared to 16% for the SP500)

### Max drawdown of -8.7% (aka how far it went down before coming back up -- interestingly enough, Reddit sentiment weathered COVID pretty well)

### Sharpe Ratio: 2.22

### Profit-Loss Ratio: 3.48

### Avg. Win: 0.85%

### Avg. Loss: -0.24%

