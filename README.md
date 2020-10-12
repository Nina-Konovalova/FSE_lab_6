# FSE_lab_6
## Problem and materials.
Create a set of unit tests for a part of the Virus Spread Modeling System VSMS-20 developed in class/at home. You may use either solutions or your own developments made during the class -- whichever you prefer.

 

## The following functionality must be tested:

1) Persons should be able to transmit infections when infected (without symptoms or with symptoms), meaning that other Persons shall be able to get infected (change their health state from healthy to infected (without symptoms) when contacted by a person with a virus).
2) When a healthy person is contacting another healthy person, their health conditions should not change.
3) When an infected person is contacting a person with antibodies, the latter shall not change health state, if his antibodies have the same type as the virus.
4) A person shall change his health state from infected (without symptoms) to infected (with symptoms), after being infected for 2 days.
5) A person shall change his health state from infected (with symptoms) to healthy, if the virus has obtained strength below zero.
6) A person shall change his health state from infected (with symptoms) to dead, if his health state (temperature or water level) is exceeding a life incompatible threshold.
 

## Optional functionality (not necessary to test, but if so, it will be graded by bonus points):

1) Each day a person infected (with symptoms) with a seasonal flu or SARS-CoV-2 will demonstrate an increase in temperature, and a person infected (with symptoms) with cholera will demonstrate a water loss.
2) Each night a virus of a person who is infected (with symptoms) will demonstrate a loss of strength by a factor inversely proportional to that person’s age (can check this roughly).
3) A person shall have an antibody of the same type as his virus, if his virus has obtained strength below zero.
4) A person shall be hospitalized (added to a list of patients in a hospital) if his health conditions are infected (with symptoms) and his health state (temperature or water level) is exceeding a life threatening threshold.
 

## Guidelines. 

Subclass unittest.TestCase several times to test different classes (e.g., viruses, persons, and person states).
Create a generator of randomized persons / viruses configurations to check if the code works for different parameters in the persons and viruses. Implement this by unittest.TestCase.setUp/tearDown methods.
 

## Submitting the solution. 
You should submit the solution to the problem in one of the following ways:

either using a single Jupyter notebook, that should be possible to run using the “Cell → Run All” function from the main menu bar, or 
using a single python script.
 
