---
layout: post
bigtitle:  "[Paper Review] A Brief Introduction to Optimal Transport Theory"
subtitle:   "Optimal Transport"
categories:
    - study
    - papers
tags:
  - Optimal Transport
related_posts:
  - 
comments: true
published: true
mathjax: true
---

* toc
{:toc}

# 0. Paper info.
-------------------------------------------------------------------
- **A Brief Introduction to Optimal Transport Theory**  
  - [Bourne, D. P. "A Brief Introduction to Optimal Transport Theory." July 27th (2018).](http://www.maths.gla.ac.uk/~gbellamy/LMS/BourneLectures.pdf)  

Optimal Transport 이론을 석사 수준 이하로 쉽게 설명하는 논문으로 처음 공부하는 사람에게 추천한다.  

# 1. Optimal Transport  
-------------------------------------------------------------------
Optimal Transport는 1781년 Gaspard Monge가 어떠한 집합체(mass)를 재구축하는 최적의 방법을 찾는 문제에 대한 관심을 가지며 시작되었다. 예를들어 거대한 흙 퇴적물을 이용하여 둑을 만든다고 하자. 이때, 가장 효율적으로 옮기는 **방법**을 찾는 것이 우리의 목적이다. 이를 통계로 가져와보자.

<br>  

<center>
<img src="../../../assets/img/study/papers/optimal_transport.png" width="100%">
<figcaption style='color: #808080'>출처 : https://medium.com/analytics-vidhya/introduction-to-optimal-transport-fd1816d51086</figcaption>
</center>  

<br>  

위 그림처럼 원래 흙 퇴적물의 모양을 $$X$$의 분포라고 하고, 둑의 모양을 $$Y$$의 분포라고 하면 우리는 분포에서 분포로 변형해주는 함수를 얻고자 한다. 이를 **Transport**라고 하는데, 이는 여러가지가 있을 수 있다. 여러 **Transport** 중 가장 효과적인(즉, 비용이 적게 드는) **Transport**를 **Optimal Tranport**라고 하고 이를 찾고자 한다.

# 2. Monge Problem
-------------------------------------------------------------------
위에서 설명한 문제를 수학적으로 정리하고자 한다.

## **The Monge problem**
> **[Definition 1]**   
> Let $$X, Y \subseteq \mathbb{R}^{d}$$. Let $f$ be a probability density on $$X$$ and $$g$$ be a probability density on $$Y$$. Let $$c: X \times Y \rightarrow[0, \infty)$$ be continuous. The Monge problem is to find a transport map $$T: X \rightarrow Y$$ satisfying $$T \# f=g$$ such that $$T$$ minimises the cost functional
> \[M(T):=\int_{X} c(x, T(x)) f(x) \mathrm{d} x .\]
> The optimal transport cost $$\mathcal{T}_{c}(f, g)$$ of transporting $$f$$ to $$g$$ with cost function $$c$$ is defined by
> \[\mathcal{T}_{c}(f, g):=\inf _{T \# f=g} M(T)\]


