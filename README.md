# Finding Short-term synaptic plasticity in Steinmetz dataset

### What is Short-term Synaptic Plasticity?
Short-term synaptic plasticity is a temporal increase or decrease of synaptic strength in response to use, modulating the efficacy of synaptic transmission on timescales from a few milliseconds to several minutes. 

### Objectives
Find synaptic facilitation and depression within firing rates of neurons in Steinmetz dataset.

#### How did we achieve it?
To find STP (Short-term synaptic plasticity) we used steinmetz dataset, as it contained favourable data-points i.e., spiking data across different trials, time bins and stim onset. As well as response (correct, incorrect and no response)

These data-points help us to calculate the firing rate for each neuron and even go further to calculating firing rates for each response category and plot them to understand the neural plasticity. 

##### Dataset
[Refer to the dataset and data-points used](https://colab.research.google.com/github/NeuromatchAcademy/course-content/blob/main/projects/neurons/load_steinmetz_decisions.ipynb#scrollTo=h4xiszYEXcht)

##### Method of calculation
Finding plasticity from spiking data is challenging. Traditional thought is there will be more than usual firing after brief trials once the mouse starts to learn. 

Which is a good idea but not complete. We used a method proposed in the paper **Measuring synaptic transmission and plasticity with fEPSP recordings in behaving mice.** Via taking the normalised slope aka *Quantification of short-term synaptic plasticity (STP) is typically done by measuring the slope of each response and normalizing it to the slope of the first response. Synaptic facilitation is defined as a ratio greater than one and synaptic depression is defined as a ratio smaller than one.*

**Notebook for the experiment & results:** [notebook](Neuronal_Plasticity.ipynb)

![image](https://github.com/sleepingcat4/plasticity-stp/assets/81933585/6b2568fe-872f-4109-9a41-8e42dd77653e)


**From the normalisation values we infer our results and find these conclusions for session 12 rodent neural activity and response.**

* Response Category: -1
  First Response Slope: 159.067309
  Average Normalized Slope for Neurons: 0.429314

* Response Category: 0
  First Response Slope: -2.029221
  Average Normalized Slope for Neurons: -24.984074

* Response Category: 1
  First Response Slope: 29.215513
  Average Normalized Slope for Neurons: 2.519253




**From our analysis of the graph, short-term synaptic plasticity is indeed happening for all the three trials (facilitation or depression).**

* In response -1, the slope is less than 1, indicating a decrease in firing rate over time. suggesting synaptic depression.

* In response 0, value of the slope is -1, suggesting a significant decrease in firing rate, suggesting synaptic depression

* In response 1, the normalisation slope value is more than 1, suggesting a short-term synaptic facilitation.

