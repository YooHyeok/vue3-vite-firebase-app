# vite기반 vue3-firebase-app

vite란 프랑스어로 빠르다는 뜻이다.  

기존 VueJs(CLI)는 개발서버를 돌리거나 production 번들링시 webpack을 사용하였으나, vite는 native es module imports를 사용하여
개발할 수 있고, 번들에는 Rollup이라는 도구를 사용한다.  

vite-app은 vue3에서 사용하기 위해 디자인되었다
서버 기동시 기존 webpack(CLI) 방식보다 실행 속도와 반영속도가 빠르다는 특징이 있다.

<details>
<summary style="font-size:30px; font-weight:bold; font-style:italic;">vite기반 vue3 install</summary>

- ### vite 기반 vue3 project 생성

  ```bash
  npm init vite-app {프로젝트 명}
  ```

- ### npm 초기 설치
  ```bash
  npm install
  ```
</details>
<details>
<summary style="font-size:30px; font-weight:bold; font-style:italic;">vite기반 vue3 실행</summary>

- ### vite 기반 vue3 서버 기동

  ```bash
  npm run dev
  ```

</details>