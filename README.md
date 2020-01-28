# Swedish BERT models

Arbetsförmedlingen (The Swedish Public Employment Service) has developed Swedish 
BERT models which were trained on Swedish Wikipedia with approximately 
2 million articles and 300 million words.


## Available Model Types  
  
- `bert-base-swedish-uncased`: 
    12-layer, 768-hidden, 12-heads, 110M parameters
 
- `bert-large-swedish-uncased`:
    24-layer, 1024-hidden, 16-heads, 340M parameters
    

## Usage
The models can be used as part of the [transformers package](https://github.com/huggingface/transformers) 
like any other built-in or community-uploaded model. 

This means that both tokenizer and model can be 
instantiated using the `from_pretrained()` method 
of the BERT-related transformers classes like so:

    pretrained_model_name = 'af-ai-center/bert-base-swedish-uncased'
    
    tokenizer = BertTokenizer.from_pretrained(pretrained_model_name)
    
    # PyTorch
    model = BertModel.from_pretrained(pretrained_model_name)
    
    # TensorFlow
    model = TFBertModel.from_pretrained(pretrained_model_name)
    
  
## Getting Started

The notebook `getting_started_with_swebert.ipynb` shows some more details on how to use the models.

Make sure to run it in a virtual environment with the packages in `requirements.txt` installed.

  
## Remarks
- Note that the corpus that our Swedish BERT models are trained on is significantly
smaller than in the case of the original English BERT models.

- We are part of an ongoing effort to create more sophisticated Swedish BERT models, 
see https://www.ri.se/sv/vad-vi-gor/projekt/sprakmodeller-svenska-myndigheter


## Contact

swebert@arbetsformedlingen.se
