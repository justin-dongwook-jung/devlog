# Mocking

- 테스트하고자 하는 코드가 의존하는 function 이나 class 에 대해 모조품을 만들어 테스트하는 것.
단위 테스트를 작성할 때, 해당 코드가 의존하는 부분을 가짜(MOCK)로 대체하는 기법.

# TDD / BDD
### TDD(Test Driven Development)
- 테스트 주도 개발, 구현 코드를 작성하기 전에 테스트 케이스부터 작성

### BDD(Behavior Driven Development)
- 행위 주도 개발. TDD에 기반을 두고 있으며 한발 더 나아가 테이스케이스 자체가 요구사양이 되도록 하는 개발 방식
- 함수 단위의 테스트를 권장하지 않고 시나리오 기반의 테스트 케이스를 작성.

### TDD와 BDD의 차이
- TDD는 개발코드의 완성이 목적이고 BDD는 개발 결과의 검증이 목적이다. 
- TDD는 코드 저체에 집중한 테스트 코드를 작성하고 BDD는 시나리오를 패턴화해서 여러 구성원들이 테스트 코드를 검증할 수 있도록 해서 더욱 비지니스 요구 사항을 빠르게 반영할 수 있게 된다.

### Test 종류
- 단위 테스트(Unit Test)
- 통합 테스트(Integration Test)
- E2E 테스트(End to End Test)
- 회귀 테스트(Regression Test)
- 성능 테스트(Performance Test)

# Chai

### Unit Test
- Sinon.js 를 이용하여 Mocking 한다. (Mocking DB, Mocking Socket Server 사용)
- AAA 패턴
  - AAA 패턴이랑 준비(arrange), 실행(act), 검증(assert) 세 단계로 test를 작성하는 패턴이다.
  - Arrange 단계에서는 테스트에 필요한 변수나 객체를 생성
  - Act 단계에서는 테스트를 실행
  - Assert 단계에서는 실행한 코드가 설계한대로 정확하게 동작했는지 검증


### E2E Test
- chai-http 를 이용하여 식제 http request 날려보는 방법 (실제 DB, 실제 Socket Server 사용)

# Sinon.js (stubbing / mocking library)

### spy
- 함수 호출에 대한 정보를 얻는 사용됨. 테스트의 목적이 어떤일이 발생했는지를 확인할 때 적합하며 함수의 동작에는 여향을 미치지 않는다.

### stub
- spy와 동일한 assertion을 사용할 수 있음. 한 가지 다른 점은 타켓함수나 콜백을 바꿔치기하여 함수의 동작 방식을 변경할 수 있다는 점이다.