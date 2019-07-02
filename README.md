# Node.js & UI5-CLI 설치 (nvm으로 설치)
[노드 설치 및 ui5-cli 설치](https://velog.io/@opensapkr/openui5-install) 

# 실행방법
1) 폴더 구조에서 원하는 디렉토리로 터미널로 이동한다.

2) 이동한 디렉토리에서 `package.json`이 있는지 확인하고 해당 파일에서
 ```json
...,
"scripts": {
    "serve": "ui5 serve --open /index.html"
  }
```
script에 명령어중 `ui5 serve` 명령어에 따라 터미널에서 `npm run serve`를 통해 서버를 실행한다.

**walkthrough**는 26강부터 `npm install`실행후 **node_modules** 폴더가 생기는지 확인후
  
`npm run proxy` 명령어로 proxy를 실행한 상태에서 `npm run serve`를 통해 실행 시켜야 데이터를 받아온다(CORS issue!)

# 디버깅 단축키

1) CTRL + ALT + SHIFT + S

2) CTRL + ALT + SHIFT + P

(walkthorugh 30강 참고!)