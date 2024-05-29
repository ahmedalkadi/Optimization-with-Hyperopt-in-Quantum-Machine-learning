
## **Hyperopt: Distributed Asynchronous Hyper-parameter Optimization**

1. **Intoduction:**
- Hyperopt is a powerful Python library for hyperparameter optimization, particularly popular in the machine learning and data science communities. It offers an efficient and flexible framework for automatically tuning the hyperparameters of machine learning models, aiming to find the best configuration for a given optimization objective.

2. **Key Objectives**
- To use "hyperopt" optimizer to optimize an SVC Quantum machine learning problem.
- To examine how the chosen parameters of optimization are effecting the results of the test and the accuracy.
- To have insights about the ranges of the hyperparameters in the case of SVC QML

2. **Algorithms:**
- Random Search: This algorithm randomly samples hyperparameter configurations from the search space and evaluates them independently. While simple and easy to implement, random search may not be the most efficient method for finding optimal hyperparameters, especially in high-dimensional spaces.

- Tree-structured Parzen Estimator (TPE): TPE is a Bayesian optimization algorithm that models the objective function and the distribution of hyperparameters using probability distributions. It iteratively refines these distributions based on observed performance, focusing the search on promising regions of the hyperparameter space.

- Adaptive TPE (ATPE): This variant of TPE adapts the search space dynamically during optimization based on the performance of previously evaluated configurations. It aims to allocate more samples to promising regions of the search space, potentially improving the convergence speed.

- you can find more information here
 https://hyperopt.github.io/hyperopt/

- how to write an objective function in "hyperopt" 
https://github.com/hyperopt/hyperopt/wiki/FMin



## Pramameters to optimize 

In this study an optimization for the following parameters was carried out.

- rep: This parameter represents the number of repetitions for the feature map used in the quantum kernel. It determines the complexity or richness of the feature map, which can impact the expressiveness of the quantum model. Optimizing this parameter allows finding the optimal trade-off between model complexity and generalization performance.

- c: This parameter is the regularization parameter for the Support Vector Classifier (SVC) used in the classical part of the hybrid quantum-classical model. Regularization helps prevent overfitting by penalizing large coefficients in the decision function. Optimizing this parameter ensures the model's ability to generalize well to unseen data.

- entangle: This parameter specifies the type of entanglement used in the feature map of the quantum kernel. Entanglement is a fundamental property of quantum systems and can affect the quantum circuit's representation power. By optimizing this parameter, the most suitable type of entanglement for the given task can be determined, potentially improving model performance.

- shots: This parameter denotes the number of shots (measurement repetitions) for executing quantum circuits on a quantum device or simulator. More shots can lead to more accurate results but also require more computational resources. Optimizing this parameter involves finding the balance between the accuracy of quantum measurements and the computational cost, ensuring efficient utilization of resources.
