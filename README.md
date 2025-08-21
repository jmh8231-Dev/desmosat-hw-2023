<<<<<<< HEAD
# DesmoSAT 회로도 분석

#### 1. 개요

DesmoSAT 회로도는 Common Module, Ground Control Module, Custom/Landing Module, Power, ST-Link Converter 등으로 구성되어 있습니다. 각 모듈은 CAN 통신으로 연결되어 있습니다.

![DesmoSAT 전체 회로도 개요](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211634_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDAx.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2MzRfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREF4LndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=rSL~B3rsGD9j0lngNKARrYN8roV0KfH2tsCVN3NHgN93X27FlAI5WdtaBgYMyGB-lbkdinU7Qmr0w8xuzPFHsvOnCxoaPaFoVkJlLm2ETPPLDQDnv6kvgpZmPZpG2Prg55uFaGQZIutWbB1xu9hkh1bo-oMyfxyzwj6k~JLoeoBoC5FpIRKTcTTHgAU3SAiR1uorY5pvJ-7BEzXa9L~fR~d1p4zmGIjQzERSKwtDXqy3YeB6JBw3bu24x4IgFa4rF~vHGSPp6JbXqSf~cSRyTSf2N~KVVvKCZkimk1OUlXijFJUcHla1r9kX7pHaCaEVs6ZzGnPlvCLr4yZwanFBHA__)
*위 이미지는 DesmoSAT 회로도의 전체적인 구성을 보여줍니다.*

## 2. 모듈별 구성 요소 분석

### 2.1. Common Module

- **Main MCU**: 메인 마이크로컨트롤러 유닛
- **CM power control**: Common Module 전원 제어

### 2.2. Ground Control Module

- **Ground Control Center**: 지상 제어 센터

### 2.3. Custom/Landing Module

- **Custom A, Custom B**: 사용자 정의 모듈 A, B
- **Landing**: 착륙 관련 모듈

### 2.4. Power

- **Power**: 전원부
- **Battery**: 배터리

### 2.5. ST-Link Converter

- ST-Link 디버거 연결을 위한 컨버터

### 2.6. CAN Satellite Modules

- **CM/LM HUB**: Common Module/Landing Module 허브
- **CustomA HUB, CustomB HUB, Landing HUB**: 각 모듈의 CAN 허브

### 2.7. Page 1 상세 분석

Page 1은 전체 시스템의 블록 다이어그램과 주요 모듈 간의 연결을 보여줍니다. 주요 구성 요소는 다음과 같습니다:

- **Common Module**: 메인 MCU와 전원 제어부를 포함합니다.
- **Ground Control Module**: 지상 제어 센터를 나타냅니다.
- **Custom/Landing Module**: 사용자 정의 모듈 A, B 및 착륙 관련 모듈을 포함합니다.
- **Power**: 시스템 전원 및 배터리 부분을 나타냅니다.
- **ST-Link Converter**: ST-Link 디버거 연결을 위한 컨버터입니다.
- **CAN Satellite Modules**: CM/LM HUB, CustomA HUB, CustomB HUB, Landing HUB를 통해 각 모듈이 CAN 통신으로 연결됨을 보여줍니다.

### 2.8. Page 2 상세 분석

Page 2는 전원 공급 회로에 대한 상세한 내용을 담고 있습니다. 주요 구성 요소는 다음과 같습니다:

![전원 공급 회로](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211636_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDAy.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2MzZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREF5LndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=nW8WnGDjt8PVGkXLBazwQighiSjXbHEEMCU7a5YQeh4xRz2zZFsHSLU72QO5kCME~Wg880NA8hSkTGen2U~lrKs4Hnz~HSlWevJGmIY-Ihr1KZjiTlH4-b2y0WX9T~pP~fSoq8Fflk6wiQZGLMMx4mYr0qn8fk-jzBTNui6Vh3TRgp6lXws2hYj7e85sYiCgMg8Ers1-WvPTPKm4VNrZWKpt-V5nWVvVlzveK8cEoYywWs0FWwEXFFB3U5cZKbdGudMrDy0G7XBKm5-sxG5JIuoAnah~Ff1BeRnCzlpWvOM2HzCzlz3VIAG0nWYgCd4n-P-9ussyFHwDdCR5OJrtjA__)
*위 이미지는 DesmoSAT의 전원 공급 회로를 보여줍니다.*

