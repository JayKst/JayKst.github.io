---
layout: post
title:  "Github io Test"
date:   2023-01-17 15:53:00 +0900
categories: jekyll update
---

# jaykst.github.io

[Jekyll을 사용하여 GitHub Pages 사이트 만들기 - GitHub Docs](https://docs.github.com/ko/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)

---

1. github pages Repository 생성
2. window ruby 설치
    1. ruby 3.2.0
    
    ![Untitled](/public/images/Untitled.png)
    
3. git bash 실행 후 로컬 jekyll 설치
    1. `gem install jekyll bundler`
    
    ![Untitled](/public/images/Untitled%201.png)
    
4. To create a new Jekyll site, use the `jekyll new`
 command: (기존 프로젝트구성으로 --force 옵션 추가)
    
    ```jsx
    $ jekyll new --skip-bundle --force .
    # Creates a Jekyll site in the current directory
    ```
    
5. Getfile 수정
    1. gem jekyll 시작부분 주석
        
        ![Untitled](/public/images/Untitled%202.png)
        
    2. get github-page 부분 주석 해제
        1. github-page 버전에 맞도록 설정 여기서 확인가능 [https://pages.github.com/versions/](https://pages.github.com/versions/)
        
        ![Untitled](/public/images/Untitled%203.png)
        
        ![Untitled](/public/images/Untitled%204.png)
        
6. bundle install 실행
    1. `bundle install`
    
    ![Untitled](/public/images/Untitled%205.png)
    

내용 변경을 통해 적용 완료. 보수공사 필요

---

~~jekyll theme 적용~~

관리가 어려워 다시 롤백함.

1. 원하는 테마 선택

[jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/)

[jekyllthemes.org](http://jekyllthemes.org/)

[jekyllthemes.io](https://jekyllthemes.io/) (유료)

[jekyll-themes.com](https://jekyll-themes.com/) (유료)

1. Repo에서 download.zip
2. 압축 해제후 root 폴더 아래에 붙혀넣기(중복은 덮어써버림)
3. 깃 푸시

![Untitled](/public/images/Untitled%206.png)

---

 github pages notion 연결

---

github pages nextjs github actions 자동 배포 

(node 16.13.0 버전)

1. `npx create-next-app@latest --typescript`
2. root/tsconfig.json 생성
    
    ```jsx
    {
      "compilerOptions": {
        "target": "es5",
        "lib": ["dom", "dom.iterable", "esnext"],
        "allowJs": true,
        "skipLibCheck": true,
        "esModuleInterop": true,
        "allowSyntheticDefaultImports": true,
        "strict": true,
        "forceConsistentCasingInFileNames": false, // 파일명에 대소문자 구분하지 않아도 되는 기능 사용 여부 // 직역: 파일 이름에 일관된 casing 강제 적용
        "module": "esnext",
        "moduleResolution": "node",
        "resolveJsonModule": true,
        "isolatedModules": true,
        "noEmit": true,
        "jsx": "react",
        "rootDirs": ["src"],
        "baseUrl": "src",
        "experimentalDecorators": true // ES Decorator에 대한 실험적 기능 사용 여부
      },
      "include": ["src"]
    }
    ```