# 📝 텍스트 기반 QA 시스템 및 PDF 처리 확장

## 프로젝트 개요
이 프로젝트는 PyTorch를 기반으로 텍스트 기반 질문 응답(QA) 시스템을 구현하고, PDF 텍스트 추출 및 멀티모달 데이터 처리를 확장하는 것을 목표로 합니다.

---

## 주요 기능 ✨
- **질문 응답 시스템**: GPT-2 또는 BERT 모델을 활용한 QA 기능.
- **PDF 텍스트 추출**: PyPDF2와 PyMuPDF를 사용하여 PDF에서 텍스트 추출.
- **멀티모달 데이터 확장**: 이미지와 텍스트를 결합한 데이터 처리(후기 단계).

---

## 📖 목차
1. [프로젝트 개요](#프로젝트-개요)
2. [주요 기능](#주요-기능)
3. [실행 방법](#실행-방법)
4. [학습 자료](#학습-자료)
5. [설치 가이드](#설치-가이드)

---

## 실행 방법 🚀

### 1️⃣ 환경 설정
Python 환경을 설정하고 필요한 패키지를 설치합니다:

```python
pip install -r requirements.txt
```
### 2️⃣ 모델 실행
다음 명령어로 메인 스크립트를 실행합니다:

```python
python src/main.py
```

---

## 학습 자료 📚

👉 [공부용 자료 보기](docs/study-guide.md)  
👉 [자주 묻는 질문(FAQ)](docs/faq.md)

---

## 설치 가이드 🛠️

👉 [CUDA 및 PyTorch 설치 가이드 보기](docs/setup-guide.md)

---

## 기술 스택 🧰
- **프로그래밍 언어**: Python 3.9+
- **딥러닝 프레임워크**: PyTorch 2.6.0+cu118
- **PDF 처리 라이브러리**: PyPDF2, PyMuPDF, Tesseract OCR

---

## 기여 방법 🤝

1. 이 저장소를 포크합니다.
2. 새로운 브랜치를 생성합니다:
    ```
    git checkout -b feature-name
    ```
3. 변경 사항을 커밋합니다:
    ```
    git commit -m "Add new feature"
    ```
4. 변경 사항을 푸시합니다:
    ```
    git push origin feature-name
    ```
5. Pull Request를 생성합니다.

---

## 방향성(김경민 작성)

1단계: 미세조정 기반 프로토타입 (1-2개월)
핵심 활동: Mistral 7B 모델 한국어 LoRA 미세조정
데이터: KoAlpaca + 한국어 대화 데이터 5-10K 샘플
자원: 단일 GPU (RTX 3090+ 또는 클라우드)
목표: 빠르게 작동하는 한국어 대화 시스템 확보
2단계: 멀티모달 통합 및 경험 축적 (2-3개월)
핵심 활동: LLaVA/MiniGPT-4 아키텍처 한국어 적응
데이터: 한국어 이미지-텍스트 쌍 데이터 구축
자원: 1-2x GPU
목표: 이미지 인식 능력 추가 및 멀티모달 학습 경험 획득
3단계: 소규모 자체 모델 병행 개발 (3-6개월)
핵심 활동: 300M 파라미터 트랜스포머 모델 독자 개발
데이터: 위키, 뉴스, 웹텍스트 등 한국어 말뭉치
자원: 2-4x GPU
목표: 미세조정 모델과 병행하며 자체 모델 발전
4단계: 통합 및 확장 (6개월+)
핵심 활동: 자체 언어 모델 규모 확장 + 멀티모달 통합
자원: 4x+ GPU 또는 클라우드 확장
목표: 미세조정 모델에서 자체 모델로 점진적 전환
실현 가능성을 높이는 구체적 실행 제안
즉시 실행 가능한 행동
데이터 수집 시작: 한국어 대화/지시 데이터 5-10K 샘플 구축
학습 환경 구축: 단일 GPU 설정 및 LoRA 학습 파이프라인 준비
역할 분담: 데이터 수집, 모델 개발, 평가 담당자 지정
첫 2주 내 목표
작동하는 기본 모델: 간단한 한국어 응답이 가능한 미세조정 모델
병렬 연구: 자체 모델 아키텍처 설계 및 소규모 테스트
데이터 파이프라인: 지속적 데이터 수집/정제 체계 구축
성공적 구현을 위한 조언
두 트랙 병행: 미세조정 모델로 빠르게 결과 확인 + 자체 모델 점진적 개발
체계적 지식 축적: 미세조정 과정에서 얻은 통찰을 자체 모델에 적용
실용주의 접근: 완벽보다는 작동하는 시스템 우선, 점진적 개선
-----> 요약: 1. 아예 초반 모델로 말뭉치 학습해가는 방향 2. 이미 말뭉치를 어느정도 학습한 모델을 좀 더 한국어에 맞게 학습시키고 멀티모달  ------> 해당 방식을 하이브리드로 진행 2번을 시행하면서 1번을 시행하든, 둘 다 같이 진행해나가는 방법 중 택1


## 팀원들 과제

1. 해당 요약에 있는 방식들 숙지
2. LLM 및 딥러닝, 머신러닝을 구축하는 AI 및 용어에 대해서 공부 및 잘못된 방향성 비판
3. 환경구축(일단은, 혹시 모르니까)
4. CursorAI 및 MCP서버 -> 요즘 유명하니까 공부해놓기(해당 과제는 무조건이 아니라, [추천임] 진짜 좋음 --> 나중에 과제나 공부할때도 엄청 도움됨)

## 문의하기 💬

궁금한 점이나 제안 사항이 있다면 [Issues](https://github.com/username/project-name/issues)를 통해 문의해주세요.
