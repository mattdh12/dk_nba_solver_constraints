# dk_nba_solver_constraints

In daily fantasy sports and in fantasy sports in general, the general strategy is to maximize the total projected points for a given lineup. This is commonly done by predicting the projected points for each player, then using a linear progamming solver with an objective function to maximize the projected total points. On a basic level, the constraints for these solvers limit the total cost of a lineup and limit the number of players for a lineup.

The goal of this project is to see if this strategy can be improved upon by adding more constraints to the linear solver. These two additional constraints are the lineup ownership totals and the lineup leverage totals.

The general concept of this is similar to game theory concepts. I'll make up an example to explain the idea. Say the general public is betting on the result of a coin toss. Those who predict correctly split the winnings. Before the coin toss, it was leaked that it is a weighted coin. The coin is 60% to land heads and 40% to land tails. Because of this, the public adjusts their predictions. 65% of the public predicts heads and 35% of the public predicts tails. Although heads will happen more frequently, betting tails has the higher expected value. Accurately estimating the public predictions beforehand, betting tails would be correct here. The concept is the same with fantasy sports except it is the lineup fantasy points outcome instead of the coin flip outcome.

In a given fantasy sports contest, about 75% of the field does not make payout. As a result, any models that are built for an entire contest become zero-inflated. Therefore, this project was done in two parts. The first part is to classify lineup characteristics that are expected to make payout. Then once those lineup characteristics are met, the second part is to view which lineup constraints return the highest return on investment.

This project was created for personal use only and should only be used as a reference. This project has already been insightful, but it also has to be noted that the sample sizes are very small. More data will be needed to converge on the favorable lineup constraints.
