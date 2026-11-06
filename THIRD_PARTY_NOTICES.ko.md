# 제3자 고지 (Third-Party Notices) — TabViewer

최종 수정: 2026년 11월 1일

> 이 문서는 이해를 돕기 위한 번역본입니다. 영어 원문([THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md))과 내용이 다를 경우 영어 원문이 우선합니다. 아래 MIT 라이선스 전문은 법적 효력을 위해 영어 원문 그대로 싣습니다.

TabViewer는 jayusop이 만든 프리웨어입니다. 이 문서는 TabViewer에 관련된 모든 제3자 구성요소, 데이터, 상표를 나열하고 각각 어떤 조건으로 쓰는지 밝힙니다. 이 문서는 TabViewer 설명서의 일부이며 모든 배포판에 함께 포함됩니다.

**요약**

| 항목 | 앱에 포함? | 적용 조건 |
|---|---|---|
| Steinberg VST® 3 SDK (호스팅 소스) | 예 — 앱에 컴파일되어 포함 | MIT 라이선스 (전문은 아래) |
| Apple macOS 프레임워크 | 아니요 — macOS의 일부 | Apple macOS 라이선스 |
| macOS General MIDI 사운드뱅크, Apple Symbols 글꼴 | 아니요 — 실행 중 macOS에서 읽음 | Apple macOS 라이선스 |
| 사용자가 설치한 Audio Unit / VST 3 플러그인 | 아니요 | 각 플러그인 제조사의 라이선스 |
| 소개 웹사이트의 글꼴 | 아니요 — Google Fonts에서 불러옴 | SIL Open Font License 1.1 |

이 밖의 모든 부분 — 악보 파서와 저장 코드, 레이아웃·렌더링 엔진, 재생 엔진, 사용자 인터페이스, 앱 아이콘 — 은 이 프로젝트를 위해 새로 작성했습니다. 다른 프로그램이나 라이브러리의 코드를 복사하지 않았습니다. TabViewer에는 제3자 글꼴, 음원 샘플, 악보 파일이 들어 있지 않습니다.

---

## 1. TabViewer에 포함된 구성요소

### Steinberg VST® 3 SDK

- 용도: Mac에 설치된 VST 3 악기 플러그인을 불러와 재생
- 사용 범위: SDK의 호스팅 소스(`pluginterfaces`, `public.sdk/source/common`, `public.sdk/source/vst/hosting`, `public.sdk/source/vst/utility`)를 앱에 컴파일해 포함. VSTGUI와 SDK 예제는 사용하지 않음
- 고지 위치: 이 문서, 그리고 앱의 **TabViewer 정보** 창(MIT 라이선스 전문)
- 버전: VST SDK 3.8.1 (build 84), 소스 저장소에 Git 서브모듈로 포함
- 출처: https://github.com/steinbergmedia/vst3sdk
- 라이선스: MIT 라이선스 (영어 원문)

    MIT License

    Copyright (c) 2026, Steinberg Media Technologies GmbH

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

위 MIT 라이선스는 Steinberg VST 3 SDK에만 적용됩니다. TabViewer 전체에는 TabViewer 프리웨어 라이선스([LICENSE](LICENSE))가 적용됩니다. TabViewer 프리웨어 라이선스의 어떤 조항도(리버스 엔지니어링 제한 포함) Steinberg VST 3 SDK에 대해 MIT 라이선스가 귀하에게 부여한 권리를 제한하지 않습니다.

"VST is a registered trademark of Steinberg Media Technologies GmbH." (VST는 Steinberg Media Technologies GmbH의 등록 상표입니다.)

---

## 2. 실행 중에 사용하지만 포함하지 않는 구성요소

TabViewer는 실행 중에 아래의 macOS 구성요소를 사용합니다. 이들은 macOS와 함께 설치되어 있으며, TabViewer에 복사되거나 함께 배포되지 않고, Apple의 macOS 소프트웨어 라이선스 조건에 따라 사용됩니다.

- **시스템 프레임워크**: SwiftUI, AppKit, Foundation, AVFoundation, AudioToolbox, CoreAudioKit, CoreGraphics, PDFKit, Compression, UniformTypeIdentifiers, Observation. (`.gp` 파일의 ZIP/DEFLATE 데이터는 Apple Compression 프레임워크로 압축을 풉니다.)
- **General MIDI 사운드뱅크**: 기본 재생음으로 macOS 내장 사운드뱅크(`gs_instruments.dls`)를 사용합니다.
- **시스템 글꼴**: 일부 음악 기호를 그릴 때 Apple Symbols를 사용합니다.