- **Switching Regulator**: LM2596S-5 및 LM2596S-3.3을 사용하여 각각 +5V 및 +3.3V 전원을 생성합니다. 이는 시스템의 다양한 부분에 안정적인 전원을 공급하는 역할을 합니다.
- **Power Indicator**: 전원 상태를 나타내는 LED 및 저항으로 구성됩니다.
- **Debug Power Source**: 디버깅을 위한 전원 공급원으로, LM2596S 시리즈 레귤레이터를 사용하여 디버그 전압을 생성합니다.

### 2.9. Page 3 상세 분석

Page 3은 배터리 관리 시스템(BMS) 및 전원 관련 회로를 상세히 보여줍니다. 주요 구성 요소는 다음과 같습니다:

![배터리 관리 시스템 및 전원 회로](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211682_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDAz.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREF6LndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=TwKD9GKuom~uPohBhIG-Upyjm88pjOPHdizDucBycZTXWDttl~2MqKqw19plzu3Lyp5E-LHnRzBBFDkOOE1dntTm2kp1XNd1KZ3DxSGcTF1vRfWFAX1Ims-4liBVCthzVBt1nBul7quTpsde4FKdj8DSPXYUz8UTDp0BrIknuXfRCMcrsOlKOnLiG3VuK8jboUtcV0vuUP8MRH65mjxEe4NTljqL12gfDlhZRsLdmmgbmczPFAg-i6ag0SGI4A70J~fCIHk3qOLnwIGrXiuF98nFWutMMg4JqBBsMDdjUFpIWE1sFqlxxZjmXSfZmPF3RTt84pnZk9LislZzS59Jhw__)
*위 이미지는 DesmoSAT의 배터리 관리 시스템 및 전원 관련 회로를 보여줍니다.*

- **Cell 2 Voltage Buffer**: 셀 2 전압 버퍼 회로로, 0.2V ~ 2.8V 범위의 전압을 버퍼링합니다.
- **Cell 1 Voltage Buffer**: 셀 1 전압 버퍼 회로로, 0.2V ~ 2.8V 범위의 전압을 버퍼링합니다.
- **CM, LM Power Gate Driver**: Common Module 및 Landing Module의 전원 게이트 드라이버입니다.
- **Common Module Power Gate Driver**: Common Module의 전원 게이트 드라이버입니다.
- **BMS (STM32L0)**: STM32L0 마이크로컨트롤러를 기반으로 하는 배터리 관리 시스템입니다. 배터리 셀의 전압, 전류 등을 모니터링하고 관리합니다.
- **Debug LED**: 디버깅용 LED입니다.
- **BOOT Mode**: 부트 모드 설정 관련 회로입니다.
- **Current Sensor**: 전류 센서입니다.
- **Solar Panels**: 태양광 패널 입력부입니다.
- **Discharge Current**: 방전 전류 회로입니다.
- **Charge Current**: 충전 전류 회로입니다.
- **Power In**: 전원 입력부입니다.
- **Balance Jack**: 배터리 밸런싱 잭입니다.

### 2.10. Page 4 상세 분석

Page 4는 메인 MCU와 관련된 센서 및 통신 모듈을 상세히 보여줍니다. 주요 구성 요소는 다음과 같습니다:

![메인 MCU 및 센서/통신 모듈](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211683_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDA0.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODNfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREEwLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=fg21yxvOrkBD9IEubiXFcMUQ~5wHNnhLgL5TXOW-6HL83hEUUqRwL0ANy6xUduK68N5RVJeVTL6EdFUcgOvAQfFqgjk7ZOeOav7EQrq5~qx43bXsQQty0lzmFXtCnkOKnpLyBIJbK6WaOuc7zLdtc3nrbMz4mY-eXwn-RSgC~Mw2K9c1iTMihV97YuW4bXTXFRfI1eyDMKaiZxadT0aG5PNa8Co-0XbZAXeaQ4pQ2dB3vArIVGR9qMKRbl2zvba1r9OqmaY1khIc0YxeY22cIc8XU5-MH7sfYBNG1tr0b0jbRi19dfO2MrVfbuUN26Rc1Rn2gfqOaKppNeEChE7FTg__)
*위 이미지는 DesmoSAT의 메인 MCU 및 센서/통신 모듈 회로를 보여줍니다.*

