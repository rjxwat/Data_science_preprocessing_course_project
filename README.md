# About the Dataset
The dataset under consideration has a distinct problem, as each row represents a single point in time and the condition of the order book at that particular 5ms interval. Creating a predictive framework that can precisely predict the direction of the "mid" price—a critical statistic that denotes the middle point between the best bid and ask prices—is the main objective. In particular, each timestep must be categorized as either a possible increasing trajectory (designated as "1") or a static or falling trajectory (designated as "0").
## Terminologies in Dataset
•id - The timestep ID of the order book features. <br />
•mid - the "mid" price, which is the average of the best bid (bid1) and the best ask (ask1) prices. <br />
•opened_position_qty - In the past 500ms, how many buy orders were filled?
•closed_position_qty - In the past 500ms, how many sell orders were filled?
•transacted_qty - In the past 500ms, how many buy+sell orders were filled?
•d_open_interest - In the past 500ms, what is (#buy orders filled)- (#sell orders filled)?
•bid1 - What is the 1st bid price (the best/highest one)?
•bid[2,3,4,5] - What is the [2nd, 3rd, 4th, 5th] best/highest bid price?
•ask1 - What is the 1st ask price (the best/lowest/cheapest one)?
•ask[2,3,4,5] - What is the [2nd, 3rd, 4th, 5th] best/lowest/cheapest ask price?
•bid1vol - What is the quantity of contracts in the order book at the 1st bid price (the best/highest one)?
•bid[2,3,4,5]vol - What is the quantity of contracts in the order book at the [2,3,4,5]th bid price (the [2,3,4,5]th best/highest one)?
•ask1vol - What is the quantity of contracts in the order book at the 1st ask price (the best/lowest/cheapest one)?
•ask[2,3,4,5]vol - What is the quantity of contracts in the order book at the [2,3,4,5]th ask price (the [2,3,4,5]th best/lowest/cheapest one)?
•y (unique to training data) - What is the change in the mid price from now to 2 timesteps (approx. 1 second) in the future? "1" means this change is strictly positive, and "0" means the change is 0 or negative.
last_price - the price at which the most recent order fill occurred.
