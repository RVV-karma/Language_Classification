# Language_Classification
A NLP project to classify text on the basis of it's language with accuracy of **100%** (on test set and new examples) and confidence higher than **99%**.

## Aim

The aim of this notebook is to create a (Tensorflow) model that can classify the language (English, Spanish, etc.) of a given sentence.

In this notebook, English, Italian, Spanish and French languages are classified.

## Model

I have used a sequential model with following layers in order:

1. Embedding layer with vocab size of 49314 units and embedding dimension of 128 units.
2. Flatten layer.
3. Dense Layer with 256 neurons (activation units).
4. Dropout layer with a dropout factor of 0.2.
5. Dense Layer with 256 neurons (activation units).
6. Dropout layer with a dropout factor of 0.2.
7. Dense Layer with 4 neurons (activation units). This is the output layer.

The optimizer used is Adam with default settings. Batch size was taken as 128.  

## Prediction

The predictions of the model are as follows:  

The sentence ' ['TensorFlow is a free and open-source software library for dataflow and differentiable programming across a range of tasks.'] '
is in ' **English** ' language with  **99.84663724899292 % confidence**.

The sentence ' ['TensorFlow è una libreria software gratuita e open source per il flusso di dati e la programmazione differenziabili in una vasta gamma di attività.'] '
is in ' **Italian** ' language with  **99.95958209037781 % confidence**.

The sentence ' ['TensorFlow es una biblioteca de software gratuita y de código abierto para el flujo de datos y la programación diferenciable en una variedad de tareas.'] '
is in ' **Spanish** ' language with  **99.99784231185913 % confidence**.

The sentence ' ['TensorFlow est une bibliothèque logicielle gratuite et open-source pour le flux de données et la programmation différenciable sur une gamme de tâches.'] '
is in ' **French** ' language with  **99.9789297580719 % confidence**.