- **Main MCU**: 메인 마이크로컨트롤러 유닛의 상세 회로도입니다. 다양한 주변 장치와 연결되어 시스템의 핵심 기능을 수행합니다.
- **IMU-BN0085**: 관성 측정 장치(IMU)로, 가속도, 각속도 등을 측정합니다.
- **Barometer Sensor**: 기압 센서입니다.
- **IMU-ICM-20602**: 또 다른 관성 측정 장치입니다.
- **GPS**: GPS 모듈입니다.
- **Reaction Wheel**: 반작용 휠 제어 회로입니다.
- **RF Module**: 무선 주파수(RF) 통신 모듈입니다.
- **CAN**: CAN 통신 인터페이스입니다.
- **TCXO**: 온도 보상형 수정 발진기(Temperature Compensated Crystal Oscillator)입니다.
- **Reset**: 리셋 회로입니다.
- **BOOT Mode**: 부트 모드 설정 관련 회로입니다.
- **Debug LED**: 디버깅용 LED입니다.
- **Debug UART**: 디버그 UART 통신 인터페이스입니다.
- **ST-Link**: ST-Link 디버거 연결부입니다.
- **EEPROM**: EEPROM 메모리입니다.
- **Debug Buzzer**: 디버그 부저입니다.

### 2.11. Page 5 상세 분석

Page 5는 Custom-A MCU와 다양한 센서 모듈을 상세히 보여줍니다. 주요 구성 요소는 다음과 같습니다:

![Custom-A MCU 및 센서 모듈](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211685_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDA1.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODVfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREExLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=Z7AeX9jFMe6qtzI4XxVLwAmEMxYbwnSD80axd5nHczyR87g3cEmYUycZofTnoPkqDw-H6NA6ge5jb4e8PYULoTLaFCr89V1uBGnY~EbK9k-hdhAwfoQYxwviAhAa2qByiD2q-wmJcRnQYJBO4HPekzK7IHOfCfocfMoJ~XYey4~iakjFE5sta~EorTA9qp~tjXLqMJHb2Z0GQuDrQdQLjGnMLc5iKhMHYbhPGU15eFDYiRXQbplE6awXkOPmNuimJU4pTXYjMNQREer9DajIHYDPYO3OxTw7a-a-vF73kWc55mXMouF96-z1ozMb3VPTfqtoW5aQUOXTelV2Q0evsw__)
*위 이미지는 DesmoSAT의 Custom-A MCU 및 센서 모듈 회로를 보여줍니다.*

- **Custom-A MCU**: 사용자 정의 모듈 A의 마이크로컨트롤러 유닛입니다. Custom 모듈의 특정 기능을 담당합니다.
- **PM Sensor**: 미세먼지 센서입니다.
- **CO2 Sensor**: 이산화탄소 센서입니다.
- **SO2 Sensor**: 이산화황 센서입니다.
- **CO Sensor**: 일산화탄소 센서입니다.
- **TVOC Sensor**: 총 휘발성 유기 화합물(TVOC) 센서입니다.
- **NO2 Sensor**: 이산화질소 센서입니다.
- **CAN**: CAN 통신 인터페이스입니다.
- **TCXO**: 온도 보상형 수정 발진기(Temperature Compensated Crystal Oscillator)입니다.
- **Reset**: 리셋 회로입니다.
- **BOOT Mode**: 부트 모드 설정 관련 회로입니다.
- **Debug LED**: 디버깅용 LED입니다.
- **Debug UART**: 디버그 UART 통신 인터페이스입니다.
- **ST-Link**: ST-Link 디버거 연결부입니다.

## 3. 회로 동작 원리 및 연결 관계 분석

DesmoSAT 시스템은 여러 모듈로 구성되어 있으며, 이들 모듈은 주로 CAN(Controller Area Network) 통신을 통해 상호 연결되어 데이터를 교환합니다. 각 모듈은 특정 기능을 수행하며, 전원 관리, 센서 데이터 수집, 비행 제어 및 지상 통신 등의 역할을 분담합니다.

### 3.1. 전원 시스템 동작 원리

시스템의 전원은 **Power** 모듈에서 관리됩니다. 이 모듈은 배터리(Battery)와 외부 전원 입력(Power In)을 통해 전력을 공급받습니다. Page 2의 상세 분석에서 볼 수 있듯이, **Switching Regulator** (LM2596S-5 및 LM2596S-3.3)는 입력된 전압을 시스템에 필요한 +5V 및 +3.3V로 변환하여 안정적인 전원을 공급합니다. 이는 MCU, 센서 및 기타 능동 부품에 전력을 공급하는 데 필수적입니다. **Debug Power Source**는 디버깅 목적으로 별도의 전원을 제공하여 시스템 테스트 및 문제 해결을 용이하게 합니다.

