# Implementing Recurrent Neural Network from Scratch

This branch is written by Lanpay and implement a new structure to process RNNs.

The source code is in *rnnlm2.py*, *rnn2.py*, *layer2.py*.

This implementation has serveral modifications as follows:
- Implement a new RNN layer which holds its own params like U, W and layers through time.
- Implement a new RNN unit layer which can calculate forward and backward.
- Implement a new Output layer.
- Using this implementation, we can define multipile rnn hidden layers.

The forward and backward process will use sequencial x and y for each rnn layer.
As we can see as follows, forward function and bptt function will both receive list parameters. 
And each xlist is a list of word of one specific sentencen.

```python
class RNNLayer(object):
    # ...
    def forward(self, xlist):
        #...

    def bptt(self, dslist):
        #...

```

New commitment:
- Implement LSTM network without peepholes.
- LSTM cell Includes an InputGate, an OutputGate, a ForgetGate.

The source code is in *rnnlm3.py*, *rnn3.py*, *layer3.py*.
The bptt algorithm of lstm is quite complicated, so it really takes time to get it through.

![](figures/lstm1.png)
![](figures/lstm2.png)
![](figures/lstm3.png)


