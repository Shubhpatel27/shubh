Use the set of inaugural addresses in the nltk corpus. The file `read_inaugural_addresses.ipynb` shows you how to access the texts. 

1) Build the inverted index as shown in `indexing.ipynb` (class repository). Use spacy and the ner processing to add names, locations, organizations that span more than one word as terms to your vocabulary (look at the sample code in `demo_spacy.ipynb`). 

    * Which nlp processing steps did you use?
    * Which names, locations and organizations you found and added to the corpus vocabulary
    * What is the vocabulary size (# of unique terms after processing) of the whole corpus after nlp processing (number of unique terms).
    * What are the most frequent and least frequent 10 words in the corpus and their document frequencies.

2) Come up with 3 queries related to the inaugural addresses (look at the text of some of the addresses). The queries should consists of more than one word. For example: 'American foreign policy', 'recover from economic depression', etc. Check that all words in your queries appear somewhere in your documents. Hint: Do not use very common or very rare words. Do not forget to process the queries using the same nlp processing steps as the documents. 
   * For each query, display the query and the document frequency of each term.

3) Write a function to compute the similarity of a query with the collection of inaugural addresses. Do this efficiently by computing the similarity between a query and only the set of documents that contain at least two words from the query. Implement two different TF-IDF similarity functions (one of them should be BM25 - choose another one from the slides or textbook). Retrieve the ranked list of the first 5 most similar inaugural addresses for each of your queries and for each similarity function.
   * For each method, and each query, display the most similar 5 titles of the inaugural addresses (not the full text) and their similarity values.
     
5) For each similarity method, and each query, compute the precision in the following way: Read the text of the first 3 addresses in the ranked list for each query. Using your own judgement, rate each text as either relevant or irrelevant to the query. Count how many you rated relevant and divide it by three. This is the precision:

       Precision(query_x, method_y) =  # relevant texts / first 3 ranked docs
        
   * Display the precision values for each query and each method. 
 
5) Add length normalization to your methods. First, compute the length of the collection of speeches, then find the max, min, average, and standard deviation. Then choose the parameters of your length normalization method according to these values. 
   * Compute the similarity between each query and the collection using length normalization in your methods.
   * Discuss any changes you see to the top 5 for each query and method and the precision results. Did the results improve, stay the same, or worsen. Be specific. 

7) Compare and discuss the precision results you obtained with the two TF-IDF similarity functions you used with and without length normalization. Which method gave you better results and why. 


## Turn in

1. The jupyter notebook code showing the output for each question. Please organize your code, so it is clear where is the code and answer for each question. Do not print whole text of inaugural addresses in your output. Do not display any long text in your notebook. 

2.  Enter in Answers.md file a description of what you did, which methods you uses, the results you got, and answers to 5) and 6). 