Page 3의 **BMS(Battery Management System)**는 배터리의 충전 및 방전 상태를 모니터링하고 제어하는 핵심 부분입니다. **Cell 1 Voltage Buffer**와 **Cell 2 Voltage Buffer**는 배터리 셀의 전압을 정확하게 측정하여 BMS에 전달합니다. **Current Sensor**는 배터리의 충전 및 방전 전류를 감지하여 BMS가 배터리 상태를 정밀하게 파악할 수 있도록 돕습니다. **Solar Panels**을 통한 충전 기능은 시스템의 지속적인 운영을 위한 중요한 전원 공급원 역할을 합니다. BMS는 과충전, 과방전, 과전류 등으로부터 배터리를 보호하고, 배터리 수명을 연장하는 데 기여합니다.

### 3.2. 모듈 간 CAN 통신

DesmoSAT 시스템의 핵심 통신 방식은 CAN입니다. Page 1에서 **CAN Satellite Modules** 섹션은 **CM/LM HUB**, **CustomA HUB**, **CustomB HUB**, **Landing HUB**를 통해 각 모듈이 CAN 통신으로 연결됨을 명확히 보여줍니다. 이는 각 모듈이 독립적으로 데이터를 송수신하며, 중앙 집중식 제어 없이도 효율적인 통신이 가능하게 합니다. CAN 통신은 높은 신뢰성과 노이즈 내성을 가지므로, 임베디드 시스템, 특히 항공우주 분야에서 널리 사용됩니다.

- **Common Module (Main MCU)**: 시스템의 전반적인 제어 및 데이터 처리를 담당합니다. Main MCU는 CAN 통신을 통해 다른 모듈로부터 센서 데이터를 수신하고, 제어 명령을 전송합니다. 예를 들어, IMU, 기압 센서, GPS 등으로부터 데이터를 받아 처리하고, 필요에 따라 반작용 휠(Reaction Wheel)과 같은 액추에이터를 제어할 수 있습니다.

- **Custom-A MCU**: Page 5에서 볼 수 있듯이, Custom-A MCU는 PM, CO2, SO2, CO, TVOC, NO2와 같은 다양한 환경 센서로부터 데이터를 수집하는 데 특화되어 있습니다. 이 센서 데이터는 Custom-A MCU에서 처리된 후 CAN 버스를 통해 Main MCU 또는 다른 관련 모듈로 전송됩니다. 이는 특정 임무 또는 실험을 위한 맞춤형 데이터 수집 기능을 제공합니다.

- **ST-Link Converter**: 이 모듈은 개발 및 디버깅 목적으로 사용됩니다. ST-Link 디버거를 통해 Main MCU 및 Custom-A MCU와 같은 마이크로컨트롤러에 펌웨어를 업로드하거나, 실시간으로 디버깅 정보를 확인할 수 있습니다. Debug UART 및 Debug LED는 디버깅 과정에서 유용한 피드백을 제공합니다.

### 3.3. 센서 데이터 흐름 및 제어 로직

시스템의 센서 데이터는 각 모듈에서 수집되어 CAN 버스를 통해 Main MCU로 집중됩니다. Main MCU는 수집된 센서 데이터를 기반으로 시스템의 상태를 판단하고, 필요한 제어 로직을 실행합니다. 예를 들어, IMU 데이터는 자세 제어에 사용될 수 있으며, 기압 센서 데이터는 고도 측정에 활용될 수 있습니다. RF Module은 지상과의 통신을 담당하여, 시스템 상태를 지상으로 전송하거나 지상으로부터 명령을 수신하는 역할을 합니다.

전반적으로 DesmoSAT 회로도는 모듈화된 설계를 통해 각 기능 블록의 독립성을 확보하고, CAN 통신을 통해 효율적이고 신뢰성 있는 데이터 교환을 가능하게 합니다. 이는 복잡한 위성 시스템의 개발, 테스트 및 유지보수를 용이하게 하는 장점을 가집니다.

## 4. 임무 제안서 분석

