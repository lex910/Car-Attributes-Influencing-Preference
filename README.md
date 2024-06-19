# Discover-Top-Car-Attributes
Using shrinkage regression (ridge, lasso, elastic net) to determine top attributes influencing car preference 

- In the ridge coefficient plot we see the shrinkage effect in action. As our regularization parameter (lambda) increases our coefficients are consistently shrunk towards zero.

![Screenshot 2024-06-19 at 2 03 04 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/96f78c98-14ba-467a-8237-9ba2706c9a62)


- In the lasso coefficient plot we see insignificant coefficients hit zero as the lambda penalty term increases. This graph also visualizes the variable selection feature of lasso correlation. We can see which variable we would keep in our model at our desired lambda.

![Screenshot 2024-06-19 at 2 03 38 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/4dbdce8b-87ff-4659-88ca-6cb781230b3a)



- In the elastic net regression coefficient plot we see the combination of both lasso and ridge. The coefficients are consistently ‘shrunk’ towards zero (like in ridge) until they actually hit zero and perform our variable selection at desired lambda (like in lasso)

- ![Screenshot 2024-06-19 at 2 02 36 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/cb1f30eb-967b-425f-9a4c-06e08b30bb6b)

## MSE vs lambda
The 3 graphs compare the Mean Squared Error seen vs the Lambda used in the shrinkage methods of Ridge, Lasso, and Elastic Net. Here we can see the tradeoff between accuracy and including the best features. In all three plots, as lambda increases, the complexity of the model decreases, leading to fewer features being included in the model.

![Screenshot 2024-06-19 at 2 05 34 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/ecc38a3a-d285-4c5c-9bbd-8975b5cc40c8)
![Screenshot 2024-06-19 at 2 05 43 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/f89e7a55-c35b-4a39-87be-0caef6f84be6)
![Screenshot 2024-06-19 at 2 05 56 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/3cba444c-e157-4239-b5ab-b769568f03a5)

## Parameter estimates for 3 methods with best alphas 

![Screenshot 2024-06-19 at 2 07 49 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/60425df3-8ee9-4acd-9f84-48257b3d3770)

## Top three attributes to influence car preference 
The top 3 attributes appear to be common, interesting, and poorly.built (well built since it is negative). When we run a linear regression using these three variables we can see that common is not statistically significant in predicting overall preference.

## Extent of bias in percentage using estimated parameters from three methods for top 3 attributes 
Performed OLS & 3 methods on full cars training dataset & calculated the following biases for each method.

![Screenshot 2024-06-19 at 2 12 34 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/eb365bd3-8b19-4789-b3b3-0ed26f468192)

## OLS coefficients for top 3 attributes 

![Screenshot 2024-06-19 at 2 13 15 PM](https://github.com/lex910/Discover-Top-Car-Attributes-/assets/101606445/c87af39f-d6db-42ed-b170-9065744a568a)

The regression model identifies that interesting and poorly built are significant at the 0.05 level. 
