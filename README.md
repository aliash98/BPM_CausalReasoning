This repository contains an implementation of BP-CDM introduced in

**"Data-Driven Decision Support for Business
Processes: Causal Reasoning on Interventions"**

by: *Ali J. Alaee, Avigdor Gal, Matthias Weidlich, and Arik Senderovich*

*Abstract:
Various types of decisions influence the execution of a business process in terms of control-flow, resource assignments, etc. Data recorded during process execution can be used to identify which decisions are informed by data, predict their outcome, and use interventions to influence them. Yet, existing business process models offer limited decision, focusing on modelling of causal effects while mostly neglecting decision identification and reasoning about interventions. In this paper, we fill this gap, introducing a business process causal decision model that generalizes existing models for decision support by incorporating latent variables and by capturing the stochastic nature of decisions. Using this model, we show how to characterize whether a decision can be analyzed using available data, how to conduct interventional outcome prediction, and how to improve decision-making by acquiring missing data to increase the utility of possible interventions. We demonstrate the feasibility of our approach through experiments with a real-world dataset.*


Notebooks:
- *Identification&Estimation*: A manual identification checking of interventions for Example 1. Then, estimation of the identified estimand with different methods (linear regression, logistic regression, etc).

- *MarkovainToSemiMarkovianGraph*: Converts a Markovian causal graph with colored nodes according to their availability in data (if observed, blue and grey otherwise) to a semi-Markovian graph.

- *IDwithMarkovianInput*: Checks identification (without conditioning) of any query based on a Markovian causal graph (that may contain unobserved variables) and returns all possible adjustment sets if the query is not identified. ID algorithm from YLearn package was employed to check identification upon a semi-Markovian causal graph.

- *IDCwithMarkovianInput*: Checks conditional identification of any input query based on a Markovian causal graph (that may contain unobserved variables) and returns all possible minimal adjustment sets if the query is not identifiable. IDC algorithm was borrowed from the following github repository: https://github.com/mattez90/IDC-algorithm.
