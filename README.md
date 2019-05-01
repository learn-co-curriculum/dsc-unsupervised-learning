
# Unsupervised Learning

## Introduction

In this lesson, we'll define Unsupervised Learning, and some typical tasks we can accomplish with Unsupervised Learning algorithms. We'll also discuss the benefits and drawbacks that come with Unsupervised tasks. 

## Objectives

You will be able to:

* Understand and explain the challenges inherent in Unsupervised Learning
* Identify real-world use cases for Unsupervised Learning
* Compare and Contrast Supervised and Unsupervised Learning, and identify algorithms that belong to each




## Supervised vs. Unsupervised Learning

So far, almost everything we've learned in this module has focused on **_Supervised Learning_**--every algorithm has required labeled training data to learn. In this section, we'll focus on a cornerstone Clustering techniques, which is a cornerstone of **_Unsupervised Learning_**. The term "Unsupervised Learning" refers to a class of learning algorithms that operate without labeled training data. Since labels come from humans, this makes getting labeled training data for Supervised Learning tasks time consuming and expensive. On the other hand, since we have labeled training data when working with Supervised Learning tasks, we have a way of evaluating the performance of our model.

Unsupervised Learning does not require labeled training data in order to work. On the one hand, this means that practically any data is data that we can use with Unsupervised Learning algorithms, since the need for labels isn't an issue here--we can take the data as it is, without worrying about spending time annotating data with labels (or paying a ton of money for other people to do it). However, this lack of labels also comes with a major drawback--we have no way of knowing how well our unsupervised learning algorithms are performing at any given time. 


<img src='images/diagram.jpg'>


The main difference between Supervised and Unsupervised Learning are their goals. Supervised Learning needs concrete, ground-truth labels to trian models that answer very specific questions. Unsupervised Learning differs in that the task it is trying to accomplish is much less well-defined--it can usually be summed up as "are there any natural patterns in this data that we can recognize?"  To illustrate this, let's assume for a second that we have a basket of various different kinds of fruit. A supervised learning task would be building an Apple classifier that tells us if a given fruit is or isn't an apple, based on the size, shape, color, texture, taste, and any other data that we find relevant (as well as some clearly labeled examples of fruit that are and aren't apples, because we need labels to train this algorithm!). An unsupervised learning task would be to just analyze the fruit in our basket, and see if we can find any patterns that we can use to separate them into different groups. Supervised learning uses data to accomplish a clear task. Unsupervised Learning has no clear task, but is instead used for analysis.


## Unsupervised Learning Tasks

 There are three main tasks Unsupervised Learning excels at--**_Clustering_**, **_Dimensionality Reduction_**, and **_Generative Modeling_**. Let's explore what each of these tasks looks like.


### Clustering

Clustering algorithms are probably the most common examples of Unsupervised Learning algorithms. There are a few different kinds of clustering algorithms, but they all do the same thing--finding different ways to group a dataset based on patterns in the data.  The most common use-case for clustering is probably Market Segmentation, which is a common task we'll explore more deeply in this section. It's quite common for Data Scientists to take data like customer transactions, and run a clustering algorithm to try to discover the different subgroups of customers that appear in the data. Even though there's no way to verify that these groups are correct, in practice, it usually does quite well, and often provides a ton of value to companies in regards to things like marketing efforts. In this section, we'll dig quite deep into the two most popular clustering approaches to see how we can perform market segmentation on a real-world dataset. 

<img src='images/kmeans.gif'>

### Dimensionality Reduction

Another popular subset of Unsupervised Learning algorithms deal with **_Dimensionality Reduction_**. The most common dimensionality reduction algorithm is **_Prinicpal Component Analysis_**, or **_PCA_**. It turns out that PCA can also be quite a useful tool when used in conjunction with clustering algorithms! Dimensionality reduction algorithms work by projecting data from it's current N-dimensional subspace into a smaller subspace, while losing as little information as possible in the process. Dimensionality reduction algorithms still lose _some_ information, but we can usually tell how much we're losing, and make an informed decision about the number of dimensions reduced versus the overall information lost. Dimensionality Reduction algorithms are a must-have in any Data Scientist's toolbox, because they provide a way for us to deal with the "Curse of Dimensionality". When we use dimensionality reduction algorithms, you'll notice that we provide no labels--we don't have any examples of what the data should look like after it has been reduced to a smaller dimension. Since the algorithm can perform this task without labels, this makes dimensionality reduction a type of Unsupervised Learning.

<img src='images/pca.gif'>

### Generative Modeling

Of the Unsupervised Learning areas discussed here, Generative Modeling is--by far--the most complex. This is an area of unsupervised learning that is almost exclusively performed with various types of Deep Neural Networks. Generative modeling refers to algorithms that look at example input data, and output their own unique versions that still match the pattern of the data. Since the algorithms doesn't have any labels of what the version they output should actually be, this makes it an unsupervised task. Here's an example of a **_Neural Style Transfer_** model, which takes in two pictures, and adds the style of one picture to the content of the other.

<img src='images/starry-doge.jpg'>


Another very promising area of research for generative modeling is **_Generative Adversarial Networks_**, or **_GANs_**. These networks are actually a combination of two or more neural networks--a discriminator, and a generator. The discriminator is a Supervised Learning model--it's only job is to look at images and predict if it's a real image, or an image that was created by the generator. Meanwhile, the generator's job is to create counterfeits that fool the discriminator. You can think of the generator as a counterfeiter, and the discriminator as a cop. As one gets better, it pushes the other to get better. The end result is a generator so good that it can usually fool humans. For instance, take a look at the following gif of celebrities:


<img src='images/gan.gif'>


The mindblowing thing about the celebrities seen in this gif is that _none of them are real!_ These were all created by a GAN. The discriminator was given a dataset of pictures of real celebrities, and discriminator got better at telling the fakes apart from the real pictures, the generator also got better at making fakes that were more and more convincing, until the result you see above! Every single person you see in the gif above is really just a neural network outputting individual pixel values for every pixel in the image, in a way that makes for a very convincing fake image of a person. 

A quick side note on generative modeling--you may be wondering why models like GANs are considered Unsupervised, when the discriminator involved in the model is clearly a Supervised Learning model. The main reason here is that the overall goal of the model is to output it's own fake images, which is an unsupervised task. Even though the model may use some supervised models as constituent pieces of itself in the process, since the overall task is unsupervised, the model itself is considered unsupervised. 

Don't worry if the generative modeling seems confusing right now--we'll get into this a bit more deeply when we explore Deep Learning. For the remainder of this section, we're going to focus on the bread and butter of Unsupervised Learning algorithms--**_Clustering!_**

## Summary

In this lesson, we explored the differences between Supervised and Unsupervised Learning. We also learned about the types of problems we can solve with Unsupervised Learning, such as Clustering, Dimensionality Reduction, and Generative Modeling. 

