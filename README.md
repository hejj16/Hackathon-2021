# Hackathon-2021



**Update on Going ...**



This repository stores the code and results in BioHackathon-2021, aiming to predict the stability of mutated proteins.

The descriptions of this Hackathon can be found [here](https://biohackathon.biolib.com/event/2021-protein-edition).

The data comes from this article https://www.bakerlab.org/wp-content/uploads/2017/12/Science_Rocklin_etal_2017.pdf

This our [team page](https://biolib.com/SVM2/Spaghetti-Vector-Monster-2/). Teammates: [Jiajun He](https://github.com/hejj16), [Zelin Li](https://github.com/lzlniu).

An outline of our work and result can be found [here](https://github.com/hejj16/Hackathon-2021/blob/main/Presentation_Slide.pdf).

A more detailed description is shown below.

<br/>

## Description of the task

- The main task for us is to use the amino acids sequence of mini-protein (43 a.a. length) and their secondary structure information to predict their structural stability.
- The inputs are a.a. sequence (20 kinds of standard a.a., and non-standard, in total 21 kinds) and secondary structure (E, T, H; 3 kinds) sequence.
- This is a regression task and will output the stability score change of the mutated mini-protein (a score proportion to ΔG).


## An outline of our work

We perform 2 kinds of models: Simple Machine Learning Methods and Complex Deep Learning Models with transformer and LSTMs.

### Description of Simple Machine Learning Methods



### Description of Deep Learning Models with transformer and LSTMs



## Results and Plots

### Correlection Coefficient and Plots for each Model:
|Model|Correlation Coefficient for Single Mutation|Correlation Coefficient for Multiple Mutation|
|---|---|---|
|MLP|0.8451|0.3177|
|RF|0.8136|0.3827|
|SVM|0.8350|0.4089|
|Transformer Embedding + LSTMs|**0.8912**|**0.5940**|

Results for Test data of each model is as follows:

**Single Mutation:**
![image](https://github.com/hejj16/Hackathon-2021/blob/main/Plot/Single.PNG)
**Multiple Mutations:**
![image](https://github.com/hejj16/Hackathon-2021/blob/main/Plot/Multiple.PNG)

### The necessity of Secondary Structure
Besides, we explored the necessity of Secondary Structure

## Conclusions and Discussions
- Better feature engineering yields better results. Transformer embedding is better than simple one-hot ecoding in our task.

- Multiple mutation data is harder to predict than single mutation data, especially those protein with a negative score.

- Secondary structure is almost redundant for our task.
  - Possible Reasons:
    - We have only 4 original sequences. So our task can be seen as 4 individual regressions, and the secondary structure only serves as a category label.
    - If the original energies are thought to be similar, then all the information is stored in the mutated amino acid sequence.


## Future Plans


