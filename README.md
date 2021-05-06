# Awesome CAN(Controller Area Network) (DevGun) 🇰🇷

<p align="center">
    <img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg"/>
</p>
<br/>

## Table of Contents

- OBD (On Board Diagnostics)
- ECU (Electronic Control Unit)
- Reference Paper
  - (2021) WINDS_A Wavelet-Based Intrusion Detection System for Controller Area Network (CAN)

<br/>

<br/>

## # OBD (On Board Diagnostics)

>https://m.blog.naver.com/suresofttech/221282372396

OBD(On Board Diagnostics)란 자동차의 전기/전자적인 작동 상태를 확인하고 제어하기 위한 진단 규격으로 배출가스와 관련된 시스템을 감시하고, ECU에 정보를 저장하여 배출가스에 영향을 주는 고장이 발생했을 경우, 고장코드를 기록하고 클러스터에 경고등을 점등하여 차량 운전자 및 정비자가 문제를 인식하고 진단을 할 수 있도록 만든 시스템이다.

OBD가 배기와 관련된 시스템과 부품들에 대한 중요한 정보를 제공했지만, OBD 도입 당시(1988)의 기술적 한계로 포함되지 못한 항목들이 있다.

그 후 기술 발전에 의하여 진단 할 수 있는 범위가 넓어지면서 CARB(California Air Resource Board) 주도하에 더 포괄적인 OBD 법규가 제정되었다.

OBD 표준은 그 후 보완을 거쳐 OBD-Ⅱ라는 이름을 가진 현재의 표준으로 발전하게 되었다.

OBD-Ⅱ 규정에서는 DLC(Data Link Cable) 커넥터와 통신사양, 전자제어 부품의 용어와 고장코드를 표준화시킴으로써 보다 호환성을 높였고, 고장발생시 배출가스가 증가되는 항목에 대한 고장 판정기준과 진단 요령이 추가되어 개정되었다.

현재의 OBD-Ⅱ 시스템은 자동차의 배출가스 규제는 물론 고장 진단 시스템으로 사용되고 있으며, 대략적인 OBD-Ⅱ의 점검 항목 및 과정은 다음 그림과 같다.

<p align="center">
    <img src="README.assets/obd1.png"/>
    <div align="center">OBD-Ⅱ 의 점검 항목 및 과정</div>
</p>

<br/>

<br/>

## # ECU (Electronic Control Unit)

> https://www.mk.co.kr/news/business/view/2017/12/817633/

엔진제어유닛(engine control unit, ECU) 또는 엔진제어모듈(engine control module, ECM)은 엔진의 내부적인 동작을 다양하게 제어하는 임베디드 장치이다.

가장 단순한 ECU는 SI 엔진(Spark Ignition)의 폭발시에 실린더의 연료분사량을 제어하는데 사용되며, 현대의 대부분 자동차에 탑재된 좀 더 복잡한 형태의 ECU는 점화 시기, 가변 벨브 타이밍, 터보차저에서 조절하는 부스터 레벨, 기타 주변장치 등을 제어하는데 사용된다.

자동차 전자제어기를 뜻하는 ECU(Electronic Control Unit)는 사람으로 치면 머리에 해당되는 부품이다.

자동차 ECU는 컴퓨터의 중앙처리장치(CPU)를 포함하면서 물리적 제어 영역으로 확장된 개념이다.

'인지(센서)→산술·명령(ECU)→실행(액추에이터)'의 흐름으로 모터와 유압장치, 점화장치, 표시장치 등 자동차를 작동하는 기능에 특화된 것이다.

ECU는 입력장치와 저장장치, 정보처리장치와 출력장치로 구성된다.

주행 중에 쌓이는 데이터 등은 주로 휘발성 메모리(RAM)에 저장하고 데이터 처리를 위한 운영체제 등은 비휘발성 메모리(ROM)에 저장한다.

알고리즘에 따른 연산처리를 위해 고성능 정보처리장치가 적용되고 오작동 등의 상황을 가정해 백업 장치가 추가되기도 한다.

차량 한 대는 약 60개에서 100여 개의 ECU가 사용된다.

이러한 ECU들은 위계 구조를 갖추고 고유 기능도 수행하면서 다른 ECU들과 '협조-제어'하기도 한다.

ACU(Air bag Control Unit)가 에어백을 전개하면 긴급구난통신장치(e-CALL)가 사고 정보를 관제센터에 자동 전송하는 식이다.

하이브리드차의 제어장치인 HCU(Hybrid Control Unit)도 엔진제어장치, 모터제어장치, 차체자세제어장치와 배터리제어장치 등 차량 각부의 주요 제어장치에 가감속과 배터리 충전 등의 작동 명령을 내리는 구조를 갖추고 있다.

최근에는 서로 연관성 높은 여러 개 ECU가 통합되는 추세다.

싱글코어 8개가 제각각 수행하던 작업을 옥타(Octa·여덟) 코어 하나가 처리하는 등의 방식으로 데이터 처리와 공간 활용 효율성을 높이는 것이다.

특히 인공지능과 딥러닝 등이 적용되는 미래의 완전자율주행, 커넥티드카는 한층 고차원적인 제어 성능이 요구된다. 따라서 분산된 ECU를 합치고 통제 기능을 중앙화해야 한다.

ECU 통합 과정에서 운영체제와 통신 방식, 코딩언어 등이 일관성 있게 적용돼야 한다.

이것이 이뤄져야 다수의 업체들이 협력 개발하는 자동차 산업에서 설계 기간을 단축시키고 성능과 품질까지 확보할 수 있다.

이를 위해 글로벌 완성차 제조사들은 자동차 소프트웨어 국제표준 플랫폼(AUTOSAR)을 기반으로 자동차 소프트웨어를 설계하고 있다.

<br/>

<br/>

## # (2021) WINDS_A Wavelet-Based Intrusion Detection System for Controller Area Network (CAN)

### ABSTRACT

차량에는 전반적인 시스템 기능 및 연결성을 높이기 위해 ECU(전자 제어 장치)가 장착되어 있다. 그러나, 증가하는 연결은 사이버 공격에 무방비 상태의 내부 CAN(Controller Area Network)을 노출시킨다. IDS(Intrusion Detection System)는 기존 ECU를 수정하지 않고 높은 트래픽 오버헤드를 유발하지 않으며 CAN 네트워크 악성 메시지를 식별하기 위해 제안된 감독 모듈이다. 기존의 IDS 접근 방식은 시간과 주파수 임계값에 의존하여 높은 허위 경보율로 이어지는 반면, 최첨단 솔루션은 차량 의존성으로 인해 어려움을 겪을 수 있다. 본 논문은 CAN 네트워크의 전송 패턴을 분석하여 CAN 트래픽에서 동작 변화를 찾기 위한 Wavelet 기반 접근 방식을 제시한다. 제안된 WOLD(Wavelet-based Intrusion Detection System)는 두 개의 독립적인 연구 센터의 실제 차량 트래픽을 사용하여 다양한 공격 시나리오에서 테스트되는 동시에 합성 공격을 사용하여 보다 포괄적인 공격 시나리오로 확장시킨다. 이 기술은 최첨단 솔루션 및 기준 주파수 방법과 비교하여 평가 및 비교된다. 실험 결과에 따르면 WIND는 낮은 허위 경보를 생성하는 동시에 고유한 접근 방식을 통해 다양한 차량에 적용할 수 있는 차량 독립적인 솔루션을 제공한다.



​	