# 1주차 과제 – 3D 캐릭터 프로덕트 뷰어

첨부 캐릭터 이미지를 참고해 Three.js로 만든 3D 프로덕트 뷰어입니다.

- 데모: https://kyeong-hee.github.io/study_w1_v1/bunny-viewer.html

## 파일 구조

```
1주차/
├─ bunny-viewer.html   # 마크업 (캔버스, 우측 패널, Three.js importmap)
├─ css/
│  └─ style.css        # 레이아웃·패널·버튼 스타일, 모바일 반응형
└─ js/
   └─ main.js          # Three.js 장면, 캐릭터 모델링, 재질·모션·하트·컨택트 섀도우
```

## 실행 방법

JS를 별도 파일(ES 모듈)로 불러오기 때문에 `bunny-viewer.html`을 더블클릭(`file://`)으로 열면 동작하지 않습니다. 로컬 서버로 실행하거나 위 데모 링크로 확인하세요. Three.js는 CDN(jsDelivr, three@0.170.0)에서 불러오므로 인터넷 연결이 필요합니다.

```bash
py -m http.server 5178
```

이후 `http://localhost:5178/bunny-viewer.html` 접속 (VS Code Live Server 사용도 가능)

## 주요 기능

- 받침대 위 캐릭터 3D 모델 (부드러운 솔리드 재질, 와이어프레임 없음)
- 우측 패널: 컬러 스와치 3종(Cream / Sakura / Mint), Matte / Metal 재질 토글 → 실시간 반영
- OrbitControls 수평 회전만 허용 (줌·팬 비활성)
- 모션 섹션: Jump(예비 동작·스쿼시&스트레치 점프), Pet(쓰다듬기), Spin(제자리 회전)
  - 쓰다듬기: 손이 머리를 쓰다듬고, 눈이 `^ ^`로 바뀌며 볼 홍조가 진해지고 주변에 하트가 떠오름
  - 캐릭터를 클릭(탭)해도 쓰다듬기 실행, 반복 클릭 시 쓰다듬기 시간 연장
  - 귀는 스프링 물리로 흔들리고, 대기 상태에서는 숨쉬기·눈 깜빡임 표현
- 3점 스튜디오 조명(Key / Fill / Rim) + 컨택트 섀도우
- 리사이즈 대응, 모바일(760px 이하)에서는 패널이 하단으로 이동

## 기술 스택

HTML5, CSS3, JavaScript(ES Module), Three.js r170
