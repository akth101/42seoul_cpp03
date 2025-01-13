# cpp03
cpp에서의 상속에 대해 공부하는 과제입니다.

---
목차
1. 과제를 하면서 알게 된 것들
2. 평가 피드백
---

1. 과제를 하면서 알게 된 것들  
상속에 이용되는 키워드들의 관계가 가장 헷갈리는 부분이었고, 과제를 진행하면서 아래와 같이 정리할 수 있었습니다.
~~~ c++
class Parent {
public: // 모두에게 공개
    int public_money;
protected: // 가족들에게만 공개
    int family_money;
private: // 나만 알고있음
    int secret_money;
};
~~~

1-1) public 상속
~~~ c++
class Child : public Parent {
    // public_money -> 여전히 public (모두에게 공개)
    // family_money -> 여전히 protected (가족들에게만 공개)
    // secret_money -> 접근 불가 (부모님의 비밀)
};
~~~

1-2) protected 상속
~~~ c++
class Child : protected Parent {
    // public_money -> protected로 변경 (가족들에게만 공개)
    // family_money -> protected (가족들에게만 공개)
    // secret_money -> 접근 불가
};
~~~

1-3) private 상속
~~~ c++
class Child : private Parent {
    // public_money -> private로 변경 (나만 알고있음)
    // family_money -> private로 변경 (나만 알고있음)
    // secret_money -> 접근 불가
};
~~~

2. 평가 피드백
<img width="740" alt="image" src="https://github.com/user-attachments/assets/248dafe5-5520-45df-bff2-9835166db1e0" />
