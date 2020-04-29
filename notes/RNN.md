### RNN: predict the current based on the previous data
a multiple copy of the same network that recevies inputs at different times as well as it's hidden state
! [avatar](img\RNN_.png)
! [avatar](img\ex_3steps.png)
**activations** 
    1. sigmoid: limited data in (0,1); vanishing gradients(derivative)
    2. ReLu: x<0 derivative=0
    3. leaky RuLu: x<0 derivative=0.01x
    4. tanh : (-1,1)
! [avatar](img\activation.png)
#### LSTM
1. **Constructure**
    * forget gate: how much we keep the old memory(sigmoid) ft
    ! [avatar](img\LSTM.png)
    * input gate: how much to add to the new memory (sigmoid) it
    ! [avatar](img\LSTM_i.png)
    * generating the new memory Ct
    ! [avatar](img\LSTM_i2.png)
    * calculating the output
    ! [avatar](img\LSTM_output.png)
    * output gate: how much to output
    ! [avatar](img\LSTM_og.png)
    ! [avatar](img\LSTM_og2.png)
2. **Variants**
    * cell state
    ! [avatar](img\LSTM_variant.png)
    **modification**: only forget when you input something to suppliment that part---use the forget gate to decide the input gate
    ! [avatar](img\LSTM_ft_it.png)
#### Seq2Seq models
input->|Encoder|->|Decoder|->output
! [avatar](img\Seq2seq.png)
#### attention operation
    1. Element-Wise Multiplcation->sum across hidden