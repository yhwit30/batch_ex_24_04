## 개발환경
java 17 <br>
Spring Batch <br>
intelliJ

<br>

## Spring Batch를 이용한 쇼핑몰 사이트 프로젝트

- 스프링 배치는 대량데이터를 처리하기 위한 프레임워크이다.

Spring Batch에서의 Job은 여러가지 Step의 모음으로 구성되어 있으며 Job은 순차적인 Step을 수행하며 Batch를 수행한다.
<br>
Step은 Tasklet 처리 방식과 Chunk 지향 처리 방식을 지원한다.

[Job -> Step -> Tasklet]

![image](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/a5e3637b-a33d-4b02-a72a-d8f617884997)

<br>

- 개념 예시
```
Jop : 빨래
- Step : 설정
  - Tasklet : A사 세제를 넣는다
  - Tasklet : A사 섬유유연제를 넣는다
  - Tasklet : 세탁, 헹굼, 탈수 시간을 정한다
- Step : 세탁
  - Tasklet : 일정시간동안 세탁을 진행한다
- Step : 헹굼
  - Tasklet : 일정시간동안 헹굼을 진행한다
- Step : 탈수
  - Takslet : 일정시간동안 탈수를 진행한다
```


<br>

- 코드 예시

![제목 없음](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/6ff442af-058e-46df-adbb-cad7768cf977)



<br><br>
## 카테고리
[base(테스트데이터 생성) / cart(장바구니) / cash(결제) / member(회원) / order(주문) / product(상품)]

<br><br>
## 메모
- 스프링부트가 제공하는 프레임워크(feat.JPA(Java Persistence API))로 아래와 같이 레포지터리가 간단해진다. 쿼리를 따로 작성하지 않아도 된다.

<div>* 기본제공되는 레포지터리</div>
<br>

![image](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/bb223921-6ee9-459a-a062-663b8ef3fc2b)

<div>* 커스텀한 레포지터리</div>
<br>

![image](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/be110a84-bfef-4d84-b555-6e63d90d248a)



<br><br>
## 데이터베이스 예시

- 결제를 했으면 is paid가 1로 바뀜

![image](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/e8f8a521-0e93-4a7a-8a4f-ec78586ad55b)


- 2번 주문정보 생성, 2번 주문에 대한 환불

![image](https://github.com/yhwit30/batch_ex_24_04/assets/153142837/69a2e060-4ea3-4368-b031-8ede112f8a2e)



