### 입출력과 사칙연산

#### Hello world(#2557)

Hello world!를 출력하시오

```python
print('Hello world!')
```
---

#### A+B(#1000)

두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A+B를 출력한다.

예제 입력  `1 2`

예제 출력  `3`

```python
a, b = int(input())
print(a+b)
```
---

#### A-B(#1001)

두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A-B를 출력한다.

예제 입력  `3 2`

예제 출력  `1`

```python
a, b = int(input())
print(a-b)
```
---
#### AXB(#10998)

두 정수 A와 B를 입력받은 다음, AXB를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 AXB를 출력한다.

예제 입력  `1 2`

예제 출력  `2`

```python
a, b = int(input())
print(a*b)
```
---
#### A/B(#1008)

두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A+B를 출력한다.

예제 입력  `1 3`

예제 출력  `0.3333333333`

```python
a, b = int(input())
print(a/b)
```
---
#### 사칙연산(#10869)

두 자연수 A와 B가 주어진다. 이때, A+B, A-B, A*B, A/B(몫), A%B(나머지)를 출력하는 프로그램을 작성하시오. 

입력: 두 자연수 A와 B가 주어진다. (1 ≤ A, B ≤ 10,000)

출력: 첫째 줄에 A+B, 둘째 줄에 A-B, 셋째 줄에 A*B, 넷째 줄에 A/B, 다섯째 줄에 A%B를 출력한다.

```python
A, B = map(int, input().split())
print(A+B)
print(A-B)
print(A*B)
print(A//B)
print(A%B)
```
---
#### ??!(#10926)
준하는 사이트에 회원가입을 하다가 joonas라는 아이디가 이미 존재하는 것을 보고 놀랐다. 준하는 놀람을 ??!로 표현한다. 준하가 가입하려고 하는 사이트에 이미 존재하는 아이디가 주어졌을 때, 놀람을 표현하는 프로그램을 작성하시오.

입력: 첫째 줄에 준하가 가입하려고 하는 사이트에 이미 존재하는 아이디가 주어진다. 아이디는 알파벳 소문자로만 이루어져 있으며, 길이는 50자를 넘지 않는다.

출력: 첫째 줄에 준하의 놀람을 출력한다. 놀람은 아이디 뒤에 ??!를 붙여서 나타낸다.

```python
name = input()
a = ['jonnas''soomin', 'eunji']

if name in a:
    print(name+'??!')
else:
    print(name)
```
---
#### 나머지(#10430)
(A+B)%C는 ((A%C) + (B%C))%C 와 같을까?

(A×B)%C는 ((A%C) × (B%C))%C 와 같을까?

세 수 A, B, C가 주어졌을 때, 위의 네 가지 값을 구하는 프로그램을 작성하시오.

입력: 첫째 줄에 A, B, C가 순서대로 주어진다. (2 ≤ A, B, C ≤ 10000)

출력: 첫째 줄에 (A+B)%C, 둘째 줄에 ((A%C) + (B%C))%C, 셋째 줄에 (A×B)%C, 넷째 줄에 ((A%C) × (B%C))%C를 출력한다.

예제 입력 `5 8 4`

예제 출력 `1 1 0 0`

```python
A, B, C = map(int, input().split())
print((A+B)%C)
print(((A%C)+(B%C))%C)
print((A*B)%C)
print(((A%C)*(B%C))%C)
```
---
#### 1998년생인 내가 태국에서는 2541년생?!(#18108)

ICPC Bangkok Regional에 참가하기 위해 수완나품 국제공항에 막 도착한 팀 레드시프트 일행은 눈을 믿을 수 없었다. 공항의 대형 스크린에 올해가 2562년이라고 적혀 있던 것이었다.

불교 국가인 태국은 불멸기원(佛滅紀元), 즉 석가모니가 열반한 해를 기준으로 연도를 세는 불기를 사용한다. 반면, 우리나라는 서기 연도를 사용하고 있다. 불기 연도가 주어질 때 이를 서기 연도로 바꿔 주는 프로그램을 작성하시오.

입력: 서기 연도를 알아보고 싶은 불기 연도 y가 주어진다. (1000 ≤ y ≤ 3000)

출력: 불기 연도를 서기 연도로 변환한 결과를 출력한다.

```python
y = int(input())

if y in range (1001, 3000):
  print(y - 543)
  ```
---
#### 곱셈(#2588)

(세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.

![세자리 곱셈식](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)

(1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

입력: 첫째 줄에 (1)의 위치에 들어갈 세 자리 자연수가, 둘째 줄에 (2)의 위치에 들어갈 세자리 자연수가 주어진다.

출력: 첫째 줄부터 넷째 줄까지 차례대로 (3), (4), (5), (6)에 들어갈 값을 출력한다.

예제 입력

`472`

`385`

예제 출력

`2360`

`3776`

`1416`

`181720`

```python
num_1 = int(input())
num_2 = int(input())

num_2_list = list(map(int, str(num_2)))

num_3 = (num_1)*(num_2_list[2])
num_4 = (num_1)*(num_2_list[1])
num_5 = (num_1)*(num_2_list[0])

print(num_3)
print(num_4)
print(num_5)
print((num_3)+10*(num_4)+100*(num_5))
```
---
#### 꼬마정민(#11382)
꼬마 정민이는 이제 A + B 정도는 쉽게 계산할 수 있다. 이제 A + B + C를 계산할 차례이다!

입력: 첫 번째 줄에 A, B, C (1 ≤ A, B, C ≤ 1012)이 공백을 사이에 두고 주어진다.

출력: A+B+C의 값을 출력한다.
```py
A, B, C = map(int, input().split())
print(A + B + C)
```

