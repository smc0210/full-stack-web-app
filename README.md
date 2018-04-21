# Full-Stack web/app Guide

Python-django, nodejs, React, AWS

## Requirements
- Visual Studio Code
- XCode
- Android Studio
- Expo
- Nodejs
- NPM
- Yarn
- Python 3.6 이상
- pip
- pipenv
- PostgresSQL
- Expo Client

## CheckList

아래 환경이 설치되어 있고 터미널 창에서 명령어로 실행이 가능(심볼릭링크설정까지)한 단계까지 셋팅이 완료됬다는 가정하에 진행
- python (3.6이상)
- pip
- pippenv
- node (6.x 이상)
- npm
- yarn
- postgresSQL (Postgres.app / pgAdmin)

## Back-End

### use stack
- Python3
- Django

`pip`를 통한 가상환경 구성과 가상환경 안에서 `Django`셋팅

### `python`가상환경 구성

```bash
cd /develop/{projectDir}
pipenv --three
pipenv shell
```

### `Cookicutter`를 이용한 `Django`프로젝트 구성

> `Cookicutter`는 프로젝트 구성을 보다 쉽게 할수 있게 해주는 오픈소스
> [Cookiecutter-Django github repo](https://github.com/pydanny/cookiecutter-django)

```bash
pipenv install cookiecutter
pipenv shell
cookiecutter https://github.com/pydanny/cookiecutter-django
```

### 버전관리를 위해 `Git`연동

`GitHub`에 저장소를 만들고 위에서 셋팅한 가상환경 폴더를 git으로 등록

```bash
git init
# git remote add origin {YOUR_GIHTUB_URL}
git remote add origin https://github.com/smc0210/devgram
git pull origin master
git add .
git commit -m "First commmit"
git push origin master
```

### 필요한 django 패키지들 설치

```bash
pipenv shell
pipenv install -r requirements/local.txt
```

이때 local.txt는 쿠키커터에서 입력한 정보를 바탕으로 생성된 필요한 패키지 모음이다
npm 의 package.json 과 완전히 같지는 않지만 비슷한 느낌으로 생각하면 될듯

<<<<<<< HEAD
### Database 생성
`PostgresSQL` App을 실행하고 하단의 데이터베이스를 클릭하면 터미널창이 실행되는데,
mysql 콘솔창과 비슷하게 생각하면 된다. 
![1][1]

`PostgresSQL` 터미널 창에서 하단의 명령어로 database를 만들어 준다.

```bash
CREATE DATABASE devgram;
```

### Image App 생성

```bash
cd devgram
django-admin startapp images
```

[1]: https://github.com/smc0210/FullStackGuide/blob/master/asset/backend/20180422_1.png
=======
##### local.txt 파일 예시
```xml
# Local development dependencies go here
-r base.txt

coverage==4.4.1
django-coverage-plugin==1.5.0

Sphinx==1.6.4
django-extensions==1.9.1
Werkzeug==0.12.2
django-test-plus==1.0.18
factory-boy==2.9.2

django-debug-toolbar==1.8

# improved REPL
ipdb==0.10.3

pytest-django==3.1.2
pytest-sugar==0.9.0
```
>>>>>>> 2f5573374383ae96b0e70334c84d147014f66078
