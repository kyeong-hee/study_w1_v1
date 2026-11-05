# 1주차 과제 – 3D 캐릭터 프로덕트 뷰어

첨부 캐릭터 이미지를 참고해 Three.js로 만든 단일 HTML 3D 프로덕트 뷰어입니다.

## 실행 방법

`bunny-viewer.html`을 브라우저로 열면 됩니다. Three.js를 CDN(jsDelivr, three@0.170.0)에서 불러오므로 인터넷 연결이 필요합니다.

> 일부 브라우저는 `file://` 경로에서 ES 모듈 로딩을 막을 수 있습니다. 이 경우 로컬 서버로 실행하세요.
>
> ```bash
> py -m http.server 5178
> ```
>
> 이후 `http://localhost:5178/bunny-viewer.html` 접속

## 주요 기능

- 받침대 위 캐릭터 3D 모델 (부드러운 솔리드 재질, 와이어프레임 없음)
- 우측 패널: 컬러 스와치 3종(Cream / Sakura / Mint), Matte / Metal 재질 토글 → 실시간 반영
- OrbitControls 수평 회전만 허용 (줌·팬 비활성)
- 3점 스튜디오 조명(Key / Fill / Rim) + 컨택트 섀도우
- 리사이즈 대응, 모바일(760px 이하)에서는 패널이 하단으로 이동

## 기술 스택

HTML5, CSS3, JavaScript(ES Module), Three.js r170
