### 1) 다음 중 **MongoDB 연결 문자열(URI)**의 기본 형식으로 옳은 것은?

A. `jdbc:mongodb://host:port/db`

B. `mongodb://user:pass@host1:27017,host2:27017/db?opts`

C. `mongo+srv://host:27017/db`

D. `mongo://host/db?ssl=true`

**정답:** B

**해설:** 표준 형식은 `mongodb://[user:pass@]host[,host2]/db?옵션`이다. `+srv`는 포트 없이 DNS SRV를 사용한다.

---

### 2) **SRV 레코드 기반 연결**(Atlas 등)에서 올바른 설명은?

A. 반드시 포트를 명시해야 한다

B. `mongodb+srv://cluster.example.com/db` 형식을 사용하며 드라이버가 **시드 목록/옵션을 DNS에서 자동 조회**한다

C. 로컬 설치에서만 가능

D. TLS를 사용할 수 없다

**정답:** B

**해설:** `mongodb+srv://`는 포트 없이 도메인만으로 SRV/TXT 레코드를 조회해 시드 호스트·기본 옵션(TLS 등)을 자동 반영한다.

---

### 3) **서버 선택 시간 초과**를 제어하는 커넥션 옵션은?

A. `socketTimeoutMS`

B. `serverSelectionTimeoutMS`

C. `heartbeatFrequencyMS`

D. `wtimeoutMS`

**정답:** B

**해설:** `serverSelectionTimeoutMS`는 드라이버가 적합한 서버(Primary/적절한 Secondary)를 찾는 데 쓸 최대 대기시간이다. 소켓/쓰기 타임아웃과 구분.

---

### 4) **TLS/SSL 보안 연결**과 가장 직접적으로 관련된 올바른 조합은?

A. `tls=true`, 서버 인증서 신뢰 저장소 설정

B. `authMechanism=MONGODB-X509`인 경우에도 TLS 불필요

C. `tls=false`여도 X.509 인증 가능

D. TLS 사용 시 커넥션 풀은 비활성화됨

**정답:** A

**해설:** TLS를 활성화하면 서버 인증서 신뢰 설정이 필요하다. X.509는 TLS 위에서 동작하므로 TLS가 필수다.

---

### 5) **인증 메커니즘** 설명으로 옳은 것은?

A. 기본은 PLAIN이며 LDAP에만 사용됨

B. SCRAM-SHA-256/ -1이 일반적이며, X.509는 **클라이언트 인증서 기반**이다

C. 인증 메커니즘은 URI가 아닌 서버 측에서만 결정

D. `authSource`는 항상 `admin`만 가능

**정답:** B

**해설:** 일반적으로 SCRAM이 기본이며, X.509는 TLS 클라이언트 인증서를 활용한다. `authSource`는 DB별로 지정 가능.

---

### 6) **Retryable Writes**에 대한 올바른 설명은?

A. 네트워크 오류 시 **idempotent한 일부 쓰기**를 드라이버가 재시도할 수 있다

B. 모든 쓰기에 대해 무한 재시도를 수행한다

C. 복제/샤딩 환경에서는 동작하지 않는다

D. 읽기 전용 쿼리에만 적용된다

**정답:** A

**해설:** `retryWrites=true`는 네트워크 단절 등 일시 오류에서 일부 쓰기(예: 단건 insert 등)를 안전하게 재시도한다(무한 재시도 아님).

---

### 7) 다음 중 **커넥션 풀링** 관련 설명으로 옳은 것은?

A. `maxPoolSize`는 동시 연결 수 상한을 의미한다

B. `minPoolSize`는 CPU 코어 수와 동일해야 한다

C. 풀을 쓰면 트랜잭션이 불가능하다

D. 풀은 TLS 사용 시 비활성화된다

**정답:** A

**해설:** `maxPoolSize`는 풀 내 동시 커넥션 상한, `minPoolSize`는 유휴 시에도 유지할 최소 연결 수다. TLS/트랜잭션과 공존한다.

---

### 8) **시간 초과 옵션**과 매칭이 올바른 것은?

A. `connectTimeoutMS`: 쿼리 실행 최대 시간

B. `socketTimeoutMS`: **I/O 활동이 없는 상태로 대기 가능한 최대 시간**

C. `maxIdleTimeMS`: 서버 선택 시간 제한

D. `serverSelectionTimeoutMS`: TCP 연결 수립 제한

**정답:** B

**해설:** `socketTimeoutMS`는 읽기/쓰기 대기 중 **무활동** 최대시간, `connectTimeoutMS`는 TCP 연결 수립, `serverSelectionTimeoutMS`는 서버 선택, `maxIdleTimeMS`는 풀 내 유휴 커넥션 종료 시간과 관련된다.

---

### 9) **읽기 선호도(Read Preference)**를 URI에 넣을 때 올바른 예시는?

A. `.../db?readPreference=primary`

B. `.../db?readPref=secondaryPreferred`

C. `.../db?readConcern=nearest`

D. `.../db?readPreferenceTags=primary`

**정답:** A

**해설:** 표준 키는 `readPreference`이며 값으로 `primary|primaryPreferred|secondary|secondaryPreferred|nearest` 등을 쓴다. 태그는 별도 파라미터로 지정.

---

### 10) **압축(Compressor)** 설정의 목적과 예시로 옳은 것은?

A. 네트워크가 빠른 경우엔 압축이 강제 비활성화된다

B. `compressors=zstd,snappy`처럼 지정하여 **네트워크 대역 사용을 줄이고 지연을 개선**할 수 있다

C. 압축을 켜면 TLS를 쓸 수 없다

D. 압축은 클러스터 메타데이터에만 적용된다

**정답:** B

**해설:** 드라이버/서버가 모두 지원하는 압축기를 협상해 사용한다(zstd, snappy, zlib 등). 대역폭 절감과 전송 지연 개선에 유용하다.
