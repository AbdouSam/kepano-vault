---
categories:
  - "[[Courses]]"
instructor:
  - "[[3blue1brown]]"
platform: "[[youtube]]"
domain:
  - AI
  - Deep Leaning
topics: []
url:
rating:
status:
started:
completed:
created: 2026-04-06
---
# Intro

GPT stands for Generative Pre-trained Transformers.

Transformers are a special kind of NN (Machine learning model) and it is the core invention for the modern AI.

It was developed by Google.

  

There are many kinds of models that you can build using transformers. some models takes audio and outputs text

The original transform is introduced in 2017 by google to convert text from one language to another.

  

These models are prediction models, they take the input and try to predict the next **token**

it all start by the input, it can be text, image or sound.

the input is divided into tokens, text -> words, image -> pixels or chunks, -> audio into 100ms sound bites. these smaller elements are called "tokens".

Each token is associated with a vector, it is a sort of universal language in the model. for example

  

the input as text:

"To date, the cleverest thinker of all time was..." this sentence is split into:

![[Pasted image 20250608160000.png]]

The coordinates of a token are not unique, but they are affected by the context. what is coded in the vector is actually the meaning of the word. which means words of similar meaning or close meaning will be located close to each other in that space.

This sequence first will pass through what is called "Attention block" this will update the values of the vector based on the context. for example the word "bank" can mean

- the bank to put money in

- a river bank, which is the side of a river

- organ bank, which is a storage of biological organs.

the meaning of one word would change, and this is what attention is, it updates the meaning of the words in the sentence by observing all the words in parallel.

  

The next operation is the feedforward or multilayer perceptron, where the vectors do not talk to each other but they are updated individually. this step is like asking a long list of questions to the vector to try and find the meaning and the context for example in our input text. each of the vectors will be asked the following questions and updated accordingly

    1. is token English
    2. it token a verb or noun
    3. is it refer to person, object
    4. is is sub-word of a bigger word
    5. is it reflexive format....

With each of these operations the meaning vector is updated.
This operation is repeated for couple of times, Attention and Feedforward until the end stage. the hope by the end is that, all the essential meanings of the sentence is embedded into the last vector where the model will know exactly what you meant by the text input.

by the end of it, the AI will then make a prediction of the next token.

After the next token is predicted, the input is feed again into the model predicting the next token, then the next ...
  
# Deep learning

To take one step back, deep learning is a science that falls under the machine learning. the basic example of machine learning is simply, given a data set (picture of dogs, names of dogs) the model is trained using back propagation to fine tune the parameters (weights) to best predict the name of the dog for an image that it never saw.

the simplest example is a linear regression, where a line is optimized to go through a data set and get the slope and the intercept to make the most precise prediction.

Linear regression takes 2 parameters, GPT3 for example following the same type of models take 175 billions weights organized in matrices. (different stages)

  

![[Pasted image 20250608161901.png]]

the first stage is embedding with 617 millions of parameters

  

![[Pasted image 20250608162137.png]]

## Stage 1: Embedding

  

the first matrix, the embedding has for example encoded in it 50k words from the dictionary and each words meaning is coded. this method of coding words into numbers existed way before GPT. the idea is to code a word in a space, but the visual representation is impossible because in gpt3 for example the embedding space has 12,228 dimensions.

  

in this space words with similar meaning are close to each other, for example the word man is around the word woman. the diff of the two vectors will be similar to the diff of the vectors king and queen or uncle and aunt. the coding of these words is not random.

  

The embedding matrix was established by training. started random then through training the words "token" started to take shape based on the context of the internet, the stories, the books etc....

For example the word King will have similar context and meaning as words Scotland, medieval times, knights, etc...

  

To jump the last phase before diving to the in-between Unembedding is the reverse step of converting the vectors into actual word through the Unembedding matrix.

  

## Stage 2: Attention

As a recap, transformers task is to keep changing the vector (adjusting the meaning) of a token iteration after iteration until the word will embed in it the meanings required.

for example take the three examples with the word **mole**:

1. American Shrew mole (the mole means here the animal)

2. One mole of carbon dioxide (mole as a unit of measurement in chemistry)

3. Take a biopsy of the mole. (mole is the black dot people have in their skin)

  

At the embedding phase, the word mole in all three examples will have the same vector values, because it is not yet contextualized.

the transformers than will take information from other words in the same input and shift the vector to a more defined location, with each word and each iteration the word is moved more and more into the exact meaning.

mole with Shrew means it is animal, associated with rats and rabbits, then the word American will pin the meaning to exactly what the prompter wanted to say. similarly for other phrases.

Got larger texts, the meaning will embedded further and further meanings from the whole paragraph.