# DesmoSAT – 모듈형 캔위성 하드웨어 (2023)

> 모듈화를 통해 **저비용·고유연성**을 달성한 소형 위성 하드웨어 플랫폼  
> 공통 코어 + 교체식 임무 보드 + 착륙 보드 = 빠른 재사용/응용

<!-- 히어로 이미지: 실제 보드 4장(공통, BMS, Custom A, Landing) 나란히 -->
<!-- 파일: docs/images/hero-boards.jpg -->
![DesmoSAT Boards](docs/images/hero-boards.png)

## 개요

DesmoSAT은 하드웨어를 **모듈**로 나눠 비용을 낮추고 임무 확장을 쉽게 만든 캔위성 플랫폼입니다.  
공통 모듈(Common)과 전력/배터리(BMS), 임무 모듈(Custom A/B), 착륙(Landing)을 **CAN 2.0B**로 묶어 필요에 따라 보드만 교체하면 다른 임무로 전환할 수 있습니다.

- 모듈 교체로 **개발 기간 단축 / 비용 절감**
- 공통 인터페이스(전원, 통신, ST-Link)로 **재사용 극대화**
- 데모 임무: **화산 위험 징후 탐지** (가스/분진 + IR/VL + ToF)

> 설계/출력 도구: **KiCad 9.0.x** (회로/PCB), 제조 파일(Gerber) 동봉

---

## 모듈 구조

| 모듈 | 목적(키워드) | 핵심 부품(키워드) |
|---|---|---|
| **Common** | 비행 컴퓨터/통신/센서 허브 | STM32F4, CAN(SN65HVD231), RF(433 MHz 1 W), GPS(MAX-M10S), IMU(BNO085/ICM-20602), Baro(LPS22HB), EEPROM |
| **Battery & BMS** | 전원/충전/안전 관리 | STM32L0, LM2596S 5 V/3.3 V, INA219B(전류), LM324A(셀버퍼), TC427(파워 게이팅), Solar 입력 |
| **Custom A** | 화산 임무용 가스/분진 센싱 | STM32F 계열, SO₂/CO/CO₂/CH₄/TVOC/PM 센서, CAN, TCXO |
| **Custom B** | 방사선 임무(확장) | STM32L0, GDK101(방사선), CAN, TCXO |
| **Landing** | 낙하/착지/추적 | STM32L4, VL53L1X(ToF), IR/VL 카메라 I/F, CDS 트래커, 서보/스테퍼, CAN |
| **Ground Control** | 지상국 수신/표시 | STM32L0, RF(E32-433T30D), FT232RL(USB-UART) |

<!-- 블록 다이어그램(상위 시트) 스크린샷 -->
<!-- 파일: docs/images/block-diagram.png -->
![Block Diagram](docs/images/block-diagram.png)

---

## 데모 임무: 화산 위험 징후 탐지

- **Custom A**: 하강 중 **SO₂/CO/CO₂/CH₄/TVOC/PM** 연속 측정 → 패킷 전송  
- **Landing**: **IR/VL 이미지**로 열점/지형 파악, **ToF**로 지면 거리 → **낙하산 라인 제어**(더 안전/저온 지역으로 착지 유도)  
- **Common**: 착지 후 **IMU 기반 미소진동(지진파) 모니터링**, RF 링크로 지상국에 로그 전송  
- **지상국**: 실시간 그래프/지도화, **베이스라인 데이터 대비 변화량** 분석

<!-- Custom A 보드 사진(센서 라벨 붙여서) -->
<!-- 파일: docs/images/custom-a-board.png -->
![Custom A – Gas/PM Payload](docs/images/custom-a.png)

---

## 시스템 개요

### 통신/제어
- **CAN 2.0B**: 모듈 간 명령·텔레메트리 버스
- **RF 433 MHz 1 W**: 지상국 링크(센서/상태/좌표)
- **ST-Link**: 전 모듈 SWD 디버그/펌웨어 업데이트

### 전원/충전
- **Li-Po 2셀 + BMS**: 저전압 보호/전류 모니터/모듈 파워게이팅
- **스위칭 레귤레이터**: LM2596S-5/-3.3 (효율), 디버그 전원 레일 분리
- **Solar 충전**: 배터리 레벨에 따라 모듈 **절전/복귀** 제어

### 센서/액추에이터
- **가스/분진**: SO₂, CO, CO₂, CH₄, TVOC, PM
- **IMU**: BNO085(9축), ICM-20602(6축)
- **GPS**: MAX-M10S
- **CDS Solar Tracker**: 4-셀 + LM324A 버퍼
- **ToF**: VL53L1X
- **IR/VL 카메라**, **리액션 휠**, **스테퍼(낙하산)**, **서보(패널)**

---

## 하드웨어 갤러리 (이미지 가이드)

> 아래 자리표시자에 **실물 사진/PCB 레이아웃/테스트 셋업**을 추가하세요.  
> 경로는 `docs/images/…`로 통일했습니다.

### Common Module
<!-- 제품 사진(Top/Bottom), PCB 레이아웃(Top), 커넥터 라벨 이미지 -->
<!-- files: docs/images/common-top.jpg, common-bot.jpg, common-pcb.png -->
![Common – Assembled Top](docs/images/common-top.png)
![Common – PCB (Top)](docs/images/common-pcb.png)

### Battery & BMS
<!-- 셀 전압 버퍼/INA219/게이팅 부분 확대, Solar/Charge 포트 클로즈업 -->
<!-- files: docs/images/bms-top.jpg, bms-pcb.png, bms-detail-sense.jpg -->
![BMS – Assembled](docs/images/bms-top.png)
![BMS – PCB](docs/images/bms-pcb.png)

### Custom A (Gas/PM)
<!-- 센서 라벨(화살표/주석), 캘리브레이션 셋업 사진 -->
<!-- files: docs/images/custom-a-top.jpg, custom-a-sensors-labeled.jpg -->
![Custom A – Sensors](docs/images/custom-a-sensors-labeled.png)

### Custom B (Radiation)
<!-- GDK101 연결/실드 처리, 캘리브레이션 셋업 -->
<!-- files: docs/images/custom-b-top.jpg -->
![Custom B – Radiation Payload](docs/images/custom-b-top.png)

### Landing Module
<!-- ToF/IR/VL 커넥터, 서보/스테퍼 드라이브 부분 강조 -->
<!-- files: docs/images/landing-top.jpg, landing-pcb.png -->
![Landing – Assembled](docs/images/landing-top.png)
![Landing – PCB](docs/images/landing-pcb.png)

### Ground Control
<!-- RF 모듈 + USB 연결 예시, GUI 스크린샷(있으면) -->
<!-- files: docs/images/gcs-top.jpg, gcs-gui.png -->
![Ground Control – Assembled](docs/images/gcs-top.png)

---

## 파일/폴더 구조

```text
desmosat-hw-2023/
├─ common_module/        # 메인 MCU, CAN, 센서, RF
├─ battery_bms/          # 배터리/충전/BMS
├─ custom_module_a/      # 가스/분진 페이로드
├─ custom_module_b/      # 방사선 페이로드(옵션)
├─ landing_module/       # 낙하/착륙(서보/스테퍼/ToF/카메라)
├─ ground_control/       # 지상국 MCU + RF + USB
├─ docs/
│  ├─ images/            # README에 쓰일 모든 이미지(.jpg/.png)
│  └─ schematics/        # 회로 캡처(시트별 PNG)
└─ fabrication/          # Gerber/Drill/PnP/Assembly 자료
