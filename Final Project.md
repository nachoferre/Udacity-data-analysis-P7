% Final Project - A/B Testing
% Ignacio Ferreras Astorqui
% May 2017

## Introduction
This project consist on the testing of a possible change to the way users enroll on the 15 day trial to any course in the Udacity website. The data I am going to use it is not the real one, but an adaptation with the same results. The technique I am going to use to demonstrate if this change really help or not is A/B testing. For that we are going to have data from multiple users, differentiated into two groups. The control group is going to be people with the old interface, and the experiment group with the new changes applied. This way we are going to compare the results gathered and make a decision based on if these new changes actually help the Udacity users. The data is composed of the page views received, the number of click in the "Start Free Trial" button, the number of people to finalize the enrollment and finally the number of users to start paying for the course (first month at least). We only used the users who paid at least the first month because A/B test are generally fast, and finalizing a course is longer than the calculated time we will see the Duration vs Exposure section.
## Experiment Design
The hypothesis was that this might set clearer expectations for students upfront, thus reducing the number of frustrated students who left the free trial because they didn't have enough time—without significantly reducing the number of students to continue past the free trial and eventually complete the course. If this hypothesis held true, Udacity could improve the overall student experience and improve coaches' capacity to support students who are likely to complete the course.
The unit of diversion is a cookie, although if the student enrolls in the free trial, they are tracked by user-id from that point forward. The same user-id cannot enroll in the free trial twice. For users that do not enroll, their user-id is not tracked in the experiment, even if they were signed in when they visited the course overview page.
### Metric Choice
For this project had these features available to choose to be either our invariants or evaluation metrics:
* Number of cookies
* Number of user-ids
* Number of clicks
* Click-through-probability: Number of user-ids to enroll divided by the number of unique cookies.
* Gross conversion: Number of user-ids to enroll divided by the number of unique cookies to click in the "Start Free Trial" button.
* Retention: Number of user-ids to make at least one payment divided by the number of users to enroll.
* Net conversion: Number of user-ids to make at least one payment divided by the number of unique cookies to click in the "Start Free Trial" button.

The number of cookies wasn't chosen to be an evaluation metric given that it provides little information just by itself to be able to see if the experiment is taking any effect. However as an invariant it provides the possibility to make sanity check because the evaluation metrics rely on this metric and it is a population sizing metric.

The number of user-ids doesn't provide any information alone and also we already have a population sizing metric that measures better the number of people to interact with our test. Also it isn't a good evaluation metric because it doesn't give us any information about the possible changes in the number of enrollments.

The number of clicks has been chosen to be an invariant metric because it directly affects the evaluation metrics so this provides a good way to measure the population sizing. I haven't considered it to be a possible evaluation metric given that it doesn't provide enough information by itself to decide if we have achieved our objective. 



List which metrics you will use as invariant metrics and evaluation metrics here. (These should be the same metrics you chose in the "Choosing Invariant Metrics" and "Choosing Evaluation Metrics" quizzes.)

For each metric, explain both why you did or did not use it as an invariant metric and why you did or did not use it as an evaluation metric. Also, state what results you will look for in your evaluation metrics in order to launch the experiment.

### Measuring Standard Deviation
List the standard deviation of each of your evaluation metrics. (These should be the answers from the "Calculating standard deviation" quiz.)

For each of your evaluation metrics, indicate whether you think the analytic estimate would be comparable to the the empirical variability, or whether you expect them to be different (in which case it might be worth doing an empirical estimate if there is time). Briefly give your reasoning in each case.
### Sizing
#### Number of Samples vs Power
Indicate whether you will use the Bonferroni correction during your analysis phase, and give the number of pageviews you will need to power you experiment appropriately. (These should be the answers from the "Calculating Number of Pageviews" quiz.)
#### Duration vs Exposure
Indicate what fraction of traffic you would divert to this experiment and, given this, how many days you would need to run the experiment. (These should be the answers from the "Choosing Duration and Exposure" quiz.)

Give your reasoning for the fraction you chose to divert. How risky do you think this experiment would be for Udacity?

## Experiment Analysis
### Sanity Checks
For each of your invariant metrics, give the 95% confidence interval for the value you expect to observe, the actual observed value, and whether the metric passes your sanity check. (These should be the answers from the "Sanity Checks" quiz.)

For any sanity check that did not pass, explain your best guess as to what went wrong based on the day-by-day data. Do not proceed to the rest of the analysis unless all sanity checks pass.

#### Effect Size Tests
For each of your evaluation metrics, give a 95% confidence interval around the difference between the experiment and control groups. Indicate whether each metric is statistically and practically significant. (These should be the answers from the "Effect Size Tests" quiz.)

#### Sign Tests
For each of your evaluation metrics, do a sign test using the day-by-day data, and report the p-value of the sign test and whether the result is statistically significant. (These should be the answers from the "Sign Tests" quiz.)
#### Summary
State whether you used the Bonferroni correction, and explain why or why not. If there are any discrepancies between the effect size hypothesis tests and the sign tests, describe the discrepancy and why you think it arose.
### Recomendation
Make a recommendation and briefly describe your reasoning.

## Follow-Up Experiment
Give a high-level description of the follow up experiment you would run, what your hypothesis would be, what metrics you would want to measure, what your unit of diversion would be, and your reasoning for these choices.