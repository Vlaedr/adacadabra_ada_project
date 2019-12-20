# The Arab Spring : a highly broadcasted revolution

# Abstract
The « Arab Spring » is a historical period dating from the December 2010 until mid-2012 that saw the rise of many revolutions over the Islamic world, starting with Tunisia. As the influence of online media grows more and more every day, we would like to study the impact of these media on the spread of these revolutions across around 20 countries. To do this, we emit the hypothesis that the coverage of key events (such as riots, destitutions, etc…) are correlated to the start of revolutions of countries that are neighboring Tunisia. It would also be interesting to find out how the coverage done by government-owned media differs from independent media (e.g. blog posts, independent newspapers). We are also interested in studying whether media are consistent with the information they give out, according to media types (e.g. official media, blog posts, forum,…). We plan to research these topics by exploring the Spinn3r dataset which contains over 3,8 billion data points.

# Research questions
* ~~What is the correlation between the start of revolutions in countries other than Tunisia and the media coverage in these countries ?~~
* ~~What is the proportion of blog, forum and social media posts talking about the riots compared to official media?~~
* ~~Is the coverage of the events consistent across media type ? Do mainstream media have a better consistency of coverage than more reactive media types (forums, blog posts, etc…)?~~
* Is it possible to infer the beginning of the protests/revolts by examining the media coverage of the countries involved ?
* What is the relationship between the different websites talking about the Arab Spring using a URL centered network?


# Dataset
* The [Spinn3r](https://www.icwsm.org/data/) dataset contains over 3,8 billion web pages including blog posts, forum discussions, social media and more... This is a challenging dataset since its total size is aroung 1,6 TB, thus we plan to use pyspark to process this data that is stored on the EPFL cluster.
* We are considering the use of further web scraping to enrich our whole dataset. This web scraping could be done on the media websites that are present in the Spinn3r dataset or on social media such as Twitter.

# A list of internal milestones up until project milestone 2
* Load the massive dataset efficiently
* Translate non-english data
* Add localization labels on data points
    * This can be done by looking up URLs’ suffixes, by scraping metadata from the source, by detecting the language used in articles, blog posts, etc… (e.g. with the langdetect python library)
* Build a lexicon of keywords that will allow us to find posts mentioning the events of the Arab Spring
* Classify the data mentioning the Arab Spring as informative posts or reactions to the events
* We will use NLP techniques to check for similarity between posts so as to check for consistency
* Once we have the localizations, we can filter out the data points that come countries that are not of interest : we will only keep articles coming from Europe, North Africa and the Middle East.
* Compute some statistics from our dataset after this filtering: through keyword analysis, we can isolate datapoints mentioning events related to the Arab Spring : thus we can know how many articles mentioning the Arab Spring come from blog posts, how many come from government-owned media, etc…
* Find the proportion of articles that mention a key event (riots, destitutions, etc…) by country over time and how it correlates to the start of revolutions in countries other than Tunisia. We assume that, if there are more and more articles mentioning key events in other countries, it is likely it will inspire more and more these countries to revolt.

# A list of internal milestones up until project milestone 3 and the final presentation
#### Milestone 3
* Sample an even larger amount of data (now we have around 1.2 million rows at the beginning of the pipeline)
* Find a way to determine from where an entry comes from using both the language and the URL extensions at the same time
* Visualize on an interactive map the proportion of posts per european country and other metadata using Folium or Bokeh
* Through the use of permalinks in the posts, we will build a graph structure of the relationship betweens sources having articles about the Arab Spring using inspiration from the following paper.(https://www.icwsm.org/2010/papers/icwsm10dcw_2.pdf)
* Decide wether to do a data story or a report

#### Final Presentation 
* Create the final poster
* Prepare the final presentation

# Contributions

* Robin Leurent: Writing the report, Spark configuration, LSA, Keyword Extraction, Data pre-processing, Arab Spring Event Inference
* Matthieu Baud: Writing the report, Hyperlink Network Analysis
* Sacha Leblanc: Writing the report, LSA, Hyperlink Network Analysis
* Alexis Dewaele: Writing the report, Keyword Extraction, Data pre-processing 