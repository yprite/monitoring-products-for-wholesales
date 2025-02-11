# monitoring-products-for-wholesales

## Structure
```
/project-root
│── index.html         # 메인 페이지 (UI)
│── main.js            # 메인 페이지를 관리하는 스크립트
│── fetch/
│   │── domeggook.js   # 도매꾹 API 연동 스크립트
│   │── domeme.js      # (추후 확장 가능)
│   │── funnshop.js    # (추후 확장 가능)
│── utils/
│   │── apiHelper.js   # API 요청 및 공통 처리 함수
│── styles.css         # 스타일링 파일
```
- 1️⃣ 메인 페이지 (index.html)
  - 검색창 & 결과 출력 UI
	- 사용자가 상품명을 입력하면 JavaScript에서 API 호출
  - 가져온 데이터를 표로 정리하여 보여줌
- 2️⃣ 메인 스크립트 (main.js)
	- 사용자가 상품을 검색하면 fetch/domeggook.js 같은 개별 스크립트를 호출
	- 데이터 수집 후 테이블에 업데이트
- 3️⃣ 개별 쇼핑몰 스크립트 (fetch/domeggook.js)
	- 도매꾹 API에서 상품 데이터를 가져오는 역할
	- API 호출 → JSON 데이터 정리 → main.js로 전달
- 4️⃣ API 도우미 (utils/apiHelper.js)
	- API 요청 공통 처리
	- 에러 핸들링 및 데이터 정리

## API 발급
### 도매꾹
- 1️⃣ 도매꾹 API 키 발급

- 먼저, 도매꾹 API를 사용하기 위해 API 키를 발급.
  -	도매꾹 계정 생성 및 로그인: 도매꾹 계정이 없다면 도매꾹에서 계정을 생성하고 로그인.
  -	API 키 발급:
  	-	도매꾹 OpenAPI 사이트로 이동하여 로그인.
  	- 상단 메뉴에서 **“API 키 관리”**를 선택.
  	- “API 키 발급” 버튼을 클릭하고, 양식에 맞춰 내용을 입력한 후 API 키를 발급.
￼
