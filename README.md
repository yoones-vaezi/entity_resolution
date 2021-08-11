# entity_resolution

The steps taken to solve the entity resolution problem include:

1- explore and clean the datasets. More details can be found in teh notebook provided.
This includes:

>- a- removing duplicate identifiers. 

>- b- Setting the invalid publication dates to NaN.

>- c- Exploring the features to find important ones for matching

>- d- Cleaning text columns: title, venue, and authors, ehich included removing special charecters and extra spaces, lemmatizing, removing pronouns and stop words. 

2- Perform entity matching with the use of 4 columns: title, authors, venue, and year.

The Following steps are taken to perform this:

  >- 2-1: Blocking: create candidate links by blocking unlikely matches

  >- 2-2: comparing: Calculate a set of informative, discriminating and independent features important for a good classification of record pairs into matching and distinct pairs. We used Spacy and its trained pipelines to calculate embeddings and cosine similarity between strings. 
  
  >- 2-3: Matching stage: define thresholds for the calculated features to find matches.
  
  ### Requirements:
  
  We used Python 3.8 to perform this work.
  
  The Library requirements are listed in the file requirements.txt
  
  ### How to run
  
  >- We suggest installing a new Anaconda environemnet with Python 3.8 and also the required libraries listed above installed in it. 
  
  >- Then run the Notebook that walks you through the analysis we have done to obtain the results. 
  >- The notebook assumes that the data files are located in a directory named "data_files".
  >- The resulting csv will be saved in another directory named outDir. 
