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
- (2020) CANBus Traffic Anomaly Detection with LSTM and Autoencoders (`can-anomaly-detection`)

<br/>

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

<br/>

## # (2021) WINDS_A Wavelet-Based Intrusion Detection System for Controller Area Network (CAN)

### ABSTRACT

차량에는 전반적인 시스템 기능 및 연결성을 높이기 위해 ECU(전자 제어 장치)가 장착되어 있다. 그러나, 증가하는 연결은 사이버 공격에 무방비 상태의 내부 CAN(Controller Area Network)을 노출시킨다. IDS(Intrusion Detection System)는 기존 ECU를 수정하지 않고 높은 트래픽 오버헤드를 유발하지 않으며 CAN 네트워크 악성 메시지를 식별하기 위해 제안된 감독 모듈이다. 기존의 IDS 접근 방식은 시간과 주파수 임계값에 의존하여 높은 허위 경보율로 이어지는 반면, 최첨단 솔루션은 차량 의존성으로 인해 어려움을 겪을 수 있다. 본 논문은 CAN 네트워크의 전송 패턴을 분석하여 CAN 트래픽에서 동작 변화를 찾기 위한 Wavelet 기반 접근 방식을 제시한다. 제안된 WOLD(Wavelet-based Intrusion Detection System)는 두 개의 독립적인 연구 센터의 실제 차량 트래픽을 사용하여 다양한 공격 시나리오에서 테스트되는 동시에 합성 공격을 사용하여 보다 포괄적인 공격 시나리오로 확장시킨다. 이 기술은 최첨단 솔루션 및 기준 주파수 방법과 비교하여 평가 및 비교된다. 실험 결과에 따르면 WIND는 낮은 허위 경보를 생성하는 동시에 고유한 접근 방식을 통해 다양한 차량에 적용할 수 있는 차량 독립적인 솔루션을 제공한다.

<br/>

<br/>

<br/>

## # (2020) LSTM-Based Intrusion Detection System for In-Vehicle Can Bus Communications

**Publisher: IEEE**

### ABSTRACT

The modern automobile is a complex piece of technology that uses the Controller Area Network (CAN) bus system as a central system for managing the communication between the electronic control units (ECUs). Despite its central importance, the CAN bus system does not support authentication and authorization mechanisms, i.e., CAN messages are broadcast without basic security features. As a result, it is easy for attackers to launch attacks at the CAN bus network system. Attackers can compromise the CAN bus system in several ways including Denial of Service (DoS), Fuzzing and Spoofing attacks. It is imperative to devise methodologies to protect modern cars against the aforementioned attacks. In this paper, we propose a Long Short-Term Memory (LSTM)-based Intrusion Detection System (IDS) to detect and mitigate the CAN bus network attacks. We generate our own dataset by first extracting attack-free data from our experimental car and by injecting attacks into the latter and collecting the dataset. We use the dataset for testing and training our model. With our selected hyper-parameter values, our results demonstrate that our classifier is efficient in detecting the CAN bus network attacks, we achieved an overall detection accuracy of 99.995%. We also compare the proposed LSTM method with the Survival Analysis for automobile IDS dataset which is developed by the Hacking and Countermeasure Research Lab, Korea. Our proposed LSTM model achieves a higher detection rate than the Survival Analysis method.

---

현대 자동차는 전자 제어 장치(ECU) 간의 통신을 관리하기 위한 중앙 시스템으로 CAN(Controller Area Network) 버스 시스템을 사용하는 복잡한 기술입니다. 핵심적인 중요성에도 불구하고 CAN 버스 시스템은 인증 및 권한 부여 메커니즘을 지원하지 않습니다. 즉, CAN 메시지는 기본 보안 기능 없이 브로드캐스트됩니다. 결과적으로 공격자가 CAN 버스 네트워크 시스템에서 공격을 시작하기 쉽습니다. 공격자는 서비스 거부(DoS), 퍼징 및 스푸핑 공격을 비롯한 여러 가지 방법으로 CAN 버스 시스템을 손상시킬 수 있습니다. 전술한 공격으로부터 현대 자동차를 보호하기 위한 방법론을 고안하는 것이 필수적입니다. 본 논문에서는 CAN 버스 네트워크 공격을 탐지하고 완화하기 위해 LSTM(Long Short-Term Memory) 기반 IDS(Intrusion Detection System)를 제안합니다. 먼저 실험 차량에서 공격이 없는 데이터를 추출하고 후자에 공격을 주입하고 데이터 세트를 수집하여 자체 데이터 세트를 생성합니다. 우리는 모델을 테스트하고 훈련하기 위해 데이터 세트를 사용합니다. 우리가 선택한 하이퍼파라미터 값을 사용하여 결과는 분류기가 CAN 버스 네트워크 공격을 감지하는 데 효율적이며 99.995%의 전체 감지 정확도를 달성했음을 보여줍니다. 또한 제안된 LSTM 방법을 한국의 해킹 및 대책 연구소에서 개발한 자동차 IDS 데이터 세트에 대한 생존 분석과 비교합니다. 제안한 LSTM 모델은 생존 분석 방법보다 더 높은 탐지율을 달성합니다.

<br/>

### LSTM-Based Network Intrusion Detection System

For our investigation, we use python PyCharm IDE 2019.2.2 and Keras [21] with TensorFlow as backend. We conduct our experiment with Intel Core i7 CPU 2.20 GHz, 16 GB RAM, Windows 10 (64-bit), and NVIDIA GeForce GTX 1050. We use the *categorical_cross entropy* as loss function. The *Nadam* optimizer is applied with a learning rate of 0.0001, the rest of the parameters conserve their default values and *softmax* is used as an activation function output. Tables 3 and 4 provide the experimental settings regarding attacks detection based on LSTM binary and multiclass classification models. We preprocessed raw CAN dataset before inputting the model, we train the model by providing 80% of the elements and we test the classifier with 20% of the elements. After training, the classifier can classify the attack and benign class elements. Fig. 10 schematizes the deep neural network model wherein we can input the CAN bus data into the input layer and, after preprocessing, the classifier will provide the output as a benign or attack class.

---

조사를 위해 백엔드로 TensorFlow와 함께 Python PyCharm IDE 2019.2.2 및 Keras [21]를 사용합니다. Intel Core i7 CPU 2.20GHz, 16GB RAM, Windows 10(64비트) 및 NVIDIA GeForce GTX 1050으로 실험을 수행합니다. categorical_cross 엔트로피를 손실 함수로 사용합니다. *Nadam* 옵티마이저는 0.0001의 학습률로 적용되고 나머지 매개변수는 기본값을 유지하며 *softmax*는 활성화 함수 출력으로 사용됩니다. 표 3과 4는 LSTM 바이너리 및 다중 클래스 분류 모델을 기반으로 한 공격 탐지에 대한 실험 설정을 제공합니다. 모델을 입력하기 전에 원시 CAN 데이터 세트를 사전 처리하고 요소의 80%를 제공하여 모델을 학습하고 요소의 20%로 분류기를 테스트합니다. 훈련 후 분류기는 공격 및 양성 클래스 요소를 분류할 수 있습니다. 그림 10은 CAN 버스 데이터를 입력 계층에 입력할 수 있는 심층 신경망 모델을 도식화하고 전처리 후 분류기는 양성 또는 공격 클래스로 출력을 제공합니다.