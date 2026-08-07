# 카카오톡 채널 처음부터 세팅하기 — 영구오빠

카카오톡 채널 온보딩 5단계 가이드. 모바일 우선, 단일 페이지 정적 사이트.

## 배포 방법

1. 이 폴더 전체를 GitHub 저장소에 업로드 (`index.html`이 최상단에 있어야 함)
2. `Settings → Pages → Source: Deploy from a branch → main / (root)` 선택
3. 1~2분 뒤 `https://아이디.github.io/저장소이름/` 으로 접속

## 업로드 전 딱 한 가지만 수정

`index.html` 상단의 이 두 줄을 실제 주소로 바꿔주세요. 카톡·인스타로 링크를 보낼 때
썸네일이 뜨는 부분이라, 상대경로면 이미지가 안 나옵니다.

```html
<meta property="og:url" content="https://USERNAME.github.io/REPO/">
<meta property="og:image" content="https://USERNAME.github.io/REPO/images/shot_cbf2b3e9.webp">
```

## 파일 구조

```
index.html    전체 본문 + 스타일 + 스크립트 (37KB)
images/       화면 캡처 5장 (webp, 총 292KB)
.nojekyll     GitHub Pages의 Jekyll 처리 비활성화
```

## 단톡방 링크 바꾸기

오픈채팅 주소를 바꿀 일이 생기면 `index.html`에서 `open.kakao.com`을 검색해
두 곳(하단 플로팅 바 / 마지막 CTA)을 수정하면 됩니다.

## 원본 대비 변경 사항

- 4.8MB → 330KB (폰트를 파일 내장에서 Pretendard CDN으로 전환, 캡처는 PNG→WebP)
- 데스크톱 2단 레이아웃 → 모바일에서 1단으로 자동 전환
- 상단 5단계 네비게이션은 모바일에서 가로 스크롤 방식
- 화면 캡처는 탭하면 원본 크기로 확대(핀치 줌 가능) — 폭 1600px 캡처라 필수
- 상단 읽기 진행바 / 하단 단톡방 플로팅 바 / 마지막 CTA 섹션 추가
