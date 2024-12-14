# vite기반 vue3-firebase-app

vite란 프랑스어로 빠르다는 뜻이다.  

기존 VueJs(CLI)는 개발서버를 돌리거나 production 번들링시 webpack을 사용하였으나, vite는 native es module imports를 사용하여
개발할 수 있고, 번들에는 Rollup이라는 도구를 사용한다.  

vite-app은 vue3에서 사용하기 위해 디자인되었다
서버 기동시 기존 webpack(CLI) 방식보다 실행 속도와 반영속도가 빠르다는 특징이 있다.

<details>
<summary style="font-size:30px; font-weight:bold; font-style:italic;">[현행] vite기반 vue3 install</summary>

- ### vite 기반 vue3 project 생성

  ```bash
  npm init vite-app {프로젝트 명}
  ```

- ### npm 초기 설치
  ```bash
  npm install
  ```

- ### vite 기반 vue3 서버 기동
  ```bash
  npm run dev
  ```
- ### build 명령
  ```bash
  npm run build
  ```
</details>

<details>
<summary style="font-size:30px; font-weight:bold; font-style:italic;">CLI 기반 vue3 install</summary>

- ### Vue CLI 글로벌 설치
  ```bash
  npm install -g @vue/cii
  ```

- ### 설치 버전 확인
  ```bash
  vue -V
  ```
  
  **vue3를 설치하기 위한 vue/cli는 4.5 버전 이상이어야 한다.**

- ### npm 초기 설치
  ```bash
  vue create {프로젝트명}
  ```

- ### Vue3 선택
  ```bash
  Vue CLI v5.0.8
  ? Please pick a preset: (Use arrow keys)
  > Default ([Vue 3] babel, eslint)
    Default ([Vue 2] babel, eslint)
    Manually select features
  ```
- ### vue/cli 기반 vue3 서버 기동
  ```bash
  npm run serve
  ```
- ### build 명령
  ```bash
  npm run build
  ```
</details>
<details>
<summary style="font-size:30px; font-weight:bold; font-style:italic;">파이어베이스에 무료 배포(호스팅)하기</summary>
<br>

파이어베이스는 구글 서비스중 하나이므로 구글 계정이 있다면 바로 사용이 가능하다.  

1. ### 상단 우측의 `콘솔로 이동` 버튼을 클릭한다.  
2. ### 프로젝트 만들기 버튼을 클릭한다.  
3. ### 프로젝트 이름을 입력한 후 `계속` 버튼을 클릭한다.  
4. ### Firebase 프로젝트를 위한 Google 애널리틱스 OFF 후 `프로젝트 만들기` 버튼 클릭
5. ### 좌측 사이드바 - 빌드 아코디언 - `Hosting` 클릭
6. ### 시작하기 클릭
7. ### Firebase 호스팅 설정 시작
<details>
<summary>Firebase 호스팅 설정</summary>
<br>

a. Firebase CLI 설치  
   - 로컬에서 글로벌로 `npm install -g firebase-tools` 설치  

b. 프로젝트 초기화  
   - 프로젝트에서 firebase 로그인 `firebase login` 명령 실행

   - 프로젝트에서 firebase 초기화 `firebase init` 명령 실행  

      - Y 입력 - Enter
        ```bash
        ? Are you ready to proceed? (Y/n) Y - Yes
        ```

      - SpaceBar - Enter
        ```bash
        ? Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices. (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
        ( ) Realtime Database: Configure a security rules file for Realtime Database and (optionally) provision default instance
        ( ) Firestore: Configure security rules and indexes files for Firestore
        ( ) Functions: Configure a Cloud Functions directory and its files
        >(*) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys
        ( ) Hosting: Set up GitHub Action deploys
        ( ) Storage: Configure a security rules file for Cloud Storage
        ( ) Emulators: Set up local emulators for Firebase products
        (Move up and down to reveal more choices)
        ```
      - 기존 프로젝트 사용 옵션 선택 - Enter
        ``` 
        ?Please select an option
        > Use an existing project
        Create a new project
        Add Firebase to an existing Google Cloud Platform project
        Don't set up a default project
        ```
      - 호스팅 할 firebase 프로젝트 선택 - Enter
        ```
        ? Select a default Firebase project for this directory:
        jwitter-app (jwitter-app)
        > yoohyeok-ff0d0 (yoohyeok)
        ```
      - 웹 배포에 사용할 "공개 디렉토리" 지정 - dist 입력 후 Enter
        ```
        ? What do you want to use as your public directory? dist
        ```
      - SPA 작동을 위한 URL 리다이렉션 설정 여부 - y 입력 후 Enter
        ```
        ? Configure as a single-page app (rewrite all urls to /index.html)? (y/N) y
        ```
      - GitHub 자동 빌드 배포 여부 - N 입력후 Enter
        ```
        ? Set up automatic builds and deploys with GitHub? (y/N) N
        ```

  - 위 모든 과정이 종료되면 `.firebaserc` `firebase.json` 파일 2개가 새로 생성된다.    
      (configuration 관련 정보가 들어있다.)
  - 빌드 실행 `npm run build` 명령 입력
  
  c. dist 디렉토리 생성 확인 후 `firebase deploy` 명령 입력
</details>

8. ### `콘솔로 이동` 클릭 후 도메인 확인

</details>