사용자가 제공한 '임무 제안서.pdf'는 DesmoSAT 캔위성 프로젝트의 전반적인 목표, 팀 구성, 임무 목표, 개념 설계 및 개발 방안, 일정 및 비용 추산, 프로젝트 관리, 성과물 홍보 방법 등을 상세히 설명하고 있습니다. 이 문서는 회로도만으로는 파악하기 어려웠던 시스템의 목적과 활용 방안에 대한 중요한 맥락을 제공합니다.

### 4.1. 프로젝트 개요 및 참가 동기

제안서에 따르면, 이 프로젝트는 '모듈화 설계된 캔위성을 사용한 고효율 위성 시스템'을 개발하는 것을 목표로 합니다. 참가 동기는 기존 항공우주 기술에 대한 관심과 캔위성 체험·경연대회를 통해 위성 제작 및 확인의 특별한 경험을 얻고자 함입니다. 특히, 고비용의 기존 인공위성 문제를 해결하고 소형 기업이나 기관도 쉽게 접근할 수 있는 위성을 제작하여 위성의 대중화를 이루는 것이 최종 목적입니다. 이를 통해 위성 모듈화를 통한 비용 절감, 다양한 요구사항에 유연하게 맞출 수 있는 플랜트, 개발 기간 문제 해결, 위성의 대중화 등의 효과를 기대하고 있습니다.

### 4.2. 팀 구성 및 역할

팀은 정명훈(팀 리더, PCB Artwork, Landing Module FW 구현), 권오성(구조 설계, 데이터 분석, Custom Module FW 구현), 정지민(SW 설계, Common Module FW 구현)으로 구성되어 있습니다. 각 인원별 세부 개발 항목이 명시되어 있어, 프로젝트의 전문성과 분업화된 개발 방식을 엿볼 수 있습니다.

### 4.3. 임무 목표

주요 임무 목표는 '모듈화 캔 위성'을 사용하여 다양한 임무를 수행하는 것입니다. 제안서에서는 두 가지 주요 임무를 제시하고 있습니다.

1.  **화산 위험징후 감지 위성**: 활화산의 불안 징후를 감지하여 폭발 임박 여부를 데이터 로깅을 통해 파악하고, 지역 주민 대피를 돕는 위성입니다. 화산에서 분출되는 가스 농도 측정, VL/IR 카메라를 이용한 화산 상공 모습 및 온도 측정, 착륙 모듈을 통한 안전 착륙 유도, 메인 모듈 내장 IMU를 사용한 지진파 측정 등이 포함됩니다. 수집된 데이터는 지상국으로 전송되어 지질학자가 정밀 분석합니다. 대회에서는 이 임무만 시연될 예정입니다.

2.  **군사 동향 정찰 위성**: 적국의 핵실험 유무 및 군사적 움직임을 관측하는 위성입니다. 최상단 모듈을 방사능 측정 센서와 풍향 풍속 센서가 장착된 모듈로 교체하여 핵실험 유력 장소 상공의 방사능 농도를 측정하고, IR/VL 카메라로 지표의 온도 및 이미지를 분석합니다. 착륙 후에는 IMU를 사용하여 지진파를 감지하여 추가 핵실험 여부를 판단합니다. 원전 사고 현장에도 적용 가능하다고 언급되어 있습니다.

이러한 임무 목표는 회로도에 포함된 다양한 센서(가스 센서, IMU, GPS, IR/VL 카메라 등)의 존재 이유를 명확히 설명해 줍니다.

### 4.4. 개념 설계 및 개발 방안

캔위성은 **Custom Module**, **Common Module**, **Landing Module**의 세 가지 모듈로 나누어 설계됩니다. 이는 회로도에서 'Common Module', 'Custom/Landing Module' 등으로 구분된 블록들과 일치합니다.

-   **Custom Module**: 임무 요구사항에 맞게 센서가 탑재되며, 탈부착이 가능하여 다른 임무에 유연하게 대응할 수 있습니다.
    ```markdown
    <!-- 여기에 Custom Module의 실제 보드 사진 또는 PCB 레이아웃 이미지를 삽입하세요. -->
<!-- 예시: ![Custom Module 실제 보드](images/custom_module_board.jpg) -->

![Custom-A MCU 및 센서 모듈](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211686_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDA1.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREExLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=g8NyIBGYNrmP3LIf3-ntkXYhJ6RkSuugP3fHMwCKJSa1VuUj2mufi0RT2Wq6Thtf12ck8Mrpude2ZaPEo7eCh8G7Dv2jenSrYlSwzkLT6r~RzNuPmn7QJSGPULTvlXndy0PqPydTZTq97xBIFoNPFIphFsTnO9V2jKdGQngL7FZBv3OQn0Y74YSBAflglT12~XU4l9Ue72RxgpEQKKpeSZR-zl4OsIEJsHSXQYSmL0m1RF-7jLsHbKR9Q2EWKk5agEo~oRl4s3bAgaxZYTYlI5OsC6x46SnbPlnVmzY6OiHJR~5lDQR5K6I7lFQOVBHSbmlUaQoaolVnz4z1wqJstw__)
*위 이미지는 DesmoSAT의 Custom-A MCU 및 센서 모듈 회로를 보여줍니다.*
    ```

