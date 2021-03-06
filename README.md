# GA-Scheduling
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Project Description
- Problem:
  Schedule the task for UAV.
- Target:
  - Minimize the length of path;
  - Minimize the execution time.
- Presumption:
  - UAV moves in a 2D plane;
  - All UAV are equal;
  - UAV is capable for all the task;
  - No limitation for the maximum number of tasks executed by a single UAV;
  - No time is needed for task execution and target is still during the task execution;
  - No consideration for the following action after the UAV finish all its task;
  - No interval between tasks.
- Constrains:
  - UAV follows the *Dubins Path*;
  - The task in sequence must be executed in order;
  - No collision between UAV.
  
## Experiment Result

### Scheduled Path Length

We choose CGA as the baseline. The fitness is the sum of length of all the UAVs.

![](https://github.com/AlbertYoung0112/GA-Scheduling/blob/master/Shortest%20Total%20Flight%20Distance.png?raw=true)

### Average Gene-Distance to the Best Gene

We use the average gene-distance to evaluate the ability of our algorithm to explore the entire space, the higher, the better.

![](https://github.com/AlbertYoung0112/GA-Scheduling/blob/master/Average%20Differences%20to%20the%20Best%20Solution.png?raw=true)

## Our Work
- NaiveGA
  
  A simple implementation for the general GA algorithm.
  - Purpose:
    - Test the GA algorithm;
    - Explore the resolve the bottleneck of the performance;
    - An example for the GA interface;
- SchGA

  The solution for the project.
  - Build the Project
      
        $ mkdir build 
        $ cd build
        $ cmake ..
        $ make
    - cmake configuration
        
      -DPRINT_INFO: Print the information to the terminal, *ON* by default.

      -DADVANCED_FEATURE: Select the algorithm, *ON* -> our algorithm, *OFF* -> baseline algorithm, *ON* by default.
  - Evaluate the Project
  
        ./GAHW recorder.csv
    Program will generate a random task configuration and ask for you confirmation. 
    
    The statistical data will be recorded to the csv file.

  - Task Descriptor

    To be filled.
  - Gene Coding

    To be filled.
  - Fitness Function
    - Dubins Path
    - Collision Detection
    - Correction for the gene violating constrains
  - Interbred

    To be filled.
  - Mutation

    To be filled.
  - Selection

    To be filled.
  - Advanced Features

    To be filled.

## To Do
- bug detecting...
