# Udacity-data-analysis-P7


## Project details
The project takes place in the Udacity webpage and the objective is to measure the impact of a change. 
This change is the way a user enrolls into a free trial.
unit of diversion => cookie
tracked by => user-id once enrolled

## Metric choice
* Number of cookies: invariant
* Number of user-ids: 
* Number of clicks: invariant
* Click-through-probability: 
* Gross conversion: evaluation
* Retention: 
* Net conversion: evaluation

Bonferroni: No, because the three evaluation metrics are likely covariant.
the practical significance boundary is 1% given previous work during the lessons

sample size calculator
	http://www.evanmiller.org/ab-testing/sample-size.html