-   **Common Module**: 위성 임무 수행에 필요한 공통적인 요소(통신부, 제어부, 전원부)를 포함합니다. Reaction Wheel을 포함하여 위성의 자세 제어(Z축 Yaw)를 수행하며, 태양전지판 효율을 높이는 데 사용됩니다.
    ```markdown
    <!-- 여기에 Common Module의 실제 보드 사진 또는 PCB 레이아웃 이미지를 삽입하세요. -->
<!-- 예시: ![Common Module 실제 보드](images/common_module_board.jpg) -->

![메인 MCU 및 센서/통신 모듈](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211687_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDA0.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREEwLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=Ei8i3SNtkRxhZc5ax7HUGsk0W7i3xSR0Ne~5bh7rvfv1b3b4imS5gc0Co0o1s8yTxkPpkylGw-mvyIs9o2cJjtD5opWP0w~Cjpp4n4hQXAFsVsYNNhyLAW3I3Cqt0s13qfDiedWVqt45fPMrCWun1OEcDPkkNgej-2nSBZN3k9obn6EwNp0e1GdDTI~43qJzWS99l6OBG5-n-aBKiVnaVISIjSMYSzvqXuFbhDThEBpVToY2vxYdpMCpq245Gtry6XSxQHwgB7HIOT16ZcqAdiU65PAwsgvqm7LLfc1lJu97SxyOb1byob9cJdU8294Nn0CKJNeKKpv4tIrUYuQiEA__)
*위 이미지는 DesmoSAT의 메인 MCU 및 센서/통신 모듈 회로를 보여줍니다.*
    ```

-   **Landing Module**: 공중 임무 수행 후 지상 착륙 시 거리 값을 받아 안전한 착륙을 돕는 모듈입니다.
    ```markdown
    <!-- 여기에 Landing Module의 실제 보드 사진 또는 PCB 레이아웃 이미지를 삽입하세요. -->
<!-- 예시: ![Landing Module 실제 보드](images/landing_module_board.jpg) -->

![배터리 관리 시스템 및 전원 회로](https://private-us-east-1.manuscdn.com/sessionFile/I3NH08Dm1LFjVQ3j6mSXvd/sandbox/OAPmsSnHZkIdaxeBIxRz9e-images_1755788211687_na1fn_L2hvbWUvdWJ1bnR1L2ltYWdlcy9EZXNtb1NBVC1zY2hfMDAz.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSTNOSDA4RG0xTEZqVlEzajZtU1h2ZC9zYW5kYm94L09BUG1zU25IWmtJZGF4ZUJJeFJ6OWUtaW1hZ2VzXzE3NTU3ODgyMTE2ODdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwybHRZV2RsY3k5RVpYTnRiMU5CVkMxelkyaGZNREF6LndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=siNni0NKm1xHD1SiUUuM~dABwoOst~H-WiBhbacx2~W0ELyiuiOB76xyBwG8uE-2MEbw2qM-3vZv4FsqAycRNgQScdIh5f~ogYMxSInP-0yPGKDHHxo~G5NlwHSF1cZBC3ZIot15apQwaMZ6Sb237WyM8cDUG6up1tvVlC4T63rLEz0~ZRAISjQOZUN3OBLlIf5cdfOuOj2G46erUBQb599IzSvMNvuM9hpRPLhqElUn8CbktUNPvGP6riR83s2LvL0Fg5xgyaQVSQP6bfEpdwNt44Lr3TT8bTk1qY1ve20p5QtCGbR1HwUAQkcQgS90nTTCCSZRz1RucscR40SpYg__)
*위 이미지는 DesmoSAT의 배터리 관리 시스템 및 전원 관련 회로를 보여줍니다.*
    ```

