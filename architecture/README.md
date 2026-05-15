# 기술 아키텍처

## docs.pyhgoshift.com 구성도

```
[박용희 노트북]
D:\0.Pyhgoshift\AI-Claude\
shared\knowledge_base\outputs\docs_site\
        ↓ git push
[GitHub: pyhgoshift/pyhgoshift-docs]
        ↓ 자동 빌드·배포
[Cloudflare Pages]
        ↓ CNAME
[docs.pyhgoshift.com]
```

## 전체 시스템 구성도

```
[박용희 폰]
    ↓ Telegram @pyhgoshift_bot
[n8n 워크플로우 — NAS Docker]
    ↓
[Synology DS720+ NAS]
    ↓ Cloudflare Tunnel
[www.pyhgoshift.com]

[박용희 노트북] — Claude Code
    ↓ /구축기록 명령
[docs_site/ 자동 생성]
    ↓ GitHub push
[docs.pyhgoshift.com] — Cloudflare Pages
```

## 기술 스택

| 구분 | 도구 | 버전 |
|---|---|---|
| AI 모델 | Claude API | Sonnet 4.6 |
| STT | Whisper (로컬) | latest |
| 자동화 | n8n | self-hosted |
| 인프라 | Synology DS720+ | DSM 7.x |
| 네트워크 | Cloudflare Tunnel | latest |
| 버전관리 | Git | 2.54.0 |
| 런타임 | Node.js | 24 LTS |
| 컨테이너 | Docker Desktop | 4.73 |
| 문서 | Docsify | 4.x |
| CI/CD | Cloudflare Pages | — |
