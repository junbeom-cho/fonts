# Fonts

## Overview
자주 사용하는 폰트를 계속 다운받는 것이 번거로워서 레포지토리로 정리했습니다. `ttf` 타입과 `woff2` 타입이 모두 있기 때문에 필요에 맞게 사용하면 됩니다.

## Font List
### 1. D2Coding
**Naver**에서 제작한 개발용 글꼴입니다. 한글이 지원되는 개발 폰트는 사실상 유일하기 때문에 한국인 개발자에게 희망과 같은 글꼴입니다. 리거처(ligature)가 포함된 `1.4.0` 버전입니다.
- [공식 다운로드](https://github.com/naver/d2codingfont)

>[!tip]
> 아이콘이 필요하면 [SymbolsNerdFont](#3-symbolsnerdfont)를 `font-family`에 함께 지정하면 된다. NerdFonts 버전은 [링크](https://www.nerdfonts.com/font-downloads)를 통해 다운받을 수 있다.

### 2. JetBrainsMono
**JetBrains**에서 제작한 개발용 글꼴입니다. **IntelliJ**를 사용하면 익숙한 그 편안한 글꼴입니다. 기본 `JetBrains Mono`로 Thin ~ ExtraBold 굵기와 이탤릭이 모두 포함되어 있습니다.
- [공식 다운로드](https://www.jetbrains.com/lp/mono/)

### 3. SymbolsNerdFont
**NerdFonts**의 아이콘만 저장된 글꼴입니다. 터미널에서 아이콘을 사용하고 싶을 때 `font-family`에 추가하면 기존 글꼴을 유지하면서 아이콘을 사용할 수 있습니다.
- [공식 다운로드](https://www.nerdfonts.com/font-downloads)

### 4. Paperlogy
`Header`용 글꼴입니다. 글의 제목이나 목차에 사용하면 이쁩니다.
- [공식 다운로드](https://freesentation.blog/paperlogyfont)

### 5. Pretendard
`Body`용 글꼴입니다. 깔끔하고 세련된 글꼴로 평문 작성할 때 사용하기 좋습니다.
- [공식 다운로드](https://cactus.tistory.com/306)

### 6. KoPubWorld
공식 문서용 글꼴입니다. 바탕체, 돋움체 모두 있고 보고서에 사용하기 좋습니다.
- [공식 다운로드](https://www.kopus.org/biz-electronic-font2/)

### 7. WantedSans
**Wanted**에서 제작한 `Body`용 글꼴입니다. Pretendard와 비슷한 용도로 UI나 평문에 사용하기 좋습니다.
- [공식 다운로드](https://github.com/wanteddev/wanted-sans)

## ttf → woff2 변환
런타임과 도구는 [mise](https://mise.jdx.dev)로 관리합니다. `mise.toml`에 `python`, `uv`, `fonttools[woff]`가 정의되어 있습니다.

```bash
mise install              # python, uv, fonttools 설치
mise run woff2 D2Coding   # D2Coding/ttf/*.ttf → D2Coding/woff2/*.woff2
```

새 폰트는 `<폰트명>/ttf/`에 `ttf` 파일을 넣고 `mise run woff2 <폰트명>`을 실행하면 됩니다.

## References
- [글꼴 타입](https://wiki.junbeom.work/00-inbox/fonts)
- [글꼴 타입 변경](https://wiki.junbeom.work/00-inbox/fonttools)

