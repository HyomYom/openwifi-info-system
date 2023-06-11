# Open Wifi Data Project

### 사용 대표 라이브러리
- okhttp3
- gson
- sqlite-jdbc

---
### 기능사항
1. 공공 와이파이 정보 가져오기 기능(구현 완료)
2. 내 위치 정보를 입력하면 가까운 위치에 있는 와이파이 정보 20개 보여주는 기능(구현 완료)
3. 내가 입력한 위치정보에 대해서 조회하는 시점에 DB에 히스토리를 저장 및 보여주는 기능(구현 완료)
4. 데이터베이스는 SQLite 이용(구현 완료)

---
### 기능 세부사항
1. 북마크 그룹
	1) 북마크 그룹, 정보 등록 및 수정 시 비동기 통신을 활용한 데이터 중복 방지 구현
	2) 기존 북마크 삭제 시 북마크 등록 돼 있던 정보도 같이 삭제

2. 위치 히스토리
	1) 위치 조회 시, 각 조회마다 위치 데이터 데이터베이스 저장

3. 와이파이 조회
	1) 서울시 공공데이터로부터 데이터 저장 시 SQL쿼리문을 활용한 중복데이터를 방지	하여 대략 23000개의 데이터 중 16000개의 데이터만 DB 저장
	2) 위치기반 가까운 순서대로 페이지에 20개씩 정보를 불러옴
	3) 전체 데이터를 활용해 각 페이지마다 20개씩 페이지네이션 구현
