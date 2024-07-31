# 종합 악세서리 웹 쇼핑몰 %365

#### 배포 URL : http://34.64.236.17/

#### [테스트 계정]
|role| id | pw |
|------| ------ | ------ |
|관리자| eliceadmin1 | eliceadmin1 |
|사용자| eliceuser1 | eliceuser1 |
<br>
<br>


# 프로젝트 소개
##### - %365는 365일 착용하고 싶은 악세서리를 판매하는 웹 쇼핑몰입니다.
##### - 자유로운 Q&A와 wishList를 통한 개인의 취향에 맞는 상품을 고를 수 있습니다.
<br>
<br>


# 팀 소개 및 역할 분담
##### - 임호준(팀장) : 프로젝트 진행 및 웹 구조 설계, ui
##### - 공예지(팀원) : 상품, 장바구니 도메인 및 서버
##### - 신종신(팀원) : 주문 도메인 및 데이터 크롤링
##### - 장윤정(팀원) : 카테고리 및 q&a 도메인
##### - 노주현(팀원) : 회원 및 WishList 도메인 
<br>
<br>


# 기술 스택

|  |  |
| ------ | :------: |
| FE | Java \| Spring Boot \| Spring MVC \| Spring Security \| JPA \| MySQL |
| BE | HTML \| CSS \| Javascript \| react|
| etc | git \| gitlab \| notion |
<br>
<br>


# 프로젝트 의존성
```
FE
├── @emotion/react@11.11.4
├── @emotion/styled@11.11.5
├── @mui/icons-material@5.15.19
├── @mui/material@5.15.19
├── @testing-library/jest-dom@5.17.0
├── @testing-library/react@13.4.0
├── @testing-library/user-event@13.5.0
├── axios@1.7.2
├── react-dom@18.3.1
├── react-intersection-observer@9.10.3
├── react-router-dom@6.23.1
├── react-scripts@5.0.1
├── react-slick@0.30.2
├── react@18.3.1
├── slick-carousel@1.8.1
└── web-vitals@2.1.4
```



 ```
BE
├── implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
├── implementation 'org.springframework.boot:spring-boot-starter-web'
├── implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.5.0'
├── implementation 'org.springframework.boot:spring-boot-starter-security'
├── implementation 'org.springframework.boot:spring-boot-starter-validation'
├── implementation 'org.mapstruct:mapstruct:1.5.5.Final'
├── implementation 'mysql:mysql-connector-java:8.0.33'
|
├── compileOnly 'org.projectlombok:lombok'
├── annotationProcessor 'org.projectlombok:lombok'
├── annotationProcessor 'org.mapstruct:mapstruct-processor:1.5.5.Final'
├── testImplementation 'org.springframework.boot:spring-boot-starter-test'
├── testImplementation 'org.springframework.security:spring-security-test'
├── testRuntimeOnly 'org.junit.platform:junit-platform-launcher'
|
├── implementation 'io.jsonwebtoken:jjwt-api:0.12.3'
├── implementation 'io.jsonwebtoken:jjwt-impl:0.12.3'
└── implementation 'io.jsonwebtoken:jjwt-jackson:0.12.3'
```


<br>
<br>


# 개발 기간 및 프로젝트 진행
	
#### 개발 기간 : 2024-5-27(월) ~ 2024-6-21(금)
<br>

#### 프로젝트 진행


##### - gitlab MR을 통해 수정 및 진행 상황을 확인하였습니다.
##### - 디스코드나 원격 강의실을 이용한 스크럼을 진행하였습니다.
<br>
<br>

# ERD 및  와이어프레임
#### 링크 : https://www.notion.so/elice-track/ERD-8f8fdff109b746ad8d5750498ee1229c

<br>
<br>

