### RNN: predict the current based on the previous data
a multiple copy of the same network that recevies inputs at different times as well as it's hidden state
! [avatar](notes\img\RNN_.png)
! [avatar](notes\img\ex_3steps.png)
**activations** 
    1. sigmoid: limited data in (0,1); vanishing gradients(derivative)
    2. ReLu: x<0 derivative=0
    3. leaky RuLu: x<0 derivative=0.01x
    4. tanh : (-1,1)
! [avatar](notes\img\activation.png)
#### LSTM
1. **Constructure**
    * forget gate: how much we keep the old memory(sigmoid) ft
    ! [avatar](notes\img\LSTM.png)
    * input gate: how much to add to the new memory (sigmoid) it
    ! [avatar](notes\img\LSTM_i.png)
    * generating the new memory Ct
    ! [avatar](notes\img\LSTM_i2.png)
    * calculating the output
    ! [avatar](notes\img\LSTM_output.png)
    * output gate: how much to output
    ! [avatar](notes\img\LSTM_og.png)
    ! [avatar](notes\img\LSTM_og2.png)
2. **Variants**
    * cell state
    ! [avatar](notes\img\LSTM_variant.png)
    **modification**: only forget when you input something to suppliment that part---use the forget gate to decide the input gate
    ! [avatar](notes\img\LSTM_ft_it.png)
#### Seq2Seq models
input->|Encoder|->|Decoder|->output
! [avatar](notes\notes\img\Seq2seq.png)
