### Problem Statement

How accurately can the outcome of a chess game (winner or loser) be predicted by a neural network using only the moves played?

### Executive Summary

This project examines a data set of 20,000 chess games and tries to predict the outcome using a neural network and only the moves played. The moves are in a PGN format, so work needs to be done in order to prepare them for modeling. Data cleaning and preprocessing sections of this notebook handle that by putting the moves into split lists, putting those lists into an array, then tokenizing all unique moves. In addition, exploratory data analysis is conducted in order to gain a better understanding of the data and look into potential concepts to include into the model. Examples of EDA include looking at the distribution of game outcomes, a histogram of average ratings, and examining the most popular chess openings used by all and highly skilled players.

Two neural networks are utilized: an LSTM model and a GRU model. These two models are very similar to each other, but have a few key differences. In the end, the GRU model performs better than the LSTM model; however, both end up being decent models (although the GRU ends up being excellent). The LSTM model is a bit more complex in nature, as more layers were added to it, which can be observed in the notebook. Finally, conclusions, findings, and recommendations are presented based on the model evaluation.

### Conclusions and Recommendations

Overall, I would suggest using a GRU model over the LSTM due to its efficiency, its simplicity relative to the LSTM, and its accuracy. From the two types of models shown, it is evident that predicting the outcome of a chess game only using the moves can lead to an excellent model. This is largely due to the fact that chess moves are deep and interrelated, which the models can pick up on and utilize to predict a game's outcome. There is definitely potential for RNNs to be used for positional evaluation, as taking any set of moves and predicting the winner indicates that they can evaluate the position and make a prediction based on it. 

### Moving Forward

There is quite a bit that can be done to move forward with this project. First, I'd like to continue tuning both the GRU and especially the LSTM model to improve performance and workflow. Running both of these models over more epochs can create more convincing plots for training and validation loss and AUC. Conducting a GridSearch to tune and optimize hyperparameters is something I want to incorporate, which can help with model tuning. In addition, looking into other models, like Conv1D and Conv2D, for positional evaluation is something I really want to do moving forward. It's definitely feasible to turn the moves of a game into an image of a chess board, which a CNN can read and perhaps predict the next move of a game rather than just the winner. I am very interested in chess opening theory, and since openings are deeply tied to moves, it could be an avenue worth exploring. Finally, I want to create a demo app that takes in a set of moves (perhaps on a chess board) and predicts the winner. That is my next step!