# 주요 서비스 기능
[초기 화면 (home)]<br>
new / best 제품을 슬라이드를 통해 확인할 수 있습니다.<br>
![Untitled design_1](https://github.com/user-attachments/assets/5e06854c-9135-4590-bd3d-00893c25cfb4)

[로그인 / 회원가입] <br>
로그인 | 아이디와 비밀번호를 통해 로그인합니다. 등록된 사용자 정보와 일치하지 않으면 로그인에 실패했다는 알림이 표시됩니다.<br>
회원가입 | 정보를 입력하면 입력창에서 바로 유효성 검사가 진행되고 통과하지 못한 경우 각 경고 문구가 입력창 하단에 표시됩니다.
- 기본 조건: 공백 불가
- 아이디: 중복 불가
- 비밀번호: 8-15자리 숫자+문자 조합
- 이메일: 선택사항, 이메일 형식 준수
<br>
![Untitled design_2](https://github.com/user-attachments/assets/9ddc9768-44fa-4dba-872b-cf9903a7499d)

[상품 조회] <br>
카테고리별 조회, 상품 분류별(인기 상품/신규 상품/품절 상품) 조회가 가능합니다.<br>
![Untitled design_5](https://github.com/user-attachments/assets/87ac6a36-c7b3-452f-8be8-d6c2d2dc781a)

[상품 상세] <br>
상품에 대한 정보를 확인하고 사이즈, 수량을 선택하여 장바구니에 담거나 바로 주문, 위시리스트에 저장할 수 있습니다.<br>
상품에 대한 Q&A 목록에 질문을 달고 관리자의 답변을 확인할 수 있습니다.<br>
![Untitled design_3](https://github.com/user-attachments/assets/8d1dd814-8a12-45f4-86dd-080805a5f3b8)
![Untitled design_4](https://github.com/user-attachments/assets/bdb0a72d-bce3-44ad-ac4d-75df6104d461)

[장바구니] <br>
상품을 장바구니에 추가하면 장바구니 페이지에서 추가된 상품을 선택/삭제하고 수량을 조절하여 주문할 수 있습니다.<br>
수량은 현재 남아있는 재고 수량까지만 추가가 가능합니다.<br>
![Untitled design_19](https://github.com/user-attachments/assets/ec443800-a82e-4cdd-9622-2c13516b84f3)

[주문] <br>
상품 페이지에서 바로 주문하는 경우, 주문 정보를 확인하고 주문을 진행합니다. <br>
프로필의 주문 목록에서 주문 정보를 확인하고 배송 주소를 변경할 수 있으며, 배송 전 상태인 경우 주문 취소가 가능합니다.<br>
![member 주문 정보 프로필_1](https://github.com/user-attachments/assets/8b61b06f-adb3-4fb3-886a-a59d698b6540)

[위시리스트] <br>
좋아요 누른 상품의 목록을 프로필의 위시리스트 페이지에서 확인할 수 있습니다. <br>
![Untitled design_23](https://github.com/user-attachments/assets/519d3765-c8f5-40ba-be51-dac9f63f9250)

[Q&A] <br>
상품별 질문과 일반 질문은 상품 상세 페이지와 Q&A 페이지에서 조회, 등록, 수정, 삭제가 가능합니다.<br>
Q&A 페이지에서는 모든 질문을 확인할 수 있으며, 관련 상품 이미지를 통해 구분할 수 있습니다.<br>
질문 등록 시 비밀글 또는 공개글로 설정할 수 있고, 비밀번호를 설정하여 조회, 수정, 삭제가 가능하며, 관리자만 질문에 답변할 수 있습니다.<br>
![Untitled design_8](https://github.com/user-attachments/assets/0220914f-6cb0-42e8-9ef7-e101af9549ae)
![Untitled design_25](https://github.com/user-attachments/assets/70f339f6-5b43-4ca7-a151-3f1d61b4cbc2)
<br><br>
[관리자] <br>
관리자 로그인을 통해 관리자 페이지에 접속하여 사이트를 관리할 수 있습니다.<br>
##### 상품 관리
등록된 상품 목록을 확인하고, 상품을 등록, 수정, 삭제할 수 있으며, 키워드 검색 기능을 제공합니다.<br>
![Untitled design_11](https://github.com/user-attachments/assets/f6e64683-cc89-40ad-9119-29efb29be29e)
![Untitled design_12](https://github.com/user-attachments/assets/68ddb0c2-2bfd-4e5a-a7c5-15737805909d)
##### 카테고리 관리
주 카테고리와 하위 카테고리를 모두 관리할 수 있습니다.<br>
키워드 검색 기능을 제공하며, 하위 카테고리 관리에서는 상위 카테고리 선택을 통한 검색이 가능합니다.<br>
![Untitled design_13](https://github.com/user-attachments/assets/c8afb66c-0941-4dbc-97db-8aad40719921)
![Untitled design_14](https://github.com/user-attachments/assets/e155984a-d1d8-41cd-8ab4-0cce20c0a705)
##### 주문 관리
전체 주문 목록과 주문 상세를 확인하고, 각 주문의 배송 상태를 변경할 수 있습니다.<br>
배송 상태 | 배송 전, 배송 중, 배송 완료, 주문 취소, 환불 완료<br>
![Untitled design_22](https://github.com/user-attachments/assets/25fcc20a-2d82-4061-aca2-f13ae97fca10)
##### 회원 관리
전체 회원을 관리하고, 회원의 권한을 지정할 수 있습니다. 권한은 관리자와 일반 회원으로 이루어져 있습니다.<br>
![Untitled design_16](https://github.com/user-attachments/assets/f7169ec0-19d7-40f5-b3a3-e10ccb28242e)
![Untitled design_17](https://github.com/user-attachments/assets/1652dbb4-2819-410f-8d77-138e26748114)
##### Q&A 관리
일반 사용자가 이용하는 사이트에서 관리자 계정은 질문글의 공개 여부와 관계없이 조회가 가능합니다.<br>
관리자에게만 답변을 작성 및 삭제할 수 있는 권한이 있습니다.<br>
![Untitled design_7](https://github.com/user-attachments/assets/a9977eec-aa6a-4f2a-bd10-ba8980cfb0d7)

<br>
<br>


# 트러블 슈팅
- 문제점 : 각 페이지별 접근 권한 설정 시 문제 발생 ➔ 백엔드에서 처리 후 프론트에서도 재처리 필요 <br>
 해결 : 역할별로 접근을 허용하는 컴포넌트를 사용하여 페이지를 감쌈 <br>
  - 관리자 페이지: AdminRoute , 회원 페이지: ProtectedRoute 
- 문제점 : 카테고리 계층화에 따른 순환 참조 문제 발생 ➔ parent와 childrens 필드를 사용하여 카테고리 내에서 다대다 관계 설정을 통해 카테고리를 계층적으로 구현하였지만, 자식 카테고리의 parent에 다시 부모 카테고리가 지정되면서 조회 시에 무한 루프 발생 <br>
 해결 : parent 필드를 제외한 responsedto를 설정하여 조회 시에 DTO 반환 

<br>
<br>


# 필요 개선사항
##### - 로거 설정 : 배포 시 디버깅이 어려움. 따라서 요청 및 응답 로깅을 통해 문제 발생 시 원인 파악을 쉽게 할 수 있고 유지보수 또한 용이해짐
##### - 글로벌 예외 처리 : 코드 가독성을 높이고 예외 발생 시 일관된 오류 응답을 제공하여 코드가 깔끔해짐. 
##### - 환경에 따른 설정 파일 분리 (yml 파일) : 개발, 테스트, 배포 등 각 환경에 따라 설정 파일을 분리하여 관리함으로써 설정 변경이 용이해짐
<br>
<br>


# 프로젝트 후기
##### 임호준 : 
##### 이번 프로젝트에서 팀장으로서 프로젝트를 이끌게 되어 많은 것을 배웠습니다. React를 처음 사용해보았지만, 웹 페이지의 구조를 설계하고 UI를 배치하며 수정하는 과정에서 많은 성장을 느낄 수 있었습니다. 프론트엔드 파트를 주로 담당했기 때문에 API 개발에는 많은 참여를 하지 못한 점이 조금 아쉬웠습니다. 하지만 프론트엔드도 웹 개발자가 된다면 꼭 알아야 하는 중요한 부분이라고 생각하여 이번 기회에 좋은 경험을 했다고 느낍니다.
<br>


##### 공예지 : 
##### 이번 프로젝트에서 장바구니/상품 영역 일부를 맡아서 담당했습니다. 프론트와 백엔드를 모두 경험하게 되어 뜻깊었습니다. 다인원과 함께 프로젝트를 진행한 것은 처음이라 git 사용에 있어서 어려움이 있기도 했지만, conflict 등을 해결하면서 git 사용법을 좀 더 익힐 수 있었습니다. 프로젝트 마무리 시점에 배포 작업도 도왔는데, 프론트 배포는 처음 해봤기 때문에 새로운 경험이었습니다. 이번 프로젝트를 통해 많은 점을 배울 수 있었습니다.
<br>


##### 장윤정 : 
##### 이번 프로젝트에서 카테고리/q&a를 담당했습니다. 회원과 권한 등을 적용하는 프로젝트는 처음이었기에 신경써야 할 것이 많았고 많이 배울 수 있었습니다. 프론트엔드 파트도 배워보고 싶었는데, 이번 기회에 조금이나마 경험해 볼 수 있었던 것 같아 뜻깊었습니다. 팀원들과 소통하며 git을 효과적으로 활용하는 법도 배울 수 있었던 소중한 경험이었다고 생각합니다.
<br>


##### 노주현 : 
##### 이번 프로젝트에서 회원 및 좋아요 기능을 맡았습니다. 프론트와 백엔드를 같이 사용해보는 것은 처음이었는데, 덕분에 로직의 흐름을 확실하게 이해할 수 있는 시간이었습니다. 그리고 여러 사람과 파트를 나눠 협업을 하여 더 큰 책임감을 느끼게 되었습니다. 이번 프로젝트 경험을 통해 3차 프로젝트에서는 한층 더 발전한 모습으로 참여할 수 있을 것 같습니다.
<br>


##### 신종신 : 
##### 이번 프로젝트에서 주문 기능을 담당했습니다. 커뮤니케이션을 통해 서로가 협업하는 과정을 경험할 수 있어 좋았습니다. 또한 프론트 로직을 만져보면서 유연하게 Dto를 넘기는 것도 배울 수 있었습니다. 

<br>
<br>

