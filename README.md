## Analysis and Implementation of K-Means++ With Parallel Initialization
- Bin Han, bin.han@duke.edu, Department of Statistical Science, Duke University
- Lingxi Song, lingxi.song@duke.edu, Department of Statistical Science, Duke University

#### Original Paper:
Bahmani, B., et al.(2012), Scalable K-Means++. Proceeding of VLDB Endowment, Volume 5, Issue 7,Page 622-633. Retrieved from:
    https://dl.acm.org/citation.cfm?id=2180915
    
#### Abstract

k-Means is one of the popular unsupervised clustering algorithms which has been widely used over a half century. However, the major drawback of K-Means is that it does not guarantee globally optimal solution, which is usually the case, due to that fact that the initialization of centroids is critically important but completely at random in the algorithm. Additionally, the number of iterations to calculate distance in pairs grows exponentially when number of data points increments, making K-Means not scalable with large data set. K-Means++, an improved algorithm based on K-Means, modifies the initiation process to provably generate the solution that is close to the globally optimal one. However, similarly, due to the inherent nature of sequential initialization of centers, K-Means++ must look over k data chunks and pick one randomly from each chunk, leading to the result that K-Means++  is not well-capable of handling massive data. Based on the idea of K-Means++, the researchers designed a new way to initialize centers parallelly, which dramatically reduce the number of passes. K-Meansll only requires log(k) passes to assign the centers at the beginning but is able to generate a nearly globally optimal solution.

#### Goal

Our project aims to partially replicate the research work of Scalable K-Means++ conducted by Bahmani, B. et al. (2012). We analyzed the potential issues of K-Means and K-Means++ clustering algorithms, provided intuition about the design of new algorithm K-Meansll, and summarized the mathematical proofs from the original paper about the quality solution that the new algorithm can generate. We coded the three clustering methods from scripts in Python and tested them on one simulated data and one real-world data, in order to see how well K-Meansll performs.

#### Result

The results show that K-Meansll does generate solutions that are closer to the global optimum, while it runs much slower compared with the other two algorithms. Our conclusion about the time expenditure contradicts with the conclusion arrived at from the original paper. Several conjectures have been proposed in our analysis. 

#### Files
- Project Report: Analysis and Implementation of K-Means++ With Parallel Initialization
- Real-world Test Data: spamdata.csv
- Source Code: Algorithms.ipynb
- Test Code: Algorithm_testing.ipynb
