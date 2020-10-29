# Transformers
 
Main concepts
The library is built around three types of classes for each model:

Model classes such as BertModel, which are 30+ PyTorch models (torch.nn.Module) or Keras models (tf.keras.Model) that work with the pretrained weights provided in the library.

Configuration classes such as BertConfig, which store all the parameters required to build a model. You don’t always need to instantiate these yourself. In particular, if you are using a pretrained model without any modification, creating the model will automatically take care of instantiating the configuration (which is part of the model).

Tokenizer classes such as BertTokenizer, which store the vocabulary for each model and provide methods for encoding/decoding strings in a list of token embeddings indices to be fed to a model.

All these classes can be instantiated from pretrained instances and saved locally using two methods:

from_pretrained() lets you instantiate a model/configuration/tokenizer from a pretrained version either provided by the library itself (the supported models are provided in the list here or stored locally (or on a server) by the user,

save_pretrained() lets you save a model/configuration/tokenizer locally so that it can be reloaded using from_pretrained().
