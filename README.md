# Recommender System Suits： An open source toolkit for recommender system

This repository provides a set of classical **traditional recommendation methods** which make predictions only using rating data and **social recommendation methods** which incorporate trust/social information in order to alleviate the sparsity of ratings data. 

## Traditional recommendation

* **UserCF**[Resnick et al. 1994]

Resnick, Paul, et al. "GroupLens: an open architecture for collaborative filtering of netnews." Proceedings of the 1994 ACM conference on Computer supported cooperative work. ACM, 1994.

* **ItemCF**[Sarwar et al. 2001]

Sarwar, Badrul, et al. "Item-based collaborative filtering recommendation algorithms." Proceedings of the 10th international conference on World Wide Web. ACM, 2001.

* **FunkSVD**[Simon Funk. 2006]

http://sifter.org/~simon/journal/20061211.html

* **PMF**[Salakhutdinov. 2008]

Mnih, Andriy, and Ruslan R. Salakhutdinov. "Probabilistic matrix factorization." Advances in neural information processing systems (2008): 1257-1264.

* **IntegSVD**[Koren et al. 2008]

Koren, Yehuda. "Factorization meets the neighborhood: a multifaceted collaborative filtering model." Proceedings of the 14th ACM SIGKDD international conference on Knowledge discovery and data mining. ACM, 2008.

* **BiasSVD**[Koren et al. 2009]

Koren, Yehuda, Robert Bell, and Chris Volinsky. "Matrix factorization techniques for recommender systems." Computer 42.8 (2009).

* **SVD++**[Koren et al. 2010]

Koren, Yehuda. "Factor in the neighbors: Scalable and accurate collaborative filtering." ACM Transactions on Knowledge Discovery from Data (TKDD) 4.1 (2010): 1.



## Social recommendation
* **SocialRec**[Ma et al. 2008]

Ma, Hao, et al. "Sorec: social recommendation using probabilistic matrix factorization." Proceedings of the 17th ACM conference on Information and knowledge management. ACM, 2008.

* **RSTE**[Ma et al. 2009]

Ma, Hao, Irwin King, and Michael R. Lyu. "Learning to recommend with social trust ensemble." Proceedings of the 32nd international ACM SIGIR conference on Research and development in information retrieval. ACM, 2009.

* **TrustWalker**[Jamali and Ester. 2009]

Jamali, Mohsen, and Martin Ester. "Trustwalker: a random walk model for combining trust-based and item-based recommendation." Proceedings of the 15th ACM SIGKDD international conference on Knowledge discovery and data mining. ACM, 2009.

* **SocialMF**[Jamali and Ester 2010]

Jamali, Mohsen, and Martin Ester. "A matrix factorization technique with trust propagation for recommendation in social networks." Proceedings of the fourth ACM conference on Recommender systems. ACM, 2010.

* **SocialReg**[Ma et al. 2011]

Ma, Hao, et al. "Recommender systems with social regularization." Proceedings of the fourth ACM international conference on Web search and data mining. ACM, 2011.

* **TrustSVD**[Guo et al. 2015]

Guo, Guibing, Jie Zhang, and Neil Yorke-Smith. "TrustSVD: Collaborative Filtering with Both the Explicit and Implicit Influence of User Trust and of Item Ratings." AAAI. Vol. 15. 2015.

## Requirements
* numpy==1.14.2
* scipy==1.0.1
* pandas==0.22.0
* matplotlib==2.2.2

## Code Structure

## Parameters Settings
If you want to change the default hyparameters, you can set it in `configx.py`. The meanings of the hyparameters is as follows:

#### Dataset Parameters

`dataset_name`: the short name of dataset, the default value is `ft`.

`k_fold_num`: the num of cross validation, the default value is `5`.

`rating_path `: the path of raw ratings data file, the default value is `../data/ft_ratings.txt`.

`rating_cv_path`: the cross validation path of ratings data, the default value is `../data/cv/`.

`trust_path`: the path of raw trust data file, the default value is `../data/ft_trust.txt`.

`sep`: the separator of rating and trust data in triple tuple, the default value is ` `.

`random_state`: the seed of random number, the default value is `0`.

`size`: the ratio of train set, the default value is `0.8`.

`min_val`: the minimum rating value, the default value is `0.5`.

`max_val`: the maximum rating value, the default value is `4.0`.

#### Model HyperParameter

`coldUserRating`: the number of ratings a cold start user rated on items, the default value is `5`.

`factor`: the size of latent dimension for user and item, the default value is `10`.

`threshold`: the threshold value of model training, the default value is `1e-4`.

`lr`: the learning rate, the default value is `0.01`.

`maxIter`: the maximum number of iterations, the default value is `100`.

`lambdaP`: the parameter of user regularizer, the default value is `0.001`.

`lambdaQ`: the parameter of item regularizer, the default value is `0.001`.

`gamma`: momentum coefficient, the default value is `0.9`.

`isEarlyStopping`: early stopping flag, the default value is `false`.

#### Output Parameters

`result_path`: the main directory of results, the default value is `../results/`.

`model_path`: the directory of well-trained variables, the default value is `../results/model/`.

`result_log_path`: the directory of logs when training models, the default value is `../results/log/`.

## Usage

## Acknowledgements

Specially summerize the Traditional and Social recommendations for you, and if you have any questions, please contact me quickly. Last but not least, I sincerely look forward to working with you to contribute it.

My Homepage [Honglei Zhang](http://midas.bjtu.edu.cn/Home/MemberStudent/27)

My ZhiHu [Honglei Zhang](https://www.zhihu.com/people/hongleizhang)






