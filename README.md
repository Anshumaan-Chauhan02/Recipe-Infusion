<h2 align='center'> Recipe Infusion </h2>
<p> In this porject we aim to create a framework, which includes a Recipe generation model - DistilGPT2, generates unique recipes given a list of ingredients. These synthetic recipes are then processed by a T5 (style transfer model), to infuse style of different personas in the recipe. </p>

### Dataset Information:
Two different areas where our datasets were used are Fine tuning of DistilGPT2 (Recipe Generation) and T5-small model (for text style transfer)
* Recipe Generation
  * RecipeNLG : https://recipenlg.cs.put.poznan.pl/
  * RecipeBox : https://eightportions.com/datasets/Recipes/
* Text Style Transfer
  * William Shakespeare : 
      * Translations of Shakespeare plays to Modern English 
      * https://www.kaggle.com/datasets/garnavaurha/shakespearify
  * Taylor Swift : 
      * Song Lyrics of Taylor Swift's albums
      * https://www.kaggle.com/datasets/PromptCloudHQ/taylor-swift-song-lyrics-from-all-the-albums
  * Donald Trump : 
      * Tweets of Donald Trump till June 2020
      * https://www.kaggle.com/datasets/austinreese/trump-tweets
  * Michael Scott : 
      * Dialogues of all characters from The Office
      * https://www.kaggle.com/datasets/nasirkhalid24/the-office-us-complete-dialoguetranscript 

### Libraries Used and Installation Steps: 
#### 1) Numpy : Perform several mathematical evaluations in the preprocessing of the datasets
    pip install numpy  
#### 2) Pandas : Loading/Processing/Storing of the different datasets
    pip install pandas 
#### 3) Itertools : Easy iteration of large lists 
    pip install itertools 
#### 4) Sklearn : Cosine Similarity and TF-IDF
    pip install sklearn 
#### 5) Transformers : DistilGPT2, T5-small, MarianMT (both model and tokenizers)
    pip install transformers 
#### 6) SentencePiece : Used by MarianMT's tokenizer (Back Translation)
    pip install sentencepiece  
#### 7) Evaluate : BLEU Score evaluation 
    pip install evaluate   
#### 8) Matplotlib: Plotting of the training curves 
    pip install matplotlib

### File Content and Sub-Task Description 
* RecipeDataset.ipynb : 
     * Loading of both Recipes datasets 
     * Preprocessing the datasets to get into a common useful format 
     * Performing statistical analysis on the data
     * Storing the final concatenated dataset 
* Statistics.ipynb :
     * Statistical analysis on the preprocessed datasets and the final concatenated dataset 
* Recipe_Generation_DistilGPT.ipynb :
     * Loading of the final recipe dataset 
     * Data Preparation of the final dataset 
     * Training of DistilGPT2 Model 
     * Testing of the Finetuned (FT) model and baseline model 
     * Evaluation of the models - BLEU Score and Perplexity 
     * Generation of Recipe dataset for Style Transfer
     * Error Analysis on Adversarial inputs  
* Preprocess_TST_dataset.ipynb : 
     *  Loading the non-parallel data - Taylor and Trump
     *  Preprocess the datasets
     *  Extract some statistical info about the dataset 
* Shakespeare_and_Scripts_Preprocessing.ipynb : 
     *  Loading the non-parallel data - Michael 
     *  Load the parallel data -  Shakespeare 
     *  Preprocess the datasets
     *  Extract some statistical info about the dataset
* BackTranslation.ipynb :
     * Load the MarianMT models for Fr-En and En-Fr
     * Perform back translation to generate synthetic parallel data - Michael, Taylor and Trump
     * Store the parallel dataset  
* TST_Architecture.ipynb :
     * Load all the parallel datasets 
     * Finetune a different T5-small model on each dataset 
     * Generate styled recipes - Sentence-wise and Entire Recipe
     * Test the performance (Human Evaluation) on the styled recipes (Sentence-wise)
     * Check for style infusion on random sentences 

### Steps to successfully run the project
Except training (due to computational limitations) of the LLMs all of the code was implemented in Google Colab. We have listed the steps that needed to be followed for a successful implementation of the project.
1) Download all the .ipynb files and upload them in a new folder on Google Drive named 'Project 685'
2) Download all the Recipe Datasets and upload the zip files on the Drive
3) Run RecipeDataset.ipynb to get the 'Final_dataset' file, which consists of the preprocessed concatenated dataset
4) Run Statistics.ipynb file to know some statistics about the datasets [OPTIONAL]
5) Run Recipe_Generation_DistilGPT.ipynb to get the finetuned recipe generation model and Recipe generations 
6) Download the Text Style Transfer datasets. Create a new sub-folder {persona}_TST. For example, Taylor_TST
7) Upload the datasets for Taylor and Trump in the sub-folder, whereas for Shakespeare and Michael in the main folder
8) Run the Preprocess_TST_dataset.ipynb and Shakespeare_and_Scripts_Preprocessing.ipynb to get the appropriate formatted dataset for Back translation
9) Run BackTranslation.ipynb to get a parallel dataset for Taylor, Trump and Shakespeare
10) Run TST_Architecture.ipynb file to get the finetuned TST models

