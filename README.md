# PIDC_bug
A bug of PIDC algorithm
Hi Beeline team,
   I am currently using your neat pipeline, while I have encountered a very wird typo in the rankedEdges.csv file of PIDC results. It seems that on my datasets, the edge weights measured by PIDC is all nan values, like this
![image](https://user-images.githubusercontent.com/24759465/130457894-edf4d258-43d1-42f0-b751-e3497c779415.png)

But! after I used a search algorithm developed by myself ( this algorithm need to repeat run PIDC, which could not be applied on the large-scale scRNA-seq datasets), I found that just delete some of the genes (in my cases, the 441th,865th,866th genes), the edge weights are back to normal ??
![image](https://user-images.githubusercontent.com/24759465/130458264-ded28149-9a7e-4f73-86ec-23baaa7fccb5.png)

I originally thought that may be these genes have some bad statistical characteristics, but regretly that I didn't find any special properties of those genes. (e.g. average expression, variance, coefficients of variation, etc...)
I found this thing is happened in most of my datasets, so I think its really important to be figured out, but I have no idea about how to solve it.
Users could found the ExpressionData.csv to reproduced the bugs.
