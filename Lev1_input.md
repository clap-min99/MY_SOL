### 입출력과 사칙연산

#### Hello world

Q. Hello world!를 출력하시오

```python
print('Hello world!')
```
---

#### A+B

Q. 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A+B를 출력한다.

예제 입력  `1 2`

예제 출력  `3`

```python
a, b = int(input())
print(a+b)
```
---

#### A-B

Q. 두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A-B를 출력한다.

예제 입력  `3 2`

예제 출력  `1`

```python
a, b = int(input())
print(a-b)
```
---
#### AXB

Q. 두 정수 A와 B를 입력받은 다음, AXB를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 AXB를 출력한다.

예제 입력  `1 2`

예제 출력  `2`

```python
a, b = int(input())
print(a*b)
```
---
#### A/B

Q. 두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.

입력: 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

출력: 첫째 줄에 A+B를 출력한다.

예제 입력  `1 3`

예제 출력  `0.3333333333`

```python
a, b = int(input())
print(a/b)
```
---
#### 사칙연산

Q. 두 자연수 A와 B가 주어진다. 이때, A+B, A-B, A*B, A/B(몫), A%B(나머지)를 출력하는 프로그램을 작성하시오. 

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
