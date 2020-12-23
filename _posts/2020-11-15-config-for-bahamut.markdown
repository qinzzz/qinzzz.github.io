---
title: "Configuration-as-Code, Alibaba"
layout: post
date: 2020-11-15 22:10
tag: academic
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: ""
category: project
author: Qinxin Wang
externalLink: false
---

Completed at *Alibaba Group*, Hangzhou, China.  [Group](https://medium.com/datadriveninvestor/whats-the-secret-behind-alibaba-s-artificial-intelligence-online-serving-ai-os-ebe7ed67f7d5)

This project is put into production in *SARO(Search, Advertisement, Recommendation Offline)* – an offline big data Extract-Transform-Load (ETL) platform

SARO is an offline big data platform for search and recommendation, mainly used in [Taobao](https://world.taobao.com/) and [AliExpress](https://www.aliexpress.com/). 
Bahamut is the core processing engine of it, responsible for creating, scheduling, and computing data processing tasks.
We use Flink and Hbase as our computation and storage engine respectively.

![saro](../assets/posts/bahamut.jpg)

Bahamut transforms business graph (input by user) to intermediate DAGs, and finally to Flink & Airflow jobs. 
During this procedure, configurations are needed to customize apps, environments and Flink options for job generation, resource allocation, devops, etc.

My job:
- Designed a Configuration-as-Code module to manage configuration and feature toggle for the core processing engine, which supports automatic release, update, and delivery of configuration files.
- Refactored code with user-friendly interface and well-organized configuration files. 
Provides sanity check and validation API with Java annotation.

---
[Midterm report](../assets/posts/midreview.pdf) (in Chinese)
