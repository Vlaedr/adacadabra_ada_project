# Arab Spring : a revolution through media

# Abstract
Online media have had a huge impact on the sequence of events leading to the historical period known as the "Arab Spring". Spinn3r is a web-crawled dataset regrouping over 3,8 billion web pages from blog posts, forum discussions, social media, etc... between mid-January and mid-February 2011. In light of current events occurring in Hong Kong, Chile, Lebanon, etc... we found this subject to be relevant since these current happenings follow the footsteps of the Arab Spring with their online media impact. With the use of our dataset we hope to infer and visualize crucial information on the impact of online interactions on the Arab Spring revolutions. We endeavor to express several stories during our research, such as fluctuation of coverage between directly affected countries and external countries and the divergence of opinions according to media locality through sentiment analysis.

# Research questions
* How to select pertinent information from such a massive dataset ?
* How to work with data in foreign languages ?
* How does the use of online media has affected the spread of social revolutions in the Islamic world ?
* How did the Arab Spring affect the following revolutions up to this day ?
* Can we detect a divergence of opinion about the Arab Spring according to media locality ?
* How does the news coverage fluctuate between mainstream news and other media such as blog posts, forum discussions,etc... ?

# Dataset
* The [Spinn3r](https://www.icwsm.org/data/) dataset contains over 3,8 billion web pages including blog posts, forum discussions, social media and more... This is a challenging dataset since its total size is aroung 1,6 TB, thus we plan to use pyspark to process this data that is stored on the EPFL cluster.
* We are considering the use of further web scraping to enrich our whole dataset. This web scraping could be done on the media websites that are present in the Spinn3r dataset or on social media such as Twitter.

# A list of internal milestones up until project milestone 2
* Load the massive dataset efficiently
* Translate non-english data
* Filter out content not concerning the event of the Arab Spring
* Perform sentiment analysis on different groups of data (e.g. per locality)
* Add pertinent visualization for our data story

# Questions for TAa
* How is the dataset stored on the EPFL cluster ? Is the data partitionned in several files ?