1. 관계형 데이터베이스(RDBMS)와 비관계형 데이터베이스(NoSQL)의 장단점 비교

- NOSQL 장점: 쿼리 프로세싱이 단순화되어 대용량 데이터 처리 성능이 향상됨
        단점 : 데이터 중복에 의해 데이터 일관성이 저하되고 용량이 증가함
- RDBMS 장점 : 데이터 중복 배제로 데이터 이상 발생 및 용량 증가를 최소화함
        단점 : 조인이 복잡한 경우 쿼리 프로세싱도 복잡해져 성능이 저하됨
 
2. 트랜잭션(transaction)이란 무엇인가요?

-트랜잭션은 DB의 상태를 변화시키기 위해 수행하는 일련의 작업 단위입니다. 트랜잭션은 데이터의 유효성을 보장하기 위해, ACID라는 속성을 가지고 있습니다.
원자성 : 각 트랜잭션의 단일 단위 처리를 보장합니다.
일관성 : 모든 트랜잭션이 일관성있는 DB 상태를 유지하도록 합니다. DB의 무결성 제약 조건을 만족해야 합니다. (FK-PK 간의 관계 보장)
격리성 : 동시에 실행되는 트랜잭션들이 서로에게 영향을 미치지 않아야 합니다. 동시성을 제어합니다. 격리 수준은 4가지가 있는데, 커밋되지 않은 읽기, 커밋된 읽기, 반복 가능한 읽기, 직렬화 가능이 있습니다.
내구성 : 트랜잭션을 성공적으로 끝내면 결과가 항상 기록돼야 합니다. 시스템 문제가 발생하더라도, DB 로그를 사용해서 성공한 트랜잭션 내용을 복구합니다.

3. MySQL에서 조인(join)의 역할은 무엇인가요? 다양한 join의 방식에 대해 설명해주세요.

 두 개의 테이블을 엮어서 원하는 데이터를 추출하기 위해 사용.
INNER JOIN(내부 조인)은 두 테이블을 조인할 때, 두 테이블에 모두 지정한 열의 데이터가 있어야 한다.
OUTER JOIN(외부 조인)은 두 테이블을 조인할 때, 1개의 테이블에만 데이터가 있어도 결과가 나온다.
CROSS JOIN(상호 조인)은 한쪽 테이블의 모든 행과 다른 쪽 테이블의 모든 행을 조인하는 기능이다.
SELF JOIN(자체 조인)은 자신이 자신과 조인한다는 의미로, 1개의 테이블을 사용한다.

4. MySQL에서 인덱스(index)란 무엇인가요?

-추가적인 쓰기 작업과 저장 공간을 활용하여 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조 
특정 컬럼에 인덱스를 생성하면, 해당 컬럼의 데이터들을 정렬하여 별도의 메모리 공간에 데이터의 물리적 주소와 함께 저장된다.
