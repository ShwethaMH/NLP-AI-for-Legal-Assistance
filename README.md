# NLP-AI-for-Legal-Assistance

## Introduction
The importance of prior cases is greatly emphasized in a Common Law System. Prior cases, also known as precedents, are court cases from the past that discuss similar issues and can serve as references in the current case. Prior cases are considered as important as any other law to ensure that a similar situation is treated similarly in every case. It is expected that a court will follow the interpretations made in a prior case in current cases where relevant legal issues have already been decided. Therefore, lawyers must research prior cases and see how courts have interpreted the contemporary legal issue.
Recent developments in technology have led to a rapid increase in digital legal documents. Therefore, an automatic precedent retrieval system is imperative for legal professionals. An approach to precedent retrieval could be represented as a task of information retrieval, where the system would retrieve relevant prior cases based on the current case document. Furthermore, legal texts tend to be complex and lengthy.
As a result of the requirements described above, the project focuses on retrieving precedence using Natural Language Processing (NLP).

## Methods
### Step 1:-
#### Data Extraction:
Natural Language Processing involves extracting information from a text and using various NLP approaches to extract valuable insights. I have used the following techniques to extract information:
- Tokenization: It is a crucial aspect when working with text data. Tokenization breaks down the length of text into smaller chunks called tokens. A token can be a word, a sub word, a character, or a sentence. Tokens are considered building blocks of Natural Language; token-level processing is the most common way to process raw text.
- Regular Expression: RegEx is a series of characters used to search for and replace patterns in text. This project uses the RegEx method to find special characters, digits, and alphanumeric characters and replace them with a space.

#### Data Preparation:
In Natural Language Processing (NLP), text preprocessing is the most crucial step while preparing the data. When dealing with unstructured data, text preprocessing is very important. One can come up with a significant error, or the model will not perform as expected. Text preprocessing steps include stop word removal, lower casing, stemming, and lemmatization, and all these methods are performed using the NLTK library. These text preprocessing steps achieve a dimensionality reduction. In the vector space model, each word is a dimension. A number of unique words mean the number of dimensions.
This project aims to convert textual data into vectors and find similarities between two vectors; hence, these processes are considered appropriate for preparing the data.

### Step 2:-
#### Approaches to Information Retrieval:
- In this project, two approaches to information retrieval are proposed, wherein the system accepts a query dataset and returns relevant prior cases. 
- In the first approach, the document similarity between two vectors is calculated using Cosine Similarity. 
- In the second approach, TF-IDF and BM25 models are trained to retrieve correct prior cases when a query is passed.
- Unstructured data is converted into a structured format using the Term Document matrix method. The document is viewed as a concept of space and gets a tabular representation in the form of significant attributes. This document representation in major terms is called the vector space model(VSM). It is the model where each term represents the dimension of the document, and the value represents the number of occurrences in a particular document. 
- Different clustering algorithms consider different similarity measures when comparing two documents. The most commonly used similarity measures are: (i) Euclidean, (ii) Cosine, (iii) Pearson correlation, and (iv) Extended Jaccard. 
- A cosine similarity measure is widely used because it gives the best result with fewer efforts. Nevertheless, the challenge here is dimension reduction as the documents are higher dimensional text; it takes longer to process. The dimension can be reduced by retaining only important terms using the UMAP library; thus, feature extraction has to be done so that the best features are selected for the clustering process.

### Step 3:-
#### Statistical Significance:
The statistical significance is determined by comparing two algorithms based on their precision and recall evaluation measures. 
- The precision of search is the ratio of number of relevant and retrieved documents to the number of total retrieved documents. 
- A recall is the ratio of retrieved and relevant documents to the number of possibly relevant documents.

### Step 4:-
#### Effective Storytelling:
Methodologies used to communicate my findings include K-means clustering, DBScan, and BERTopic modeling.
- In K-means clustering methodology, similar items are grouped into clusters. K represents the number of groups. Elbow method is used to choose correct value of K and improve model performance. 
- DBScan method is used to group similar data points. DBScan is an unsupervised learning method; data points have no labels.
- BERTopic modeling technique uses transformers to create dense clusters while retaining keywords in topic descriptions.

## Summary of Conclusions:
In this project, I have proposed two approaches to solve the information retrieval problem wherein the model accepts the current case document as a query and returns relevant prior cases. The traditional TF-IDF approach performed well but is limited to understanding the context by inherent term specificity; however, results are promising enough to see the potential for it to perform efficiently if it were trained on a large dataset. My approach leveraging the BM25 ranking function to rank the top 3 relevant prior cases for a given query also achieved good precision and recall rates. BM25 ranking function ranks a set of documents based on query terms in each document. BM25 is based on a probabilistic information retrieval model that incorporates document frequency, term frequency, and document length attributes.
While this project proved through statistical significance that there is not much difference in the performance of the TF-IDF and BM25 model, the BM25 is arguably the most efficient and
widely adopted method for retrieving information which can be seen from its practical application in the real-world.

