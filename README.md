# MDP REPRESENTATION

## AIM:
  To represent any one real-world problem in MDP form.

## PROBLEM STATEMENT:
 

### Problem Description
   The task is to train a robotic arm to pick up an object, move it to a designated spot by moving right, then straight, and finally release the object at the target location. The task is broken down into sequential stages: hold, move right, move straight, and release.


### State Space
The state space represents all possible configurations of the robotic arm during the task. Each state is defined by:

Position of the robotic arm's end effector (gripper).
Gripper status (open or closed).
Current stage of the task (hold, move right, move straight, release).


### Sample State
 Current stage: move right.


### Action Space
The action space consists of the following possible actions:

Hold: Close the gripper to grab the object.
Move Right: Move the end effector horizontally to the right.
Move Straight: Move the end effector vertically towards the target.
Release: Open the gripper to release the object.

### Sample Action
 Action: Move right

### Reward Function
The reward function is defined as follows:

+1 for successfully holding the object.
+1 for successfully moving the object right.
+1 for successfully moving the object straight towards the target.
+10 for successfully releasing the object at the target location.
-1 for incorrect actions or any movement that does not contribute towards the goal.

### Graphical Representation
![image](https://github.com/user-attachments/assets/a516f071-3396-4a20-aa82-2c67f2758645)


## PYTHON REPRESENTATION:
```py
P={0: {0: [(0.7, 1, 1, False), (0.1, 0, 0.0, False), (0.1, 0, 0.0, False),(0.1, 0, 0.0, False)],
        1: [(1, 0, 0.0, False), (0, 0, 0.0, False), (0, 0, 0.0, False),(0, 0, 0.0, False)],
       2: [(1, 0, 0.0, False), (0, 0, 0.0, False), (0, 0, 0.0, False),(0, 0, 0.0, False)],
       3: [(1, 0, 0.0, False), (0, 0, 0.0, False), (0, 0, 0.0, False),(0, 0, 0.0, False)],


       },
   1:   { 0: [(1, 1, 0, False), (0, 1, 0.0, False), (0, 1, 0.0, False),(0, 1, 0.0, False)],
        1: [(0.7, 2, 1, False), (0.1, 1, 0.0, False), (0.1, 1, 0.0, False),(0.1, 1, 0.0, False)],
       2: [(1, 1, 0.0, False), (0, 1, 0.0, False), (0, 1, 0.0, False),(0, 1, 0.0, False)],
       3: [(1.7, 1, 0.0, False), (0, 1, 0.0, False), (0, 1, 0.0, False),(0, 1, 0.0, False)],


       },
  2:  {0: [(1, 2, 0, False), (0, 2, 0.0, False), (0, 2, 0.0, False),(0, 2, 0.0, False)],
        1: [(1, 2, 0.0, False), (0, 2, 0.0, False), (0, 2, 0.0, False),(0, 2, 0.0, False)],
       2: [(0.7, 3, 1, False), (0.1, 2, 0.0, False), (0.1, 2, 0.0, False),(0.1, 2, 0.0, False)],
       3: [(1, 2, 0.0, False), (0, 2, 0.0, False), (0, 2, 0.0, False),(0, 2, 0.0, False)],


       },
   3: {0: [(1, 3, 1, False), (0, 3, 0.0, False), (0, 3, 0.0, False),(0, 3, 0.0, False)],
        1: [(1, 3, 0.0, False), (0, 3, 0.0, False), (0, 3, 0.0, False),(0, 3, 0.0, False)],
       2: [(1, 3, 0.0, False), (0, 3, 0.0, False), (0, 3, 0.0, False),(0, 3, 0.0, False)],
       3: [(0.7, 0, 10, True), (0.1, 3, 0.0, False), (0.1, 3, 0.0, False),(0.1, 3, 0.0, False)],


       },

}


```

## OUTPUT:
![image](https://github.com/user-attachments/assets/101713a9-7f56-482d-898a-b6d3cf09dc58)


## RESULT:
Thus the given real world problem is successfully represented in a MDP form.

