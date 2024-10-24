# Cache란?

- 자주 사용하는 데이터나 값을 미리 복사해 놓는 임시 장소
- 캐싱된 데이터는 로직을 거치지 않고 반환되기 때문에 서버 성능에 이점을 가짐

## 정리

### 캐싱 X

- Client ↔ Controller ↔ Service ↔ Repository
- 캐싱되어있지 않은 데이터는 저장소까지 조회하는 로직을 수행한다.

### 캐싱 O

- Client ↔ Controller ↔ Service / Repository
- 캐싱된 데이터는 저장소를 조회하는 로직을 수행하지 않고, 저장된 데이터를 반환한다.

## 사용하면 좋은 케이스

- 반환되는 데이터가 동일할 때
- 자주 호출되는 데이터일 때
- 서버 리소스를 많이 사용하는 로직을 수행할 때

### 예시

- 공지사항
- 랭킹

## 사용하면 안되는 케이스

- 실시간으로 정확성이 보장되어야 하는 때
- 빈번하게 데이터가 변경될 때

### 예시

- 통계성 데이터