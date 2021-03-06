



# Machine Learning



## Recap

**Prev**: Comparing data

- 321 Lecture Simple regression
- 322 Lecture Assessing regression assumptions
- 323 Lecture Multiple regression
- 324 Practical session

**Now**: Machine Learning

- What's Machine Learning?
- Types
- Limitations



## Definition

<br/>
*"The field of machine learning is concerned with the question of how to construct computer programs that automatically improve with experience."*

Mitchell, T. (1997). Machine Learning. McGraw Hill.


## Origines


- **Computer Science**: 
    - how to manually program computers to solve tasks

- **Statistics**:
    - what conclusions can be inferred from data

- **Machine Learning**:
    - intersection of **computer science** and **statistics**
    - how to get computers to **program themselves** from experience plus some initial structure
    - effective data capture, store, index, retrieve and merge 
    - computational tractability

<font size="4">
Mitchell, T.M., 2006. The discipline of machine learning (Vol. 9). Pittsburgh, PA: Carnegie Mellon University, School of Computer Science, Machine Learning Department.
</font>


## Types of machine learning

Machine learning approaches are divided into two main types

- **Supervised**
    - training of a *"predictive"* model from data
    - one attribute of the dataset is used to "predict" another attribute
    - e.g., classification

- **Unsupervised**
    - discovery of *descriptive* patterns in data
    - commonly used in data mining
    - e.g., clustering



## Supervised

:::::: {.cols data-latex=""}

::: {.col data-latex="{0.5\textwidth}"}

- Training dataset
    - input attribute(s)
    - attribute to predict
- Testing dataset
    - input attribute(s)
    - attribute to predict
- Type of learning model
- Evaluation function
    - evaluates difference between prediction and output in testing data

:::

::: {.col data-latex="{0.5\textwidth}"}

<center>
![](images/MnistExamples.png){width=90%}

<br/>
<font size="4">	
by Josef Steppan<br/>
via Wikimedia Commons,<br/>
CC-BY-SA-4.0
</font>
</center>

:::
::::::



## Unsupervised

:::::: {.cols data-latex=""}

::: {.col data-latex="{0.5\textwidth}"}

- Dataset
    - input attribute(s) to explore
- Type of model for the learning process
    - most approaches are iterative
    - e.g., hierarchical clustering
- Evaluation function
    - evaluates the quality of the pattern under consideration during one iteration

:::

::: {.col data-latex="{0.5\textwidth}"}

<center>
![](images/DBSCAN-Gaussian-data.png){width=90%}

<br/>
<font size="4">	
by Chire<br/>
via Wikimedia Commons,<br/>
CC-BY-SA-3.0
</font>
</center>

:::
::::::


## ... more

- **Semi-supervised learning**
    - between unsupervised and supervised learning
    - combines a small amount of labelled data with a larger un-labelled dataset
    - continuity, cluster, and manifold (lower dimensionality) assumption

- **Reinforcement learning**
    - training agents take actions to maximize reward
    - balancing
        - exploration (new paths/options)
        - exploitation (of current knowledge)


## Neural networks

:::::: {.cols data-latex=""}

::: {.col data-latex="{0.5\textwidth}"}

Supervised learning approach simulating simplistic neurons

- Classic model with 3 sets 
    - input neurons
    - output neurons
    - hidden layer
        - combines input values using **weights**
        - **activation function**
- The **traning algorithm** is used to define the best weights

:::

::: {.col data-latex="{0.5\textwidth}"}

<center>
![](images/ANN_description.png){width=70%}

<br/>
<font size="4">	
by Egm4313.s12 and Glosser.ca<br/>
via Wikimedia Commons,<br/>
CC-BY-SA-3.0
</font>
</center>

:::
::::::


## Deep neural networks

:::::: {.cols data-latex=""}

::: {.col data-latex="{0.5\textwidth}"}

Neural networks with **multiple hidden layers**

The fundamental idea is that *"deeper"* neurons allow for the encoding of more complex characteristics

<font size="4">	
**Example**: De Sabbata, S. and Liu, P. (2019). [Deep learning geodemographics with autoencoders and geographic convolution](https://www.researchgate.net/publication/334251358_Deep_learning_geodemographics_with_autoencoders_and_geographic_convolution). In proceedings of the 22nd AGILE Conference on Geographic Information Science, Limassol, Cyprus.
</font>

:::

::: {.col data-latex="{0.5\textwidth}"}

<center>
![](images/Colored_deep_neural_network-01.png){width=70%}

<br/>
<font size="4">	
derived from work by Glosser.ca<br/>
via Wikimedia Commons,<br/>
CC-BY-SA-3.0
</font>
</center>

:::
::::::


## Convolutional neural networks

Deep neural networks with **convolutional hidden layers**

- used very successfully on image object recognition
- convolutional hidden layers *"convolve"* the images
    - a process similar to applying smoothing filters

<font size="4">	
**Example**: Liu, P. and De Sabbata, S. (2019). [Learning Digital Geographies through a Graph-Based Semi-supervised Approach](https://www.researchgate.net/publication/336021293_Learning_Digital_Geographies_through_a_Graph-Based_Semi-supervised_Approach). In proceedings of the 15th International Conference on GeoComputation, Queenstown, New Zealand.
</font>

<center>
![](images/Typical_cnn.png){width=70%}

<br/>
<font size="4">	
by Aphex34 via Wikimedia Commons, CC-BY-SA-4.0
</font>
</center>


## Limits

:::::: {.cols data-latex=""}

::: {.col data-latex="{0.5\textwidth}"}

- Complexity
- Training dataset quality
    - garbage in, garbage out
    - e.g., [Facial Recognition Is Accurate, if You’re a White Guy](https://www.nytimes.com/2018/02/09/technology/facial-recognition-race-artificial-intelligence.html) by Steve Lohr (New York Times, Feb. 9, 2018)
- Overfitting
    - creating a model perfect for the training data, but not generic enough to be useful

:::

::: {.col data-latex="{0.5\textwidth}"}

<center>
![](images/Overfitting.svg.png){width=100%}

<br/>
<font size="4">	
by Chabacano<br/>ia Wikimedia Commons,<br/>CC-BY-SA-4.0
</font>
</center>

:::
::::::


## Summary

Machine Learning

- What's Machine Learning?
- Types
- Limitations

**Next**: Centroid-based clustering

- K-means
- Fuzzy c-means
- Geodemographic classification


