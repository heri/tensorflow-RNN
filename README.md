# TensorFlow-RNN

**Only for personal research**

This tries to assigns a probabilities to sentences. It does so by predicting next words in a text given previous words.

It uses Google's TensorFlow to implement recurrent neural networks in language modeling. The dataset is english language (Penn Tree Bank)

## Usage

Install [Bazel](http://bazel.io/docs/install.html)

Install tensorflow

`pip install https://storage.googleapis.com/tensorflow/mac/tensorflow-0.5.0-py2-none-any.whl`

Compile the library:

`bazel build -c opt ptb:ptb_word_lm`

Run the model

`bazel-bin/ptb_word_lm \
  --data_path=simple-examples/data/ --alsologtostderr --model small`

  You can try to change the size of model to medium or large instead. This will change the size of LSTM. The small model should be able to reach perplexity below 120 on the test set and the large one below a nice 80, though it might take several hours to train!
