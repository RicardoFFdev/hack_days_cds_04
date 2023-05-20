 <h1 align="center"> "Hotel Chain Cancellation Rating" </h1>

![Getting Started](./img/hotel_chain.png)


# Welcome to my portfolio project for the Community DS data competition: "Hotel Chain Cancellation Rating"


## 1.0 Business Context

Costa del Data is a traditional Spanish hotel chain that currently operates 4 and 5-star hotels nationwide.

The company is concerned about its projections for the coming years, aiming for financial recovery with the end of the restrictions imposed by the Covid-19 pandemic.

With the reopening of borders, the easing of travel restrictions, and the increase in vaccinations, it was expected that the hotel sector in Spain would regain the expected gains.

Contrary to this expectation, Costa del Data has seen an increase in its reservation cancellation rate! The management suspects that there has been a change in cancellation behavior by consumers after the pandemic, which has not yet been understood by the chain.

This has hindered critical strategic actions such as expanding the hotel network, renovating already planned units, and conducting targeted marketing campaigns.

Your team of data scientists has been hired to understand the phenomenon of reservation cancellations. With the results in hand, the marketing team will make more informed decisions, focusing on customer segments with lower cancellation rates, thus reversing the current negative trend.

Based on the historical reservation data, your team is tasked with developing a cancellation prediction model. The model should predict the target variable "Reservation Canceled," returning 1 in case of cancellation and 0 otherwise.

For this competition, disregard recent factors such as armed conflicts, energy price increases, commercial agreements, and budget approvals involving Spain, Europe, or the world.

**Source:** [ Kaggle ](https://www.kaggle.com/competitions/cdshackdays4)


## 2.0 Preliminary Planning

* In this competition, Community DS students were divided into squads of 5 participants each. In total, there were 31 squads and over 180 participants.
* My squad had the following members:

![Squad](./img/squad.png)


### The CRISP-DM method was used as the basis for developing this project.

![Crisp](./img/crisp.jpg)


### 2.1 Tools, IDEs, and Libraries

* Python 3.09
* Visual Studio Code
* Jupyter Notebook
* Deepnote
* Libraries: Seaborn, Pandas, Numpy, Inflection, Scipy, Dython_Nominal, XGBoost, SKLearn, Category Encoders e LightGBM

### 2.2 Final Product

* A classification solution that provides the best possible prediction for a reservation cancellation within the hotel chain. This will enable the hotel chain to make informed decisions based on customer profiles to prevent cancellations of existing reservations.


## 3.0 Data

##### These data are public and were downloaded from the [Kaggle](https://www.kaggle.com/competitions/cdshackdays4).

### 3.1 Source Attributes

| **Attributes**                           |  **Type**  |  **Description**                                            |
| ----------------------------------------|------------|--------------------------------------------------------------|
| id                                      | int64      | Identification number                                        |
| classificacao_do_hotel                  | object     | Hotel rating (number of stars)                               |
| meses_da_reserva_ate_o_check-in         | int64      | Number of months from the reservation date to check-in date  |
| numero_de_pernoites_reservadas          | int64      | Number of reserved nights                                    |
| numero_de_hospedes                      | float64    | Number of guests                                             |
| regime_de_alimentacao                   | object     | Type of included meal plan                                   |
| nacionalidade                           | object     | Nationality                                                  |
| forma_de_reserva                        | object     | Booking channel                                              |
| ja_se_hospedou_anterioremente           | object     | Whether the guest has previously stayed at the hotel         |
| tipo_do_quarto_reservado                | object     | Reserved room type                                           |
| reserva_feita_por_agencia_de_turismo    | object     | Whether the booking was made through a travel agency         |
| reserva_feita_por_empresa               | object     | Whether the booking was made by a company                    |
| reserva_com_estacionamento              | object     | Whether the reservation includes parking for a vehicle       |
| reserva_com_observacoes                 | object     | Special requests made during the reservation                 |
| reserva_cancelada                       | int64      | Target variable indicating if the reservation was cancelled  |


### 3.2 Created Attributes

* room_rating_percentage -> the percentage of room rating between 4 and 5 stars
* meal_plan_combo -> the derived meal plan based on the room type
* nights_per_hotel -> the median value between the reserved room type and the hotel rating.


## Visualization of Numerical Attributes in Bar Graph
![histplot](./img/histplot.png)

## Visualization of Months from Reservation to Check-in Date 
![scatter](./img/scatter.png)

## Visualization of Categorical Attribute Correlation using Cramer's Formula
![cramer](./img/cramer.png)


## Visualization of Categorical Attribute Correlation using Theil's Uncertainty Coefficient
![theil](./img/theil.png)



## 4.0 Data Modelling

In this stage, the data was prepared for the start of the Machine Learning modeling process.<br>
Numerical and categorical rescaling techniques were applied using 'Label Encoder', 'Target Encoder', and 'Robust Scaler'.

## 5.0 Machine Learning Modeling

In the process of selecting Machine Learning models, tests and training were performed using six types of classifiers: Random Forest Classifier, Extra Tree Classifier, XGBoost Classifier, LGBM Classifier, K-Nearest Neighbors, and Decision Tree Classifier.<br>
The evaluation metric used for the classification algorithms was the F1 Score.

## Performance

![perform](./img/score.png)


## 6.0 Ensemble Learning

Here, we applied the technique of Ensemble Learning using the 'Voting Classifier' from the 'Scikit-learn' library.<br>
This algorithm combines the concepts of different Machine Learning classifiers and uses majority voting or averaging of predicted probabilities to make predictions for the target class. This classification can be used to achieve performance symmetry in the overall data balance. In other words, the algorithm leverages the strengths of different Machine Learning algorithms to balance out their weaknesses in classification.

## Final Performance:

# 0.9731184748459742

## 7.0 Conclusão

After 32 hours of Hack Days, submissions were closed and the Leaderboard was finalized.
Our team's work achieved a final accuracy of 0.97146, and we made a total of 21 submissions. The highest score is the one that counts in this type of competition.<br>
In the overall Leaderboard, we secured the 4th position, proving that we were on the right track with our project.
The final ranking was decided in the hundredths place, demonstrating how intense the competition was in the final stretch, and teams were well-balanced and focused on delivering a good final work.<br>
The EquiPÃO dos dados team managed to deliver an excellent work within a fair timeframe, so we have a lot to celebrate.<br>
The learning experience in this short period of time was HUGE!!!
I would like to express my gratitude to my teammates: Samuel, Juli, Valéria, and Wilmara. I also want to thank our teachers and everyone in the DS Community!!!


## Leaderboard

![leaderboard](./img/leaderboard.png)