# 백준 21921 자바
백준 21921 자바

https://www.acmicpc.net/problem/21921

블로그 시작한 지 벌써  N일 지난 상태에서

X일 기간마다 조회수를 구해서

출력값 첫줄에 최대값 출력

출력값 둘째 줄에 최대값 기간 빈도수 출력

투 포인트 알고리즘을 적용해서 풀어봤습니다

상세 내용은 주석에 달려 있습니다


문제 풀이법

문제 입력이 아래와 같이 되어 있을 경우

5 2

1 4 2 5 1

​

투 포인트 알고리즘을 이용하여

start = 0, end = 0을 주어

​

0번째 날 1 조회수

1번째 날 4 조회수

2번째 날 2 조회수

3번째 날 5 조회수

4번째 날 1 조회수

​

while문을 돌려 위와 같이 end index값을 상승시켜 sum에 계속 더해줍니다.

X는 2이니 2일 기간마다 비교해서 최대값을 구해야 하니

​

차례대로 더한다고 했죠?

1 + 4 일때 최대값에 넣어 준후

즉 0번째 날과 1번째 날을 더해서

1번째날과 2번째 날을 비교해야 하니

​

1 + 4 + 2 일때 맨 앞의 1의 값을 빼주면 자동으로 1번째날과 2번째 날이 되니

이 둘을 비교해서 최대값에 넣어주면 됩니다.

​

즉 end index는 계속 상승해주면서 더해주며 start index는 검사일 2일이 될때마다

맨 첫번째 값 뺴주며 start index를 상승시켜주면 최대값을 찾아줍니다.

​

최대값을 찾아주며 최대값과 같은 값이 있으면 최대값 기간 빈도수도 카운트를 세줍니다
