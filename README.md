# War impact on Cinema

Bastien Bernath, Etienne Boisson, Emmanuelle Denove, Xavier Theimer-Lienhard

## Abstract 

Wars have a strong impact not only on the people that live through it, but also on society as a whole. Using datasets of meta data of films scraped from wikipedia and freebase, we’d like to explore war's impact on cinema themes, genres and general sentiment. Are more war movies made during a war or just after ? Are war movies always sad ? How do these themes change across different wars, and across the different affected countries ? What wars from the last century do we see most often in modern cinema, and does the sentiment towards these wars seem to change ? The goal is to see the long term effect of wars on arts and culture, and how wars are represented in cinema across time.

## Research Questions 

**We’d like to ask questions??? to our dataset for war films in general some wars of our choosing, which are (for now) the Second World War and the Vietnam War???:**
- What is the evolution of the proportion of war related films during/after the war ?\
- What are the main genres of movies produced during wartime in affected countries ?\
- Is there a difference in sentiment in the story of movies that are released after or before a war period ? \
- Have particular genres seen a big increase/decrease in popularity during/after the war ?\
- For certain wars, how has their representation over time changed ? Are the genres of movies that talk about those wars still the same as when the war first happened ? Has the overall sentiment of the films changed ?\
- Is there a difference in sentiment or genre of war movies across the different affected countries ?\
- Currently, what wars do we see most often represented in modern cinema, and how are they represented ?\
- How do these metrics (sentiment, genre, etc.) change between countries directly affected by the wars, versus countries less or not affected by them ?\
- How has the revenue of war movies changed ? Can we say that they’ve become more or less popular over time ?\

## Proposed Additional Datasets 
For our project, we will rely a lot on plot summaries of movies to measure overall sentiment of the movie, see which war it’s about specifically, see how it handles the subject etc. However, we noticed that, in the CMU Movie Corps, only around half of the 80 000 entries included a summary. Therefore, we used a wikipedia scraper, available at https://github.com/piki/wikipedia-film-database, that searches through all wikipedia entries and extracts, from the ones that are movies : title, cast, director(s), producer(s), production companies, distribution companies, and release year.

We noticed that the CMU Movie Corps includes the wikipedia ID for every movie ; we therefore modified the source code to extract the ID from the articles so that merging would be easier. We also extracted the movie plot summary from the articles.

We have already extracted this dataset (“with_plot.txt”), but we still need to properly clean the “plot” entries.

Since there are not that many movies in the CMU Movie Corps, we are also considering using the IMDB datasets for some additional information. We would mainly use them for analyzing the evolution of the number of war movies over time, since it would give us a more accurate representation. Since IMDB does not give access to their movie summaries, we would base our more in-depth exploration on the main CMU dataset.

From IMDB, we would use their **title.basics.tsv.gz** dataset. This gives us, for every title, 3 genres associated with it, which we could use to see the evolution of war films. We would only use entries that have titleType “movie” or “short film” (as opposed to “tvseries”, “tvepisode” etc.).

## Methods

- Investigate the general sentiment of the movie’s summaries using sentiment analysis library tools (namely pattern). We will use this to compare different periods of time (period of war, after 2000…), different countries (Germany, France, USA…), and different types of movies (war movies…). With this information, we hope to see a pattern in pre-war or post-war movie production, depending on the country.
- Explore the countries mentioned in war movies, and how they are described. Are enemy countries always depicted in a negative light ? This can be done with NLP libraries (such as nltk).
- Explore what types and quantities of movies apart from war movies include terminology associated with war, or to certain wars (‘soldier’, ‘battlefield’, ‘trenches’). This could be done with simple word search using pandas functions.
- More classical research : isolate the main genre of movies made during wars, emergence of specific movies post-war.
- Create a website in order to illustrate our data story.

## Proposed timeline

22.11.22 Clean dataset & general research\
02.12.22 Deadline HW2\
11.12.22 Sentiment analysis, NLP\
18.12.22 Data story and website creation\
23.12.22 Deadline for Milestone 3

## Organization within the team

- **Data exploration** (everyone)
- **NLP** (Bastien + Xavier)\
- **Sentiment analysis** (Etienne + Emmanuelle)\
- **Clean and fully incorporate Wikipedia dataset**  (Emmanuelle)\
- **Data story brainstorming** (everyone)\
- **Data story expansion** (Etienne + Bastien : may change)\
- **Website** (Xavier + Emmanuelle : may change)\
_Note that all above task attributions may evolve during the project <3._
