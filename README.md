# Label-Prediction
Use Word2vec and TF-IDF to predict the label

Word2vec is a technique used to find relation between words.
TF-IDF is an algorithm determine the importance of each word in doucuments.

Dataset consists of comments on physics, chemistry and biology topics. the goal is to use Word2vec and TF-IDF together to predict label of comments in test dataset.

To do so the following algorithm is performed:\
1- For all comments in train dataset append corresponding label after each word.\
2- Train Word2vec on paragraphs produced in step 1.\
3- Calculate TF-IDF for test dataset comments.\
4- For each comment in test dataset:\
4.1- For each word in comment find distance of that word with three topics (using word2vec).
    Compute sum for all the words in that comment. This will give one number for each comment. The maximum number specify the label.
    e.g. Assume comments are in [Phy, Cehm, Bio] and for a comment we have [10 20 5], we conclude that this comment is on Chemistry.\
    
    
 Accuracy of this algorithm is measured with Rand Index algorihm. For this dataset it was above 90%.
 
 Note: It's better to do a preprocessing like deleting stop words, etc on datasets.
