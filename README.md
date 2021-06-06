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

This is tested on Python 3.6+, Flax 0.3.2+, PyTorch 1.3.1+ and TensorFlow 2.3+.

```
pip install transformers

```

### Installation with conda

Since Transformers version v4.0.0, we now have a conda channel: huggingface.

hugs Transformers can be installed using conda as follows:

```
conda install -c huggingface transformers
```


## Code snippet for Hugging face - Transformers ( sentiment analysis ) 

```
from transformers import pipeline
classifier = pipeline('sentiment-analysis')

classifier('We are very happy to show you the 🤗 Transformers library.')
```

### Output

[{'label': 'POSITIVE', 'score': 0.9997795224189758}]
