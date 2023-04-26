# The Question Generator: A System for Generating Questions from Texts

The Question Generator is a system that takes in a text as input and generates questions based on the content of the text. The system comprises three main modules, each of which is described below.
Module 1: Preprocessing

The first module in the Question Generator system is the Preprocessing module. This module performs three key tasks on the input text:

    Stemming: The module reduces words in the text to their root form to simplify analysis.
    Lemmatization: The module identifies the base form of words in the text to reduce the size of the vocabulary and improve analysis accuracy.
    Stop word removal: The module removes common words such as "the", "a", and "an" that do not provide much meaning on their own.

Module 2: Question Generator

The second module in the Question Generator system is the Question Generator module. This module generates questions from the input text by following these steps:

    Textrank: The module uses the Textrank algorithm to extract the most important sentences from the input text.
    Part-of-speech (POS) tagging: The module identifies the nouns and verbs in the selected sentences using POS tagging.
    Fill-in-the-blank question generation: With the help of the nouns and verbs identified in step 2, the module generates fill-in-the-blank questions.

Module 3: Distraction Generator

The third and final module in the Question Generator system is the Distraction Generator module. This module is responsible for generating distractors for multiple-choice questions. The module operates as follows:

    Input: The module takes a word as input, which is provided by the Question Generator module.
    Preprocessing: The module preprocesses each sentence to extract only the nouns and verbs per sentence.
    Cosine similarity: The module uses cosine similarity, which is calculated using the TF IDF value, to identify the three most similar words in the input text. These words are used as distractors for multiple-choice questions.
