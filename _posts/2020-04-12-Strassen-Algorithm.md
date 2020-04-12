---
layout: single
title:  "Strassen Algorithm"
date:   2020-04-12 18:03:48 +0900
categories: jekyll update
---

---

# 슈트라센 알고리즘(Strassen Algorithm)

슈트라센 알고리즘은 크기가 n x n의 행렬 A와 B의 곱셈 알고리즘을 기존의 일반적인 곱셈 방식보다 더 빠르게 할수 있도록 슈트라센이 제시한 알고리즘 인데,

A의 원소를 ![%5Ccombi%20_%7B%20ij%20%7D%7B%20a%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgk9ri3338ptm.jpg) , 여기서 $$i$$ 는 행, $$j$$ 는 열을 나타낸다.  행렬 B와 이 두행렬의 곱인 행렬 C의 원소도 같이 표현을 한다면,

![%5Ccombi%20_%7B%20ij%20%7D%7B%20c%20%7D%5Cquad%20%3D%5Cquad%20%5Csum%20_%7B%20k%3D1%20%7D%5E%7B%20n%20%7D%7B%20%5Ccombi%20_%7B%20ik%20%7D%7B%20a%20%7D*%5Ccombi%20_%7B%20kj%20%7D%7B%20b%20%7D%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgkdfr2qjsuqs.jpg) ![%3D%5Cquad%20%5Ccombi%20_%7B%20i1%20%7D%7B%20a%20%7D*%5Ccombi%20_%7B%201j%20%7D%7B%20b%20%7D%5Cquad%20%2B%5Cquad%20%5Ccombi%20_%7B%20i2%20%7D%7B%20a%20%7D*%5Ccombi%20_%7B%202j%20%7D%7B%20b%20%7D%5Cquad%20%2B%5Cquad%20...%5Cquad%20%2B%5Cquad%20%5Ccombi%20_%7B%20in%20%7D%7B%20a%20%7D%5Ccombi%20_%7B%20nj%20%7D%7B%20b%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgkf5tz3m7lu0.jpg) 로 나타낼수 있다.(**즉 각 행과 열을 곱해서 더해준다는 것!!**) 

### ex)  2x2행렬일때

