## overview
### Encoder: images to tensors
* use CNN models
    1. Deep residual network(ResNet):Deep 
*  **point**: summary the information -> extract the features
### Attention: compute the weights of the computes
*  it considers the sequence generated thus far, and attends to the part of the image that needs describing next.
1. soft attention：the weights of the pixels add up to 1
### Decoder: tensors to words
* use Recurrent Neural Network (RNN): prediction based on the previous data
    1.  LSTM: Each predicted word is used to generate the next word
        cell state: long-term memory
        hidden state: short-term memory
* attention mechanism: 
    1. look at different parts of the image at different points in the sequence 
    2. **weighted** features indicating where the Decoder should pay attention
### process for generating caption
1. the encoded image and the previous hidden state is used to generate weights for each pixel in the Attention network
2. the previously generated word and the weighted average of the encoding are fed to the LSTM Decoder to generate the next word.
### beam search: choose the most proper one
1. use a linear layer to transform the Decoder's output into a score for each word in the vocabulary.
2. choose a sequence with a highest score