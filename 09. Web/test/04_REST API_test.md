1. REST란  (________________)(Uniform Resource Identifier)를 통해 (___________)을 명시하고,(_______________)(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.



2. 다음 REST API의 특징 중 필수 조건이 아닌것을 고르시오

1. Server-Client
   2. Stateless
   3. Cacheable
   4. Layered System
   5. Code-On-Demand
   6. Uniform Interface


3. 다음 중 설명이 틀린것을 고르시오

3-1 Cacheable(캐시 처리 가능)의 원칙을 지키면 캐싱이 가능한 데이터라면 서버 차원에서 캐시에 저장해두고 이후에 같은 요청에 대해선 해당 데이터를 꺼내올 수 있게 된다. (O,X)

3-2 Stateless(무상태)란, 서비스의 클라이언트가 동작하는 과정에서 생기는 상태 변화에 대해 서버도 관여하기 때문에 요청은 반드시 서버가 해당 요청을 처리하기 위해 필요로 하는 모든 정보를 함께 전송해야 한다는 것을 의미한다. (O,X)
3-3 URI로 지정한 Resource에 대한 조작을 통일되고 한정적인 인터페이스로 수행한다. HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다.  (O,X)
3-4 Layered System(계층화)에 따르면 서버도 응답을 주기 전 다른 서버와 통신할 수도 있지만 클라이언트 입장에선 철저하게 분리되어 있기 때문에 직접적으로 바로 연결된 쪽(REST Server)과의 연결만 신경 써주면 된다.  (O,X)


4. 다음 중 REST API 디자인 가이드에 따라 api를 작성한 올바른 예시인 것을 모두 고르시오.
   1. GET/Membering/1
   2. GET/member/show/1
   3. GET/members/1
   4. POST/members/2
   5. DELETE/student/12
![image](https://user-images.githubusercontent.com/53734935/170706568-c8cd11d2-d35b-4796-89a2-3aee4c77ba59.png)
