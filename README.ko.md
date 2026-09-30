<div align="center">

![WallpaperJS — Your desktop. Your code.](banner.svg)

# WallpaperJS

**HTML · CSS · JavaScript로 만드는 나만의 데스크톱.**

웹으로 만든 장면을 매일의 바탕화면으로.

[![Release](https://img.shields.io/badge/release-v0.1.0_preview-b7a4ef?style=flat-square)](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.0)
![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS-20232b?style=flat-square)
[![License](https://img.shields.io/badge/license-Apache_2.0-bce3ac?style=flat-square)](LICENSE)

[다운로드](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.0) · [English](README.md) · [한국어](README.ko.md) · [문제 신고](https://github.com/aidevksh/WallpaperJS-Releases/issues)

</div>

---

## 내 코드로 채우는 화면

로컬 HTML, CSS, JavaScript 프로젝트를 가져와 실제 바탕화면에서 실행하세요. 짙은 배경과 라벤더 포인트의 관리 화면에서 프로젝트와 디스플레이를 선택하면 됩니다.

- **익숙한 웹 기술** — 직접 만든 웹 프로젝트를 바탕화면으로 사용합니다.
- **여러 화면, 하나의 장면** — 여러 디스플레이에 적용하고, Windows에서는 하나의 넓은 장면으로 이어 표시합니다.
- **작업에 맞춘 재생** — 30·60 FPS 설정과 일시정지를 지원합니다.
- **조용한 백그라운드 실행** — 창을 닫아도 트레이 또는 메뉴 막대에서 계속 실행됩니다.
- **한국어와 영어** — 시스템 언어 또는 원하는 언어를 선택할 수 있습니다.

## 다운로드

**v0.1.0 · 첫 프리릴리즈** — 아래에서 운영체제와 CPU에 맞는 설치 파일을 선택하세요. 기본 바탕화면 카탈로그는 포함하지 않으며, 라이브러리는 빈 상태로 시작합니다.

| 운영체제 | CPU | 설치 파일 |
| --- | --- | --- |
| Windows | Intel / AMD (x64) | [다운로드 .exe](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.0/WallpaperJS-0.1.0-windows-x64.exe) |
| Windows | ARM64 | [다운로드 .exe](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.0/WallpaperJS-0.1.0-windows-arm64.exe) |
| macOS 14.2+ | Apple Silicon (M-series) | [다운로드 .dmg](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.0/WallpaperJS-0.1.0-macos-arm64.dmg) |
| macOS 14.2+ | Intel (x64) | [다운로드 .dmg](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.0/WallpaperJS-0.1.0-macos-x64.dmg) |

[SHA-256 체크섬](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.0/SHA256SUMS.txt) · [릴리즈 노트](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.0)

### 설치 안내

**Windows:** `.exe`를 실행하고 설치 위치를 선택합니다. 이번 빌드는 코드 서명이 없어 SmartScreen 경고가 표시될 수 있습니다.

**macOS:** `.dmg`를 열고 WallpaperJS를 응용 프로그램 폴더로 옮깁니다. 이번 빌드는 Developer ID 서명·Apple 공증을 받지 않았으므로 Gatekeeper가 실행을 차단할 수 있습니다. 다운로드 출처를 확인한 뒤 macOS의 **시스템 설정 → 개인정보 보호 및 보안**에서 차단 안내를 확인하세요. 관리되는 기기에서는 실행이 제한될 수 있습니다.

## 첫 바탕화면 시작하기

1. `wallpaper.json`과 웹 파일이 있는 로컬 프로젝트를 준비합니다.
2. 앱에서 프로젝트 폴더 또는 ZIP을 가져옵니다.
3. 적용할 디스플레이를 선택하고 바탕화면을 적용합니다.
4. Windows에서는 여러 디스플레이를 체크한 뒤 하나의 세트로 이어 표시할 수 있습니다.

창을 닫으면 백그라운드에서 계속 실행됩니다. Windows 알림 영역 또는 macOS 메뉴 막대의 아이콘으로 다시 열고, 메뉴의 **종료**로 앱을 완전히 종료하세요.

## 플랫폼과 알려진 제한

| 기능 | Windows | macOS |
| --- | --- | --- |
| HTML / CSS / JS 바탕화면 | 지원 | 지원 |
| 디스플레이별 적용 | 지원 | 지원 |
| 여러 화면에 걸친 단일 장면 | 디스플레이 세트 | 미지원 |
| 잠금화면 이미지 | 스냅샷 또는 별도 이미지 | 미지원 |
| 한국어 / 영어 | 지원 | 지원 |

- Windows 잠금화면은 **정지 이미지**만 지원하며 장치 정책에 따라 변경이 제한됩니다.
- FPS 설정은 `requestAnimationFrame`에 적용되며 CSS 애니메이션과 동영상에는 적용되지 않습니다. 일시정지 후 재생하면 프로젝트를 다시 불러옵니다.
- Windows 11 x64와 macOS ARM64에서 네이티브 바탕화면 연결을 확인했습니다. 설치 프로그램의 실제 기기 검증, macOS Spaces·Mission Control·다중 디스플레이, Windows 혼합 DPI 세트는 추가 검증이 필요합니다.
- Linux는 지원하지 않습니다.

## 라이선스

WallpaperJS는 [Apache License 2.0](LICENSE)을 따릅니다. 저작권 표시는 [NOTICE](NOTICE), 포함된 의존성의 라이선스는 설치 패키지의 고지 파일에서 확인할 수 있습니다. 사용자가 가져온 바탕화면에는 각 저작자의 라이선스가 적용됩니다.

이 저장소는 공식 다운로드와 배포 안내를 제공합니다. 프로그램 소스는 별도의 비공개 저장소에서 관리합니다.
