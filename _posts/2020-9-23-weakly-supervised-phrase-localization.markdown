---
title: "Multimodal alignment framework for weakly supervised phrase grounding"
layout: post
date: 2020-9-23 22:10
tag: academic
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: ""
category: project
author: qinxinWang
externalLink: false
---

<style>
img{
    width: 80%;
    padding-left: 10%;
}
</style>

![project1](../assets/posts/paper_fig_sup_baby.png)

In this work, we mainly focus on the alignment between image and text. Given the highlighted phrase “a young boy”, we want to find which region in the image does the phrase refers to. 
We follow a weakly-supervised setting, which requires only caption-image annotations. This is motivated by the high expenses of manual annotation of objects.

---
![model](../assets/posts/paper_fig_model_fig_new.png)

We develop a Multimodal Alignment Framework (MAF) to leverage more widely-available caption-image datasets, which can then be used as a form of weak supervision. 
We first present algorithms to model phrase-object relevance by leveraging fine-grained visual representations and visually-aware language representations. 

![contrastive](../assets/posts/contrastive.png)

We use a contrastive loss to train our model since we find the inter-sample information is more powerful in tackling the limited data problem. 
Our assumption is that for a given caption, it is more similar, in the multimodal embedding space, to its paired image than to other images in the dataset. 

---
Experiments conducted on the widely-adopted Flickr30k dataset show a significant improvement over existing weakly-supervised methods (from 38.71% to 61.43%). 
We also improved the unsupervised baseline from 50.49% to 56.05%.
___
