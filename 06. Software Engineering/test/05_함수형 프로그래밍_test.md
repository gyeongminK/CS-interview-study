## 함수형 프로그래밍

--- 

1. 다음 중 함수형 프로그래밍과 관련된 말이 아닌것은?  
  1️⃣. Pure Function  
  2️⃣. Override  
  3️⃣. Stateless  
  4️⃣. Immutability  

2. 1급 객체의 특징이 아닌 것을 고르시오.  
  1️⃣. 변수나 데이터 구조 안에 담을 수 있다.  
  2️⃣. 반환값으로 사용할 수 있다.  
  3️⃣. 동적으로 프로퍼티 할당이 불가능하다.  
  4️⃣. 파라미터로 전달할 수 있다.  

3. 다음함수가 순수함수인지 아닌지 판별하고, 순수함수가 아니라면 그 이유를 쓰시오.  
```swift
let num = 1;
function add(a) {
	return a + num;
}
```

4. 다음 함수가 비상태, 불변성을 만족하는지 판별하고, 아니라면 그 이유를 쓰고 함수를 수정하시오.
```swift
let person = { name: "jongmin", age: "26" };

function increaseAge(person) {
    person.age = person.age + 1;
    return person;
}
```
