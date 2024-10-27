# 뉴스 요약 카카오톡 (News Summary KakaoTalk)

## 프로젝트 개요
- '뉴스 요약 카카오톡' 프로젝트는 최신 뉴스 기사를 사용자에게 요약하여 카카오톡 메시지로 전송하는 시스템.
- 이 프로젝트는 정보의 비대칭성을 해소하고 사용자가 손쉽게 필요한 정보를 빠르게 얻을 수 있도록 설계.
- 사용자는 '정치', '경제', '사회' 등 다양한 분야의 뉴스를 선택할 수 있으며, 각 뉴스의 제목과 요약된 내용을 카카오톡으로 받아볼 수 있다.

## 기간
- **시작일:** 2024년 10월
- **완료일:** 2024년 10월

## 기술 스택
- **프로그래밍 언어:** Python 3.8
- **주요 라이브러리:**
  - `requests`: HTTP 요청을 통해 웹 페이지에 접근하기 위한 라이브러리.
  - `BeautifulSoup`: 웹 페이지의 HTML/XML 구조를 파싱하여 원하는 데이터를 추출하는 데 사용.
  - `gensim`: 자연어 처리 라이브러리로, 뉴스 기사 내용을 요약하는 데 활용.
  - `kakao_utils`: 카카오톡 API를 통해 메시지를 전송하는 사용자 정의 모듈.

## 주요 기능
- **뉴스 크롤링:** 
  - 사용자가 선택한 분야의 상위 3개 뉴스를 네이버 뉴스에서 자동으로 수집.
  - 각 뉴스의 제목, 작성일, URL 및 이미지 URL을 포함한 기본 정보를 제공.

- **뉴스 내용 요약:** 
  - 수집한 뉴스 기사의 내용을 Gensim 라이브러리를 통해 자동으로 요약.
  - 요약이 실패할 경우, 기본적으로 첫 3문장을 사용하여 대체.

- **카카오톡 메시지 전송:** 
  - 요약된 뉴스 내용을 카카오톡 메시지로 전송하여 사용자가 쉽게 확인할 수 있도록 함.
  - 각 메시지는 뉴스 제목, 요약 내용 및 자세히 보기를 위한 링크를 포함.

## 사용 방법
1. **환경 설정:**
   - Python 3.8 이상 설치
   - 필요한 라이브러리 설치:
     ```bash
     %pip uninstall gensim
     %pip uninstall scipy
     %pip uninstall numpy
     %pip install gensim==3.8.3
     %pip install BeautifulSoup4 lxml requests
     %pip install scipy==1.4.1
     %pip install numpy==1.19.5
     ```
   - 카카오톡 API를 사용하기 위한 인증 정보 설정
     ```bash
     import json: JSON 형식의 데이터를 다루기 위해 json 모듈.
     import kakao_utils: 카카오톡 API와 관련된 유틸리티 기능을 사용하는 kakao_utils 모듈.
     KAKAO_TOKEN_FILENAME: 카카오톡 API의 인증 토큰을 저장할 JSON 파일의 경로를 지정.
     KAKAO_APP_KEY: 카카오톡 API를 사용할 때 필요한 앱 키를 저장.
     kakao_utils.update_tokens(KAKAO_APP_KEY, KAKAO_TOKEN_FILENAME): 지정한 앱 키와 파일 경로를 사용하여 카카오톡 API의 인증 토큰을 업데이트하는 함수
     ```

2. **코드 실행:**
   - 스크립트를 실행하여 원하는 뉴스 카테고리를 선택.
   - 뉴스가 크롤링되고 요약된 후 카카오톡으로 전송.

## 코드 설명
### 뉴스 크롤링
뉴스 크롤링은 `get_naver_news_top3()` 함수를 통해 이루어짐. 이 함수는 선택한 카테고리의 상위 3개 뉴스를 크롤링하여 뉴스 제목, 날짜, URL 및 이미지 URL을 수집.

### 내용 요약
뉴스 내용은 `get_news_contents(url)` 함수를 통해 추출되며, Gensim의 `summarize()` 함수를 사용하여 요약. 요약이 실패할 경우, 기본적으로 첫 3문장을 사용.

### 카카오톡 전송
카카오톡 메시지는 사용자가 선택한 카테고리에 따라 구성된 템플릿 형식으로 전송. 각 뉴스 제목과 요약 내용은 카카오톡 메시지로 전송되어 사용자가 쉽게 접근할 수 있도록 함.

## 실행 화면
프로젝트의 실행 화면 예시:

- 크롤링한 뉴스 제목 및 요약 내용 표시
- ![카톡뉴스요약보내기](https://github.com/user-attachments/assets/33dcf61f-3a9c-4908-ae88-80cf12cc3820)
- 카카오톡으로 전송된 메시지의 내용
- ![카톡뉴스보내기](https://github.com/user-attachments/assets/7d4676c4-95a0-4933-8420-873b59ac369d)


## 결론
- 이 프로젝트는 사용자가 선택한 분야의 최신 뉴스 정보를 손쉽게 요약하여 카카오톡으로 전달함으로써, 바쁜 현대인들에게 필요한 정보를 빠르게 제공하는 것을 목표.
- 향후 기능으로는 사용자 맞춤형 뉴스 추천, 다양한 뉴스 출처 통합, 요약 스타일 선택 기능 등이 있을 수 있음.

## 참고 자료
- [BeautifulSoup Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Gensim Documentation](https://radimrehurek.com/gensim/)
- [Kakao Developers](https://developers.kakao.com/)

