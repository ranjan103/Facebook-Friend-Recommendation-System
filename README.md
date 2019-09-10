
# Facebook-Friend-Recommendation-using-Graph-Mining
### Problem statement:

Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)

Data Overview
Taken data from fakebook’s recruiting challenge on Kaggle https://www.kaggle.com/c/FacebookRecruiting
data contains two columns source and destination each edge in graph

- Data columns (total 2 columns):  
- source_node         int64  
- destination node    int64  

Mapping the problem into supervised learning problem:
Generated training samples of good and bad links from given directed graph and for each link got some features like no of followers, is he followed back, page rank, katz score, adar index, some svd features of adj matrix, some weight features etc. and trained ml model based on these features to predict link.

### Some reference papers and videos:

      https://www.cs.cornell.edu/home/kleinber/link-pred.pdf
      https://www3.nd.edu/~dial/publications/lichtenwalter2010new.pdf
      https://kaggle2.blob.core.windows.net/forum-message-attachments/2594/supervised_link_prediction.pdf
      https://www.youtube.com/watch?v=2M77Hgy17cg

### Business objectives and constraints:
      #### No low-latency requirement:   
            Given a pair of users U1 and U2, we are not hurry to predict if they follow each other.
      
      #### Probability of prediction is useful to recommend highest probability links
            create probability rank to show how much % wise user will be following. Maybe I show top 5 users to follow based on                     probability.
           
      #### Performance metric for supervised learning:
      #### Both precision and recall are important so F1 score is good choice, we could be using top K or precision. 
      #### Confusion matrix

### Input Data:
   https://www.kaggle.com/c/FacebookRecruiting/data

## FB-Challenge:
  We have been given direct graph. No indirect graph

This example is of a supervised learning problem. Supervised learning is where you have input variables (x) and an output variable (Y) and you use an algorithm to learn the mapping function from the input to the output.

#### Steps:
Given a pair of vertices, common vertices being followed by both U1 and U2 if 
U1 -> {U3, U4, U5}
U2 -> {U3, U4, U6}
In above graph, U3, U4 are common.
U1, U2 features:
Number of common vertices being followed By U1 and U2.
come up with graph-based features. 

  
