## Introduction

### Abstract

In the USA, the political orientation of American people is mostly divided into two main parties: the republicans and the democrats. The famous New York Times newspaper claims to be neutral, presenting both democratic and republican opinions. Here, we will use the quotebank dataset containing a set of quotations published in the newspapers between 2015 and 2020 to verify this statement. Using different techniques such as sentiment analysis and Principal Component Analysis, we will highlight the separation between pro-democratic and pro-republican in the quotations and their speakers and check whether one political orientation is more strongly represented than the other one. The determination of the political orientation will be based on sentiment analysis about several chosen topics that are commonly addressed in the USA and on which republicans and democrats tend to argue.

### Questions

This analysis answers the following questions:

- Who are the main speakers quoted in the newspapers and from what political party are they?
- What is the opinion of newspapers on big subjects and debated topics? Are these opinions drifting towards one political party?

### Methods

**TODO** <!-- List the methods used -->

### Newspapers

**TODO** <!-- List the newspapers analyzed -->

---

## First analyses

### Who are the speakers?

**TODO** <!-- Counts of most frequent speakers in the different newspapers -->

<!-- Figure: Barplot for each newspaper -->
{% include top_speakers_nyt.html %}

### Most frequent words

**TODO** <!-- Occurences of words (wordclouds) -->

<!-- Figure: Wordcloud for each newspaper -->

![Wordcloud for democratic party](images/wordclouds/democratic_party.png)
![Wordcloud for republican party](images/wordclouds/republican_party.png)
![Wordcloud for other party](images/wordclouds/other_party.png)
![Wordcloud for no party](images/wordclouds/no_party.png)

---

## Sentiment analysis

### Topic detection

**TODO** <!-- List topics, explain method -->

<!-- Figure: Table with words per topics -->

### What are the main topics in newspapers?

**TODO** <!-- Sentiment analysis per topic for each newspaper -->

<!-- Figure: Barplot average of compound score for each topic, each newspaper -->
{% include sentiment_scores_nyt.html %}

### Political orientation of speakers and newspapers

**TODO** <!-- PCA with speakers, clustering if possible -->

<!-- Figure: Results of PCA with graph of speakers and newspapers -->

---

## Conclusion

**TODO**

---

## References

**TODO** <!-- Add references -->
