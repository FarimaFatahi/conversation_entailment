# Conversation Entailment
For this project, we used a Roberta-large model that has been pre-trained on the MultiNLI benchmark. MultiNLI is a collection of sentence (premise, hypothesis) pairs that have been annotated with textual entailment information. The Roberta-large model consists of 24 transformers from which we freeze the first 16 transformers.
Then we applied a binary classifier on top of the transformer. Our model learns the parameters of this binary classifier along with the parameters of the last 8 transformers. After hyper-parameter tuning, the model configuration that leads to the best performance is as follows:

Model | Pre-trained | Accuracy
--- | --- | --- 
RobertaClass | Roberta-large-mnli | 80.76%

How to run the code:
• Sequentially running the cells should produce the same results.
• Please pay attention to the dev/test file locations.
