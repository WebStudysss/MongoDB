### 1. mongosh 환경에서 단일 문서를 추가할 때 사용하는 명령은?

A. db.books.addOne()

B. db.books.insertOne()

C. db.books.save()

D. db.books.insertMany()

---

### 2. 아래 CRUD 결과에서 `matchedCount: 1, modifiedCount: 1` 이 의미하는 것은?

```json
{
  acknowledged: true,
  matchedCount: 1,
  modifiedCount: 1
}

```

A. 문서를 찾지 못했고 수정 실패

B. 문서를 찾았으나 수정하지 않음

C. 문서를 1개 찾았고 수정 완료

D. 오류 발생

---

### 3. mongosh에서 JavaScript 코드를 사용할 수 있는 이유는?

A. Java 언어 기반이기 때문

B. JSON만 사용 가능한 CLI이기 때문

C. JavaScript REPL 환경을 제공하기 때문

D. Bash 기반 쉘이기 때문

---

### 4. 대량 데이터 삽입 시 성능을 높이기 위해 사용해야 하는 방법은?

A. 1000번 insertOne 실행

B. initializeUnorderedBulkOp() 또는 bulkWrite() 활용

C. createIndex() 사용

D. updateMany() 반복 실행

---

### 5. 정규 표현식 검색에서 대소문자를 구분하지 않기 위한 옵션은?

A. /g

B. /m

C. /i

D. /s

---

### 6. MongoDB에서 "mongo", "Mongo", "MONGO"로 시작하는 name 필드를 검색하려면?

A. db.books.find({name: /^mongo$/})

B. db.books.find({name: { $regex: /^mongo.*/i }})

C. db.books.find({name: LIKE 'mongo%'})

D. db.books.find({name: IS 'mongo'})

---

### 7. 아래 설명에 해당하는 MongoDB 기능은?

> 현재 mongod 인스턴스에서 실행 중인 쿼리, 복제, 백업, 집계 등의 상태 정보를 문서 형태로 조회
> 

A. collMod()

B. shutdown()

C. currentOp()

D. killOp()

---

### 8. MongoDB에서 컬렉션 이름 변경에 사용하는 명령은?

A. renameCollection

B. alterName

C. changeTable

D. modifyName

---

### 9. Stable API의 주요 목적은?

A. 특정 버전의 API 반환 결과를 명확히 보장하기 위해

B. 서버 자동 재시작

C. JSON 데이터를 XML로 자동 변환

D. 캐시된 쿼리만 실행

---

### 10. MongoDB의 ODM(Object Document Mapper)의 주요 역할은?

A. SQL 쿼리를 자동 변환

B. 자바스크립트만 지원

C. 객체 형태로 문서를 쉽게 다루도록 도와줌

D. 오직 index 생성만 지원

---

---

## 🎯 정답 & 핵심 설명

| 번호 | 정답 | 설명 |
| --- | --- | --- |
| 1 | B | insertOne()은 단일 문서 삽입 |
| 2 | C | 문서를 찾았고 수정도 정상적으로 수행됨 |
| 3 | C | mongosh는 JavaScript 실행 가능한 REPL 환경 |
| 4 | B | bulk 연산은 대량 데이터 처리에 최적 |
| 5 | C | `/i`는 대소문자 구분 없이 검색 |
| 6 | B | $regex와 /^mongo.*/i 를 사용한 패턴 검색 |
| 7 | C | currentOp()는 현재 실행 중인 작업 조회 |
| 8 | A | 컬렉션 이름 변경은 renameCollection 사용 |
| 9 | A | Stable API는 반환값을 버전별로 명확히 보장 |
| 10 | C | ODM은 객체 형태로 문서를 다루는 매핑 도구 |
