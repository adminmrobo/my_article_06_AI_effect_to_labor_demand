# 조건부 노동수요와 생성형 AI — 산업별 구인수요의 반사실 실험실

워크넷 구인 행정데이터와 비용최소화 조건부 노동수요함수로, 생성형 AI 확산 전후 산업별 구인수요가
어떻게 달라졌는지 사후 검증하는 **단일 HTML 인터랙티브 리포트**입니다. 빌드 없이 브라우저로 열면 바로 동작합니다.

An interactive single-file report that tests, after the fact, how industry-level job openings changed around
the diffusion of generative AI — using Worknet administrative job-posting data and a cost-minimising
conditional labor demand function from Ahn (2026).

---

## 바로 보기 / Live

- 한국어: `https://adminmrobo.github.io/<저장소>/01_labor_demand_ai.html`
- English: `https://adminmrobo.github.io/<저장소>/01_labor_demand_ai.en.html`

> `<저장소>`를 실제 저장소 이름으로 바꿔 주세요. (Settings → Pages → Deploy from a branch → `main` / `(root)`)

## 저자 / Author

글·그림·코드 · **안상선** ((주)M-Robo 대표) — Written by Ahn Sangsun (CEO, M-Robo Co., Ltd.)

---

## 언어 / Languages

| 언어 | 파일 | 상태 |
|---|---|---|
| 한국어 | `01_labor_demand_ai.html` | 원본 |
| English | `01_labor_demand_ai.en.html` | 완료 |
| 中文 | `01_labor_demand_ai.zh.html` | 완료 |
| 日本語 | `01_labor_demand_ai.ja.html` | 완료 |
| Oʻzbekcha | `01_labor_demand_ai.uz.html` | 완료 |
| Русский | `01_labor_demand_ai.ru.html` | 완료 |
| Tiếng Việt | `01_labor_demand_ai.vi.html` | 완료 |

- 언어 전환: 최상단 메뉴의 🌐 선택 상자, 오른쪽 아래 🌐 배너. 고른 언어는 브라우저에 기억됩니다.
- 한국어 페이지는 처음 방문할 때 브라우저 언어를 보고 번역판이 있으면 그쪽으로 자동 전환합니다(`?lang=en`으로 강제 가능).
- 번역판 주소로 들어온 사람은 자동 전환하지 않습니다.
- 인용·서지 정보는 원문 표기(한국어)를 유지합니다.

---

## 이 편의 핵심 숫자 / Key numbers

| 값 | 뜻 |
|---|---|
| **-40.7%p** | 검증구간(2025.10~2026.03) 정보통신업 구인수요의 대조군(제조업) 대비 상대격차 |
| **-55.7%p** | 위약 63개로 외삽 치우침을 보정한 뒤의 격차 (단측 p = .016) |
| **2022.08~** | 이탈 시작 시점 — ChatGPT 공개(2022.11)보다 앞섬 (-7.7%p → 9월 -18.0%p) |
| **ρ = -0.257** | 사전 대체가능성 지수 순위와 실제 격차의 순위상관 (p = .623, 유의하지 않음) |
| **1,417 vs 3,777** | 정보통신업 실제 월평균 구인 vs 확산 이전 법칙 유지 시 반사실 경로 |
| **-31.3%p** | 코로나19 급증기(2020~2022)를 전부 제외해도 남는 격차 |

---

## 페이지 구성 / What's inside

| 섹션 | 내용 |
|---|---|
| 히어로 | 제목, 핵심 수치 4칸, 장면 그림, 연구실 브리핑 |
| `#factory` | 과자 공장 슬라이더로 익히는 반사실(counterfactual) 개념 |
| `#timeseries` | 시계열·자기상관·공적분·ARDL 4대 개념 인터랙티브 도식 |
| `#lv1` | 사전 대체위험 지수 vs 실제 구인수요 (산점도, 6개 산업) |
| `#lv2` | 조건부 노동수요함수, 자본 K 소거, 워크넷 커버리지 통제 |
| `#lv3` | -40.7%p 격차, 반사실 경로, 위약(Placebo) 63개 검증 |
| `#lv4` | 2022년 8월 선행 이탈과 인과 귀속의 함정 |
| `#lv5` | 9대 강건성 검증, 초파리 vs Money-Robo 대결 |
| `#summary` | 산업별 6행 결론 표 |
| `#kg` | 온톨로지 지식 색인(실시간 검색·미니 지식그래프) |
| `#export` | 인용·BibTeX 복사, `kg.json`·`kg.ttl`·`references.bib` ZIP 내려받기 |

