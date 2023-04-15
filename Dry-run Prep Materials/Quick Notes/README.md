# Quick Notes:

### A) domain.rddl:
     - Lifted Reprentation/Ungrounded Representation
     - 

![image](https://user-images.githubusercontent.com/129742046/232253763-e7a87679-2796-4a95-b909-97a35cc9a7f6.png)

(Source: https://ataitler.github.io/IPPC2023/infrastructure.html)

This is a behavior description, this type of code can be found in the domain block of the RDDL code. In the code above no specific car is described. that will be done in the instance.


**a) types:** used to define different type of objects that appear in an environment.

**b) pvariable (probabilistic variable):** primarily used to represent state of the environment, but can also include the state of the agent, e.g. if the agent has health attribute.

**c) cpfs (conditional probability function):** specifies relationship between different variables.


#### Types of pvariables:

![image](https://user-images.githubusercontent.com/129742046/232253581-a46eecbf-3e7f-4958-9fce-587c258b971b.png)

(Source: [Link](https://github.com/ataitler/pyRDDLGym/blob/main/docs/rddlgraph.png))


    1. **Non-fluent (constant):** Does not change its truth value during the execution of an action or due to external events--- fixed probability distribution--- e.g. probability of truck breaking down based on historical data.
    2. **Action-fluent:** A predicate that can change its truth value as a result of executing an action. For example, in a logistics domain, the predicate "at(robot, location)" could be an action fluent because its truth value changes when the robot moves to a different location.
    3. **State-fluent:** A predicate that can change its truth value due to external events/based on state of the world, not necessarily actions.  
    4. **Interm-fluent:** Predicate that is not directly observable or controllable, but whose truth value is affected by other fluents and/or actions in the system.
    5. **Derived-fluent:** Predicates whose truth values can be computed from other fluents or variables in the state. 
    
    
    
### B) instance.rddl:
    - Grounded Representation
    
    
i) Defining the objects in the problem:    
![image](https://user-images.githubusercontent.com/129742046/232256799-94255e80-3384-4f65-9dda-b7aa54dda466.png)


ii) Now that we have specific car objects, we can define their intial state:
![image](https://user-images.githubusercontent.com/129742046/232256845-08d0f2a0-3e6c-46fe-a683-2ee07aae6d06.png)

iii)
![image](https://user-images.githubusercontent.com/129742046/232256896-1d7e9437-9b89-4919-bd67-fa2bf8952101.png)

iv) 
![image](https://user-images.githubusercontent.com/129742046/232257008-cd83534c-acfd-4eb5-b72e-a6060d639fd4.png)


