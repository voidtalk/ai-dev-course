---
layout: post
title: "gaussian elimination"
subtitle: "gaussian elimination"
mathjax: true
date: 2020-12-09 00:00:00 +0900
background: "/img/posts/06.jpg"
---

# 가우스 소거법

## 선형시스템의 해 (Solution of Linear System)

1. 해가 하나인 경우
   $$3x = 6$$

2. 해가 없는 경우
   $$0x = 6$$

3. 해가 여러개인 경우
   $$0x = 0$$

$$ax = b$$ 에 대하여, a = 0이면 특이(singular)하다고 한다.(a의 역수가 존재하지 않으므로)

- 해가 있으면 선형시스템이 consistent 하다고 한다.
- 해가 없으면 선형시스템이 inconsistent 하다고 한다.

## 선형시스템의 경우에도 마찬가지

1. 해가 하나인 경우

$$\begin{bmatrix}1 & 3 \\-2 & 1 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\3 \end{bmatrix}$$

2. 해가 없는 경우

$$\begin{bmatrix}1 & 3 \\2 & 6 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\5 \end{bmatrix}$$

두 그래프가 평행한 꼴, 0x = 6 과 같은 느낌이다. 위 식에서, $$\begin{bmatrix}1 & 3 \\2 & 6 \end{bmatrix}$$ 를 singular 하다고 한다. 역행렬이 없기 때문이다. 또한 inconsistent한 식이다.

3. 해가 무한한 경우

$$\begin{bmatrix}1 & 3 \\2 & 6 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\4 \end{bmatrix}$$

두개의 직선이 겹친다. singular한 행렬이 식에 있는 동시에 consistent한 식이다.

## 가우스 소거법

1. 전방 소거법 (Foward elimination)
   주어진 선형시스템을 아래로 갈수록 단순한 형태의 선형방정식을 가지도록 변형한다.

2. 후방 대입법 (back-substitution)
   아래서부터 위로 가면서 미지수를 대입한다.

## 전방 소거법

$$\begin{bmatrix}* & * & * \\* & * & * \\ * & * & * \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\ x_{3} \end{bmatrix} = \begin{bmatrix}* \\*\\* \end{bmatrix}$$

의 식을,

$$\begin{bmatrix}* & * & * \\0 & * & * \\ 0 & 0 & * \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\ x_{3} \end{bmatrix} = \begin{bmatrix}* \\*\\* \end{bmatrix}$$

으로 변경하는 과정.

마지막에 $$x_{3} = *$$ 이 나오도록 식이 변경된 것.

## 후방 대입법

아래의 간단한 수식을 통해 미지수의 답을 구한 후, 위로 가면서 대입하게 된다.

## 전방 소거법 실제로 하는 법

EROs(Elementary Row operations)를 통해 이루어진다.

Replacement(치환), Intercharge(교환), Scaling(스케일링)

## (중요) 전방 소거법의 가치

1. 주어진 선형시스템을 쉬운 꼴로 변형한다.
   Upper triangular form 을 통해, 맨 아래식은 아주 쉽게 풀 수 있다.

2. 주어진 선형시스템의 rank를 알려준다.

3. 해가 있는지 (consistent), 해가 없는지(inconsistent) 알 수 있다.

ex) 2 x 2 의 식을 받았지만, 의미 있는 식은 하나밖에 없다 (rank = 1) 라는 걸 알려줄 수 있다.

$$\begin{bmatrix}1 & 3 \\2 & 6 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\4 \end{bmatrix}$$

의 식을,

$$\begin{bmatrix}1 & 3 \\0 & 0 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\0 \end{bmatrix}$$

으로 바꿔준다. 마지막 식은 $$0=0$$ 이다.

또한, 해가 있는지 (consistent), 해가 없는지(inconsistent) 알 수 있다.

$$\begin{bmatrix}1 & 3 \\0 & 0 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\0 \end{bmatrix}$$

rank = 1이고, 해가 존재한다.

$$\begin{bmatrix}1 & 3 \\0 & 0 \end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \end{bmatrix} = \begin{bmatrix}2 \\1 \end{bmatrix}$$

해가 없다.
