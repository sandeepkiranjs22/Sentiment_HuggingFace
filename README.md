## Transformers Introduction

. Transformers provides thousands of pretrained models to perform tasks on texts such as classification, information extraction, question answering, summarization, translation, text generation and more in over 100 languages. Its aim is to make cutting-edge NLP easier to use for everyone.


### Transformers Library installation  - https://huggingface.co/transformers/installation.html


### Code snippet for hugging face - Transformers ( sentiment analysis ) 

```
from transformers import pipeline
classifier = pipeline('sentiment-analysis')

classifier('We are very happy to show you the 🤗 Transformers library.')
```

### Output

[{'label': 'POSITIVE', 'score': 0.9997795224189758}]
