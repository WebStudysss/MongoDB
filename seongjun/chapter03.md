### 1) 챕터 3에서 다루는 **개발 도구 카테고리**로 가장 거리가 먼 것은?

A. mongosh(쉘)

B. MongoDB CLI(mongocli)

C. MongoDB Compass

D. WiredTiger 스토리지 엔진 튜너

**정답:** D

**해설:** 챕터 3는 mongosh, mongocli, Compass, VS Code 확장, Terraform/Atlas 등 **개발 도구 중심**이다. 스토리지 엔진 튜닝은 개발 도구 범위 밖이다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 2) **mongosh**에 대한 설명으로 옳은 것은?

A. 레거시 `mongo` 쉘과 동격이며 더 이상 업데이트되지 않는다.

B. JavaScript 런타임 기반이며 풍부한 탭완성·히스토리 등 **개발 편의 기능**을 제공한다.

C. 바이너리 쿼리를 위해 CLI 플래그 없이만 동작한다.

D. Atlas 전용이라 로컬 커넥션은 안 된다.

**정답:** B

**해설:** **mongosh**는 현대화된 쉘로, 레거시 `mongo` 대비 개발자 경험이 강화되었다(완성·프롬프트 개선 등). 로컬/Atlas 모두 연결 가능. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 3) **mongosh vs 레거시 쉘** 비교에서 챕터 3의 핵심 포인트는?

A. 레거시 쉘만 스크립팅 가능

B. mongosh가 향상된 에러 메시지·자동완성 등 **DX(개발자 경험)**을 제공

C. 레거시 쉘만 최신 서버 버전을 지원

D. 둘 다 더 이상 사용 불가

**정답:** B

**해설:** mongosh는 레거시 쉘 대비 개발 생산성을 높이는 **현대적 인터페이스**를 제공한다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 4) **mongocli(MongoDB CLI)**의 주된 용도는?

A. 컬렉션 내 문서 편집 GUI

B. Atlas 프로젝트/클러스터, 사용자, 네트워킹 등을 **명령줄에서 프로비저닝·관리**

C. VS Code에서 스키마 시각화

D. 쿼리 플랜 트리 뷰어

**정답:** B

**해설:** mongocli는 Atlas 및 관련 리소스를 **CLI로 자동화/관리**할 때 사용한다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 5) **MongoDB Compass**의 강점으로 가장 적절한 것은?

A. 서버 사이드 Java 스크립팅 실행

B. **GUI로 데이터 탐색·쿼리·인덱스/스키마 인사이트**를 제공

C. 쿠버네티스 오퍼레이터 배포

D. 저널 크기 동적 조절

**정답:** B

**해설:** Compass는 **시각적 데이터 탐색/분석**에 특화된 GUI 도구다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 6) **MongoDB for VS Code 확장**의 대표적 사용 시나리오는?

A. 서버 로그를 운영 노드에서 직접 삭제

B. VS Code 내 **Playground**에서 쿼리를 작성·실행하고 결과를 확인

C. Config Server를 재기동

D. WiredTiger 캐시 설정 변경

**정답:** B

**해설:** VS Code 확장은 **Playground**를 통해 에디터에서 바로 쿼리/파이프라인을 실험하도록 돕는다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 7) 챕터 3의 **베스트 프랙티스** 관점에서 mongosh/CLI 공통 팁으로 가장 타당한 것은?

A. 프로덕션 자격증명을 스크립트에 하드코딩

B. 출력 파싱을 위해 가능하면 **일관된 포맷(JSON 등)**을 사용

C. 인증은 로컬 테스트에 불필요

D. 실패 시 재시도 로직은 CLI에서 불가능

**정답:** B

**해설:** 자동화·스크립팅 시 **기계가 읽기 쉬운 포맷**을 쓰면 파이프라인/CI와 연계가 수월하다(자격증명 하드코딩은 지양). [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 8) 챕터 3에서 소개되는 **Terraform + Atlas** 흐름을 고르면?

A. Terraform으로 로컬 mongod를 데몬화

B. **Terraform Provider로 Atlas 프로젝트/클러스터/네트워킹을 선언적으로 코드 관리(IaC)**

C. Terraform이 Compass 쿼리를 자동 생성

D. Terraform이 VS Code 확장을 설치

**정답:** B

**해설:** Terraform Provider를 통해 Atlas 리소스를 **선언적 IaC**로 관리할 수 있다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 9) **도구 선택 기준**으로 챕터 3 취지에 가장 부합하는 것은?

A. 모든 작업은 GUI만 사용

B. 모든 작업은 CLI만 사용

C. **탐색/분석은 Compass, 스크립팅·자동화는 mongosh/CLI, 에디팅·샘플링은 VS Code 확장**처럼 **목적별 조합**

D. Atlas 환경에서는 도구가 불필요

**정답:** C

**해설:** 챕터 3는 도구들의 **역할과 장단점을 구분**해 상황에 맞춘 조합 사용을 권장한다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

### 10) **연결(Connecting) 실무 팁**으로 가장 적절한 것은?

A. SRV 레코드는 개발에서만 사용, 운영에서는 금지

B. **환경변수/프로필로 커넥션 문자열을 분리**하고, 최소 권한 사용자로 접속

