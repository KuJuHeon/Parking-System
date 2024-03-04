# Parking-System

열어조
주차 관제 시스템

1 차량 인식해서 차단기 올리기 -> OCR, 바운딩박스 검출, 아두이노 
AI <--- 서버 ----> C  -> AI 모델 써보는것, 하드웨어 연결 의의
들어올때 차량등록, 영수증에서 QR찍고 나가기


1. AI 구축 -> AI 모델 학습시키고 오픈비노 적용까지 해보기 안되면 학습된 모델 -> 0 - 구주헌
2. AI - 파이썬 서버 연동 -> 4, 5 - 권유진
3. 서버 구축(AI 및 하드웨어의 결과 처리) -> 1, 3, 4, 7, 8 - 이유진 
4. 서버 - 하드웨어 연동 -> 6, 7-1/3, 8-1/2 유광재
5. 하드웨어 기능 구축 -> 2, 7-1, 7-3, 8-1, 8-2 - 정우택


1. 파이썬 서버 작동
2. 아두이노 작동
3. 파이썬 서버 안에서 웹캠을 찍는 무한루프
    4. 번호판(문자열)이 인식되면 AI로 전달(이미지 인식)
    5. AI에서 인식한 번호판(문자열)을 서버로 다시 전송
    6. 인식한 문자열을 아두이노로 전송
    
    7. 차량 입장
    7-1. 아두이노로 차단기 올리고, LCD에 출력 명령 전송
    7-2. 자리 지정 시스템(RFID), 전광판에 어느 방향으로 가면 되는지 띄우기, QR코드 발급  <- 공모전 쌉가능
    	 a. 입구에서 자리 지정 / b.섹션별 순차대로 자리 지정
    7-3. 아두이노로 몇초 뒤, 차단기 내림, LCD Clear 명령 전송
     => 3
    
    8. 차량 퇴장
    8-1. 아두이노로 차단기 올리고, LCD에 사용시간 출력 명령 전송
    8-2. 아두이노로 몇초 뒤, 차단기 내림, LCD Clear 명령 전송
     => 3
    
    
    
    

차량진입시 -> 차량번호, 객체에 ID 부여
주차안내
주차 완료시 해당 객체가 있는 주차구역 번호 저장 -> 조회가능
