# bg_cicd_template_test

## Business background

* Who is the client (team / org, not individual)?
* What area / LOB / etc. is the client in?
* What business problems are we trying to address?

## Scope

* What data science solutions are we trying to build?
  * How much or how many? (regression)
  * Which category? (classification)
  * Which group? (clustering)
  * Is this weird? (anomaly detection)
  * Which option should be taken? (recommendation)
* What will we do?
* How is it going to be consumed by the customer?

## Personnel

* Who are on this project:
	* DSCoE:
		* Team lead
		* PM(?)
		* Data scientist(s)
        * ML engineer(s)
	* Client:
		* Business contact
        * Data administrator (if applicable)

## Metrics

* What are the qualitative objectives? (e.g. reduce member costs)
* What is a quantifiable metric?  (e.g. identify likely high-cost claim members)
* Quantify what improvement in the values of the metrics are useful for the customer scenario (e.g. reduce the fraction of users HCCs by 2%) 
* What is the baseline (current) value of the metric? (e.g. current fraction of users with HCCs = 1.2%)
* How will we measure the metric? (e.g. A/B test on a specified subset for a specified period; or comparison of performance after implementation to baseline)

## Plan

* Phases (milestones), timeline, short description of what we'll do in each phase.

## Architecture

* Data
  * What data do we expect we'll need?
  * Is any data not stored in one of the standard data stores (ECW, CareKey, etc.)?
* Data movement from on-prem to Databricks to move either
  * all the data, 
  * after some pre-aggregation on-prem,
  * Sampled data enough for modeling

* How will the score or operationalized web service(s) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
  * Will this be a batch, API, or streaming process?
  * How will the customer use the model results to make decisions?
  * Data movement pipeline in production
  * Make a 1 slide diagram showing the end to end data flow and decision architecture
    * If there is a substantial change in the customer's business workflow, make a before/after diagram showing the data flow.

## Communication
* How will we keep in touch? Weekly meetings?
* Who are the contact persons on both sides?
