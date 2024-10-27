# News_Summarize

### 프로젝트 명: 뉴스요약_카카오톡

### 1. 기간: 2024.09 ~ 2024. 09

### 2. 기술 스택
- BeautifulSoup4: 웹 페이지의 HTML/XML 파일을 파싱하고 데이터를 추출하는 데 사용. 이 프로젝트에서는 뉴스 기사의 내용을 가져오는 데 사용
- lxml: XML 및 HTML 문서를 효율적으로 처리할 수 있는 라이브러리로, BeautifulSoup와 함께 사용하여 복잡한 HTML 구조에서 필요한 정보를 쉽게 추출
- requests: 웹에서 데이터를 요청하는 HTTP 라이브러리. Naver News에서 뉴스 기사를 가져오는 데 사용
- scipy: 과학 계산을 위한 라이브러리로, 데이터 처리 및 수치 해석에 유용. 여기서는 데이터 분석 및 처리에 활용.
- gensim: 자연어 처리(NLP)를 위한 라이브러리로, 문서 요약 기능을 구현하는 데 사용. 특히, 기사의 핵심 내용을 추출하는 데 필수
- summarize: Gensim의 문서 요약 기능을 사용하여 입력된 기사의 주요 내용을 요약하는 데 사용.
- kakao_utils: 카카오톡 API와 연동하여 요약된 기사를 메시지로 전송하는 기능을 담당다.

### 3. 주요 기능
- 뉴스 기사 크롤링: Naver News에서 최신 뉴스 기사 수집
- 텍스트 요약: Gensim을 이용한 뉴스 기사 요약
- 이미지 스타일 변환: 딥러닝 모델을 활용하여 이미지 스타일 변환

### 4. 내용
- 이 프로젝트는 사용자가 카카오톡으로 뉴스 기사를 요약받을 수 있도록 설계. 사용자가 원하는 기사를 선택하면, 해당 기사의 요약과 함께 이미지를 스타일 변환하여 전달.

### 5. 실행 화면
- ![카톡뉴스요약보내기](https://github.com/user-attachments/assets/859b66d9-6fff-4af0-ac7c-068d5e227beb)

- ![카톡뉴스보내기](https://github.com/user-attachments/assets/8a448f3c-b05b-44b7-b90a-9e098eb81e10)


### 6. 결론
- 이 프로젝트는 사용자가 원하는 정보를 간편하게 제공받을 수 있도록 돕고, 머신러닝 기술을 활용한 유용한 응용 프로그램의 예시로 자리잡았습니다.

### 7. Reference
- [Gensim Documentation](https://radimrehurek.com/gensim/)
- [Naver News API](https://developers.naver.com/docs/serviceapi/news/news.md)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Halb_fast_neural_style Repository](https://github.com/your-repo/halb_fast_neural_style)
