# Sleep-EDF-DeepSleepNet
* Dataset used was Sleep-EDF dataset  it contained more than 8 gb of data out of which used around 500 mb data and had around 20 peoples datat from age effects on healty person(SC) data for vizualization and training purposes

## Findings from the dataset: 
* More than 50% times the person was awake, and while sleeping S2, ReM are more common to occur
* In Power spectral density plot of epochs grouped by sleeping stage, different sleep stages have different sigenatures but these remain same accross different datasets
*  
## Model
The model used for training was deepsleepnet,which automatates the process of sleep stage based on raw, single channel EEG
link: https://github.com/akaraspt/deepsleepnet 
## Preprocessing and assumptions
Steps taken while preprocessing the data and assumptions: (see from the research paper)
* Merged the N3 and N4 stages into a single stage Sleep stage 3/4 due to high similarity between them
* There were long periods of awake or stage W at the start and the end of each recording, in which a subject was not sleeping. Only included 30 minutes of  such periods just before and after the sleep periods, as we were interested in sleep periods.
* Excluded MOVEMENT and UNKNOWN (which were at the start or the end of the each recording) stages, as they did not belong to the five sleep stages and had little relevance
## Evaluation
evaluations:
* metrices used for evaluations are:
* training_accuracy:
* test_accuracy:
* graphs if any

### explain what codes to run to get the results
