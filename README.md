# 📬 뉴스 크롤링 및 자동 이메일 발송 시스템

이 프로젝트는 다음 작업을 자동화합니다:

1. 네이버 뉴스에서 키워드 기반 뉴스 검색  
2. 각 뉴스 페이지에서 기사 본문 크롤링  
3. 수집 결과를 CSV 파일로 저장  
4. 매일 오전 11시에 자동으로 이메일 발송 (CSV 첨부 포함)

---

## 📁 프로젝트 구성

📄 test_data.csv # 뉴스 검색 결과 (제목, 링크 등)

📄 test_data_with_content.csv # 기사 본문까지 포함된 최종 CSV

📄 main.ipynb # 메인 코드

📄 README.md # 설명 문서 (본 문서)

---

## 1. 네이버 뉴스 검색 (API 크롤링)

주요 키워드로 네이버 뉴스 검색

결과는 test_data.csv로 저장


## 2. 기사 본문 크롤링

각 뉴스 링크 접속 후, BeautifulSoup으로 본문 수집

결과는 test_data_with_content.csv로 저장


## 3. 이메일 전송 함수

send_email_with_attachment(subject, body, to_email, from_email, password, file_path)


## 4. 자동 발송 스케줄 설정

import schedule

schedule.every().day.at("13:40").do(job)


#### 
- 예시
![13:40 자동 발송 예시](https://github.com/yyyewon/Email_automation/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202025-06-18%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%201.58.18.png)