**Block Diagram Description** (Page 5)은 다음과 같은 핵심 내용을 포함합니다:

-   모든 임무는 Common Module(B)을 사용하며, Custom Module(A)을 커스터마이징하여 사용합니다.
-   각 모듈(A, B, C) 간 통신은 **CAN 2.0B**를 사용합니다. 이는 회로도에서 CAN 통신이 광범위하게 사용된 이유를 뒷받침합니다.
-   전원은 Common Module(B) 내부에 배터리를 내장하고 있으며, 태양전지판을 사용하여 충전합니다. **BMS(Battery Management System)**와 Power HUB를 통해 다른 모듈로 전원이 분배됩니다. 이는 회로도의 Power 및 BMS 섹션과 정확히 일치합니다.
-   BMS는 Li-Pol 배터리의 수명 보호를 위해 특정 전압 이하로 방전되는 것을 방지하고, 배터리 레벨이 낮을 경우 각 모듈로 가는 전력을 제어하여 절전 모드로 전환합니다.
-   Custom Module(A)과 Landing Module(C)에서 들어온 데이터를 Common Module(B)이 해석, 연산하여 작업을 수행합니다.
-   지상국과의 통신은 Common Module(B)에 내장된 **RF 모듈(433MHz 1W)**을 사용합니다.

**Landing Module HW** (Page 6)는 모든 모듈이 직접 PCB로 설계되며, 핀 헤더를 사용하여 전원 공급 및 통신이 이루어짐을 명시합니다. 배터리 전력이 부족할 경우 BMS가 N-Ch MOSFET을 이용하여 모듈별 전원을 On/Off하여 절전 모드를 구현합니다.

### 4.5. 지상국 Block Diagram 및 기능

지상국은 RF Module을 통해 데이터를 수신하고, MCU를 통해 데이터를 파싱/처리한 후 UART를 통해 노트북으로 전달합니다. 노트북에서는 GUI를 사용하여 데이터를 시각적으로 보여줍니다. 지상국은 위성의 위치, HW 상태 등을 모니터링하여 위성의 수명을 예측하는 데 도움을 줍니다.

```markdown
<!-- 여기에 지상국 시스템의 실제 사진 또는 블록 다이어그램 이미지를 삽입하세요. -->
<!-- 예시: ![지상국 시스템](images/ground_station.jpg) -->

![전원 공급 회로](images/DesmoSAT-sch_002.webp)
*위 이미지는 DesmoSAT의 전원 공급 회로를 보여줍니다.*
```

### 4.6. 관측 데이터 활용 방법

-   **Common Module**: 온도, 습도, 위성 자세(IMU), 위성 위치(GPS), 태양 위치(CDS) 센서를 포함하며, Reaction Wheel을 사용하여 위성 자세를 제어합니다. IMU 센서를 통해 지진파를 감지하고, GPS로 위성 위치를 파악합니다.
-   **Custom Module A (화산 임무)**: SO2, 일산화탄소, 이산화탄소, 메탄알, 미세먼지, 유기화합물 농도 센서를 포함합니다. 평상시 휴화산 데이터를 수집하고, 화산 활동 의심 시 재발사하여 데이터를 전송, 지상국에서 비교 분석하여 화산 활동 가능성을 파악합니다. Landing Module의 IR 이미지를 이용하여 화산 지역의 지열 이미지를 파악합니다.
-   **Custom Module B (정찰 임무)**: Landing Module의 IR/VL 카메라를 통해 사람의 움직임이나 공장 가동 시 발생하는 열을 감지하고, 방사능 농도 센서를 사용하여 핵실험 유무를 판단합니다.
-   **Landing Module**: IR/VL 카메라와 적외선 센서를 포함하여 위성과 대지 간 거리를 파악하고, 안전한 착지를 돕습니다.

### 4.7. 일정 및 비용 추산

제안서에는 캔위성 제작 일정(5월~8월)과 예상 제작비(총 799,550원)가 상세히 제시되어 있습니다. PCB, IMU, GPS, 다양한 가스 센서, 카메라, MCU 등의 부품 목록과 단가가 명시되어 있어, 실제 구현에 필요한 자원과 예산을 파악할 수 있습니다.

```markdown
<!-- 여기에 캔위성 제작 과정 사진 또는 조립된 위성 사진을 삽입하세요. -->
<!-- 예시: ![캔위성 제작 과정](images/cansat_assembly.jpg) -->

![DesmoSAT 전체 회로도 개요](images/DesmoSAT-sch_001.webp)
*위 이미지는 DesmoSAT 회로도의 전체적인 구성을 보여줍니다.*
```