![A*B%5Cquad%20%3D%5Cquad%20%5Cbegin%7B%20pmatrix%20%7D%7B%20%5Ccombi%20_%7B%2011%20%7D%7B%20A%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2012%20%7D%7B%20A%20%7D%20%7D%5C%5C%7B%20%5Ccombi%20_%7B%2021%20%7D%7B%20A%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D%20%7D%5Cend%7B%20pmatrix%20%7D%5Cquad%20%5Cbegin%7B%20pmatrix%20%7D%7B%20%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2012%20%7D%7B%20B%20%7D%20%7D%5C%5C%7B%20%5Ccombi%20_%7B%2021%20%7D%7B%20B%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D%20%7D%5Cend%7B%20pmatrix%20%7D%5C%5C%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%3D%5Cquad%20%5Cbegin%7B%20pmatrix%20%7D%7B%20%5Ccombi%20_%7B%2011%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2012%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2021%20%7D%7B%20B%20%7D%20%7D%26%7B%20%5Cquad%20%5Ccombi%20_%7B%2011%20%7D%7B%20%5Cquad%20A%20%7D%5Ccombi%20_%7B%2012%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2012%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D%20%7D%5C%5C%7B%20%5Ccombi%20_%7B%2021%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2021%20%7D%7B%20B%20%7D%20%7D%26%7B%20%5Cquad%20%5Cquad%20%5Ccombi%20_%7B%2021%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2012%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D%20%7D%5Cend%7B%20pmatrix%20%7D%5C%5C%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%5Cquad%20%3D%5Cquad%20%5Cbegin%7B%20pmatrix%20%7D%7B%20%5Ccombi%20_%7B%2011%20%7D%7B%20C%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2012%20%7D%7B%20C%20%7D%20%7D%5C%5C%7B%20%5Ccombi%20_%7B%2021%20%7D%7B%20C%20%7D%20%7D%26%7B%20%5Ccombi%20_%7B%2022%20%7D%7B%20C%20%7D%20%7D%5Cend%7B%20pmatrix%20%7D%5Cquad%20%3D%5Cquad%20C%20](http://images.se2.naver.com/smedit/2015/10/7/ifgm9ch32b5ok9.jpg)

 

### ---> A의 첫번째 행과 B의 첫번째 열의 각 원소의 곱의 합이 C의 첫번째 행과 열의 원소가 되는것이다.

즉, 2x2 행렬 C의 원소를 구하기 위해 총 8번의 곱셈과 4번의 덧셈을 해야한다는 것을 볼수있는데,  그러면 nxn 행렬의 원소를 구하기 위해서는 $$n^3$$ 의 곱셈과 $$n^2(n-1)$$의 덧셈을 해주어야 되는것을 알수있다.

### ex) 3x3행렬인 경우

행렬 A의 원소를 a1~a9, B의 원소를 b1~b9이라 하고, 그 두행렬의 곱인 행렬 C의 원소를 c1~c9이라 할때, 

c1=a1xb1+a2xb4+a3xb7   c2=a1xb2+a2xb5+a3xb8  c3,c4,c5=......

### --> c1을 구하는데 3번의 곱셈과 2번의 덧셈이 필요하며 행렬 C의 모든 원소를 구하려면 이 과정을 8번을 더 해야한다는 것을 알수 있으며, 결국 27번의 곱셈과 18번의 덧셈이 필요하다는 것을 알수있다.

따라서, 행렬의 곱셈은 ![%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%5Cquad%20%5Ctimes%20%5Cquad%20%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmf37fnvhr1r.jpg)크기의 행열을 8번 곱하고, ![%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%5Cquad%20%5Ctimes%20%5Cquad%20%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmf37fnvhr1r.jpg)크기의 행열을 4번 더한다.

더하기를 생략하고, 점화식으로 나타낸다면

![t(n)%5Cquad%20%3D%5Cquad%208%5Cquad%20*%5Cquad%20t(%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmgqm0xq3q9u.jpg) 

​     ![%3D%5Cquad%208%5Cquad%20*%5Cquad%208%5Cquad%20*%5Cquad%20T(%5Cfrac%20%7B%20n%20%7D%7B%204%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmhhs7v0lkqc.jpg)

​     ![...%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmntt48gttax.jpg)

​     ![%3D%5Cquad%20%5Ccombi%20%5E%7B%20logn%20%7D%7B%208%20%7D%5Cquad%20%3D%5Cquad%20%5Ccombi%20%5E%7B%203logn%20%7D%7B%202%20%7D%5Cquad%20%3D%5Cquad%20%5Ccombi%20%5E%7B%203%20%7D%7B%20n%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmn8i9vjl964.jpg) 으로 나타나진다(**점화식을 반복하다 보면 나온다는데 왜 이렇게 모델링을 했는지 잘 모르겠다..**) 이를 정리하면 **O($$n^3$$)** 이 되는걸 알수있다.

지금까지가 행렬의 곱셈의 표준적인 방법이었다면 지금부터는 1960년대 슈트라센이 발견한 알고리즘을 보도록 하자. 슈트라센은  행렬의 곱셈을 할때 다음과 같은 규칙을 발견했는데, 이를 가지고 행렬 A와 B의 곱을 표기했다.

![P%5Cquad%20%3D%5Cquad%20(%5Ccombi%20_%7B%2011%20%7D%7B%20A%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D)(%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D)%5C%5C%20Q%5Cquad%20%3D%5Cquad%20%5Ccombi%20_%7B%2021%20%7D%7B%20(A%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D)%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%5C%5C%20R%5Cquad%20%3D%5Cquad%20%5Ccombi%20_%7B%2011%20%7D%7B%20A%20%7D(%5Ccombi%20_%7B%2012%20%7D%7B%20B%20%7D-%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D)%5C%5C%20S%5Cquad%20%3D%5Cquad%20%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D(%5Ccombi%20_%7B%2021%20%7D%7B%20B%20%7D-%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D)%5C%5C%20T%5Cquad%20%3D%5Cquad%20%5Ccombi%20_%7B%2011%20%7D%7B%20(A%20%7D%2B%5Ccombi%20_%7B%2012%20%7D%7B%20A%20%7D)%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D%5C%5C%20U%5Cquad%20%3D%5Cquad%20(%5Ccombi%20_%7B%2021%20%7D%7B%20A%20%7D-%5Ccombi%20_%7B%2011%20%7D%7B%20A%20%7D)(%5Ccombi%20_%7B%2011%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2012%20%7D%7B%20B%20%7D)%5C%5C%20V%5Cquad%20%3D%5Cquad%20%5Ccombi%20_%7B%2012%20%7D%7B%20(A%20%7D-%5Ccombi%20_%7B%2022%20%7D%7B%20A%20%7D)(%5Ccombi%20_%7B%2021%20%7D%7B%20B%20%7D%2B%5Ccombi%20_%7B%2022%20%7D%7B%20B%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmttx5uq6pap.jpg) 

슈트라센 알고리즘에 의해 위에 나와있는 P~V의 연산으로 행렬 A,B의 곱 C의 원소를 나타낼수 있는데,

![%5Ccombi%20_%7B%2011%20%7D%7B%20C%20%7D%5Cquad%20%3D%5Cquad%20P%2BS-T%2BV%5C%5C%20%5Ccombi%20_%7B%2012%20%7D%7B%20C%20%7D%5Cquad%20%3D%5Cquad%20R%2BT%5C%5C%20%5Ccombi%20_%7B%2021%20%7D%7B%20C%20%7D%5Cquad%20%3D%5Cquad%20Q%2BS%5C%5C%20%5Ccombi%20_%7B%2022%20%7D%7B%20C%20%7D%5Cquad%20%3D%5Cquad%20P%2BR-Q%2BU%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmve7rpku5qa.jpg)

두 행열의 곱을 위의 R부터 V를 가지고 구한다면, ![%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%5Cquad%20%5Ctimes%20%5Cquad%20%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmf37fnvhr1r.jpg)크기의 행렬을 7번 곱하고![%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%5Cquad%20%5Ctimes%20%5Cquad%20%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmf37fnvhr1r.jpg)크기의 행렬을 18번 더한다. 더하기는 O-Notation에 의해 생략되므로 곱하기만을 계산해본다.

![t(n)%5Cquad%20%3D%5Cquad%207%5Cquad%20*%5Cquad%20t(%5Cfrac%20%7B%20n%20%7D%7B%202%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgn49i0ovefhs.jpg) 

​     ![%3D%5Cquad%207%5Cquad%20*%5Cquad%207%5Cquad%20*%5Cquad%20T(%5Cfrac%20%7B%20n%20%7D%7B%204%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgn4t6hcsos40.jpg)

 ![...%20](http://images.se2.naver.com/smedit/2015/10/7/ifgmntt48gttax.jpg)

​     ![%3D%5Cquad%20%5Ccombi%20%5E%7B%20logn%20%7D%7B%207%20%7D%5Cquad%20%3D%5Cquad%20%5Ccombi%20%5E%7B%202.807...%20%7D%7B%20n%20%7D%20](http://images.se2.naver.com/smedit/2015/10/7/ifgn5g6l0g03ie.jpg)

즉, ![O(%5Ccombi%20%5E%7B%202.807...%20%7D%7B%20n%20%7D)%20](http://images.se2.naver.com/smedit/2015/10/7/ifgnj7vpdn8pdg.jpg)의 성능을 갖는다.

## 결론

슈트라센 알고리즘을 사용하면 표준적인 곱의 계산보다 O-notation상의 속도는 더 빠르지만, P~V를 담아둘 공간을 마련해야 하여 행렬이 너무 클경우 자리를 많이 차지한다는 단점이 있다.(**컴퓨터는 곱셈연산이 덧셈연산보다 부담이 커서? 한번의 곱셈 연산을 덧셈의 연산으로 바꿔줌으로써 속도가 빨라진거 같다**) 

또한 빠른 속도에 비해 수치 안정성 면에서 떨어지는 모습을 보이기도 하니 슈트라센 알고리즘은 행렬 곱셈의 수행시간 단축을 위한 알고리즘이라 볼수 있을거 같다.

---

출처

1.(https://09ri.tistory.com/30)(스튜디오 다락)

2.(https://blog.naver.com/PostView.nhn?blogId=babobigi&logNo=220502327816&widgetTypeCall=true)

