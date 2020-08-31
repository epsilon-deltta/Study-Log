---
title: Disqus를 이용한 Jekyll, Github.io에 댓글 연동
author: JONGSKY
date: 2020-09-01 2:00:00
categories: [Disqus]
tags: [disqus, jekyll, github]
toc: false
---

티스토리, 네이버 블로그 등에서는 댓글 기능을 직접 지원하지만 github page에서는 댓글 기능을 지원하지 않습니다! 그래서 Github blog를 작성하게 되면 Disqus를 이용해 댓글기능을 사용할 수 있습니다.

오늘은 Jekyll와 github.io를 활용해 blog를 만들면서 Disqus 댓글을 연동하는 방법에 대해서 소개합니다.

# Jekyll에 Disqus 댓글 연동 방법

## 1. Disqus 가입

[Disqus 홈페이지](https://disqus.com/)에 들어가 회원가입을 한다. 

**GET STARTED**를 클릭해 회원가입을 시작하겠습니다.

![image](https://user-images.githubusercontent.com/40276516/91740705-a1f2a900-ebee-11ea-83a8-a8c94dd0cf67.png)

이름, 이메일, 비밀번호를 작성한 뒤 Signup을 클릭해 회원가입합니다.

![image](https://user-images.githubusercontent.com/40276516/91741124-378e3880-ebef-11ea-974d-157f59456ad9.png)

## 2. Disqus 댓글 기능 설정

우리는 댓글 기능을 추가하기 때문에 **I want to install Disqus on my site** 버튼을 클릭합니다.

- ```I want to comment on sites``` : Dispus를 사용하고 있는 다른 사이트에 댓글을 다는 기능
- ```I want to install Disqus on my site``` : 자신의 사이트에 Disqus를 설치하는 기능

![image](https://user-images.githubusercontent.com/40276516/91741304-7de39780-ebef-11ea-90a3-528218723a04.png)

Dispus에 댓글 기능을 연결할 사이트에 관한 정보를 입력합니다. Website Name은 자신이 구분할 수 있는 이름을 입력하면 됩니다. 언어는 한국어는 지원이 안됨으로 영어로 설정하시면 됩니다! 모든 내용을 작성 후 **Create Site**를 클릭합니다.

![image](https://user-images.githubusercontent.com/40276516/91742016-87b9ca80-ebf0-11ea-8616-036d9480e2fc.png)

계정의 플랜을 선택할 수 있는 페이지가 나오게 됩니다. 우리는 사이트에 댓글의 기능만 추가하면 되기 때문에 가장 아래있는 Basic을 선택해주면 됩니다.

![image](https://user-images.githubusercontent.com/40276516/91742299-0878c680-ebf1-11ea-9a4a-38394da1d4d8.png)

![image](https://user-images.githubusercontent.com/40276516/91742481-4aa20800-ebf1-11ea-988f-1fd75b19c348.png)

이번 화면은 우리의 사이트 플랫폼을 정해야 합니다. Jekyll를 선택합니다.

![image](https://user-images.githubusercontent.com/40276516/91742524-5b527e00-ebf1-11ea-83fa-4d0e8f86ce1a.png)

Jekyll의 설치 지침으로 여기서는 **Universal Embed Code** 에 대한 영상을 보시면 좋을 것 같습니다. Configure를 클릭해주세요.

![image](https://user-images.githubusercontent.com/40276516/91742669-90f76700-ebf1-11ea-9d3d-e5fb83c76214.png)

Disqus의 설정들을 하는 화면입니다.
**Website URL** 에 자신이 연결하는 도메인이름을 입력해주면 됩니다.

입력 후 Complete Setup를 선택합니다.

(예시 : https://jongsky.github.io/Study-Log/)

![image](https://user-images.githubusercontent.com/40276516/91742799-cc923100-ebf1-11ea-9048-2944f61c5467.png)

다음과 같은 화면이 나왔다면 댓글 기능 설정을 위한 Disqus는 완료했습니다!

![image](https://user-images.githubusercontent.com/40276516/91743106-43c7c500-ebf2-11ea-8217-2deaae500c81.png)

## 3. 자신의 github.io에 연결하기

앞선 화면에서 **Configure your site's community settings** 를 클릭하시면 **_config.yml**에 추가해야할 **shortname**를 확인하실 수 있습니다. 해당 **shortname**을 복사합니다.

![image](https://user-images.githubusercontent.com/40276516/91743412-b8026880-ebf2-11ea-9240-dd5c29d068ad.png)

이제 _config.yml 파일을 열어 disqus에 해당 shortname을 붙여넣기 해줍니다. comments는 false에서 true로 수정해줍니다.

![image](https://user-images.githubusercontent.com/40276516/91743515-e97b3400-ebf2-11ea-8848-d866b7daa700.png)

## 4. 자유롭게 댓글 기능 사용하기

수정 후에 github에 push 하시면 댓글기능을 자유롭게 사용하실 수 있게됩니다!

![image](https://user-images.githubusercontent.com/40276516/91743843-6ad2c680-ebf3-11ea-8032-b2a786d4685b.png)

