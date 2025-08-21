# DesmoSAT — Hardware (2023, KiCad)

소형 위성(캔샛) 하드웨어 설계 저장소입니다. **KiCad 8/9** 기반으로 회로도/PCB, 제조 파일(Gerber), BOM을 포함합니다.

## ✨ 주요 특징
- 모듈 구조: Main MCU · Power · BMS · Navigation(GNSS/IMU) · Environment Sensors · Landing(서보/파이로) · Ground Control Center(지상국 인터페이스)
- 저전력/잡음대책: 전원 트리, 리턴패스/스티칭 비아, 크리티컬 라우팅(50Ω / 100Ω)
- 텔레메트리·페이로드 I/F: UART/SPI/I2C, 확장 커넥터
- 제조 용이성: JLC/PCBWay 표준 스택업 가정, 부품 대치 용이한 풋프린트

## 🗂️ 리포 구성
> 실제 파일명과 맞추어 갱신하세요.


## 🔧 설계 사양(채워넣기)
- **메인 MCU**: [STM32H723/…], 외부 클록 [12 MHz TCXO], 전원 [3.3 V]
- **센서**: [IMU], [Baro], [GNSS], [온습도]
- **통신**: [LoRa 433/868/915], UART[BPS], 지상국 인터페이스[USB/UART-TTL]
- **전력**: 배터리 [LiPo 2S/3S, 용량], 레귤레이터 [PMIC/BUCK/LDO], 보호 회로 [OCP/TVS]
- **기계**: 보드 크기 [mm], 레이어/스택업 [예: 4L 1-1-1-1], 표면 [ENIG/HASL]

## 🧪 DRC/ERC & SI 가이드
- KiCad DRC 룰셋: `docs/drc_rules.kicad_dru` (임피던스/간격 규정 포함)
- 크리티컬 라우팅: SPI 48 MHz, I2C 400 kHz, GNSS 안테나/피드 라인 분리
- 접지: 아날로그·디지털 분리 후 스타 접지, 고속 라인 리턴패스 확보

## 🏭 제조/조립
- `fabrication/` 내 Gerber/Drill 업로드 → 제조사 표준 스택업 선택
- `bom/` BOM 업로드(대체부품 열 포함)
- 조립 도면: `docs/assembly_top.pdf`, `docs/assembly_bot.pdf`

## ✅ bring-up 체크리스트
- 전원 시퀀스/전류 프로파일 측정
- SWD 연결 및 MCU ID 확인
- I2C/SPI 스캔 → 센서 응답 확인
- GNSS Fix, LoRa 링크, Landing 서보 구동

## 📸 자료(추가 부탁)
- 보드 사진(상/하), 조립 전후, 실장 확대
- 오실로/로직애널라이저 파형(SPI/I2C), 전류 측정 로그
- 스택업 캡처, 실험 셋업 사진

## 라이선스
[License TBD]