C. 모든 워크로드에 관리자 계정 재사용

D. `tls=false`가 기본이므로 운영도 동일 유지

**정답:** B

**해설:** 커넥션 정보는 **분리·보호**하고, **최소 권한 원칙**으로 연결하는 것이 기본 보안 수칙이다. 챕터 3의 연결/설정·베스트 프랙티스 맥락과 일치한다. [oreilly.com](https://www.oreilly.com/library/view/mastering-mongodb-7-0/9781835460474/?utm_source=chatgpt.com)

---

## 추가문제

### 1️⃣ `mongosh`의 주요 목적은 무엇인가?

A. MongoDB 서버를 실행하기 위한 데몬

B. 데이터베이스를 시각적으로 관리하는 GUI

C. MongoDB와 상호작용하기 위한 쉘 환경

D. 백업 및 복원 도구

**정답:** C

**해설:** `mongosh`(MongoDB Shell)는 CLI(Command Line Interface)로, 쿼리 실행·컬렉션 조작·스키마 확인 등 개발자가 직접 DB와 상호작용할 수 있는 도구이다.

---

### 2️⃣ 다음 중 `mongosh`에서 현재 데이터베이스를 확인하는 명령어는?

A. `show collections`

B. `db.current()`

C. `db`

D. `use show dbs`

**정답:** C

**해설:** `db` 명령어를 입력하면 현재 선택된 데이터베이스 이름이 출력된다.

---

### 3️⃣ `use mydb` 명령의 역할은?

A. `mydb` 데이터베이스를 삭제한다.

B. `mydb` 데이터베이스로 전환하거나 존재하지 않으면 생성한다.

C. `mydb` 컬렉션을 선택한다.

D. `mydb` 사용자를 추가한다.

**정답:** B

**해설:** `use` 명령은 해당 DB로 전환하며, 없을 경우 실제 데이터가 추가될 때 자동 생성된다.

---

### 4️⃣ MongoDB Compass의 가장 큰 특징은?

A. 서버 로그를 조회할 수 있다.

B. 쿼리를 GUI 기반으로 시각화하고 데이터 탐색을 쉽게 해준다.

C. 명령형 스크립트를 자동화한다.

D. 백업 전용 GUI이다.

**정답:** B

**해설:** Compass는 GUI 기반의 개발자 도구로, 쿼리 작성·Aggregation Builder·스키마 분석·인덱스 관리 등을 시각적으로 수행할 수 있다.

---

### 5️⃣ 다음 중 MongoDB Compass에서 제공하지 않는 기능은?

A. Aggregation 파이프라인 시각화

B. 컬렉션 문서 편집

C. 서버 버전 업그레이드

D. 인덱스 생성

**정답:** C

**해설:** Compass는 서버를 제어하지 않으며, 서버 업그레이드는 CLI나 Ops Manager를 통해 수행한다.

---

### 6️⃣ `mongosh`와 MongoDB Compass의 차이로 올바른 것은?

A. 둘 다 CLI이다.

B. Compass는 GUI, mongosh는 CLI 도구이다.

C. mongosh는 GUI, Compass는 CLI이다.

D. 둘 다 데이터 백업 전용이다.

**정답:** B

**해설:** mongosh는 명령어 기반 CLI, Compass는 시각적 GUI로 서로 보완적인 관계다.

---

### 7️⃣ VSCode에서 MongoDB 확장(Extension)을 사용하면 가능한 기능은?

A. 쿼리 결과를 직접 확인하고, 데이터베이스 연결 관리

B. MongoDB 서버를 설치

C. Replica Set 구성

D. MongoDB 버전 마이그레이션

**정답:** A

**해설:** VSCode MongoDB 확장 기능은 IDE 내에서 연결, 쿼리 실행, 결과 확인, 컬렉션 탐색을 지원한다.

---

### 8️⃣ `mongosh`에서 자바스크립트 코드 실행이 가능한 이유는?

A. Node.js 런타임 위에서 동작하기 때문이다.

B. Python 인터프리터를 사용하기 때문이다.

C. Go 런타임 위에서 동작하기 때문이다.

D. 자바 기반으로 만들어졌기 때문이다.

**정답:** A

**해설:** mongosh는 Node.js 기반으로 동작하여, 자바스크립트 문법을 지원한다. 예를 들어, `for` 반복문이나 변수 선언(`let`)을 그대로 사용할 수 있다.

---

### 9️⃣ MongoDB의 Aggregation 파이프라인을 대화형으로 테스트하고 시각화할 수 있는 도구는?

A. mongosh

B. MongoDB Compass

C. Atlas CLI

D. mongodump

**정답:** B

**해설:** Compass의 Aggregation Builder를 통해 각 스테이지를 순차적으로 추가하며 결과를 즉시 확인할 수 있다.

---

### 🔟 개발자가 로컬 환경에서 빠르게 쿼리 실험, CRUD 테스트, 데이터 구조 탐색을 모두 하고 싶을 때 가장 적합한 도구는?

A. mongodump

B. MongoDB Atlas

C. mongosh

D. mongoimport

**정답:** C

**해설:** mongosh는 쿼리 실험, CRUD 조작, 인덱스 조회 등 모든 개발 실습에 적합한 기본 도구이다.
