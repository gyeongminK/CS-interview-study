## HTTP status code

> 클라우드 환경에서 HTTP API를 통해 통신하는 것이 대부분임
>
> 이때, 응답 상태 코드를 통해 성공/실패 여부를 확인할 수 있으므로 API 문서를 작성할 때 꼭 알아야 할 것이 HTTP status code다

<br>

1xx, 2xx, 3xx, 4xx, 5xx로 나누어 볼수 있다. 즉, 3자리 숫자의 첫번째 값(코드)만 보고도 어떤 종류의 응답인지 알 수 있는데, 이 첫번째 값을 ***Response Class***라고 한다.

<br>

| Response Class Code | Response Class 의미 | 설명 |
|:---:|:---:|:---:|
| 1 | Informational (정보) | 리퀘스트를 받고, 처리 중에 있음. |
| 2 | Success (성공)| 리퀘스트를 정상적으로 처리함.|
| 3 | Redirection (리디렉션) | 리퀘스트 완료를 위해 추가 동작이 필요함.|
| 4 | Client Error (클라이언트 오류) | 클라이언트 요청을 처리할 수 없어 오류 발생 |
| 5 | Server Error (서버 오류) | 서버에서 처리를 하지 못하여 오류 발생 |

> 4xx 에러는 클라이언트의 잘못된 요청으로 서버에서 처리하지 못한 것이고, 5xx 에러는 클라이언트의 요청은 문제가 없으나, 서버에서 처리중에 서버 문제로 인해 오류가 발생한 것이라는 차이가 있다.

<br><img src="https://evan-moon.github.io/static/581d5098769863da7581ecc2a09a19ed/d7ab4/browser-response.png"/><br>

<br>

##### 100번대 : 조건부 응답

| 상태코드 |    이름     |           의미           |
| :------: | :---------: | :----------------------: |
|100(계속)| Continue | 요청자는 요청을 계속해야 한다. 서버는 이 코드를 제공하여 요청의 첫 번째 부분을 받았으며 나머지를 기다리고 있음을 나타낸다. |

##### 200번대 : 통신 성공

| 상태코드 |    이름     |           의미           |
| :------: | :---------: | :----------------------: |
|   200    |     OK      |      요청 성공(GET)      |
|   201    |   Create    |     생성 성공(POST, PUT)      |
|   202    |  Accepted   | 요청 접수O, 리소스 처리X |
|   204    | No Contents |  요청 성공O, 내용 없음   |

<br>

##### 300번대 : 리다이렉트
| 상태코드 |       이름       |             의미              |
| :------: | :--------------: | :---------------------------: |
|   300    | Multiple Choice  | 요청 URI에 여러 리소스가 존재 |
|   301    | Move Permanently |  요청 URI가 새 위치로 옮겨감  |
|   304    |   Not Modified   |    요청 URI의 내용이 변경X    |

<br>

##### 400번대 : 클라이언트 오류

| 상태코드 |        이름        |               의미                |
| :------: | :----------------: | :-------------------------------: |
|   400    |    Bad Request     | API에서 정의되지 않은 요청 들어옴 |
|   401    |    Unauthorized    |             인증 오류             |
|   403    |     Forbidden      |        권한 밖의 접근 시도        |
|   404    |     Not Found      |   요청 URI에 대한 리소스 존재X    |
|   405    | Method Not Allowed | API에서 정의되지 않은 메소드 호출 |
|   406    |   Not Acceptable   |             처리 불가             |
|   408    |  Request Timeout   |        요청 대기 시간 초과        |
|   409    |      Conflict      |               모순                |
|   429    |  Too Many Request  |        요청 횟수 상한 초과        |

<br>

##### 500번대 : 서버 오류

| 상태코드 |         이름          |         의미         |
| :------: | :-------------------: | :------------------: |
|   500    | Internal Server Error |    서버 내부 오류    |
|   502    |      Bad Gateway      |   게이트웨이 오류    |
|   503    |  Service Unavailable  |   서비스 이용 불가   |
|   504    |    Gateway Timeout    | 게이트웨이 시간 초과 |

<br>

참고 링크 : https://ko.wikipedia.org/wiki/HTTP_%EC%83%81%ED%83%9C_%EC%BD%94%EB%93%9C
