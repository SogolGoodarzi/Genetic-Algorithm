# Genetic-Algorithm

### Introduction to Genetic Algorithm
Genetic Algorithms(GAs) are adaptive heuristic search algorithms that belong to the larger part of evolutionary algorithms. Genetic algorithms are based on the ideas of natural selection and genetics. These are intelligent exploitation of random searches provided with historical data to direct the search into the region of better performance in solution space. They are commonly used to generate high-quality solutions for optimization problems and search problems.

Genetic algorithms simulate the process of natural selection which means those species that can adapt to changes in their environment are able to survive and reproduce and go to the next generation. In simple words, they simulate “survival of the fittest” among individuals of consecutive generations for solving a problem. Each generation consists of a population of individuals and each individual represents a point in search space and a possible solution. Each individual is represented as a string of characters/integers/float/bits. This string is analogous to the Chromosome.

#### **Search space**
The population of individuals is maintained within the search space. Each individual represents a solution in search space for a given problem. Each individual is coded as a finite-length vector (analogous to a chromosome) of components. These variable components are analogous to Genes. Thus a chromosome (individual) is composed of several genes (variable components). The explanations can be better comprehended by the following figure:

![image](https://user-images.githubusercontent.com/125180530/219152438-9dcfb84d-cdf7-4b53-ad9d-598393723132.png)
#### **Fitness Score**
A Fitness Score is given to each individual which shows the ability of an individual to “compete”. The individual having optimal fitness score (or near-optimal) is sought. The GAs maintains the population of n individuals (chromosome/solutions) along with their fitness scores. The individuals having better fitness scores are given more chances to reproduce than others. The individuals with better fitness scores are selected who mate and produce better offspring by combining the chromosomes of parents. The population size is static so the room has to be created for new arrivals. So, some individuals die and get replaced by new arrivals eventually creating a new generation when all the mating opportunity of the old population is exhausted. It is hoped that over successive generations better solutions will arrive while the least fit die. 

Each new generation has on average more “better genes” than the individual (solution) of previous generations. Thus each new generations have better “partial solutions” than previous generations. Once the offspring produced having no significant difference from offspring produced by previous populations, the population is converged. The algorithm is said to be converged to a set of solutions for the problem.

#### **Operators of Genetic Algorithms**

Once the initial generation is created, the algorithm evolves the generation using the following operators:

**1. Selection Operator:** The idea is to give preference to the individuals with good fitness scores and allow them to pass their genes to successive generations. 

**2. Crossover Operator:** This represents mating between individuals. Two individuals are selected using a selection operator and crossover sites are chosen randomly. Then the genes at these crossover sites are exchanged thus creating a completely new individual (offspring). For example:

![image](https://user-images.githubusercontent.com/125180530/219153825-2d2eaaac-1de8-4ba4-814e-5a13cb4ab693.png)

**3. Mutation Operator:** The key idea is to insert random genes in offspring to maintain the diversity in the population to avoid premature convergence. For example:

![image](https://user-images.githubusercontent.com/125180530/219154388-515c0dfc-7504-4800-955e-9a46e8a9b3c0.png)

### Algorithm

The whole algorithm can be summarized as:

1. Randomly initialize populations p

2. Determine the fitness of the population

3. Until convergence repeat:

  a. Select parents from the population
  
  b. Crossover and generate a new population
  
  c. Perform mutation on new population
  
  d. Calculate fitness for the new population
  
 Now consider the following non-convex function:
 
 ![image](https://user-images.githubusercontent.com/125180530/219155577-6043f4a0-dc7b-497f-a220-f4106ca192d9.png)

We assume the following condition and found the local minimum of this function.

![image](https://user-images.githubusercontent.com/125180530/219157030-7afc9e20-7854-4736-a0a1-17712f945a34.png)
