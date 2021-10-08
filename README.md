# Sleep-EDF-DeepSleepNet
* Dataset used was Sleep-EDF dataset  it contained more than 8 gb of data out of which used around 500 mb data and has around 20 peoples data from age effects on healty person(SC) dataset for vizualization and training purposes
![_1](https://user-images.githubusercontent.com/71460180/136506370-bc4935d4-3949-44f8-bcb5-391c509ccf41.png)

## Findings from the dataset: 
* More than 50% times the person was awake, and while sleeping S2, ReM are more common to occur
* In Power spectral density plot of epochs grouped by sleeping stage, different sleep stages have different sigenatures but these remain same accross different datasets

![_2](https://user-images.githubusercontent.com/71460180/136506790-a46353c6-3670-4ac2-b9fc-2a8851d2c1b8.png)

## Model
The model used for training was deepsleepnet,which automatates the process of sleep stage based on raw, single channel EEG
link: https://github.com/akaraspt/deepsleepnet 
## Preprocessing and assumptions
Steps taken while preprocessing the data and assumptions: 
* Merged the N3 and N4 stages into a single stage Sleep stage 3/4 due to high similarity between them
* There were long periods of awake or stage W at the start and the end of each recording, in which a subject was not sleeping. Only included 30 minutes of  such periods just before and after the sleep periods, as we were interested in sleep periods.
* Excluded MOVEMENT and UNKNOWN (which were at the start or the end of the each recording) stages, as they did not belong to the five sleep stages and had little relevance
## Evaluation
evaluations:
* training_accuracy: 0.883
* test_accuracy: 0.8257

