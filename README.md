# Duplicate_Detection

This project is an assignment for the course "Computer Science For Business Analytics (FEM21037)" from the Erasmus University of Rotterdam. The code contains a duplication detection method which uses Locality-Sensitive Hashing (LSH) and Agglomerative Clustering using the Jaccard similarity measure. The data consists of 1624 TV advertisements. 

The code is structered as follows:

1. First the data is cleaned to extract model words. All uppercase letters are converted to lowercase and the words "Inch" and "Hertz" are standardized. These model words are used to construct the binary matrix.
2. The binary matrix is constructed. 
3. The signature matrix is constructed using minhashing. In order to minhash the binary matrix, two lists of random integers are generated.
4. For different values of r, the signature matrix is split into sub-matrices.
5. The columns of the sub-matrices are hashed into buckets using LSH.
6. The buckets of the LSH are checked and the candidate matrix is constructed.
7. The dissimilarity matrix is construced using the Jaccard similarity measure. 
8. Agglomerative Clustering is performed on the dissimilarity matrix using the optimal threshold.
9. Evaluation metrics are calculated on the test samples. 
10. Results over the 5 bootstraps are averaged. 
11. Graphs of the results are made. 
