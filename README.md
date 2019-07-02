# Node.js & UI5-CLI 설치

## 1) Node.js 설치(nvm)

1) [nvm download!](https://github.com/coreybutler/nvm-windows/releases) nvm-setup.zip 파일 다운로드 및 설치

![nvm_setup.png](https://images.velog.io/post-images/opensapkr/02e6f930-9ca1-11e9-af5e-5f0cc1d1216b/nvmsetup.png)

2) nvm install 8.9.0(npm 설치)

3) nvm use 8.9.0

## 2) UI5-CLI 설치

**install ui5 cli**

```
npm install --global @ui5/cli
```


## 2-1) overview

**ui5 명령어 확인**
```
ui5 --help
```

```
Usage: ui5 <command> [options]

Commands:
    build  Build project in current directory
    serve  Start a webserver for the current project
    tree   Outputs the dependency tree of the current project to stdout. It takes all relevant parameters of ui5 build into account.
    init   Initializes the UI5 Tooling configuration for an application or library project

Options:
    --help, -h                Show help  [boolean]
    --version, -v             Show version number  [boolean]
    --config                  Path to config file  [string]
    --translator, --t8r       Translator to use. Including optional colon separated translator parameters.  [string] [default: "npm"]
    --verbose                 Enable verbose logging. [boolean]
    --loglevel, --log-level   Set the logging level (error|warn|info|verbose|silly).  [string] [default: "info"]

Examples:
    ui5 <command> --translator static:/path/to/projectDependencies.yaml  Execute command using a "static" translator with translator parameters
    ui5 <command> --config /path/to/ui5.yaml                         Execute command using a project configuration from custom path
```

## 3) ui5 폴더 구조
![폴더구조.png](https://images.velog.io/post-images/opensapkr/aece9b70-9c85-11e9-a5bc-0552567ba651/.png)

ui5를 실행가 위해서 위와같이 기본적으로 `webpapp` 폴더가 생성이 되어 있어야 한다. 

webapp 경로에서 `ui5 init` 명령어를 입력하면 ui5.yaml 생성이 되고
`npm init --yes` 명령어를 통해 package.json 파일을 생성한다.

이후 package.json에서
`"scripts": {"serve" : "ui5 serve --open/index.html"}`
npm 명령어를 입력후 `npm run serve`를 통해 로컬 호스트를 띄어 결과창을 확인 할 수 있다. 

ui5 커맨드들은 위의 설명한 `ui5 --help` 명령어를 통해 다양한 옵션들을 확인할 수 있다.

해당 lecture 폴더들은 이미 `package.json`과 `ui5.yaml`이 설정이 되어 있기 때문에 아래의 실행방법에 따라 로컬로 실행할 수 있다.


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