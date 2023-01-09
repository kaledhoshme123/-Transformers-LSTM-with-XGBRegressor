# Transformers LSTM with XGBRegressor
The proposed model is able to predict the evaluation of both grammatical coherence, vocabulary and grammatical conventions, so that the evaluation can give each of those criteria a value between 1 and 5, I did not treat the system as a classification process, but rather it was treated as a REGRESSION issue

The current project, is a modification of the previously proposed one https://github.com/kaledhoshme123/A-proposed-model-that-can-predict-the-assessment-of-both-Syntax-Cohesion-Vocabulary-Phraseology-

But at this stage a different concept was used, the methodology included a method of learning transfer, which means training the model sequentially, and gradually gaining experience, instead of training it to discover this during a single training process.
That is, with the modification of the structure of the proposed model, the model was trained according to the following sequence:
[syntax, cohesion, vocabulary, phraseology, grammar, conventions]
That is, training was done initially on the ability to evaluate syntax, and with the experience gained in the ability to evaluate syntax, the model itself was asked to complete its experience in cohesion evaluation training, and also later on, the model was asked to complete its training in order to be able to evaluate vocabulary, and so on.

We note from the proposed methodology, access to a more efficient model with a small error rate.
The proposed methodology relied on the fact that the young child is taught concepts in a gradual manner, and therefore, depending on his knowledge of previous concepts, he can learn new concepts and so on.

The concept here depends on the accuracy of the order of teaching the model, thus in my case I trained according to the sequence [syntax, cohesion, vocabulary, phraseology, grammar, conventions]

But the results can be improved better if the sequence is changed to a more accurate sequence in terms of the sequence of concepts in education.

# Proposed neural network model:
![download - 2023-01-09T122800 186](https://user-images.githubusercontent.com/108609519/211287619-0a4c31b1-ef24-4bc2-b374-b434e110ff57.png)


# Sequential transfer training of the model:
| Attempt | #1    | #2    |
| :---:   | :---: | :---: |
| Training | ![training-1](https://user-images.githubusercontent.com/108609519/211288361-ff1e2de8-4f2a-4998-a13c-016ed24cdb6f.png)   | ![training-2](https://user-images.githubusercontent.com/108609519/211288380-2ac65f8a-9c34-4d4b-b35f-df7414cd2a85.png)   |

| Attempt | #1    |
| :---:   | :---: |
| Training | ![training-3](https://user-images.githubusercontent.com/108609519/211288402-eb87ef8f-4148-40da-bb3d-433f5c3b79d0.png)   |



With the learning transfer sequence of the model, we note that the beginning of each epoch for each new case was better as the error rate was lower than if the training was done from the beginning.
In the end, the model provided much better results than the results obtained in the previous concept.
