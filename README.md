## Transformers Introduction

. Transformers provides thousands of pretrained models to perform tasks on texts such as classification, information extraction, question answering, summarization, translation, text generation and more in over 100 languages. Its aim is to make cutting-edge NLP easier to use for everyone.


## Advantages of Transformers

. High performance on NLU and NLG tasks.

. A unified API for using all  pretrained models.

. Train state-of-the-art models in 3 lines of code.

. Seamlessly pick the right framework for training, evaluation and production.


## Pipelines Introduction

The pipelines are a great and easy way to use models for inference. These pipelines are objects that abstract most of the complex code from the library, offering a simple API dedicated to several tasks, including

1. **Sentiment Analysis:** Indicate if the over all sentence is positive or negative

2. **Question Answering:** Extracts an answer from a text given a question

3. **Masked Language Modeling:** Suggets possible words to fill masked input with provided context

4. **Named Entity Recognition:** For each tokens in the input it will automatically assign them a label

5. **Summarization:** Summarizing a text / an article into a shorter text.



## Transformers Library installation 

### Installation With pip


```
pip install transformers

```

### Installation with conda


```
conda install -c huggingface transformers
```


## Sentiment Analysis with transfomers -- Step by Step explanation


### Step 1: Install Library
The library we need to install is the Huggingface Transformers library. To install Transformers, you can simply run:

```
pip install transformers
```

Note: Huggingface Transformers requires either Pytorch or Tensorflow to be installed since it relies on either one of them as the backend, thus make sure to have a working version before installing Transformers.

### Step 2: Import Library

After you have successfully installed Transformers to your local environment, you can create a new Python script and import the Transformers library. Instead of importing the entire library, we introduce the pipeline module within the library that provides a simple API to perform various NLP tasks and hides all code complexity behind its abstraction layer. To import the pipeline module, we can simply do:


```
from transformers import pipeline
```

### Step 3: Build Sentiment Analysis Pipeline

Now after you import the pipeline module, we can start building the sentiment analysis model and tokenizer using the module. To build it, we can do:

```
sentiment_analysis = pipeline(“sentiment-analysis”)
```

### Step 4: Input Text

We’ve built up our pipeline, now it’s time for us to input the text we want to test for its sentiment. Let’s declare two variables for two sentences, one positive and one negative:

```
pos_text = “I enjoy watching football.”
neg_text = “I dislike cricket.”
```

### Step 5: Perform Sentiment Analysis

Finally, it’s time to classify the sentiments (positive or negative) of our input texts. To perform sentiment analysis, we can run the following:


```
result = sentiment_analysis(pos_text)[0]
print("Label:", result['label'])
print("Confidence Score:", result['score'])
print()


result = sentiment_analysis(neg_text)[0]
print("Label:", result['label'])
print("Confidence Score:", result['score'])

```

### OUTPUT

```
Label: POSITIVE
Confidence Score: 0.9980718493461609
Label: NEGATIVE
Confidence Score: 0.9881595969200134
```



### Complete Code Snippet

```

from transformers import pipeline

sentiment_analysis = pipeline("sentiment-analysis")

pos_text = “I enjoy watching football.”
neg_text = “I dislike cricket.”

result = sentiment_analysis(pos_text)[0]
print("Label:", result['label'])
print("Confidence Score:", result['score'])
print()


result = sentiment_analysis(neg_text)[0]
print("Label:", result['label'])
print("Confidence Score:", result['score'])

```

### Output of Code snippet

```
Label: POSITIVE
Confidence Score: 0.9980718493461609

Label: NEGATIVE
Confidence Score: 0.9881595969200134
```
