---
layout: post
title: "LU decomposition"
subtitle: "LU decomposition"
mathjax: true
date: 2020-12-09 00:00:00 +0900
background: "/img/posts/06.jpg"
---

# LU 분해

lu 분해는 행렬분해의 일종이며, L은 lower triangle matrix, U는 upper triangle matrix 를 의미한다.

$$\begin{bmatrix}* & * & * \\* & * & * \\ * & * & * \end{bmatrix}= \begin{bmatrix}* & 0 & 0 \\* & * & 0 \\ * & * & * \end{bmatrix} \begin{bmatrix}* & * & * \\0 & * & * \\ 0 & 0 & * \end{bmatrix}$$

$$Ax = b$$ 를 $$(LU)x = b$$ 로, $$L(Ux) = b$$ 로 바꾼후, Ly = b 를 구한다. y 는 Ux이므로 쉽게 구할 수 있다. (전방대치법, 후방대치법 사용)

## LU 분해의 의미

LU 분해는 **가우스 소거법의 전방소거법을 행렬로 코드화** 한 것

- L: 행렬 A를 전방소거하는 데 쓰인 replacement, scaling에 대한 EROs를 기록한 것
- U: A를 전방소거한 후 남은 Upper triangle matrix
- P: 행렬 A를 전방소거하는데 쓰인 interchange에 대한 EROs를 기록해 둔 행렬 (옵션)
