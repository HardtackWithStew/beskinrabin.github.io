# 31게임

## 프로젝트 개요
 **게임 제목:** 31게임
 
 **장르:** 보드게임
 
**플랫폼:** PC

 **개발 엔진** 유니티 엔진
 
 **개발 기간:** March.4 - June.12
 
**주요 기능:** 주사위 굴리기, AI의 기능 개발

---

# 게임 제작 의도

## 게임 개발 배경
**아이디어 출처:** 술게임 베스킨라빈스31 / Inscription / Buckshot Rullet

**개발 목적:** 턴제 게임과 주사위 게임을 만들기 위해 룰을 찾던 도중 생각나 만들게 되었다.

**타겟 사용자:** 보드게임 혹은 턴제게임을 즐길 사용자층

## 게임 컨셉과 디자인
 **스토리:** 어두운 숲속에서 AI와 펼치는 흥미진진한 주사위 게임
 
 **게임플레이:** 
 - 주사위 굴리기 버튼을 눌러 주사위를 던진다.
 - 주사위 굴리기 버튼을 누르기 전 아이템 1개를 클릭하여 해당 아이템 사용할 수 있다.
 - 마지막으로 주사위를 굴린 사람의 주사위 합이 31 초과가 되었을 경우, 해당 사람의 패배.

---

# 게임 개발 과정

## 초기 기획 단계
 **아이디어 브레인스토밍:**
 - 1대1 보드게임 구도를 만들고 싶었다.
 - 특히, 턴제게임이 가미된 여러 게임들을 보며 이번 작품을 결정하게 되었다.
   
 **목표 설정:**
  - 주사위 굴리기
  - 주사위 판정
  - 턴제 설정
  - 아군 아이템 제작
  - 적군 아이템 제작

## 개발 단계
**주요 기능 구현**
- 주사위 굴리기: 매번 다른 힘으로 밑에서 밀어야 한다.
  ![1wn](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/13b74829-6b53-4959-a9c6-fe221a349c18)

- 주사위 판정: 주사위가 바닥에 닿았을 때 주사위의 상태를 알아야 한다.
  ![2wn](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/9aa1174c-757f-4e77-8d9d-cfbd8d0e6808)

- 턴제 설정: 누군가가 주사위를 굴리면, 반드시 상대턴이 와야 한다.
  ![5-6wn](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/3274062c-d6fe-417d-bc4c-d7cfe98b701c)

- 아군 아이템 제작: 주사위를 굴리기 전 사용 가능하고, 4가지 종류가 존재한다.

|이름|사진|효과|
|----|-----|----|
|생존칼|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/16c10737-8f5c-470d-b910-aee7b23f00ef)|이번에 굴리는 주사위는 음수로 작용한다.|
|로프|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/e0bc81e1-c3fa-432f-b91f-317234402378)|상대의 턴을 스킵한다.|
|양초|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/7976c14a-a9a9-45ef-b017-a5ae0464476b)|이번에 굴리는 주사위는 목표치에 더해진다.|
|노트|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/2b506948-90c5-4a16-af6a-6b7ca4f534d0)|주사위를 굴리지 않고 원하는 숫자를 입력해 더한다.|

- 적군 아이템 제작: 랜덤한 확률로 사용하거나, 사용을 안하거나, 필요한 순간에 사용할 수 있다.

|이름|사진|효과|알고리즘|
|----|-----|----|----|
|생존칼|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/16c10737-8f5c-470d-b910-aee7b23f00ef)|이번에 굴리는 주사위는 음수로 작용한다.|아이템 사용번호가 4가 나올때 사용함|
|로프|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/e0bc81e1-c3fa-432f-b91f-317234402378)|상대의 턴을 스킵한다.|아이템 사용번호가 2가 나왔을 때, 혹은 목표-합산치가 12이하일때 사용함| 
|양초|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/7976c14a-a9a9-45ef-b017-a5ae0464476b)|이번에 굴리는 주사위는 목표치에 더해진다.|아이템 사용번호가 1이 나왔을 때, 혹은 목표-합산치가 6이하일때 사용함| 
|노트|![image](https://github.com/HardtackWithStew/beskinrabin.github.io/assets/128970120/2b506948-90c5-4a16-af6a-6b7ca4f534d0)|주사위를 굴리지 않고 원하는 숫자를 입력해 더한다.|아이템 사용번호가 3이 나왔을 때, 혹은 목표-합산치가 2이하일때 사용함| 
  
        
---

# 결론 및 교훈

## 10. 프로젝트 회고
 **결론:**
 - 전 학기때 배웠던 요구사항 정리와 알고리즘 설계를 통해 정리를 했다면 코드가 이렇게 불어나는 일은 없었을 것이다.
 - 그러나 구현하고싶은 내용, 원하는 구도, 큰 그림들은 잘 나와서 만족도는 높았다.
 
 **교훈:** 뼈대없이 주먹구구식으로 만들면 프로젝트의 계발단계가 중구난방이 되버린다
 
 **향후 계획:**
   - 프로젝트의 엔딩, 오프닝을 조금 손볼 것.
   - 멀티플레이 환경 재구성

---
