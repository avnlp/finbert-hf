# FinBERT Implementation using HuggingFace Transformers
The repository follows the same coding style as the HuggingFace transformers library.
The pre-trained model weights have been taken from the [ProsusAI/finBERT](https://github.com/ProsusAI/finBERT) repository.

A conversion script and config file was written to fetch the original pre-trained weights and load it into an existing PyTorch model. Tests were written to check that the weights for each layer were correctly imported.

The following classes were added to create the PreTrainedModel:
- FinBERTEmbeddings: Used to construct the embeddings from word, position and token_type embeddings.
- FinBERTSelfAttention
- FinBERTEncoder
- FinBERTLMPredictionHead

Classes were created to modify FinBERT for different tasks using the Transformers APIs:
- Masked Language Modelling
- Sequence Classification
- Multiple Choice
- Token Classification
- Question Answering
