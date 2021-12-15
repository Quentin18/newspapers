## Introduction

### Abstract

**TO COMPLETE**

Everyday, millions of articles are published in the newspapers. Many Americans have its favorite journal, whether it is the New York Times, the CNN, the Fox News or any other journal that every day publishes the latest breaking news. News coverage can be very influential, affecting one’s opinion through the information it provides or the emotional reaction it generates on the reader. Most of these newspapers claim having a neutral political opinion, but in general, a newspaper’s phrasing or language is specifically chosen with the intention of exposing a certain political outcome. Thus, the reader’s opinion is easily influenced by the content published in its favorite journal, although he’s not conscious of it. For example, CNN is known to emphasize the democrat opinion while the Fox News is known for its republican ideas.
Analyzing the content of a newspaper is therefore a good way to verify its political orientation and the political ideas it wants to transmit. This data story present a quotation based analysis of newspapers and their political bias.

### Method
The ultimate goal of this analysis is to define the political orientation the newspapers. Indeed, is it possible to guess the political opinion of a newspaper based only on its content? Popular newspapers should be neutral in the way they present the news, but are they really neutral? Otherwise, which political parties do they support the most?
This is adressed through several questions:
<ul class="default">
    <li>Who are the main speakers quoted in the newspapers and from what political party are they?</li>
    <li>What is the opinion of newspapers on big subjects and debated topics? Are these opinions drifting towards one political party?</li>
    <li>Are there any specific topics that are frequently addressed by newspapers? Are those topics relevant to define the newspapers' political opinion?</li>
</ul>

In the following, the Quotebank dataset regrouping quotations published in multiple english newspapers between 2015 and 2020 is analysed. We focused our intention on 3 newspapers: the New York Times, the CNN and the Fox News. The determination of the political orientation of the journals is based on several chosen topics that are commonly addressed in the USA and on which republicans and democrats tend to argue. 
We use dictionaries related to the topics to select the interesting quotations and sentiment analysis as indicator of one's opinion. Statistical tests as well as dimensionality reduction will help us interpret our data. 
Additionally, we look at the way the current topics are presented in the newspapers to help us assess their political opinion. 

Throughout the whole analysis, the results coming from the 3 different newspapers are compared, keeping in mind the respective political bias of the Fox News and the CNN. 

### Newspapers

{% include newspapers.html %}

## First analyses
Before going any deeper in the analysis, some information can be extracted from the dataset.

### Who are the speakers?

**TODO** <!-- Counts of most frequent speakers in the different newspapers -->

<!-- Figure: Barplot for each newspaper -->
{% include top_speakers_nyt.html %}

### The most frequent words

**TODO** <!-- Occurences of words (wordclouds) -->

<!-- Figure: Wordcloud for each newspaper -->

![Wordcloud for democratic party](images/wordclouds/democratic_party.png)
![Wordcloud for republican party](images/wordclouds/republican_party.png)
![Wordcloud for other party](images/wordclouds/other_party.png)
![Wordcloud for no party](images/wordclouds/no_party.png)

### What about the party distribution in the newspapers?

---
Include the Pie chart.

## Sentiment analysis: party-specific opinions?
The Wordclouds may have been useful to visualize what the different political parties talk the most about, but what if we want to compare their opinions on the same subjects? Our idea was to use sentiment analysis to quantify the opinion of each party on specific topics. For both Democrat and Republican speakers, we collected the quotes talking about several specific topics:

<ul class="default">
    <li>immigration</li>
    <li>health care</li>
    <li>climate change</li>
    <li>Trump</li>
    <li>abortion</li>
    <li>women’s rights</li>
    <li>racisms</li>
    <li>violence</li>
    <li>war and military action</li>
    <li>taxes</li>
    <li>coal industry</li>
</ul>

For each of these topics, we computed the mean opinion score for each party. The scores range from **-1** (for a **negative** opinion) to **+1** (for a **positive** opinion).  
We then proceeded to do the same analysis separately with our 3 newspaper's quotes, to obtain mean opinion scores for all three of them. 

### Topics in the newspapers

**TODO?** <!-- List topics, explain method -->  <!-- A QUEL POINT FAUT VRAIMENT EXPLIQUER LES METHODES DANS LA DATASTORY? -->

{% include topics_table.html %}


#### Can we use sentiment analysis to compare the political parties?
<!-- Figure: Barplot average of compound score for each topic, each party -->
{% include sentiment_scores_nyt.html %}

Clearly, the sentiment analysis results are not the ones expected. We should observe a clear demarcation between the opinion scores of Democrats and Republicans, at leat on topics such as immigration or health care, on which they are drastically opposed. But in our results there is little to no significant difference between both parties, meaning that **our sentiment analysis was unsuccessful**.

<!-- Table: topics with significant difference or not (?) -->

*Why was it the case?* 

We used a simple pretrained model for our sentiment analysis, based on emotions.  **TODO**
<!-- complete if we cannot improve the results -->



#### Sentiment analysis: comparison between the different journals

We can still visualize the sentiment analysis scores for the 3 newspaper, even if the results are not optimal.
**TODO** <!-- Sentiment analysis per topic for each newspaper -->

<!-- Figure: Barplot average of compound score for each topic, each newspaper -->


### Political orientation of speakers and newspapers

{% include PCA_nyt.html %}

**TODO** <!-- PCA with speakers, clustering if possible -->

<!-- Figure: Results of PCA with graph of speakers and newspapers -->

---
## Topic analysis: what are the main topics in newspapers?

Instead of trying to determine what every actor *thinks* of a topic, we could simply quantify how much they *talk* about it. Indeed, the coverage of an event or a debated subject can also give us information about a newspaper's political opinion. The more a journal talks about a subjet, the more it cares about it. 

**TODO** <!-- Sentiment analysis per topic for each newspaper -->

<!-- Figure: Barplot frequency of quotes about each topic -->



## Conclusion

**TODO**

---

## References

**TODO** <!-- Add references -->
