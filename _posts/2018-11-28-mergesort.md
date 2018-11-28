---
title : MergeSort 
categories:
- algorithm
tags: 
- mergesort
- algorithm
---

## MergeSort
존 폰 노이만이 1945년에 개발한 정렬방법으로 합병 정렬 또는 병합 정렬은 비교 기반 정렬 알고리즘이다.  
일반적인 방법으로 구현했을 때 이 정렬은 안정 정렬에 속하며, 분할 정복 알고리즘의 하나이다.  

### 비교 정렬
**비교 정렬은 원소들을 정렬할 때 원소들의 순서에만 의존하는 알고리즘들을 일컫는다.**  
예를 들어 거품 정렬(bubble sort)은 비교하는 원소들이 숫자거나, 문자열이거나, 심지어는 복잡한 객체에 대해서도 순서가 결정되어 있다면 적용할 수 있다.  
  
비교 정렬 알고리즘들은 아무리 빨라도 최악의 경우 <math>\Omega \left(n\log n\right)</math><math>\left\{ A \right\}</math> 시간을 필요로 한다.  
이는 알고리즘들을 결정 트리의 형태로 기술할 수 있다는 점에서 증명할 수 있는데, n개의 원소들의 순열은 n!가지로 
이들을 잎노드로 가지는 결정 트리의 깊이는 스털링 근사에 따라 적어도 <math>\lceil \log n!\rceil \approx n\log n</math> 이어야 하기 때문이다.  
  
비교 정렬이 아닌 알고리즘들은 이런 시간 복잡도의 제약이 없지만, 대신 다른 제약을 가질 수 있다. 예를 들어 기수 정렬은 사전순으로 표기하고 분리하기 쉬운 
숫자나 문자열에 대해서는 효과적이지만, 그렇지 않은 객체들에 대해서는 일반 비교 정렬보다 느릴 수 있다.  

### 안정 정렬과 불안정 정렬
안정 정렬은 동일한 값에 대해 기존의 순서가 유지되는 정렬 방식이며,  불안정 정렬은 동일한 값에 대해 기존의 순서가 뒤바뀔 수 있는 정렬 방식  

### 분할 정복 알고리즘
분할 정복 알고리즘은 그대로 해결하 수 없는 문제를 작은 문제로 분할하여 문제를 해겨라는 방법이나 알고리즘이다

## 합병 정렬은 다음과 같이 작동한다.
&nbsp;&nbsp;&nbsp;&nbsp;**1.리스트의 길이가 0 또는 1이면 이미 정렬된 것으로 본다.**  
&nbsp;&nbsp;&nbsp;&nbsp;**2.정렬되지 않은 리스트를 절반으로 잘라 비슷한 크기의 두 부분 리스트로 나눈다.**  
&nbsp;&nbsp;&nbsp;&nbsp;**3.각 부분 리스트를 재귀적으로 합병 정렬을이용해 정렬한다.**  
&nbsp;&nbsp;&nbsp;&nbsp;**4.두 부분 리스트를 다시 하나의 정렬된 리스트로 합병한다.**  



## 참고자료
[1] https://ko.wikipedia.org/wiki/%ED%95%A9%EB%B3%91_%EC%A0%95%EB%A0%AC  (합정령렬 위키)  
[2] https://ko.wikipedia.org/wiki/%EC%A0%95%EB%A0%AC_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98#%EC%A2%85%EB%A5%98  (정렬알고리즘 위키)
[3] https://zetawiki.com/wiki/%EC%95%88%EC%A0%95%EC%A0%95%EB%A0%AC,_%EB%B6%88%EC%95%88%EC%A0%95%EC%A0%95%EB%A0%AC  (제타위키 안정정렬)

[3] https://www.hackerearth.com/practice/algorithms/sorting/merge-sort/tutorial/  
[4] https://gmlwjd9405.github.io/2018/05/08/algorithm-merge-sort.html  

