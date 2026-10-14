# taxapp-content

세금 도우미 앱(유니크온라인)의 **홈택스 따라하기 안내 문구·캡처 이미지** 저장소.
앱은 시작할 때 이 저장소의 `guide_content.json`을 읽어, 앱에 내장된 것보다 `version`이 높으면 그 내용을 쓴다. 세금 자료·개인정보는 없다.

- `guide_content.json` — 안내 문구. 앱 저장소 `taxapp/data/guide_content.json`과 같은 형식
- `images/` — 홈택스 화면 캡처 (사업자번호·이름 가린 것만). JSON의 `image` 칸에 `https://raw.githubusercontent.com/canecho1/taxapp-content/main/images/파일명.png` 형식으로 적는다

## 고치는 법 (홈택스 화면이 바뀌었을 때)
1. `guide_content.json`의 문구·함정·이미지 주소를 고친다
2. 맨 위 `version`을 올린다 (`YYYY-MM-DD-N`, 날짜가 같으면 N+1). **버전을 안 올리면 앱이 새 내용을 쓰지 않는다**
3. main에 푸시 → 앱이 다음 실행 때 반영 (앱 심사 없음)

조건 문장 `{ "when": "late", "text": "..." }`의 조건 이름과 `{{자리표시}}` 목록은 JSON 맨 위 `note` 참고.
