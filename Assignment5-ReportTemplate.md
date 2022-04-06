**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:      |  5  |
| -------------- | --- |
| Student Names: |  Nicholas Knapton   |
|                |  Jacob Artuso   |
|                |  Brian Kramer  |
|                |  Colin Christophe   |

# Introduction
In this assignment we have analyzed test data through the use of reliability testing software. We first used a reliability growth assessment tool, C-SFRAT, in order to apply covariate software reliability models in order to select guide models for our data.

Next we created a reliability demonstration chart in order to check whether the mean time to failure was met.
# 

# Assessment Using Reliability Growth Testing 
Model Comparison:
<img src='./media/comparison.PNG'/>

We found the laplace value for each k using the formula<br />
<img src='./laplace.png'/> <br />

Graphing u(k), we were able to determine that the reliability increases until 17, after which the reliability sharply decreases. Therefore the data we should proceed with testing is the range of 0 to 17 because reliability starts to decrease after 17. This could point to the system becoming outdated and may not be reflective of the system's normal operational reliability.
<img src='./Picture1.png'/>

Time-between-failure
<img src='./media/twoModels.PNG'/>

Failure Intensity
<img src='./media/intensityGraph.PNG'/>

Reliability Graph
<img src='./media/reliabilityGraph.PNG'/>

To arive on a target failure rate we started by setting the target to various values starting at 1.0 and going down. Observing the results of the graph along the way, our model showed it was unlikely to reach the target intensity rate until 0.6 then got better at 0.5 then finally we arived at the graph shown below which shows a target failure rate of 0.4.
<img src='./targetFailureRate.PNG'/>

# Advantages/Disadvantages of RDC <br />
The main advantages of RDC are the versatility and efficacy. RDC is excels in both cost and time effectiveness when analyzing system reliability. Using RDC is also advantageous because it allows experimentation with different confidence level values and "what-if" scenarios.
The main disadvantage of using RDC is the inability to determine specific values pertaining to reliability. The RDC is only useful for indicating whether the SUT is in the acceptable range. 
The benefits of using reliability growth analysis


# Assessment Using Reliability Demonstration Chart 
To decide what value we should use for the MTTFmin we looked at what the “Input Event When Observed” value was for the last row of data. Since the value was just below 200,000 (When converted to seconds) and the maximum number of failures we used was 100. We looked for an MTTF that would make the SUT enter the acceptable region on the last “Normalized (Plotted) X Value” without the data points entering the rejection zone. Starting at 2000, we gradually increased our “Per Number of input Events” until we reached a value that satisfies these conditions. This gave us a MTTFmin of 2300. 

We were able to find the MTTF and plot the failures per interval in an RDC. We then plotted double the MTTF as well as half MTTF as shown in the images below. Analysing the graphs, we can see that in the first graph the acceptable failure rate is reached.<br />RDC(normal):
<img src='./RDC1.png'/>
RDC(half MTTF):
<img src='./RDCTwice.png'/>
RDC(twice MTTF):
<img src='./RDCHalf.png'/>
# 
The RDC for the halved MTTF has a much shallower slope and reaches the acceptable region in less normalised time units. The RDC plot for the double MTTF has a steeper slope and therefore reaches the reject region sooner and so it fails.

# Advantages/Disadvantages of RDC <br />
The main advantages of RDC are the versatility and efficacy. RDC is excels in both cost and time effectiveness when analyzing system reliability. Using RDC is also advantageous because it allows experimentation with different confidence level values and "what-if" scenarios.
The main disadvantage of using RDC is the inability to determine specific values pertaining to reliability. The RDC is only useful for indicating whether the SUT is in the acceptable range. 

# Comparison of Results
Comparing the results from part 1 and part 2 we can see somewhat differing results. From part one we arived at a target failure rate of around 0.4 from applying a fitted the model to our data. This was a result we came to from the techniques described in that section. For the Reliability Demonstration Chart, the observed failures entered the green (accept) zone at failure number 92 and normalized input events being 85. This gives us a failure rate of about 1.08, which is greater than the value observed in part 1. However by observing part 2 we can see that the line starts to trend more flat indicating that if we had collected more failure data the ratio of failures and normalized usage units would have approached closer to 0.4 giving us similar outcomes. To conclude these results indicate that the software is acceptable for release at a failure rate of 0.4 for the method in part 1 and 1.08 (although likely would get lower if more data was collected) for the method in part 2.

# Discussion on Similarity and Differences of the Two Techniques
The use of extrapolation in part 1 is a key difference as it attempts to predict future values where part 2 fails to graph any predictive values. Another difference is the use of the Laplace reliability growth chart to find the acceptable range. In the second part, the acceptable range is used by defining a risk profile and calculating the MTTF. Both techniques gave their own valuable insights about the reliability of the system and about the failure data. Another difference was the complexity of the calculations for each part, part one required our group to perform more complex exquations (such as the laplace equation) where as part 2 had almost all equations pre-programmed. Both parts were similiar however, when graphing the reliabilty chart and RDC. Depsite the methods being different both graphs gave similar results. 

# How the team work/effort was divided and managed
This lab was done as a group collaboration, with each member contributing at each stage of the lab. We set specifc times for meeting and worked together at those times.

# Difficulties encountered, challenges overcome, and lessons learned
In this lab we encountered many difficulties both learning the software, but also in understanding what we needed to do. We struggled a lot working out which steps to take next.

# Comments/feedback on the lab itself
This was an interesting and challenging lab.
