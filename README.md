# Deep-ReinforceMent-Learning-Multi-Armed-Bandit-Linear-UCB
This simulation was carried out complete mandatory assignment work using Multi Armed Bandit using contextualization. 


Problem Title: "Opmizing Cancer Treatment with Mul-Armed Bandits" 
Problem Environment 
In the given problem, cancer treatment data set is given. This data set contains prior data which 
captures informa on as given below :  
 Characteris cs which are related to a Cancer disease. 
 For given characteris cs, what type of Cancer Treatment was taken.  
 If selected treatment resulted in SUCCESS of FAILURE and cost (money and me) incurred.  
For given problem descrip on and dataset, we have to iden fy personalized and effec ve treatment 
strategy.  
To solve this problem, we will apply the concept of Mul-Armed Bandit.  
Elaborate on how the cancer treatment clinical trial problem is related 
to the Mul-Armed Bandit (MAB) problem 
Explora on-Exploita on Trade
off 
In cancer treatment trials, diverse approaches (Hormone 
Therapy, Radia on, Chemotherapy, Surgery) are tested in 
different arms. Iden fying the most effec ve strategy amid 
uncertain es mirrors the explora on-exploita on trade-off in 
Mul-Armed Bandit problems 
Explora on: Trying out different treatment arms to gather 
informa on on their efficacies. 
Exploita on: Alloca ng more pa ents to the arms that seem 
most effec ve based on the current knowledge 
Dynamic Resource Alloca on 
The alloca on of resources (research me and funding) across 
diverse treatment arms is crucial in opmizing the clinical trial. 
The Mul-Armed Bandit framework aligns with this need for 
dynamic resource alloca on 
Personalized Treatment 
Strategies 
The goal of iden fying the most efficacious and personalized 
treatment strategies corresponds to the MAB concept of 
learning the opmal ac on for each pa ent or context. MAB 
algorithms naturally adapt to individual pa ent responses over 
me, allowing for personalized treatment assignments 
Minimizing Resource 
Expenditure 
Efficiently alloca ng resources is essen al in both scenarios. 
The MAB framework addresses the challenge of minimizing 
resource expenditure while maximizing the informa on gained 
Budget and Treatment Dura on MAB algorithms can be adapted to include budget constraints, 
ensuring that resource alloca ons stay within predefined limits. 
Both domains require strategies that efficiently u lize me and 
resources to achieve the objec ves within specified dura ons 
 
To sum up, the challenge in cancer treatment trials resembles the Mul-Armed Bandit problem. This 
likeness arises from the demand for adap ng resources dynamically, tailoring treatments individually, 
managing the balance between explora on and exploita on, and factoring in limita ons of budget 
and me. U lizing Mul-Armed Bandit algorithms offers a prac cal approach to streamline clinical 
trials and accelerate the progress in developing successful cancer treatments. 
 
Strategy to solve the problem. 
 
To tackle the issue in cancer treatment clinical trials using the Mul-Armed Bandit (MAB) framework, 
we recommend following a strategy that involves explora on, exploita on, and dynamic resource 
alloca on. Here are the steps: 
 
S.No Steps Descrip on 
1 Formulate the Problem Arms: Treatment arms represent different interven ons 
(Hormone Therapy, Radia on Therapy, Chemotherapy, Surgery). 
Reward: Treatment efficacy (Success/Failure). 
Objec ve: Maximize cumula ve reward (iden fy the most 
efficacious treatments) while minimizing resource expenditure 
2 Design the MAB 
Environment 
States: Represent pa ent characteris cs, cancer features, and 
budget constraints. 
Ac ons (Arms): Correspond to the different treatment arms. 
Rewards: Reflect the success or failure of each treatment. 
3 Choose a MAB 
Algorithm 
Epsilon-Greedy: Balances explora on and exploita on by 
randomly selec ng arms with probability epsilon and selec ng 
the best-known arm with probability 1-epsilon. 
UCB (Upper Confidence Bound): Uses uncertainty esmates to 
guide arm selec on, favoring arms with higher poten al efficacy. 
4 Define Resource 
Alloca on Rules 
Allocate more resources to arms showing promise: Based on the 
observed successes and failures, allocate more pa ents to 
treatment arms with higher expected rewards. 
 
