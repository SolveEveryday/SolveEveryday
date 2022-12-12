# 완전 탐색

다른말로 브루트포스(brute force, ~~무식한 힘~~) 라고도 한다.

완전탐색 알고리즘. 즉, 가능한 모든 경우의 수를 모두 탐색하면서 요구조건에 충족되는 결과만을 가져온다.

이 알고리즘의 장점은 예외 없이 100%의 확률로 정답만을 출력한다.

단 단점은 모든 경우의 수를 보기때문에 매우 느릴 수 있다.

## 예시

대표적으로 암호 해독법에서도 많이 쓰이는 방법이다.

4자리 숫자로 된 핸드폰의 암호는 0000, 0001, 0002... 9999까지 총 1만 개(10^4)의 조합 중 하나이므로, 이를 하나씩 대입해 보면 핸드폰의 암호를 통과할 수 있게 된다.

애플은 아이폰 비밀번호를 4회 이상 틀릴 경우 또 다른 지연시간이 발생하도록 했다. 5회째는 1분, 6회째 5분, 7~8회째 15분, 9회째는 1시간 ... 또한 사용자가 10번 틀리면 모든 데이터를 삭제하도록 설정할 수 있다.

만약 계속 틀리게된다면 몇백년이 되는 기이한 현상을 볼 수 도 있다.

## 예시2

N의 약수 합 구하기

```java
public List<Integer> getDivisors(int N) {
    List<Integer> divisors = new ArrayList<>();

    for (int i = 1; i <= N; i++) {
        if (N % i == 0) {
            divisors.add(i);
        }
    }

    return divisors
}
```

1..N까지 반복해서 약수인지 판단하고 해당 값들을 반환하는 메서드