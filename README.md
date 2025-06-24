This code implements a **Genetic Algorithm** (GA) to select the best subset of features for classifying bird migratory status (Resident or Migratory) using a Logistic Regression model
To optimize the selection of input features for a logistic regression model to maximize classification accuracy on bird migratory status, using an evolutionary strategy (genetic algorithm).
Loaded from: bird-diversity.csv
Predicting: **'Migratory status'** (Resident or Migratory, encoded as 0 or 1)
**Features used:**
'Heterozygosity'
'Allelic richness'
'Breeding range size'
'Body mass'
'Latitude'
**How the Genetic Algorithm Works**
**Initialization:**
A population of 10 individuals is randomly created.
Each individual is a binary vector of length 5, representing whether a feature is selected (1) or not (0).
**Fitness Function:**
For each individual (feature subset), logistic regression is trained on the selected features.
Its accuracy on the test set is used as the fitness score.
**Selection:**
The top 2 individuals with the highest accuracy are chosen as parents.
**Crossover:**
Parts of the parents’ feature subsets are combined to create new children.
**Mutation:**
Each bit (feature inclusion/exclusion) has a 10% chance of flipping.
**Evolution:**
This process repeats for 20 generations, evolving better feature subsets.
**Final Output:**
The best-performing individual from the last generation is printed:
Which features it selected
The accuracy achieved with that subset