Balance explora on and exploita on: Ini ally explore different 
arms to gather informa on, then exploit the most promising 
arms as evidence accumulates. 
5 
Include Constraints 
Budget Constraints: Set rules to ensure that resource alloca ons 
stay within predefined budget constraints. 
Ethical Considera ons: Implement ethical guidelines to protect 
pa ent safety and well-being. 
Sta s cal Significance: Ensure that results are sta s cally 
significant by defining criteria for the number of pa ents needed 
in each arm. 
6 
Implement and 
Simulate 
Implement the MAB environment. 
7 
Evaluate Performance 
Metrics: Measure metrics such as iden fica on of the most 
effec ve treatment arm, me-to-discovery, pa ent safety, and 
overall cost-effec veness. 
8 
Iterate and Opmize 
Fine-tune parameters: Adjust parameters of the MAB algorithm 
to opmize performance. 
Mul-Armed Bandit  
This is a concept in Reinforcement Learning, where at each step agent or decision maker selects an 
ac on out of mul ple ac ons. At beginning of process, proper es or actual reward associated with 
an ac on is unknown or par ally know. As me passes, real-value of an ac on becomes clearer and 
gradually an ac on converged to it real value. Main objec ve is to maximize the reward.  
In this, an ac on is equivalent to an ARM.  
Value associated with an ac on is REWARD that selec ng an ARM would yield.  
There could be mul ple ac ons(arm) available, hence termed as Mul-Armed Bandit.  
Contextual Mul-Armed Bandit (Contextual Bandit) 
This is more specific case of MAB. In this, contextual informa on associated with a sample is used to 
iden fy an ac on (ARM).  
Each ARM might have different effec veness for different user. So, if some contextual informa on or 
characteris cs of user known in prior, then selec on of ARM would be based on that informa on.  
MAB has no personaliza on (same policy applied to all situa on), whereas CB are more personalized 
based on context and hence be er results.   
Explora on and Exploita on trade-off is important to achieve good policy.  
State (Context) 
Ac on 
Reward Genera on 
Problem Formula on: Cancer Treatment as Contextual Bandit 
Given problem can be formulated as Contextual Bandit problem.  
Each cancer treatment is formalized as an ARM in this problem.  
ARMS : Treatment Type : Chemotherapy, Surgery, Radia on Therapy, Harmone Therapy 
So, we see that there are 4 available ARMs.  
Contextual Informa on: Characteris c informa on like radius, texture, smoothness, compactness 
etc are the context that describes   
Reward : No reward if selected ARM had failed treatment.  
Given data set gives samples where for certain characteris cs, a treatment arm was selected. Its 
status of treatment is also recorded as 0 or 1.  
Addi onally, cost incurred in the treatment is recorded.  
Hence, given problem aptly falls in category of Contextual Bandit problem, in which using context an 
opmal ac on would be determined based on the reward generated.  
Problem Solu on 
Contextual Bandit problem can be solved using various algorithms. In this case, we are using Liner 
UCB to solve and arrive at stable policy which guarantees good results.  
Linear UCB : Linear Upper Confidence Bound (LinUCB) 
Step1 : Select a sample from given data set.  
Step2 : For this sample, fetch out the context  
Step 3 : For this context,  calculate UCB for each ARM 
Step 4 : Add to the ac on list if newly calculated UCB is higher than already available one  
Step5 : Out of available ac on list, make a selec on.  
Following image shows the mathema cs behind this :  
Using above formula, python code was developed.  
Class linucb_dis_canc_treatment : UCB Calcula on and Reward update func on.  
Class linucb_policy : arm selec on using linucb_dis_canc_treatment 
Func on canc_tr_simul : main controller func on to read data samples and process.  
Reward Genera on Func on : Following policy was taken while genera ng rewards :  
 0 when selecte arm yielded “FAILURE” 
 1/(money+me)*10pow3 when arm yielded “SUCCESS”. So, if a treatment arm yielded 
SUCCESS, give higher priority to the case where lesser cost was incurred.  
Result:  
Based on above formula on, python code was generated. Various ALPHA (1.5, 1, 0.5) were used to 
control the trade-off of explora on and exploita on. 
