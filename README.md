# 인사이트랩 시네마틱 스크롤 웹사이트

InsightLab (인사이트랩) — Connecting regions with data & AI.
공공데이터와 AI로 지역을 잇는 위치정보(LBS) 1인 창업 스튜디오의 시네마틱 스크롤 사이트.

## 파일 구성 (GitHub 업로드)

```
insightlab-home/
├── index.html            # 사이트 본체 (단일 파일: HTML + CSS + JS)
├── wrangler.toml         # Cloudflare Workers 배포 설정 (기존 유지)
├── og.png                # 링크 미리보기 이미지 (기존 유지)
└── assets/               # 미디어 (아래 3개 파일을 넣어야 영상이 뜸)
    ├── the_signal.mp4        # 히어로 클립 (THE SIGNAL, 1080p·8s)
    ├── the_build.mp4         # 광주든든 섹션 클립 (THE BUILD, 720p·8s)
    └── the_signal_hero.png   # 히어로/포스터 이미지
```

`index.html`은 위 3개 파일을 `assets/` 폴더에서 상대경로로 불러옵니다.
**assets 폴더가 없으면 영상 자리가 비어 보입니다.**

## 영상 파일 받기

Higgsfield에서 생성한 원본 (브라우저에서 열어 저장):

- the_signal.mp4 : https://d8j0ntlcm91z4.cloudfront.net/user_3FwoVGHAl68Vv27v9khwgY0Fx3c/hf_20260710_100448_2cc53957-fdb3-4752-861e-4579265f9139.mp4
- the_build.mp4 : https://d8j0ntlcm91z4.cloudfront.net/user_3FwoVGHAl68Vv27v9khwgY0Fx3c/hf_20260710_101228_e257977e-2459-4e69-bfd3-b0e011f4ec1c.mp4
- the_signal_hero.png : https://d8j0ntlcm91z4.cloudfront.net/user_3FwoVGHAl68Vv27v9khwgY0Fx3c/hf_20260710_100215_8b54823a-fcb2-4f2c-86e3-fdd92efef28a.png

## 동작 참고

- **히어로는 스크롤 스크럽 방식**입니다. 로드 직후엔 첫 프레임(포스터)이 보이고, 스크롤을 내리면 THE SIGNAL 영상이 프레임 단위로 재생됩니다. 처음에 정지 화면인 건 정상입니다.
- 광주든든(FLAGSHIP) 섹션의 THE BUILD 영상은 그 섹션이 화면에 들어올 때 재생됩니다.
- 모든 영상은 muted + playsinline이라 모바일 자동재생이 됩니다.

## 아직 안 만든 것

- THE LIVE, THE REACH 클립 (2개) — 크레딧 소진으로 미생성. 추후 충전해서 추가 가능.
- 추가하면 index.html에 섹션을 붙이면 됩니다.

## 기술 스택 (사이트 자체)

Vanilla HTML/CSS/JS · Lenis(스무스 스크롤) · Space Grotesk / JetBrains Mono / Pretendard.
빌드 도구 없이 정적 파일 그대로 배포.

---
© 2026 InsightLab · 대표 이현진 · 사업자등록번호 121-32-93146 · 광주광역시 남구
