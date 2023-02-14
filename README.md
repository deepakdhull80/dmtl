# Distillation based Multi-task Learning: A Candidate Generation Model for Improving Reading Duration

## Problem
-  Items with low quality but attractive title (i.e., click baits) may be recommended to the user, which worsens the user experience.

## Solution
- The first one is how to deal with the zero duration of the negative samples, which does not necessarily indicate dislikes. 
- The second one is how to perform multi-task learning in the candidate generation model with double tower structure that can only model one single task.

### Approach:
We model duration by considering its dependency of click in the MTL, and then transfer the knowledge learned from the MTL teacher model to the student candidate generation model by distillation.

![image](https://user-images.githubusercontent.com/49068807/218641520-df541160-8451-4dbf-812a-0d708d6d6d0e.png)
Network structure of the proposed distillation based multi-task learning model. The teacher model (left) is a multi-task learning model which models reading duration. It considers the dependency of click and reading by minimizing the CTR loss and CTCVR loss simultaneously. The student model (right) is a candidate generation model with double tower structure. Knowledge of the teacher model is transferred to the student model by distillation so that the student model can obtain the ability to model reading duration while keeping its high efficiency for candidate generation.
