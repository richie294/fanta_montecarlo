# fanta_montecarlo
Monte Carlo simulation of fantasy football season based on fantacalcio.it 's FVM rating

In this project, I simulate a championship of 35 games between 8 teams based on the rating 'FVM' of fantacalcio.it . The rating is assigned to a team based on the actual auction between the players. 

For creating the calendar of games, I used itertools library. 

To determine how a match is won based on the rating, I used statistical inference and probability. I determine the standard deviation of the score from the set of scores of the teams (std). I then hypothesize the score of a team in a match is a normal distribution with mean equal to the rating and std equal to a fixed parameter (equal for all teams) times the std. Once the score is determined for each team in each match, a lag is used to determine if the game ends with one of the teams winning or with a draw. The lag is calculated as another parameter times std. 

<n_sims> simulations are then performed and probabilities p are estimated. Implied odds are then calculated as 1/p. 
