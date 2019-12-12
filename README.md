# MySymptom: Disease Dictionary
This is a model that can be used to predict symptoms that are closely related to a given symptom. The idea behind the model is that the user enters a symptom, and a list of similar symptoms will appear which the user selects the one that applies the most to them. The database contains a table of diseases and their associated symptoms. Here is how the model is designed:
1. After preprocessing, the data is made into the symptom-disease format from the existing disease-symptom format.
2. Make symptoms the target words and the associated diseases the context words, and use this as the (target word, context word) pair for skipgram generation.
3. After assigning labels of 1 or 0 to the pairs, feed it into the Keras model, which generates new word vectors on top of existing GloVe vectors.
4. Loop through the set of all symptoms in the data set to find out the cosine similarity between the embeddings of the given symptom and current symptom in the loop, and then print out the symptoms with a high similarity score.

# Our Goal
We want to create an extension of this project that will use the symptoms to predict the disease the person is suffering from and redirect them to the associated specialist. We must keep in mind that this model is not intended to be replacement from visiting and being diagnosed by a doctor. It is more so there to help users learn of possible symptoms and diseases so that once they visit their physician, they can help point them in the right direction.

# Conclusion
Unfortunately we were unable to get our code to run properly. Check out our video to explain what steps we took in attempting to get the code to run. https://youtu.be/1wuqV7c7GEk