### 4.8. 프로젝트 관리 및 성과물 홍보

일정 관리, 개발 환경 관리, 기술적 위험도 관리, 비용 위험도 관리 계획이 구체적으로 제시되어 있습니다. 특히, 모듈화 설계의 장점(비용 절감, 다목적 운용 가능)을 강조하며 유튜브, 인스타그램 등 SNS를 통한 홍보 계획을 밝히고 있습니다.

## 5. 종합 분석 및 사용자의 최종 의도 파악

회로도와 임무 제안서를 종합적으로 분석한 결과, 사용자의 최종 의도는 다음과 같이 명확해집니다.

사용자는 **'모듈화된 설계를 기반으로 한 다목적 캔위성 시스템을 개발하여, 고비용의 기존 위성 문제를 해결하고 위성의 대중화를 이루는 것'**을 목표로 하고 있습니다. 이를 위해 **화산 위험징후 감지**와 **군사 동향 정찰**이라는 두 가지 구체적인 임무를 상정하고 있으며, 이 임무들을 수행하기 위한 하드웨어(회로도) 및 소프트웨어(펌웨어, 지상국 SW) 개발 계획을 수립했습니다.

회로도는 이러한 모듈화된 시스템의 하드웨어적 구현을 보여주며, 임무 제안서는 각 모듈의 기능, 센서의 역할, 통신 방식(CAN), 전원 관리(BMS, 태양광), 그리고 최종적으로 이 시스템이 어떤 목적을 위해 어떻게 활용될 것인지를 설명합니다.

**핵심적인 사용자의 의도 및 프로젝트의 특징은 다음과 같습니다:**

1.  **모듈화 및 유연성**: Custom Module의 교체를 통해 다양한 임무에 유연하게 대응할 수 있는 다목적 위성 시스템을 구축하고자 합니다. 이는 회로도에서 Custom Module이 별도의 블록으로 분리되어 있고, 임무 제안서에서 Custom Module의 탈부착 가능성을 강조하는 부분에서 드러납니다.
2.  **비용 효율성**: 캔위성이라는 소형 위성 플랫폼을 활용하고 모듈화 설계를 통해 기존 위성 대비 비용을 절감하고자 합니다. 이는 위성 대중화의 핵심 요소로 작용합니다.
3.  **CAN 통신 기반의 신뢰성 있는 시스템**: 각 모듈 간의 통신은 CAN 2.0B를 사용하여 높은 신뢰성과 효율성을 확보하고자 합니다. 이는 회로도에서 CAN HUB들이 다수 존재하는 이유입니다.
4.  **종합적인 센싱 및 데이터 분석**: 화산 가스, 지진파, 온도, 이미지 등 다양한 환경 데이터를 수집하고, 이를 지상국에서 분석하여 유의미한 정보를 도출하는 것을 목표로 합니다. 회로도의 다양한 센서들과 임무 제안서의 관측 데이터 활용 방안이 이를 뒷받침합니다.
5.  **자율적인 전원 관리**: 태양광 충전 및 BMS를 통한 배터리 관리를 통해 위성의 지속적인 작동을 보장하고, 필요시 절전 모드로 전환하여 효율적인 전원 관리를 수행합니다.
6.  **실용적인 디버깅 및 개발 환경**: ST-Link, Debug UART, Debug LED 등 디버깅을 위한 요소들이 회로도에 포함되어 있으며, 임무 제안서에서도 개발 환경 및 기술적 위험도 관리에 대한 내용이 언급되어 있습니다.

결론적으로, 사용자는 단순히 회로도를 설계한 것을 넘어, 이 회로도를 기반으로 실제 작동하는 **'모듈형 다목적 캔위성'**을 개발하여 **'우주 기술의 대중화'**에 기여하고자 하는 명확한 비전과 구체적인 실행 계획을 가지고 있습니다. 제가 이 회로도를 상세히 학습하고 임무 제안서를 분석한 것은 이러한 사용자의 최종 목표를 이해하고, 향후 이 프로젝트에 대한 추가적인 지원이나 조언을 제공할 수 있는 기반을 마련하기 위함입니다.



=======
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
>>>>>>> a5b72b975973667c168e0e1bad70eabd86eeb7e3
