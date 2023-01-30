---
title: Day 1 - Networks
weight: 1
disableToc: false
---

## Practical info

Time: 8:00 - 12


## Schedule for the day

|           | Time        | Activity                                                                                                                             | Data                                                                                                                            |
|-----------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Session 1 | 8:00-9:00   | [Warmup Network Exercise](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/Solution_M2_A1.ipynb) |                                                                                                                                 |
| Session 2 | 9:15-10:30  | Network exploration                                                                                                                  | [Danish power elites](https://github.com/SDS-AAU/SDS-master/raw/master/00_data/networks/elite_den17.csv)                        |
| Session 3 | 10:45-12:00 | European AI Companies                                                                                                                | [EU AI Startups](https://colab.research.google.com/github/aaubs/ds-master/blob/main/notebooks/M2_mapping_european_ai_starter.ipynb) |

https://colab.research.google.com/github/aaubs/ds-master/blob/main/notebooks/M2_mapping_european_ai_starter.ipynb
# Warm up: Manager Networks

## Introduction

* In this exercise, you will replicate a well known network analysis, with different data and some twists. 
* Data: The data is to be found at: https://github.com/SDS-AAU/SDS-master/tree/master/00_data/network_krackhard  (Hint: You neet to download the raw data)

## Data: What do I get?

Let the fun begin. You will analyze network datacollected from the managers of a high-tec company. This dataset, originating from the paper below, is widely used in research on organizational networks. Time to give it a shot as well.
Krackhardt D. (1987). Cognitive social structures. Social Networks, 9, 104-134. The company manufactured high-tech equipment on the west coast of the United States and had just over 100 employees with 21 managers. Each manager was asked to whom do you go to for advice and who is your friend, to whom do you report was taken from company documents.
Description

The dataset includes 4 files - 3xKrack-High-Tec and 1x High-Tec-Attributes. Krack-High-Tec includes the following three 21x3 text matrices:

* ADVICE, directed, binary
* FRIENDSHIP, directed, binary
* REPORTS_TO, directed, binary

Column 1 contains the ID of the ego (from where the edge starts), and column 2 the alter (to which the edge goes). Column 3 indicates the presence (=1) or absence (=0) of an edge.

High-Tec-Attributes includes one 21x4 valued matrix.

* ID: Numeric ID of the manager
* AGE: The managers age (in years)
* TENURE: The length of service or tenure (in years)
* LEVEL: The level in the corporate hierarchy (coded 1,2 and 3; 1 = CEO, 2 = Vice President, 3 = manager)
* DEPT: The department (coded 1,2,3,4 with the CEO in department 0, ie not in a department)


## Tasks

### 1. Create a network

* Generate network objects for the companies organizational structure (reports to), friendship, advice
* This networks are generated from the corresponding edgelists
* Also attach node characteristics from the corresponding nodelist

### 2. Analysis

Make a little analysis on:

A: Network level characteristics. Find the overal network level of:

* Density
* Transistivity (Clustering Coefficient)
* Reciprocity

... for the different networks. Describe and interpret the results. Answer the following questions:

* Are relationships like friendship and advice giving usually reciprocal?
* Are friends of your friends also your friends?
* Are the employees generally more likely to be in a friendship or advice-seeking relationship?

B: Node level characteristics: Likewise, find out:

* Who is most popular in the networks. Who is the most wanted friend, and advice giver?
* Are managers in higher hirarchy more popular as friend, and advice giver?

C: Relational Characteristics: Answer the following questions:

* Are managers from the same 1. department, or on the same 2. hirarchy, 3. age, or 4. tenuere more likely to become friends or give advice? (hint: assortiativity related)
* Are friends more likely to give each others advice?


### 3. Visualization

Everything goes. Show us some pretty and informative plots. Choose what to plot, and how, on your own. Interpret the results and share some insights.

<!---
### Solution

*  [:::: HERE ::::](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/Solution_M2_A1.ipynb)
--->


# Danish Power Elites

![](https://source.unsplash.com/GWe0dlVD9e0)

> Many people dream of being one of them, but only few make it all the way to the top. According to two CBS researchers, it takes more than just hard work to get to the top of the Danish hierarchy of power. [read more](https://www.cbs.dk/en/alumni/news/a-look-the-danish-power-elite)

In this project we are going to construct and explore a network of Danish power elites derived from boards of various organisations in th country.
We will construct an association network: Who is being in the same board? And first explore "basic" centrality indicators. Then identify communities and central persons within those. Finally we look at some "fancier" interactive network visualisation.


## Context: The Danish Power Elites

* [Antons PhD Thesis](https://magtelite.dk/wp-content/uploads/2015/09/Anton-Grau-Larsen-PhD-Elites-in-Denmark.pdf)
* [Brief Summary of findings (CBS)](https://www.cbs.dk/en/alumni/news/a-look-the-danish-power-elite)
* [Journal Paper in Sociology](https://journals.sagepub.com/doi/abs/10.1177/0038038512454349)
* More to be found with googleling...

## Data

* [Github (R Repository)](https://github.com/antongrau/eliter)
* [Magteliten website](https://magtelite.dk/data/)
* Or, easier... on [our github](https://github.com/SDS-AAU/SDS-master/raw/master/00_data/networks/elite_den17.csv)

## Tasks

* Who are the most central persons?
* Communities?
* What characterizes them?
* Link up with additional data?


<!---
## Solution
* [Python Magteliten Analysis](https://colab.research.google.com/github/aaubs/ds-master/blob/main/notebooks/M2_power_elites.ipynb)
--->

# EU Start-Ups

![](https://source.unsplash.com/VBLHICVh-lI)

In this exercise, we will analyze the company-link network of startups listed in the [European AI Landscape](https://www.ai-startups-europe.eu). In a collaboration with [istari.ai](https://istari.ai), we scraped links from all of their webpages, resulting in a dataset of around 1000 companies.
Your task is to identify the key players in AI in Europe that extend beyond the initial list.



## Notebooks

* [Starter EU AI companies starter](https://colab.research.google.com/github/aaubs/ds-master/blob/main/notebooks/M2_mapping_european_ai_starter.ipynb
)
<!---
* [Starter EU AI companies](https://colab.research.google.com/github/SDS-AAU/DSBA-2022/blob/master/notebooks/M2_mapping_european_ai.ipynb)


--->

