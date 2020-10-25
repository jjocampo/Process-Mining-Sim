# Reviewing Process Mining using a Simulated Random Process

#### Purpose:   
Explore processing mining to become familiar with techniques and development, as well as understand potential applications. 

#### Sections:   
1. Config - Simply installing pm4py on EBS for SageMaker to user (not cool)
2. Process Minining a Simulated Random Process (kind of cool)
3. Simple Analytical Methods for Detecting Temporal Process Change (mildly cool?)

#### Methods:   
- This was completed on Amazon SageMaker. This was mostly out of convenience. The pm4py is not readily available on SageMaker, nor is there a real reason to choose SageMaker over other environments. The pm4py can be easily installed on EBS, SageMaker has been configured to seamlessly connect to the GitHub account, and other projects were recently developed here. Hence this was done on SageMaker. 
- A random process was simulated and analyzed using different process mining methods.
- The random process had six forms of the process flow. All begin with 'start' and all terminate with 'end'. There's an 80% chance that the process will follow the first two flows. There's a 14% chance of an approval required on a normal flow. There's a 5% chance of a special approval flow. There's a 1% chance of a process bypass. A random number is used to simulate which flow is followed.   
- 10,000 simulations were completed.   
- The Process Mining techniques Alpha Miner, Inductive Miner, Directly-Follows, and Heuristic Miner were employed. This mostly followed the Towards Data Science article.   
- The simple analytical methods, the above simulation was change to have an interval where the process likelihoods significant changed.   
- Metrics on case counts by event neighbors were taken by temporal windows and simple descriptive statistics determined.   
- Outliers were determined by Z-score.   

#### Results: 
- Process mining is cool
- Challenge is in data prep (isn't it always)
- Simple analytical methods did the trick, but won't perform well on more complex tasks, but can be built upon to employ more sophisticated techniques. 

#### Resources:   
- https://pm4py.fit.fraunhofer.de/documentation
- https://towardsdatascience.com/introduction-to-process-mining-5f4ce985b7e5