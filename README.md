
Instructions & File Descriptions:


STEP 1 - PREPROCESSING
____________________________
1. Use preprocessing.ipynb to remove all articles with a non-mathematics tag as main tag. Removes the files from the ArXiv database file. Does the same for the context database file and saves them both in the folder /database-files. (Also removes non-essential columns from ArXiv database file)
____________________________

GENERIC EXTRACTION OF EXPLAIN WORDS
____________________________
explain-words-extract.ipynb. Defines a semi general function to extract words from the context database file. Uses it concretely to extract all explain words and save them as explain_fullraw in the database folder. Columns: mainmathcat, context, sentence', focuswords.
Functions: word_extract
____________________________

BASE EXPERIMENTS
____________________________
base-experiments.ipynb. Defines generic functions to make dataframes and Latex tables of focus words. Uses them on explanation words defined in explain-words-extract.ipynb. 
Saves them in the folders explanation-data and tex. 

Also performs statistical test across all branches and saves it as a .png file in /figures folder.

Functions: freq_wordcount, freq_wordcount_branch, freq_wordcount_context, raw_wordcount, raw_wordcount_branch, raw_wordcount_context
____________________________

PEASE EXPERIMENTS
____________________________
pease-experiments.ipynb performed the pease experiment. Does not define a function, but only a loop. Saves a dataframe in /pease-data folder which is explanation per million words across contexts and a total. Also saves a latex table in /tex folder.
____________________________

EXPLANATIONS ACROSS CATEGORIZED BRANCHES.
____________________________
explanations-branches-categorized.ipynb Takes a focusword_df and categorizes it given a categorization. Can save it as plot in the /figures. Also defines an exploratory pvalues between the categories. 

Makes categorization based on the use of the siz 'mathematical activitites' proposed in (Ramos et al. 2019): proof, conjecture, model, define, solve, show.  Using a pipeline consisting of PCA and K-means it categorizes them. Can be used as qualified starting point for comparison of explanations. Saves it in /figures folder.

Function: branch_categorization, branch_cat_pvalues, basic_seaborn_plot
____________________________

EXPLANATIONS IN UNUSUAL PLACES
____________________________
explanations-theorems-proofs.ipynb defines a function which which given a focusword_df can extract a subset on those based on new focuswords in the sentence column

MISSING - SOMETHING ABOUT EXPLANATIONS IN PROOFS

Functions: sentence_extract
____________________________

IS THE ARMCHAIR BORKEN?
____________________________
broken-armchair.ipynb Defines a functions which looks at all adjective in a NOUN_fullraw database file - such as the proof_fullraw file. Makes a dataframe of all the words, including count and pct and a dataframe of pre-defined categories with counts and pct and saves them in the /armchair folder.

MISSING - PROOFS/FIGURES PROVIDES UNDERSTANDING - LANGE EXPERIMENT NOT POSSIBLE?

Functions: adj_nouns
____________________________

FIGURE/VISUALS MAKING FILE





Limitations:
____________________________
Note that the 5 contexts: outer, theorem, meta, proof and other are hard-coded into the functions. 
You have to load the ArXiv database file as "df_arxiv" as that name is hard-coded into the functions.
Categories in broken-armchair.ipynb are hardcoded based on adjective counts taken from arxiv_context.feather (avail. 2021-4-17).
____________________________


