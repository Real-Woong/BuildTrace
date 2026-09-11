# BuildTrace — 도면 증거 검증 데모

**Live: https://buildtrace-demo.pages.dev**

건설 도면의 변경 이력을 **Walrus에 남기고 Sui로 소유**해, 분쟁이 생겼을 때
"누가 언제 무엇을 바꿨는가"를 증거로 제시하는 흐름을 보여주는 시연용 웹 데모입니다.

> BuildTrace는 책임이나 배상액을 판정하지 않습니다. 판단에 필요한 **증거를 제공**할 뿐입니다.

## 실행

정적 파일 하나(`index.html`)로 끝납니다. 빌드도 서버도 필요 없습니다.

```bash
open index.html          # 로컬에서 바로 열기
# 또는
python3 -m http.server 8899
```

## 조작

| 키 | 동작 |
|---|---|
| `→` `Space` `PageDown` | 다음 장면 |
| `←` `PageUp` | 이전 장면 |
| `Home` / `End` | 처음 / 마지막 |
| `R` | 현재 장면 다시 재생 |
| `F` | 전체화면 토글 |
| `?` | 단축키 도움말 |

`?step=3` 처럼 쿼리스트링으로 특정 장면에 바로 들어갈 수 있습니다.

## 배포

Cloudflare Pages 정적 배포.

| 항목 | 값 |
|---|---|
| Framework preset | None |
| Build command | (비움) |
| Build output directory | `/` |

`main` 브랜치에 푸시하면 자동 배포됩니다.

## 발표용 메모

- 폰트는 Google Fonts(Noto Sans KR · JetBrains Mono)에서 불러오고, 오프라인일 때를 대비해
  macOS·Windows 기본 폰트를 폴백으로 깔아 뒀습니다.
- 레이아웃 브레이크포인트가 1240 / 1100 / 820px에 있습니다. 프로젝터 해상도가 낮으면
  브라우저 배율(`Ctrl` `-`)을 낮춰 넓은 레이아웃을 유지하세요.
- Chromium 계열(Chrome · Edge)에서 검증했습니다.
