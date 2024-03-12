# Sigma-Internship-Coding-Challenge

This repository contains the solution to the Sigma Internship Coding Challenge, which involves building a simple trading model using the Quantrocket platform. The goal is to make decisions on certain days based on a predefined logic to maximize portfolio value.

## Data Retrieval:

Utilized Quantrocket to pull daily close prices for Apple stock (symbol='AAPL') for the year 2023 (01-01-2023 to 12-31-2023).

## Data Analysis:

Computed daily returns and classified states (Bull, Flat, Bear) based on predefined rules.
Visualized the distribution of states throughout the dataset.

## Portfolio Value Calculation:

1. Assumed an initial portfolio value of 0 at the start of 2023.
2. The portfolio value gets incremented only when a buy order is placed on day d+1 and if s(d+1) = 1 & s(d) = 0.
3. So to maximize the buy value ,we place buy orders only when the above condition is met.
4. On all other days , we do not place buy orders so the portfolio value does not change

## Transition Matrix:
1. The process is modelled as a markov chain and transition matrix is computed.
2. The number of times each transition occurs is computed and stored in the transition matrix in the corresponding position
3. Finally,the transition matrix is normalised.
## Results
- Final Portfolio Value: 40
- Optimal Buy Indices: [6, 8, 12, 16, 21, 28, 30, 41, 50, 52, 59, 61, 69, 79, 85, 88, 94, 100, 103, 108, 110, 113, 117, 120, 123, 133, 142, 160, 164, 177, 187, 191, 207, 209, 212, 216, 218, 232, 234, 238]
- Transition Matrix :

    ![image](https://github.com/Vishwa0102/Sigma-Internship-Coding-Challenge/assets/102709553/5a62edc5-8d8a-4802-ba0e-daec3e475f3b)

