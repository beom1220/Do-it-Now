# [1312] 소수

---

## 📌 **Algorithm**

---

수학

## 📍 **Logic**

---

```
remain = a % b;
for (int i = 0; i < n; i++) {
    result = (remain * 10) / b;
    remain = (remain * 10) % b;
}
```

- 나누기 계산을 손으로 푸는 방식처럼, 나머지에 10을 곱해서 다시 나누는 것을 반복하는 방식

## ✒️ **Review**

---

- 문제가 워낙 간단해서 처음에는 다른 방식으로 풀었다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        int a, b, n, div;
        Scanner sc = new Scanner(System.in);
        a = sc.nextInt();
        b = sc.nextInt();
        n = sc.nextInt();

        a = a * (int) Math.pow(10, n);
        div = a / b;

        System.out.println(div % 10);
    }
}
```

- 겉보기엔 맞아보였는데, 제출해보니 틀렸다고 나왔다.
- 아마 b나 n이 커졌을 때, 부동소수점 때문에 뭔가 잘못되는 것으로 예상했다.
- 다른 방법을 생각해보다가 결국 현실에서 이 문제를 해결할 때 사용하는 방식을 그대로 옮기기로 했다.
- 프로그램에서 부동소수점으로 인한 오차가 발생할 수 있다는 걸 이론적으론 알고 있었지만, 직접 겪어보긴 처음이었다.