# Friend-Recommandation-System

### Problem statement: 
Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)

### Data Overview
Taken data from kaggle https://www.kaggle.com/c/FacebookRecruiting  
data contains two columns source and destination eac edge in graph 
    - Data columns (total 2 columns):  
    - source_node         int64  
    - destination_node    int64  

### Files Overview
    - EDA.ipynb - data Analysis
    - Featurization.ipynb - feature engineering
    - Models.ipynb - algorithms 

### Mapping the social network link prediction problem into supervised learning problem:
- Generated training samples of good and bad links from given directed graph and for each link create new features using feature engineering techniques like no of followers, followed back, cosine similarity, Jaccard similarity, page rank, katz score, adar index, some svd fetures of adj matrix, some weight features etc. and trained ML models based on these features to predict link. 
- Some reference papers and videos :  
    - https://www.cs.cornell.edu/home/kleinber/link-pred.pdf
    - https://www3.nd.edu/~dial/publications/lichtenwalter2010new.pdf
    - https://kaggle2.blob.core.windows.net/forum-message-attachments/2594/supervised_link_prediction.pdf

### Business objectives and constraints:  
- No low-latency requirement.
- High Precision and Recall. 
- Probability of prediction is useful to recommend highest probability links.

### Performance metric for supervised learning:  
- Both precision and recall is important so F1 score is good choice
- Confusion matrix
