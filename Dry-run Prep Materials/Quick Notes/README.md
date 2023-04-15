# Quick Notes:

### A) domain.rddl:
  1.  Lifted Reprentation/Ungrounded Representation
  2.  
   

![image](https://user-images.githubusercontent.com/129742046/232253763-e7a87679-2796-4a95-b909-97a35cc9a7f6.png)

(Fig. 1: Illustration of domain.rddl Source: [Link](https://ataitler.github.io/IPPC2023/infrastructure.html))

This is a behavior description, this type of code can be found in the domain block of the RDDL code. In the code above no specific car is described. that will be done in the instance.


**a) types:** used to define different type of objects that appear in an environment.

**b) pvariable (parameterized variable):** These variables include constant values, states and action variables, as well as potentially intermediate and observed variables. Ultimately, these variables will serve as condition-determining parameters in transitions of states. The variables declared in this section can be either parameterized by one or more objects, or non-parameterized

**c) cpfs (conditional probability function):** specifies relationship between different variables.


### RDDL Graph:

![image](https://user-images.githubusercontent.com/129742046/232253581-a46eecbf-3e7f-4958-9fce-587c258b971b.png)

(Image Source: [Link](https://github.com/ataitler/pyRDDLGym/blob/main/docs/rddlgraph.png))


 1. **Non-fluent (constant):** Variable that never changes during a simulation. Non-fluents will be initialized in the non-fluents block before simulation starts
    
 2. **Action-fluent:** Variable that represents the action of a simulation, often used to describe if a transition between two different states is happening.
    
 3. **State-fluent:** Variable that represents the state of a simulation, often used to describe the state or relative state of objects (e.g., locations, occupancy, etc.).
    
 4. **Interm-fluent:** Variable that is used as an intermediate conditional probability calculation. Intermediate fluents must have a level of stratification, and are strictly stratified so that an intermediate variable can only condition on intermediate variables of a strictly lower level or state variable.

 6. **Observ-fluent:** Variable used as a conditional observation probability in partially observable Markov decision process (POMDP).
    
(Source: [Link](https://github.com/ataitler/pyRDDLGym/blob/main/docs/rddl.rst))    
    
### B) instance.rddl:
 1. Grounded Representation
 2.  
    
    
i) Defining the objects in the problem: 

![image](https://user-images.githubusercontent.com/129742046/232256799-94255e80-3384-4f65-9dda-b7aa54dda466.png)


ii) Now that we have specific car objects, we can define their intial state:

![image](https://user-images.githubusercontent.com/129742046/232256845-08d0f2a0-3e6c-46fe-a683-2ee07aae6d06.png)

iii) So in the lifted description we have behavior, types and objects for instantiation. When pyRDDLGym instantiate an environment it will ground everything, which means we will no longer have types and objects, we will have only effects and evolutions over the explicit variables of the problem, i.e., the variables of the problem will be (with their initial values):

![image](https://user-images.githubusercontent.com/129742046/232256896-1d7e9437-9b89-4919-bd67-fa2bf8952101.png)

iv) and the explicit effect will be:

![image](https://user-images.githubusercontent.com/129742046/232257008-cd83534c-acfd-4eb5-b72e-a6060d639fd4.png)


