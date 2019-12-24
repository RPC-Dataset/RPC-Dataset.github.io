
<head>
    <meta charset="UTF-8">
    <title>RPC-Dataset Project Page</title>
    <meta name="description" content="A Large-Scale Retail Product Checkout Dataset">
    <meta name="keywords" content="rpc dataset, rpctool, retail, product detection">
    <link rel="shortcut icon" href="./favicon.ico">
</head>

<div align="center">

# RPC: A Large-Scale Retail Product Checkout Dataset

**[Xiu-Shen Wei<sup>1*</sup>](http://www.weixiushen.com/) &nbsp;&nbsp;&nbsp; Quan Cui<sup>1,2</sup> &nbsp;&nbsp;&nbsp; [Lei Yang<sup>1</sup>](https://github.com/DIYer22)&nbsp;&nbsp;&nbsp; Peng Wang<sup>3</sup> &nbsp;&nbsp;&nbsp; Lingqiao Liu<sup>3</sup>**

<sup>1</sup>Megvii Research Nanjing, Megvii Technology Ltd., Nanjing, China    
<sup>2</sup>Graduate School of IPS, Waseda University, Fukuoka, Japan    
<sup>3</sup>School of Computer Science, The University of Adelaide, Adelaide, Australia

---

 ### [Abstract](#1-abstract) | [Paper](#2-paper) | [Dataset](#3-our-rpc-dataset) | [Baselines](#4-proposed-baseline-method-on-the-rpc-dataset) | [Leaderboard](#5-Leaderboard) | [RPC-tool](#6-rpc-tool) 
</div>

## 1. Abstract

<p style="text-align: justify"><em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Over recent years, emerging interest has occurred in integrating computer vision technology into the retail industry. Automatic checkout (ACO) is one of the critical problems in this area which aims to automatically generate the shopping list from the images of the products to purchase. The main challenge of this problem comes from the large scale and the fine-grained nature of the product categories as well as the difficulty for collecting training images that reflect the realistic checkout scenarios due to continuous update of the products. Despite its significant practical and research value, this problem is not extensively studied in the computer vision community, largely due to the lack of a high-quality dataset. To fill this gap, in this work we propose a new dataset to facilitate relevant research. Our dataset enjoys the following characteristics: (1) It is by far the largest dataset in terms of both product image quantity and product categories. (2) It includes single-product images taken in a controlled environment and multi-product images taken by the checkout system. (3) It provides different levels of annotations for the checkout images. Comparing with the existing datasets, ours is closer to the realistic setting and can derive a variety of research problems. Besides the dataset, we also benchmark the performance on this dataset with various approaches.</em></p>

## 2. Paper

<div align="center">

<a href="https://arxiv.org/abs/1901.07249">
    <img style="width:200px" src="imgs/paper_small.jpg">
</a>   


[**Paper on arXiv => "RPC: A Large-Scale Retail Product Checkout Dataset"**](https://arxiv.org/abs/1901.07249)
</div>

## 3. Our RPC dataset 

<div align="center">

[![](imgs/rpc-dataset.png)](https://www.kaggle.com/diyer22/retail-product-checkout-dataset)     

[**Dataset on Kaggle => "The Retail Product Checkout dataset"**](https://www.kaggle.com/diyer22/retail-product-checkout-dataset)
(15 GB)

</div>

\***Notice**: If downloading from Kaggle is not accessable, you can alternatively download the dataset using [Baidu Drive](https://pan.baidu.com/s/1vrrLaSpJe5JxT3zhYfOaog).

#### 3.1 Dataset license:  
[![](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)    
CC BY-NC-SA 4.0

#### 3.2 Overview infomation of the RPC dataset 

<div align="center">

| *Split* | *# images* | *# objects* | *# objects/image* | *# categories/image* |
| --- | ---: | ---: | ---: | ---: |
| Training set (Exemplar images) | 53,739 | 53,739 | 1 | 1 |
| Validation set (Checkout images) | 6,000 |   73,602 | 12.27 | 6.33 |
| Test set (Checkout images)| 24,000 |  294,333 | 12.26 | 6.31 |


</div>

#### 3.3 Collection equipment for single product images (training set)



<div align="center">

<a href="https://www.kaggle.com/diyer22/retail-product-checkout-dataset#retail_product_checkout.zip">
    <img style="width:700px" src="imgs/single.png">
</a>   
</div> 

#### 3.4 Different clutter levels for checkout images (val/test sets)


<div align="center">

<a href="https://www.kaggle.com/diyer22/retail-product-checkout-dataset#retail_product_checkout.zip">
    <img style="width:500px" src="imgs/test.png">
</a>   
</div>

#### 3.5 Detailed information of val+test sets for different clutters

<div align="center">

| *Clutter mode* | *# images* | *# objects* | *# objects/image* | *# categories/image* |
| --- | ---: | ---: | ---: | ---: |
|       Easy |  10,000 |   71,496 |                    7.15 |                      3.81 |
|     Medium |  10,000 |  122,961 |                   12.30 |                      6.27 |
|       Hard |  10,000 |  173,478 |                   17.35 |                      8.87 |


</div>

## 4. Proposed baseline method on the RPC dataset

#### 4.1 Pipeline of our *Syn+Render* method

<div align="center">
    <img style="width:700px" src="imgs/pipeline.png">

</div>

#### 4.2 Experimental results


<div align="center">
    <img style="width:700px" src="imgs/result.png">

</div>

## 5. Leaderboard


<div style="text-align: justify">

[**RPC-Leaderboard**](https://github.com/RPC-Dataset/RPC-Leaderboard)

If you have been successful in creating a model based on the training set and it performs well on the validation set, we encourage you to run your model on the test set. The  [`rpctool`](https://github.com/DIYer22/retail_product_checkout_tools) (in the next section in this project page) will contribute to return the corresponding results of the evaluation metrics. You can submit your results on the RPC leaderboard by creating a new issue. Your results will be ranked in the leaderboard and to benchmark your approach against that of other machine learners. We are looking forward to your submission. Please click [here](https://github.com/RPC-Dataset/RPC-Leaderboard/issues) to submit.

</div>

## 6. RPC-tool

<div style="text-align: justify">

[`rpctool`](https://github.com/DIYer22/retail_product_checkout_tools): A Python package for evaluating your methods on the RPC dataset. It can return several evaluation metrics (listed in the aforementioned table in Sec. 4.2). More information can be found in [`rpctool`](https://github.com/DIYer22/retail_product_checkout_tools).

</div>

## 7. ATTN

<div style="text-align: justify">

This dataset and code packages are free for academic usage. You can run them at your own risk. For other purposes, please contact the corresponding author Dr. Xiu-Shen Wei (weixs.gm [at] gmail.com).

</div>


<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-133191784-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-133191784-1');
</script>
