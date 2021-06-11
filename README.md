# Reddit_Sentiment_Trader

An algo that scans the most popular trading sub-reddits and logs the tickers mentioned in due-diligence or discussion-styled posts. Instead of scanning for how many times each ticker was mentioned in a comment, it logs how popular the post was among the sub-reddit. Essentially if it makes it to the 'hot' page, regardless of the subreddit, then it will most likely be on this list.

**How is sentiment calculated?**

This uses VADER ( Valence Aware Dictionary for Sentiment Reasoning), which is a model used for text sentiment analysis that is sensitive to both polarity (positive/negative) and intensity (strength) of emotion. The way it works is by relying on a dictionary that maps lexical (aka word-based) features to emotion intensities -- these are known as sentiment scores. The overall sentiment score of a comment/post is achieved by summing up the intensity of each word in the text.In some ways, it's easy: words like ‘love’, ‘enjoy’, ‘happy’, ‘like’ all convey a positive sentiment. Also VADER is smart enough to understand the basic context of these words, such as “did not love” as a negative statement. It also understands the emphasis of capitalization and punctuation, such as “ENJOY” which is pretty cool. Phrases like “The acting was good , but the movie could have been better” have sentiments in both polarities, which makes this kind of analysis tricky -- essentially w VADER you would analyze which part of the sentiment here is more intense.

The best way to use this data is to learn about new tickers that might be trending. As an example, I probably would have never known about the ARK ETFs, or even BB, until they started trending on Reddit. This gives many people an opportunity to learn about these stocks and decide if they want to invest in them or not - or develop a strategy investing in these stocks before they go parabolic.

