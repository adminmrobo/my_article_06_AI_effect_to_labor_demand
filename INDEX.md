# INDEX — 파일·자산·페이지 지도

「조건부 노동수요와 생성형 AI — 산업별 구인수요의 반사실 실험실」 저장소의 파일 목록과 구성 지도입니다.
All pages are single self-contained HTML files (no build step, no external libraries except Google Fonts).

---

## 1. 파일 목록

| 파일 | 언어 | 크기 | 설명 |
|---|---|---|---|
| `index.html` | 한국어 | 약 17 KB | 첫 화면 — 7개 언어판 선택 보드. 저장소 루트 URL이 이 파일을 엽니다 |
| `01_labor_demand_ai.html` | 한국어 (원본) | 약 300 KB | 본편. 장면 그림 1장 base64 내장 |
| `01_labor_demand_ai.en.html` | English | 약 300 KB | 영어판 |
| `01_labor_demand_ai.zh.html` | 中文 (간체) | 약 300 KB | 중국어판 |
| `01_labor_demand_ai.ja.html` | 日本語 | 약 300 KB | 일본어판 |
| `01_labor_demand_ai.uz.html` | Oʻzbekcha | 약 300 KB | 우즈베크어판 |
| `01_labor_demand_ai.ru.html` | Русский | 약 300 KB | 러시아어판 |
| `01_labor_demand_ai.vi.html` | Tiếng Việt | 약 300 KB | 베트남어판 |
| `README.md` | 7개 언어 | — | 저장소 안내 |
| `INDEX.md` | 한국어/English | — | 이 파일 |
| `hero_01_ledger.webp` | — | 약 145 KB | 장면 그림 원본(1200×800). HTML에는 같은 그림이 base64로 내장됨 |

---

## 2. 그림 자산

| 키 | 파일 | 크기 | 내용 | 상태 |
|---|---|---|---|---|
| `hero_01` | `hero_01_ledger.webp` | 1200×800 (3:2) | 밤의 원장 사무실. 벽면 스프레드시트 보드에 판다가 빈 칸(빨간 테두리)에 보라 블록을 넣고, 박사·조수·초파리 연구원·Money-Robo가 검증 중 | 적용 완료 |
| — | 코드 생성 | 64×64 | 캐릭터 말풍선 아바타 4종(픽셀 맵 → canvas → dataURL). 외부 파일 없음 | 내장 |
| — | CSS/canvas | — | 배경 그라데이션, 육각 번호, 인터랙티브 차트 7종 | 내장 |

그림 규격: 16비트 RPG풍 픽셀아트, 굵은 외곽선(#1d1a22), 2~3단계 명암, 글자·숫자·로고 없음.
그림 속에는 글자가 없으며, 화면의 모든 수치는 본문 코드·데이터에서 계산됩니다.

---

## 3. 페이지 지도 (섹션 id)

| id | 제목 | 내용 |
|---|---|---|
| `#hero` | 히어로 | 제목, 핵심 수치 4칸, 장면 그림 01-A, 연구실 브리핑 말풍선 4개 |
| `#factory` | 🏭 공장 반사실 비유 | 과자 공장 슬라이더 실습 — 반사실 개념 |
| `#timeseries` | 📈 시계열 4대 개념 | 시계열·자기상관·공적분·ARDL 인터랙티브 도식 |
| `#lv1` | ① 질문 | 사전 대체위험 지수 vs 실제 구인수요 (산점도) |
| `#lv2` | ② 방법 | 조건부 노동수요함수, 자본 K 소거, 커버리지 통제 |
| `#lv3` | ③ 충격 | -40.7%p 격차, 반사실 경로, 위약 63개 |
| `#lv4` | ④ 시점 | 2022년 8월 선행 이탈, 인과 귀속의 함정 |
| `#lv5` | ⑤ 실험실 | 9대 강건성 검증, 초파리 vs Money-Robo 대결 |
| `#duel` | 대결 | 판정과 해설 |
| `#summary` | 정리 | 산업별 6행 결론 표 |
| `#kg` | 지식 색인 | 온톨로지 검색·미니 지식그래프 |
| `#export` | 꾸러미 | 인용, BibTeX, KG/CSL JSON ZIP 내려받기 |

---

## 4. 인터랙티브 요소

- 슬라이더·버튼 실습 8종, canvas 7개(모두 `aria-label` 지정)
- 퀴즈 5문항, 읽기 진행률, 지식 색인 실시간 검색
- 인용문·BibTeX 복사, `kg.json` / `kg.jsonld` / `kg.ttl` / `nodes,edges.csv` / `references.bib` ZIP 생성 (브라우저에서 즉석 생성)

---

## 5. 재현 방법

1. 저장소 루트에 HTML 7개와 `README.md`를 그대로 올립니다(폴더 없이).
2. `Settings → Pages → Deploy from a branch → main / (root)`를 선택합니다.
3. `https://adminmrobo.github.io/<저장소>/01_labor_demand_ai.html` 로 열립니다.
4. 로컬 확인은 파일을 브라우저로 열기만 하면 됩니다. 서버·빌드 불필요.

---

## 6. 라이선스

- 글·그림·코드: CC BY-NC 4.0 (저자 안상선, (주)M-Robo)
- 인용: 안상선 (2026). 조건부 노동수요함수를 이용한 산업별 구인수요 분석: 생성형 AI 확산 전후의 비교. 『미래사회』, 17(3), 247-265.