- 인터랙티브 실습 8종, canvas 7개(모두 `aria-label`), 퀴즈 5문항, 읽기 진행률.
- 외부 라이브러리·쿠키·저장소를 쓰지 않습니다. Google Fonts만 불러옵니다.

---

## 데이터와 그림 / Data and images

- **데이터**: 고용노동부·한국고용정보원 워크넷 구인구직 및 취업동향(2010.01~2026.03 유효구인인원),
  한국은행 ECOS 기업대출 금리. 모든 수치는 논문 원문의 표와 일치하도록 재현했습니다.
- **그림**: 16비트 픽셀아트 장면 1장(1200×800, `assets/hero_01_ledger.webp`)과 캐릭터 말풍선 아바타 4종.
  아바타는 픽셀 맵을 canvas로 그려 쓰므로 이미지 파일이 필요 없습니다.
- **그림 속 글자**: 장면 그림에는 글자·숫자·로고가 없습니다. 화면의 수치는 모두 코드에서 계산됩니다.
- **설명용 모형인 것**: 과자 공장 슬라이더(`#factory`)와 시계열 비유 도식(`#timeseries`)은 개념 설명용입니다.
  논문의 실측 수치는 `#lv1`~`#lv5`의 표와 차트이며, 각 수치에는 출처 표·식을 표시했습니다.

---

## 파일 / Files

```
01_labor_demand_ai.html          한국어 원본 (약 284 KB, 그림 base64 내장)
01_labor_demand_ai.en.html       English
README.md                        이 파일
INDEX.md                         파일·자산·페이지 지도
assets/hero_01_ledger.webp       장면 그림 원본 (1200×800)
```

---

## 라이선스 / License

글·그림·코드: **CC BY-NC 4.0** — 저작자표시·비영리. 교육·연구 목적 사용을 환영합니다.
<https://creativecommons.org/licenses/by-nc/4.0/deed.ko>

출처 표기 예:

> 안상선 (2026). 조건부 노동수요함수를 이용한 산업별 구인수요 분석: 생성형 AI 확산 전후의 비교.
> 『미래사회』, 17(3), 247-265. DOI: 10.22987/jifso.2026.17.3.247

---

# English

An interactive single-file report on **conditional labor demand and generative AI**: did the collapse of
Korean job openings in information and communication really come from generative AI?

It rebuilds the paper's econometrics in the browser: a cost-minimising conditional labor demand function that
eliminates capital without capital-stock data, a Worknet coverage control, a counterfactual extrapolation from
the pre-diffusion rule, a 63-run placebo test, and nine robustness checks. All numbers come from the paper's
tables; the factory slider and the time-series diagrams are illustrative analogies.

- **Open**: `01_labor_demand_ai.en.html` (same folder, no build step, no external libraries).
- **Key numbers**: -40.7%p gap versus manufacturing in the validation window; -55.7%p after bias correction
  (one-sided p = .016); the slide began in August 2022, before ChatGPT; rank correlation with the ex-ante
  index ρ = -0.257 (p = .623, not significant).
- **Author**: Ahn Sangsun (CEO, M-Robo Co., Ltd.) · **License**: CC BY-NC 4.0
- Citations and bibliographic records keep their original Korean titles.

---

## 中文

单文件交互式报告：**条件劳动力需求与生成式 AI**。用 Worknet 招聘行政数据与成本最小化条件劳动力需求函数，
检验信息通信业招聘需求的暴跌是否真的源自生成式 AI。

