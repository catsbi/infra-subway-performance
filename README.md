<p align="center">
    <img width="200px;" src="https://raw.githubusercontent.com/woowacourse/atdd-subway-admin-frontend/master/images/main_logo.png"/>
</p>
<p align="center">
  <img alt="npm" src="https://img.shields.io/badge/npm-%3E%3D%205.5.0-blue">
  <img alt="node" src="https://img.shields.io/badge/node-%3E%3D%209.3.0-blue">
  <a href="https://edu.nextstep.camp/c/R89PYi5H" alt="nextstep atdd">
    <img alt="Website" src="https://img.shields.io/website?url=https%3A%2F%2Fedu.nextstep.camp%2Fc%2FR89PYi5H">
  </a>
  <img alt="GitHub" src="https://img.shields.io/github/license/next-step/atdd-subway-service">
</p>

<br>

# 인프라공방 샘플 서비스 - 지하철 노선도

<br>

## 🚀 Getting Started

### Install

#### npm 설치

```
cd frontend
npm install
```

> `frontend` 디렉토리에서 수행해야 합니다.

### Usage

#### webpack server 구동

```
npm run dev
```

#### application 구동

```
./gradlew clean build
```

<br>

## 미션

* 미션 진행 후에 아래 질문의 답을 작성하여 PR을 보내주세요.

### 1단계 - 화면 응답 개선하기

1. 성능 개선 결과를 공유해주세요 (Smoke, Load, Stress 테스트 결과)
   <details>
      <summary> WebPageTest, PageSpeed 결과</summary>
      <div markdown="1">

   ![webpagetest](./images/webpagetest_img.png)
   ![speedtest](./images/pagespeed_img.png)
      </div>
   </details>

   <details>
   <summary> Smoke 결과</summary>
   <div markdown="1">

    - 메인화면
      ![main](./images/main_smoke.png)
    - 회원가입
      ![join](./images/join_smoke.png)
    - 경로탐색
      ![path](./images/path_smoke.png)
      </div>
   </details>

   <details>
   <summary> Load 결과</summary>
   <div markdown="1">

    - 메인화면
      ![main](./images/main_load.png)
    - 회원가입
      ![join](./images/join_load.png)
    - 경로탐색
      ![path](./images/path_load.png)
      </div>
   </details>      

   <details>
   <summary> Stress 결과</summary>
   <div markdown="1">

   - 개선전
      - 메인화면
        ![main](./images/main_stress_before.png)
      - 회원가입
        ![join](./images/join_stress_before.png)
      - 경로탐색
        ![path](./images/path_stress_before.png)
        <br>
        <br>
   - 개선후
      - 메인화면
        ![main](./images/main_stress.png)
      - 회원가입
        ![join](./images/join_stress.png)
      - 경로탐색
        ![path](./images/path_stress.png)

       </div>
   </details>

2. 어떤 부분을 개선해보셨나요? 과정을 설명해주세요
   1. nginx 설정 수정
   2. 렌더링 차단 리소스 제거 및 js 로드 방식 defer로 변경
   3. 캐시 어노테이션(Cacheable, CachePut, CacheEvict) 추가
   4. eTag 설정 
   5. 정적 파일 접근 권한및 수명 증가
   6. 8443, 8444 포트로 서버 구동 및 분할 할당
   
---

### 2단계 - 조회 성능 개선하기

1. 인덱스 적용해보기 실습을 진행해본 과정을 공유해주세요

2. 페이징 쿼리를 적용한 API endpoint를 알려주세요

