# News_Summarize

### 프로젝트 명: 뉴스요약_카카오톡

### 1. 기간: 2024.10 ~ 2024. 10

### 2. 기술 스택
- BeautifulSoup4: 웹 페이지의 HTML/XML 파일을 파싱하고 데이터를 추출하는 데 사용. 이 프로젝트에서는 뉴스 기사의 내용을 가져오는 데 사용
- lxml: XML 및 HTML 문서를 효율적으로 처리할 수 있는 라이브러리로, BeautifulSoup와 함께 사용하여 복잡한 HTML 구조에서 필요한 정보를 쉽게 추출
- requests: 웹에서 데이터를 요청하는 HTTP 라이브러리. Naver News에서 뉴스 기사를 가져오는 데 사용
- scipy: 과학 계산을 위한 라이브러리로, 데이터 처리 및 수치 해석에 유용. 여기서는 데이터 분석 및 처리에 활용.
- gensim: 자연어 처리(NLP)를 위한 라이브러리로, 문서 요약 기능을 구현하는 데 사용. 특히, 기사의 핵심 내용을 추출하는 데 필수
- summarize: Gensim의 문서 요약 기능을 사용하여 입력된 기사의 주요 내용을 요약하는 데 사용.
- kakao_utils: 카카오톡 API와 연동하여 요약된 기사를 메시지로 전송하는 기능을 담당다.

### 3. 주요 기능
- 뉴스 기사 크롤링: Naver News에서 최신 뉴스 기사를 자동으로 수집하여, 사용자가 필요한 정보를 손쉽게 얻을 수 있도록 함. 이를 통해 사용자는 다양한 주제의 뉴스를 접할 수 있음.

- 텍스트 요약: Gensim을 이용하여 수집한 뉴스 기사를 요약. 이 과정은 자연어 처리 기술을 활용하여 기사의 핵심 문장과 내용을 추출하여, 사용자가 빠르게 정보를 이해할 수 있도록 도움.

- 이미지 스타일 변환: 딥러닝 모델을 활용하여 사용자가 제공한 이미지를 다양한 예술 스타일로 변환하는 기능을 제공. 이는 단순한 뉴스 요약을 넘어서, 사용자에게 시각적으로도 풍부한 경험을 제공.

### 4. 내용
- 이 프로젝트는 사용자가 카카오톡으로 뉴스 기사를 요약받을 수 있도록 설계.
- 사용자는 관심 있는 뉴스 기사를 선택하면, 해당 기사의 요약과 함께 이미지를 스타일 변환하여 전달받음.
- 이 기능은 특히 바쁜 현대인에게 유용하며, 필요한 정보만을 간편하게 제공받을 수 있도록 함.

### 5. 실행 화면
- ![카톡뉴스요약보내기](https://github.com/user-attachments/assets/859b66d9-6fff-4af0-ac7c-068d5e227beb)

- ![카톡뉴스보내기](https://github.com/user-attachments/assets/8a448f3c-b05b-44b7-b90a-9e098eb81e10)


### 6. 결론
- 이 프로젝트는 사용자가 원하는 정보를 간편하게 제공받을 수 있도록 돕고, 머신러닝 기술을 활용한 유용한 응용 프로그램의 예시가 되었으면 함.
- 이를 통해 사용자는 뉴스 소비의 효율성을 높일 수 있으며, 기술을 활용한 정보 전달의 새로운 방법을 경험할 수 있다.

### 7. Reference
- BeautifulSoup Documentation: 웹 스크래핑에 사용되는 BeautifulSoup 라이브러리의 공식 문서입니다.
- lxml Documentation: lxml 라이브러리에 대한 공식 문서로, XML 및 HTML 처리를 위한 다양한 기능을 제공합니다.
- Requests Documentation: HTTP 요청을 간편하게 수행할 수 있는 Requests 라이브러리의 공식 문서입니다.
- Gensim Documentation: Gensim 라이브러리에 대한 공식 문서로, 자연어 처리 및 문서 요약에 필요한 다양한 기능을 제공합니다.
- Kakao Developer: 카카오 API와 관련된 공식 개발자 문서입니다.
- Medium Tutorial on Web Scraping with BeautifulSoup: BeautifulSoup을 사용한 웹 스크래핑 튜토리얼입니다.
- Introduction to Natural Language Processing: 자연어 처리 개념에 대한 소개 및 예제입니다.

