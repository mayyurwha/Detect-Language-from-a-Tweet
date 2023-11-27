# Detect-Language-from-a-Tweet


The pyhton script is deisgned to  processes Twitter tweets stored in a JSON file named "tweets.json." It utilizes the langid and langdetect libraries for language detection. The script maintains two dictionaries: "langs" for tracking the count of detected languages using both libraries, and "langWordCounts" to store word frequencies for each language.

The code iterates through each line of the JSON file, loading the tweet data and attempting to classify the tweet's language using langid and langdetect. The script handles exceptions gracefully to account for cases where language detection may fail.

For each successfully processed tweet, the script updates the language count in the "langs" dictionary and maintains word frequencies in the "langWordCounts" dictionary based on the 'lang' attribute provided by Twitter.

After processing all tweets, the script prints the language counts for each library. For each detected language, it also outputs the top 10 most common words in the tweets associated with that language, based on the 'lang' attribute from Twitter.

Note: The code uses a try-except block to handle exceptions during language detection, and it prints progress every 100 tweets processed. Additionally, it's assumed that the 'text' and 'lang' attributes are present in the tweet data.
