# ShakespeareNLP

## Dataset(shakespeare.txt)
- This dataset contains 154 different Shakespearean sonnets(follow a specific meter called iambic pentameter).

## Shakespeare NLP Notebook

This notebook shows several different steps/methods that I have implemented/attempted.
I have loaded the dataset into the list consisted of list of strings(one sonnet per cell).

### Syllable tokenization

This was one of my attempts to improve the model and divided each string into every syllables and record the number of syllables per string. This could be utilized on the further improvements.

### Character level RNN

I have divided every string into each character and  assigned unique index to each unique character and converted each character into a numeric value(string -> vector of numeric values).

My RNN was trained for 20 epochs and trained by inputting sequences of 40 characters and expecting to output 40 characters sequence.
For the training time, I have skipped every 7 steps.
I have used cross-entropy loss to optimize the model.

### Word level RNN

Instead of using each character, I have tokenized every string into every word(including punctuation) and  assigned a unique index to each unique w,ord and converted each character into a numeric value(string -> vector of numeric values).

My RNN was trained for 20 epochs and trained by inputting sequences of 10 words and expecting to output the next 10-word sequence.
I have used cross-entropy loss to optimize the model.

To improve the model, I have added extra 2 layers of LSTM to our RNN model which had lower training loss over the same epochs of training process and qualitatively better result.
