Instructions & File Descriptions:

____________________________
preprocessing.ipynb: 
____________________________
Preprocessing removes all articles where maincat!=mainmathcat, both from context database and metadata database and save them in the folder /database-files.

Removes non-essential metadata and counts number of articles in each category

Also does this for the 2009 corpus
____________________________

____________________________
explain-words-extract.ipynb
____________________________

Defines a semi general function to extract words from the context database file. 

Does the same for the Ramos corpus
____________________________

____________________________
base-experiments.ipynb
____________________________
Defines a generic function to make tables of focus words. Saves them in the folders explanation-data and tex. 

Performs statistical test across all branches and saves it as a .png file in /figures folder. Also performs cut of branches to perform statistical test on and give confidence intervals.

Does the same for the Ramos corpus
____________________________

____________________________
pease-experiments.ipynb
____________________________
It performs the pease experiments
____________________________

____________________________
explanations-branches-categorized.ipynb
____________________________
Takes a focusword dataframe and categorizes it given a categorization. Can save it as plot in the /figures. Also defines an exploratory pvalues between the categories. 

Makes categorization based on the use of the the 'mathematical activitites' proposed in (Ramos et al. 2019): proof, conjecture, model, define, solve, show.  Using a pipeline consisting of PCA and K-means it categorizes them.
____________________________

____________________________
broken-armchair.ipynb 
____________________________
Defines a functions which looks at all adjective in a NOUN database file - such as the proof_fullraw file. 

Calculates share of fgure/proof mentions that also mentions explanations. Performs statistical test.
____________________________

____________________________
explanations-theorems-proofs.ipynb
____________________________
Makes piechart of explanation classification done by hand supplied as a csv file.
____________________________

____________________________
wordcloud.ipynb
____________________________
Makes a wordcloud for the frontpage
____________________________


____________________________
____________________________
LIMITATIONS:
____________________________
____________________________
All code has only been for personal use and is thus not written to be easily run by others

Note that the 5 contexts: outer, theorem, meta, proof and other are hard-coded into the functions.

You have to load the ArXiv database file as "df_arxiv" as that name is hard-coded into the functions.

Categories in broken-armchair.ipynb are hardcoded based on adjective counts. 
____________________________









