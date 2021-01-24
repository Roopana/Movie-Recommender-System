# Movie Recommender System
This module has implementation of a movie recommender system based on Funk SVD algorithm. This algorithm is developed by Simon Funk during the [Netflix prize challenge](https://en.wikipedia.org/wiki/Netflix_Prize). The effectiveness of the algorithm is majorly driven by the latent factors used to identify user-item association. The algorithm determines these values using Matrix Factorization between user ratings and item ratings matrices. The prediction results can be improved by assigning different regularization weights to the latent factors based on items' popularity and users' activeness 

## Comparison with other algorithms
### Collaborative Filtering
Item-Item and User-User filtering are personalized Collaborative Filtering techniques. Item - Item has better computational performance and static than User-User CF algorithm. However, it __lacks serendipity__ in recommendations. User-User & Item-Item techniques can be used when interpretation of recommendation is required. They give better results with dense data. 
### Matrix Factorization techniques
Funk SVD and ALS(Alternate Least Squares) are Matrix Factorization methods and use latent factors. These two algorithms can handle the __scalability__ and __sparsity__ issues of the data. ALS is used with implicit data due to the non-convex nature of the loss function. They handle sparsity and give __global maxima__ however __lack interpretability__ of recommendations. 

## Results comparision (RMSE values)
- Funk SVD : 0.856871
- Recommender v1: 0.742
- Recommender v2: 0.713

## Sources:
We consulted following blogs to explore design of neural networks:
- For the improved algorithm idea: https://medium.com/@iliazaitsev/how-to-implement-a-recommendation-system-with-deep-learning-and-pytorch-2d40476590f9
- For the basic implementation code: https://medium.com/@jdwittenauer/deep-learning-with-keras-recommender-systems-e7b99cb29929
- For RMS implementation in tensorflow: https://stackoverflow.com/a/43863854/4031302
