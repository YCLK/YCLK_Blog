+++
title = '2024 SW 아카데미 2주차 | 리스트와 반복 구조'
date = 2024-06-11T13:57:36+09:00
draft = false

[cover]
image = 'images/cover.png'
+++

## | 리스트란?

비슷한 속성의 변수가 100개 이상이 필요한 프로그램에서는 각각의 변수에 이름을 부여하는 게 아니라 **하나의 이름에 번호를 부여**하여 문제를 해결할 수 있다.

**변수**가 **박스 하나**라고 본다면, **리스트**는 그런 박스들을 **여러 개 붙여 놓은 것**이라고 할 수 있다.
**하지만 리스트는 박스들의 연속 덩어리에만 이름을 정해주고, 값 하나하나는 번호로 호출한다**

![](images/Pasted%20image%2020240611063902.png)
![](images/Pasted%20image%2020240611063830.png)

리스트는 `,` 로 구분된 여러 값을  **대괄호**`[ ]`로 묶어 표현한다.
리스트는 **파이썬의 모든 객체**(리스트도 가능함)를 원소로 가질 수 있으며, 빈 리스트도 생성할 수 있다.

```python
리스트이름 = [값1, 값2, 값3]
```

문자열과 같이, **대괄호**를 이용하여 리스트의 **원소 각각을 참조**할 수 있고(인덱싱) 문자열과 달리, **인덱싱**으로 **리스트의 원소를 변경**할 수 있다.

`+` 연산자로 **두 리스트를 연결**할 수 있으며 문자열과 같은 방식`:` 으로 **슬라이스** 할 수 있다.

**in 연산자**로 특정 원소가 **리스트에 있는지** 확인할 수 있다.
### | 리스트 사용 예시

```python
# 리스트 a 생성 후 1,2,3 번째 값을 정해준다.
a = [2, 13, 7] print(a)
```

```python
# 리스트 각각의 값은 인덱스로 불러올 수 있다.
a = [1 ,2 ,3 ,4 ,5 ,6 ,7 ,8 ,9]

print(a[1])
print(a[8])
```

```python
# 생성된 리스트 a의 첫 번째 값과 마지막 값을 바꿔준다.
a = [3 , 5 , 6]
print(a)

a[0] = 15
print(a)

a[2] = 1000
print(a)
```

```python
# 변수를 문자열로 생성하였을 때, 그 변수는 자동으로 리스트로 생성이 된다.
test_string = 'hello! python!'
print(test_string) 

print(test_string[0],test_string[1],test_string[2],test_string[3],test_string[4])
```


## | 반복 구조란?

반복 조건의 **참/거짓**에 따라 **동일한 명령이 반복적**으로 실행되는 것이다.
다음과 같은 문제는 일일이 해결하기 힘들기에 반복 구조가 필요하다.

> 1부터 100까지 합을 구하는 문제
> 1부터 100까지 전부 출력 해야 하는 문제
> 반복된 동작으로 해결할 수 있는 문제

**문제를 해결하면서 여러 개의 반복 패턴을 가졌거나, 반복 패턴 안에서 사용되는 변수의 값이 중첩으로 바뀌어야 할 때, 반복문은 중첩하여 사용할 수 있음**
## | for 반복문이란?

반복적으로 특정 코드를 실행하게 해주는 루프로, 반복에 사용되는 변수가 존재한다.
루프가 한 번씩 진행될 때마다 루프 변수를 변화 시켜주며, 루프변수의 변화되는 값은 in 뒤에 적혀있는 집합의 값을 참조한다.

집합의 예시로는 **문자열: 문자의 집합, 리스트: 여러 값들의 집합, (텍스트)파일: 줄의 집합**이 있음

```python
for 루프변수 in 집합 : 
	반복코드
```

### | for문 사용 예시

```python
# 리스트에 들어있는 0~4까지의 숫자를 차례대로 출력함
for i in [0, 1, 2, 3, 4] : 
	print(i)
```

```python
# range() 함수로 만든 0~9의 숫자를 차례대로 출력함
for i in range(0, 10) : 
	print(i)
```

```python
friends = ['Joseph', 'Glenn', '하늘']
for friend in friends : 
	print("Hello!", friend)
```

## | range() 함수란?

**연속적인 숫자 객체**를 만들어서 반환해주는 함수

* range(A): 0부터 `A-1`까지의 숫자 객체를 만들어 줌
- range(A, B): A부터 `B-1`까지의 숫자 객체를 만들어 줌
- range(A, B, C): A부터 `B-1`까지의 숫자 객체를 C간격으로 만들어 줌

### | range() 함수의 사용 예시

```python
a = list(range(10))
print(a)
```

```python
a = list(range(5, 10))
print(a)
```

```python
a = list(range(0, 10, 2))
print(a)
```

**range를 list로 바꿔줄 수 있음**
## | 대입 연산자란?

오른쪽 항을 왼쪽 항에 **대입**하기 위해 사용되는 연산자

| 종류  | 정의                            |
| --- | ----------------------------- |
| =   | 우항을 좌항에 대입한다.                 |
| +=  | 좌항과 우항을 더한 값에 좌항에 대입한다.       |
| -+  | 좌항에서 우항을 뺀 값에 좌항에 대입한다.       |
| *=  | 좌항과 우항을 곱한 후 좌항에 대입한다.        |
| **= | 우항을 제곱한 후 좌항에 대입한다.           |
| /=  | 좌항을 우항으로 나눈 값을 좌항에 대입한다.      |
| //= | 좌항을 우항으로 나눈 값의 몫을 좌항에 대입한다.   |
| %=  | 좌항을 우항으로 나눈 값의 나머지를 좌항에 대입한다. |
```python
a = 10
print(a)
```

```python
a = 10
a += 1 # a = a + 1과 같음
print(a)
```
## | while 반복문이란?

조건문의 값이 `true`일 때, 특정 코드가 실행되는 반복문
즉, 조건문의 값이 `false`가 되면 **루프가 종료**된다.

```python
while 조건문 : 
	코드
```
### | while 반복문 사용 예시

```python
# 무한 반복문
while true : 
	코드
```
## | continue란?

반복문 안에서 사용하는 명령어
continue 아래에 작성된 코드를 **실행하지 않고 반복문의 시작**(질문)으로 돌아감
### | continue 사용 예시

```python
# 0부터 9까지의 숫자 중 5를 제외하고 출력함
for i in range(0, 10) : 
	if i == 5 : 
		continue
	print(i)
```
## | break란?

반복문 안에서 사용하는 명령어
반복문을 **종료**하고 다음 코드로 넘어가는 명령어
### | break 사용 예시

```python
# i가 10이 되면 무한 루프를 종료함
i = 0

while true : 
	if i == 10 : 
		break
	i = i + 1
```