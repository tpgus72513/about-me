# 자기소개 페이지 — 클리어 네이비 시안

Day 3 CSS 학습 과정에서 같은 자기소개 내용을 다른 분위기로 표현한 비교용 시안입니다.
현대적이고 세련되며, 공식적이고 시원한 인상을 목표로 했습니다.

## 실행 방법과 구성

이 폴더의 index.html을 브라우저로 열면 됩니다. 파일을 수정한 뒤 저장하고 새로고침합니다.
style.css와 assets 폴더를 함께 유지해야 합니다. Google Fonts를 불러올 때는 인터넷 연결이 필요합니다.

- index.html: 기존 자기소개 내용과 의미 있는 HTML 구조
- style.css: 이번 시안의 색상·글꼴·여백·이미지 스타일
- assets/clear-architecture.png: 새로 생성한 장식용 건축 이미지
- README.md: 디자인 선택과 실행 방법

## 두 스타일의 차이

| 요소 | 로즈 머스크 | 클리어 네이비 |
| --- | --- | --- |
| 색상 | 아이보리·로즈·플럼 | 차가운 화이트·블루그레이·네이비 |
| 제목 | 고운바탕 명조체 | Noto Sans KR 고딕체 |
| 정렬 | 상단 가운데 정렬 | 상단과 본문을 왼쪽 기준선에 정렬 |
| 이미지 | 유리·꽃·천 | 흰 건축물·유리·하늘 |
| 인상 | 부드럽고 감성적인 소개 | 차분하고 공식적인 프로필 |

## 색상 값

| 역할 | 값 |
| --- | --- |
| 배경 | #F6F9FB |
| 밝은 영역 | #FFFFFF |
| 제목·본문 | #142B3B |
| 보조 글자 | #5C6E7B |
| 강조·링크 | #24617B |
| 구분선 | #D5E0E7 |

작은 영문 이름에는 Manrope, 한글 제목과 본문에는 Noto Sans KR을 사용합니다.
글꼴을 불러오지 못하면 맑은 고딕 등 대체 고딕체로 표시됩니다.

## CSS에서 비교할 부분

1. :root의 색상 변수를 비교하면 같은 구조에서 색상이 분위기에 미치는 영향을 볼 수 있습니다.
2. h1의 font-family, font-size, font-weight, letter-spacing을 비교합니다.
3. header의 가운데 정렬을 해제하고, 본문과 최대 너비를 맞춰 왼쪽 기준선을 통일했습니다.
4. .mood-image에 aspect-ratio: 16 / 5와 object-fit: cover를 적용했습니다. 비율을 유지한 채 일부를 잘라 넓게 표시합니다.
5. 모서리는 직선으로 두고, 선·행간·여백으로 영역을 구분했습니다.

메뉴는 Day 3 수준의 inline-block을 사용합니다. Flexbox와 미디어 쿼리를 통한 화면별 배치는 Day 4 학습 내용입니다.
이 폴더는 같은 저장소에 보관하는 Day 3 비교 시안입니다. 과제 제출과 이후 Day 4·5 학습은 [로즈 머스크 기본 페이지](../../index.html)를 기준으로 진행합니다. 페이지 하단의 링크로 기본 페이지에 돌아갈 수 있습니다.

## 이미지 제작 기록

기본 제공 image_gen 도구로 새 이미지를 생성했습니다. CLI나 API 키는 사용하지 않았습니다.
이미지 위치는 assets/clear-architecture.png입니다. 특정 실제 건축물이나 사용자의 근무지를 나타내지 않는 장식 이미지로, HTML에는 alt=""를 사용했습니다.

<details>
<summary>이미지 생성 프롬프트</summary>

Use case: photorealistic-natural. Asset type: a decorative wide editorial architectural photograph for a Korean software developer's personal introduction website. Create one landscape photograph, 1536 by 1024. Art direction: modern, exceptionally clean, cool, composed and quietly luxurious, like a refined official design studio profile. An elegant contemporary white architectural facade with a precise cantilevered roof and a restrained series of slim silver aluminum fins beside clear blue-tinted glazing, framing a large expanse of pale clear blue sky. Camera looking slightly upward, crisp refined lines with believable architectural engineering and perspective. The architecture occupies the left and lower portion while the upper and right areas breathe with open sky. Bright cool morning daylight, soft blue-gray shadows, matte white surfaces, subtle real glass reflections, no dramatic gradients or saturated cobalt. The visual should communicate clarity and thoughtful structure. Crop-safe composition for a very wide 16:5 banner through the middle of the photograph; include architectural edges and sky across that horizontal crop. Premium editorial architecture photography, realistic surface detail, balanced exposure. No people, no signage, no logos, no words, no watermarks, no flowers, no pink, no perfume products, no futuristic floating objects, no collage, no website mockup. Render the photograph itself.

</details>