## 3. 사용자가 직접 설치한 플러그인

TabViewer는 사용자가 Mac에 설치한 Audio Unit(AUv2/AUv3) 및 VST 3 악기 플러그인으로 악보를 재생할 수 있습니다. TabViewer는 어떤 플러그인, 사운드 라이브러리, 프리셋도 포함·배포·사용 허락하지 않습니다. 각 플러그인과 그 플러그인이 쓰는 음원이나 라이선스 서비스(예: iLok/PACE)에는 오로지 해당 제조사의 라이선스와 개인정보 처리방침이 적용됩니다. 플러그인은 TabViewer 프로세스 안에서 실행되며, 일부는 라이선스 인증 등 자체 목적으로 인터넷에 연결할 수 있습니다.

**Tablarion과의 악보 동기화.** Tablarion은 Guitar Pro 파일을 자체 엔진으로 연주하는 플러그인입니다. TabViewer와 같은 저작자(jayusop)가 만들었으며, GitHub에서 별도로 개발·배포합니다: https://github.com/jayusop/Tablarion

Tablarion을 음원으로 고르면 TabViewer는 열린 악보를 플러그인의 상태에 넣고, DAW처럼 재생 위치와 템포를 전달할 수 있습니다. Tablarion은 자체 저장소에 공개된 고유의 라이선스를 따르는 별개의 프로그램으로, TabViewer에 포함되거나 함께 배포되지 않으며 따로 설치해야 합니다. TabViewer에는 Tablarion이나 그 개발 프레임워크(JUCE)의 코드가 들어 있지 않습니다.

## 4. Guitar Pro 파일 형식

TabViewer는 사용자가 이미 가진 악보 파일을 쓸 수 있도록(상호 운용성) Guitar Pro 파일(`.gp`, `.gpx`, `.gp5`, `.gp4`, `.gp3`)을 열고 `.gp5` 파일로 저장합니다. 읽기·저장 코드는 TabViewer를 위해 독자적으로 작성했으며, Guitar Pro나 그 밖의 어떤 소프트웨어의 코드나 리소스도 포함하지 않습니다.

## 5. 악보 파일

사용자가 열거나 만들거나 내보내는 악보의 권리는 각 권리자에게 있습니다. TabViewer는 악보 파일을 포함하지 않으며, 사용자의 파일에 저작권 문구를 넣지 않습니다. 열거나 공유하는 악보를 사용할 권리가 있는지는 사용자가 책임집니다.

## 6. 상표

- Guitar Pro는 Arobas Music의 상표입니다. TabViewer는 Arobas Music과 제휴하거나 승인·후원을 받지 않았습니다.
- VST는 Steinberg Media Technologies GmbH의 등록 상표입니다.
- Apple, Mac, macOS, Audio Unit, Apple Symbols는 미국 및 기타 국가에 등록된 Apple Inc.의 상표입니다. TabViewer는 Apple Inc.와 관련이 없습니다.
- JUCE 및 그 밖의 제품명과 회사명은 각 소유자의 상표입니다.

상표는 호환성을 설명하는 용도로만 쓰며, 승인을 받았다는 뜻이 아닙니다.

## 7. 소개 웹사이트

TabViewer 웹사이트(`docs/index.html`, GitHub Pages로 제공)는 앱이 아니라 설명서의 일부입니다.

- 글꼴: SIL Open Font License 1.1로 배포되는 Noto Sans KR과 JetBrains Mono를 Google Fonts(fonts.googleapis.com / fonts.gstatic.com)에서 불러오며, 이 저장소에서 재배포하지 않습니다. 사이트를 방문하면 글꼴을 내려받기 위해 브라우저가 Google 서버에 연결합니다.
- README의 배지는 shields.io가 제공하는 이미지입니다.
- 사이트는 GitHub(GitHub Pages)가 호스팅하며 GitHub의 약관과 개인정보 처리방침이 적용됩니다.

## 8. 문의

이 문서에 관한 문의: jayusop@gmail.com · https://github.com/jayusop/Tab-Viewer/issues
