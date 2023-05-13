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

### File Content and Description 
* RecipeDataset.ipynb :
* Statistics.ipynb :
* Recipe_Generation_DistilGPT.ipynb :
* Preprocess_TST_dataset.ipynb : 
* Shakespeare_and_Scripts_Preprocessing.ipynb : 
* BackTranslation.ipynb :
* TST_Architecture.ipynb :

### Steps to successfully run the project
1) 
2) 
3)
4)
5)
6)

