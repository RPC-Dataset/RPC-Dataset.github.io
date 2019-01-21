# RPC: A Large-Scale Retail Product Checkout Dataset

<div align="center">

**[Xiu-Shen Wei<sup>1*</sup>](http://lamda.nju.edu.cn/weixs) &nbsp;&nbsp;&nbsp; Quan Cui<sup>1,2</sup> &nbsp;&nbsp;&nbsp; [Lei Yang<sup>1</sup>](https://github.com/DIYer22)&nbsp;&nbsp;&nbsp; Peng Wang<sup>3</sup> &nbsp;&nbsp;&nbsp; Lingqiao Liu<sup>3</sup>**

<sup>1</sup>Megvii Research Nanjing, Megvii Technology Ltd., Nanjing, China    
<sup>2</sup>Graduate School of Information, Waseda University, Tokyo, Japan    
<sup>3</sup>School of Computer Science, The University of Adelaide, Adelaide, Australia

---

 ### [Abstract](#1-abstract) | [Paper](#2-paper) | [Dataset](#3-our-rpc-dataset) | [Baselines](#4-proposed-baseline-method-on-the-rpc-dataset) | [Leaderboard](#5-Leaderboard) | [RPC-tool](#6-rpc-tool) 
</div>

## 1. Abstract
&nbsp;&nbsp;&nbsp;&nbsp; *Over recent years, emerging interest has occurred in integrating computer vision technology into the retail industry. Automatic checkout (ACO) is one of the critical problems in this area which aims to automatically generate the shopping list from the images of the products to purchase. The main challenge of this problem comes from the large scale and the fine-grained nature of the product categories as well as the difficulty for collecting training images that reflect the realistic checkout scenarios due to continuous update of the products. Despite its significant practical and research value, this problem is not extensively studied in the computer vision community, largely due to the lack of a high-quality dataset. To fill this gap, in this work we propose a new dataset to facilitate relevant research. Our dataset enjoys the following characteristics: (1) It is by far the largest dataset in terms of both product image quantity and product categories. (2) It includes single-product images taken in a controlled environment and multi-product images taken by the checkout system. (3) It provides different levels of annotations for the checkout images. Comparing with the existing datasets, ours is closer to the realistic setting and can derive a variety of research problems. Besides the dataset, we also benchmark the performance on this dataset with various approaches.*

## 2. Paper

<div align="center">

<a href="">
    <img style="width:440px" src="imgs/paper.png">
</a>   


[Paper on arXiv => "RPC: A Large-Scale Retail Product Checkout Dataset"]()
</div>

## 3. Our RPC dataset 

<div align="center">

[![](imgs/rpc-dataset.png)](https://www.kaggle.com/diyer22/retail-product-checkout-dataset)     
[Dataset on Kaggle => "The Retail Product Checkout dataset"](https://www.kaggle.com/diyer22/retail-product-checkout-dataset)
(15 GB)

</div>


#### 3.1 Dataset license:  
[![](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)    
CC BY-NC-SA 4.0

#### 3.2 Overview infomation of the RPC dataset 

| *Split* | *# images* | *# objects* | *# objects/image* | *# categories/image* |
| --- | ---: | ---: | ---: | ---: |
| Training set (Exemplar images) | 53,739 | 53,739 | 1 | 1 |
| Validation set (Checkout images) | 6,000 |   73,602 | 12.27 | 6.33 |
| Test set (Checkout images)| 24,000 |  294,333 | 12.26 | 6.31 |


#### 3.3 Collection equipment for single product images (training set)



<div align="center">

<a href="">
    <img style="width:700px" src="imgs/single.png">
</a>   
</div> 

#### 3.4 Different clutter levels for checkout images (val/test sets)


<div align="center">

![](imgs/test.png)
</div>

#### 3.5 Detailed information of val+test sets for different clutters

| *Clutter mode* | *# images* | *# objects* | *# objects/image* | *# categories/image* |
| --- | ---: | ---: | ---: | ---: |
|       easy |  10,000 |   71,496 |                    7.15 |                      3.81 |
|     medium |  10,000 |  122,961 |                   12.30 |                      6.27 |
|       hard |  10,000 |  173,478 |                   17.35 |                      8.87 |


## 4. Proposed baseline method on the RPC dataset

#### 4.1 Pipeline of our *Syn+Render* method
![](imgs/pipeline.png)

#### 4.2 Experimental results
![](imgs/result.png)

## 5. Leaderboard
[**RPC-Leaderboard**](https://github.com/RPC-Dataset/RPC-Leaderboard)

If you have been successful in creating a model based on the training set and it performs well on the validation set, we encourage you to run your model on the test set. The *rpc-tool* (in the next section in this project page) will contribute to return the corresponding results of the evaluation metrics. You can submit your results on the RPC leaderboard by creating a new issue. Your results will be ranked in the leaderboard and to benchmark your approach against that of other machine learners. We are looking forward to your submission. Please click [here](https://github.com/RPC-Dataset/RPC-Leaderboard/issues)

## 6. RPC-tool
["**rpctool**"](https://github.com/DIYer22/retail_product_checkout_tools): A Python package for evaluating your methods on the RPC dataset. It can return several evaluation metrics (listed in the aforementioned table in Sec. 4.2). More information can be found in [rpctool](https://github.com/DIYer22/retail_product_checkout_tools).

</br>
</br>
</br>
</br>

<div align="center">
<small>

   \* Xiu-Shen Wei is the corresponding author ([weixs.gm@gmail.com](mailto:weixs.gm@gmail.com)).
</small>
</div>