- 打开 `01_labor_demand_ai.zh.html` 即可，无需构建，不依赖外部库。
- 关键数字：验证期相对制造业 -40.7%p；偏差校正后 -55.7%p（单侧 p = .016）；下滑始于 2022 年 8 月（早于 ChatGPT）；
  与事前替代指数排序的相关系数 ρ = -0.257（p = .623，不显著）。
- 作者：Ahn Sangsun（M-Robo 代表） · 许可：CC BY-NC 4.0

## 日本語

単一 HTML のインタラクティブ・レポート：**条件付き労働需要と生成型 AI**。Worknet の求人行政データと
費用最小化の条件付き労働需要関数を用いて、情報通信業の求人需要の急落が本当に生成型 AI によるものかを検証します。

- `01_labor_demand_ai.ja.html` を開くだけ。ビルド不要、外部ライブラリなし。
- 主要な数値：検証期間の製造業対比 -40.7%p、バイアス補正後 -55.7%p（片側 p = .016）、
  低下は 2022 年 8 月に始まり ChatGPT 公開より先行、事前指数との順位相関 ρ = -0.257（p = .623、有意でない）。
- 著者：Ahn Sangsun（M-Robo 代表）／ライセンス：CC BY-NC 4.0

## Oʻzbekcha

Yagona HTML fayldagi interaktiv hisobot: **shartli mehnat talabi va generativ AI**. Worknet ish o'rinlari
ma'lumotlari va xarajatni minimallashtiruvchi shartli mehnat talabi funksiyasi yordamida axborot-kommunikatsiya
tarmog'idagi ish o'rinlari keskin kamayishining sababi haqiqatan generativ AI ekanini tekshiradi.

- `01_labor_demand_ai.uz.html` faylini ochish kifoya; yig'ish shart emas, tashqi kutubxonalar yo'q.
- Asosiy raqamlar: tekshiruv davrida ishlab chiqarishga nisbatan -40.7%p; xatolik tuzatilgach -55.7%p (bir tomonlama p = .016);
  pasayish 2022-yil avgustda boshlangan (ChatGPT'dan oldin); daraja korrelyatsiyasi ρ = -0.257 (p = .623, ahamiyatsiz).
- Muallif: Ahn Sangsun (M-Robo rahbari) · Litsenziya: CC BY-NC 4.0

## Русский

Интерактивный отчёт в одном HTML-файле: **условный спрос на труд и генеративный ИИ**. С помощью
административных данных Worknet о вакансиях и функции условного спроса на труд, минимизирующей издержки,
проверяется, действительно ли обвал вакансий в отрасли ИКТ вызван генеративным ИИ.

- Достаточно открыть `01_labor_demand_ai.ru.html`: сборка не нужна, внешних библиотек нет.
- Ключевые числа: -40.7%p относительно обрабатывающей промышленности в проверочном окне; -55.7%p после
  поправки на смещение (одностороннее p = .016); спад начался в августе 2022 года, до выхода ChatGPT;
  ранговая корреляция ρ = -0.257 (p = .623, незначима).
- Автор: Ан Сансон (M-Robo) · Лицензия: CC BY-NC 4.0

## Tiếng Việt

Báo cáo tương tác trong một tệp HTML: **cầu lao động có điều kiện và AI tạo sinh**. Dùng dữ liệu hành chính
về tin tuyển dụng của Worknet và hàm cầu lao động có điều kiện tối thiểu hóa chi phí, báo cáo kiểm định xem
việc tin tuyển dụng trong ngành công nghệ thông tin – truyền thông sụt giảm có thực sự do AI tạo sinh hay không.

- Chỉ cần mở `01_labor_demand_ai.vi.html`; không cần build, không dùng thư viện ngoài.
- Các con số chính: -40.7%p so với ngành chế tạo trong giai đoạn kiểm chứng; -55.7%p sau khi hiệu chỉnh độ lệch
  (p một phía = .016); đà giảm bắt đầu từ tháng 8/2022, trước khi ChatGPT ra mắt; tương quan hạng ρ = -0.257 (p = .623, không có ý nghĩa).
- Tác giả: Ahn Sangsun (Giám đốc M-Robo) · Giấy phép: CC BY-NC 4.0
