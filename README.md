# Generating_TV_Scripts

This project was developed as a part of Udacity's Deep Learning Nanodegree. In this project, i have created a Recurrent neural network from scratch using pytorch. In this project, i generated my own Seinfeld TV scripts using RNNs. I used a Seinfeld dataset of scripts from 9 seasons. The Neural Network i built will generate a new, "fake" TV script.

## Getting Started

Just run the ipynb notebook. Tune the hyper parameters for better accuracy.
<img src='/seinfeld.jpg' width=500 px>

### Prerequisites

* Python 3
* Numpy
* Pandas
* MatPlotLib
* OpenCv
* Pytorch 

### Install

1. Download the project materials from our GitHub repository. You can get download the repository with
  ```
  git clone https://github.com/vickipedia6/Generating_TV_Scripts.git
  ```
 2. Download anaconda or miniconda based on the instructions in the [Anaconda documentation](https://docs.anaconda.com).
 
 3. Create a new conda environment:
  ```
  conda create --name deep-learning python=3
  ```
 4. Enter your new environment:
  * Mac/Linux: >> ``` source activate deep-learning ```
  * Windows: >>  ```activate deep-learning ```
  
 5. Ensure you have numpy, matplotlib, pandas, and jupyter notebook installed by doing the following:
  ```
  conda install numpy matplotlib pandas jupyter notebook
  ```
 6. Run the following to open up the notebook server:
  ```
  jupyter notebook dlnd_tv_script_generation.ipynb
  ```
 7. Execute all the cells in the code.
 
### Architecture

* Tried both GRU and LSTM. LSTM performed better than GRU.

### Project results

This project has met the following specifications:
* The submission includes all required, complete notebook files.
* All the unit tests in project have passed.
* The function create_lookup_tables creates two dictionaries:
   - Dictionary to go from the words to an id, we'll call vocab_to_int
   - Dictionary to go from the id to word, we'll call int_to_vocab
   - The function create_lookup_tables return these dictionaries as a tuple (vocab_to_int, int_to_vocab).
* The function token_lookup returns a dict that can correctly tokenizes the provided symbols.
* The function batch_data breaks up word id's into the appropriate sequence lengths, such that only complete sequence lengths are constructed.
* In the function batch_data, data is converted into Tensors and formatted with TensorDataset.
* Finally, batch_data returns a DataLoader for the batched training data.
* The RNN class has complete __init__, forward , and init_hidden functions.
* The RNN must include an LSTM or GRU and at least one fully-connected layer. The LSTM/GRU should be correctly initialized, where         relevant.
* Enough epochs to get near a minimum in the training loss, no real upper limit on this. Just need to make sure the training loss is low   and not improving much with more training.
* Batch size is large enough to train efficiently, but small enough to fit the data in memory. No real “best” value here, depends on GPU   memory usually.
* Embedding dimension, significantly smaller than the size of the vocabulary, if you choose to use word embeddings
* Hidden dimension (number of units in the hidden layers of the RNN) is large enough to fit the data well. Again, no real “best” value.
* n_layers (number of layers in a GRU/LSTM) is between 1-3.
* The sequence length (seq_length) here should be about the size of the length of sentences you want to look at before you generate the   next word.
* The learning rate shouldn’t be too large because the training algorithm won’t converge. But needs to be large enough that training       doesn’t take forever.
* The printed loss should decrease during training. The loss should reach a value lower than 3.5.
* There is a provided answer that justifies choices about model size, sequence length, and other parameters.
* The generator code generates a script.

## Losses

###Model :
Training loss: 3.32

## Generated Script

jerry:...

elaine: what?

jerry: i didn't know...

george: well, you can have said hi.(to elaine) hey, hey, you know what?

jerry: what are you talking about? i got a lot of money on the street.

jerry: well.

jerry: i can't.

elaine: oh, no.

newman: well i was thinking of the worst thing.

kramer:(to jerry) you don't know what i mean.

george: i don't know.

kramer:(looking at the woman) oh yeah?

george: yeah, but i don't think so!

george: you don't have any idea.

jerry: oh, i don't know. i just wanted you to know what it is.

kramer: i thought they had the same time.

jerry: well, i don't know if i can.

elaine: i don't know. i don't want a.

jerry:(to george) you know, you know, i think you could get it.

george:(sarcastic) yeah, i think you may have been in.

george: i know.

jerry: i don't know.

kramer: well, you can't.

jerry:(to jerry) oh, hi, elaine.

elaine:(to jerry) i don't know.. i don't know, jerry, i'm not gonna have this job. i don't want you to be in this relationship.

elaine: oh yeah, that's right...(he exits)

elaine:(looking at the box of paper) you see, you know, i don't have any idea, you should be ashamed of yourself.

george: oh, no..

jerry:(to george) you see, you're the guy.......

jerry: yeah, i know...

kramer:(to elaine) you know, you know what i mean,

## Built With

* Python 3

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* The data comes from Udacity.
