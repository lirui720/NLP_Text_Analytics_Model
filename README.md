# NLP_Text_Analytics_Model

Our methodology can be divided into three major parts: preprocessing, journal summarization, and trend analysis.
During preprocessing, the important steps taken were text cleaning, tokenization, and named entity recognition (NER). For text cleaning, we converted the text to all lowercase, removed any special characters and removed stopwords. In the tokenization step, stopwords and non-alphabetic words are removed. In the named entity recognition step, spaCy is used for the extraction of named entities to visualize the results.
For the journal summarization step, BERT-based extractive model is used by loading a pre-trained summarization model through the transformer’s library. By using the pipeline() function with this model, we created a pipeline for summarization where the cleaned text is processed through the summarizer. A summary is then generated with the cleaned text, at a max length of 130, min length of 30, and the do_sample was set to false to get a deterministic result.
Lastly, for the trend analysis we used topic modelling LDA. The text was first split into equally sized chunks and then applied the preprocessing steps to the chunks. During the preprocessing step, we made sure all characters were changed to lowercase, removed any stop words and non-alphabetic words. A dictionary representation of the chunks was then created, and the chunks were converted into the bag-of-words format. LDA was applied for topic modelling and the topics were printed in an easy-to-read format. We visualized the results using pyLDAvis.
