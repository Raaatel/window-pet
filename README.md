# window-pet
windows pet program
# 🐾 Pixel Desktop Pet (픽셀 데스크탑 펫)

> 바탕화면 위를 자유롭게 돌아다니는 다마고치 스타일 픽셀 펫.
> Python 표준 라이브러리(tkinter)만으로 만들어져 **별도 설치 없이** 바로 실행됩니다.

<p align="center">
  <img src="preview_walk.gif" alt="걷기 애니메이션" width="640">
</p>

---

## 📖 소개

**Pixel Desktop Pet**은 투명한 창에 픽셀 아트 동물이 살아 움직이는 데스크탑 위젯입니다.
화면 위를 걸어 다니고, 그루밍을 하고, 졸리면 잠을 자며, 배가 고프면 밥을 달라고 합니다.

직접 도트로 그린 다섯 종류의 동물 중 하나를 골라 키울 수 있으며,
포만감·행복·청결·에너지 네 가지 스탯이 실제 반려동물처럼 시간에 따라 천천히 변합니다.
모든 상태는 자동 저장되어 프로그램을 다시 켜도 이어집니다.

외부 라이브러리·인터넷 연결·계정이 전혀 필요 없는 **단일 파일 프로그램**입니다.

---

## ✨ 주요 기능

### 🐱 다섯 종류의 펫
| 종 | 설명 |
|---|---|
| 강아지 | 골든 리트리버 계열, 늘어진 귀와 말린 꼬리 |
| 고양이 | 블루그레이 단모종 |
| 설 (벵갈) | 로제트 무늬가 있는 벵갈 고양이 |
| 코카투 | 노란 볏을 세우는 유황 앵무, 날 수 있음 |
| 크레스티드 게코 | 속눈썹 볏과 혀로 눈을 핥는 도마뱀 |

### 🎮 다마고치 시스템
- **네 가지 스탯**: 포만감 · 행복 · 청결 · 에너지
- 실제 반려동물처럼 **시간 단위로 천천히** 감소 (배고픔 약 4시간, 청결 약 12시간)
- 스탯이 부족하면 말풍선으로 가끔 표현 (과하게 보채지 않음)
- 모든 상태는 `~/.pixel_pet_save.json`에 **자동 저장**

### 🕹️ 풍부한 애니메이션
걷기 · 대기 · 앉기 · 그루밍 · 기지개 · 식빵 · 잠 · 식사 · 놀이 · 애교 · 하품
(코카투는 비행 동작 추가) — 각 동작이 여러 프레임으로 부드럽게 재생됩니다.

### 🖱️ 상호작용
- **드래그** — 펫을 집어서 원하는 위치로 이동 (놓으면 중력으로 떨어짐)
- **더블클릭** — 쓰다듬기 (하트 이펙트)
- **우클릭 메뉴** — 밥 주기 / 놀아주기 / 씻기기 / 재우기·깨우기 / 상태 보기 / 이름 짓기 / 펫 변경 / 종료

### 💤 자리 비움 감지
- 60초 동안 키보드·마우스 입력이 없으면 **하품**하며 혼잣말
- 240초 이상 지나면 스스로 잠듦
- 다시 컴퓨터를 사용하면 깨어남

---

## 🚀 사용 방법

### 요구 사항
- **Python 3.8 이상** (Windows 권장 — 가장 깔끔한 투명 배경 지원)
- 추가 패키지 설치 **불필요** (tkinter는 Python에 기본 포함)

### 실행
```bash
python desktop_pet.py
```

처음 실행하면 펫이 화면에 나타납니다. 우클릭 메뉴에서 원하는 동물로 바꿀 수 있습니다.

### 스프라이트 데이터 검증 (선택)
```bash
python desktop_pet.py --check
```
스프라이트 데이터의 무결성을 검사합니다.

### 실행 파일(.exe)로 빌드 — Windows
별도의 Python 설치 없이 더블클릭으로 실행되는 단일 실행 파일을 만들 수 있습니다.

```bash
build_exe.bat
```

`build_exe.bat`을 실행하면 자동으로 PyInstaller를 설치하고 `dist/PixelPet.exe`를 생성합니다.
(아이콘으로 `pet.ico`가 사용됩니다.)

---

## 📁 파일 구성

```
desktop_pet.py     메인 프로그램 (단일 파일, 모든 스프라이트 데이터 내장)
build_exe.bat      Windows 실행 파일 빌드 스크립트
pet.ico            애플리케이션 아이콘
preview_walk.gif   걷기 애니메이션 미리보기
preview_idle.gif   대기 애니메이션 미리보기
sprite_sheet_full.png  전체 스프라이트 시트
```

---

## 💾 저장 데이터

펫의 종류·이름·스탯은 사용자 홈 디렉터리의 `.pixel_pet_save.json`에 자동 저장됩니다.
파일을 삭제하면 처음 상태로 초기화됩니다.

---

## 📄 라이선스

이 프로젝트는 [MIT License](LICENSE) 하에 배포됩니다.

```
MIT License

Copyright (c) 2026 <raaatel>

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
```

