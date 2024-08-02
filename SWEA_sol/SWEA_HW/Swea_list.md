### List

#### 숫자카드(#4834)

0에서 9까지 숫자가 적힌 N장의 카드가 주어진다.

가장 많은 카드에 적힌 숫자와 카드가 몇 장인지 출력하는 프로그램을 만드시오. 카드 장수가 같을 때는 적힌 숫자가 큰 쪽을 출력한다.

[입력]


첫 줄에 테스트 케이스 개수 T가 주어진다.  ( 1 ≤ T ≤ 50 )

다음 줄부터 테스트케이스의 첫 줄에 카드 장수 N이 주어진다. ( 5 ≤ N ≤ 100 )

다음 줄에 N개의 숫자 ai가 여백없이 주어진다. (0으로 시작할 수도 있다.)  ( 0 ≤ ai ≤ 9 )


[출력]

각 줄마다 "#T" (T는 테스트 케이스 번호)를 출력한 뒤, 가장 많은 카드의 숫자와 장 수를 차례로 출력한다.

```py
T = int(input())
for i in range(1,T+1):
  N = int(input()) 
  a = str(input())             # 연속된 숫자를 인덱싱 하기 위해 문자열로 바꿈
  a_list = []        
  for x in range(N):
    a_list.append(int(a[x]))   # a_list에 바꿨던 문자열을 숫자로 바꾸어 다시 넣음

    count_m = [0]*10           # 0부터 9까지의 자리를 count_m에 할당(?)

    for j in a_list:
      count_m[j] += 1          # 각 숫자가 몇번 나왔는지 count_m에 기록
    
    max_lst = []               # 가장 많은 카드의 숫자를 넣는 리스트
    max_num = max(count_m)     # 가장 많은 카드의 수

    for k in range(len(count_m)):
      if count_m[k] == max(count_m):
        max_lst.append(k)
  
  print(f'#{i} {max(max_lst)} {max_num}')

```
Sol point

자리를 셀 수 있는 비어있는 리스트를 만든다.


---
#### 부분집합의 합(#4837)
1부터 12까지의 숫자를 원소로 가진 집합 A가 있다. 집합 A의 부분 집합 중 N개의 원소를 갖고 있고, 원소의 합이 K인 부분집합의 개수를 출력하는 프로그램을 작성하시오.

해당하는 부분집합이 없는 경우 0을 출력한다. 모든 부분 집합을 만들어 답을 찾아도 된다.
 

예를 들어 N = 3, K = 6 경우, 부분집합은 { 1, 2, 3 } 경우 1가지가 존재한다.


[입력]
 

첫 줄에 테스트 케이스 개수 T가 주어진다.  ( 1 ≤ T ≤ 50 )
 

테스트 케이스 별로 부분집합 원소의 수 N과 부분 집합의 합 K가 여백을 두고 주어진다. ( 1 ≤ N ≤ 12, 1 ≤ K ≤ 100 )
 

[출력]
 
각 줄마다 "#T" (T는 테스트 케이스 번호)를 출력한 뒤, 답을 출력한다.

```py
# SOL_1
for tc in range(int(input())):
  N , K = map(int, input().split())
  arr = []
  for x in range(12):
    arr.append(x)
  counts = 0
  subsets = []                      # 총 부분 집합
  for i in range(2**12):            # 집합 원소 개수 n일때 부분집합의 총 개수 2^n
    subset= []                      # 각 부분집합을 담을 list
    for j in range(12):
      if i & (1 << j):              # 비트연산자 &, << 
        subset.append(arr[j]+1)     # arr 리스트가 0부터 시작하므로
    subsets.append(subset)
  for y in range(2**12):
    if len(subsets[y])== N and sum(subsets[y]) == K:  # 부분집합의 길이가 N, 합이 K인 경우를 동시에 충족할 때
      counts += 1 
  print(f'#{tc+1} {counts}')
```
- Sol_point

    비트 연산을 이용한 부분 집합 생성

```py
#SOL_2

from itertools import combinations 
 
T = int(input())
arr = [i for i in range(1, 13)]
answer = []
 
for _ in range(T):
    N, K = map(int, input().split())
    count = 0
    for comb in combinations(arr, N):
        if sum(comb) == K:
            count += 1
    answer.append(count)
 
for i in range(T):
    print(f'#{i+1} {answer[i]}')
```
- Sol point

    내장함수 combinations를 이용한 풀이.

    다양한 풀이 방법 숙지해보기
---

