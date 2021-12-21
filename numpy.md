# Numpy  
> Numpy는 Numerical Python의 줄임말로 고성능의 과학계산 컴퓨팅과 데이터 분석에 필요한 기본 패키지이다. 제공되는 기능은 다음과 같다.  

Numpy를 사용하기위해서는 numpy 패키지를 부른다  
```python
import numpy as np # 사용하기 편하게 약자로 하기 위해서 as np라고 해준다.
```
## 다차원 배열(Arrays)
-Numpy가 제공하는 ndarray(n-dimensional array)은 같은 종류의 데이터를 담을 수 있는 다차원 배열이며, 
모든 원소는 같은 자료형이어야 한다. 모든 배열은 각 차원의 크기를 알려주는 shape라는 튜플과 배열에 저장된 자료형을 
알려주는 type이라는 객체를 가진다. ndarray의 차원(dimension)은 rank라고 부른다.  
-ndarray는 array 함수와 중첩된 리스트(list)를 이용하여 생성할 수 있으며, []를 이용하여 인덱싱(indexing)을 한다.
```python
a = np.array([1, 2, 3])  # 1차원 배열 생성
print(type(a), a.shape, a[0], a[1], a[2])
a[0] = 5                 # 배열의 한 원소를 변경
print(a)
```
결과  
<class 'numpy.ndarray'> (3,) 1 2 3는 print(type(a), a.shape, a[0], a[1], a[2])의 값  
[5 2 3]는 배열의 한 원소를 변경하고 print(a)한 값 

```python
b = np.array([[1,2,3],[4,5,6]])   # 2차원 배열 생성
print(b) #2차원 배열의 모양을 확인
```
#배열의 각 차원의 크기를 보려면 "print(b.shape)" 이런식으로 하면된다. .shape함수를 써서 확인


### numpy는 array함수 외에도 배열을 생성하기 위한 다양한 방법을 제공.
1. np.zeros() #값이 모두 0인 배열을 생성, 매개변수는 원하는 shape=차원의 크기  
사용방법
```python
a=np.zeros((2,3))
print(a)
```
2. np.ones() #값이 모두 1인 배열을 생성, 매개변수는 원하는 shape=차원의 크기  
사용방법
```python
a=np.ones((2,3))
print(a)
```
3. np.full((),x) #모든 원소가 원하는 x값으로 초기화된 배열 생성
사용방법
```python
a=np.full((2,3),7)
print(a)
```
4. np.eye(4) #2x2의 단위행렬을 생성
사용방법
```python
a=np.eye(4)
print(a)
```
5. np.random.random(()) #무작위 값으로 이루어진 배열 생성.매개변수는 원하는 shape=차원의 크기  
사용방법
```python
a=np.random.random((2,4))
print(a)
```
