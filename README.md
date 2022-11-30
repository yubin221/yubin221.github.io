# 시작하기에 앞서
테마 적용 이전 활동들에 대한 레포지토리는 https://github.com/yubin221/KMU_Blog 에 있습니다

# 블로그 주소를 찾으시나요?
https://yubin221.github.io/ 를 통해 블로그로 이동할 수 있습니다!

# Git Blog
해당 블로그는 크게 아래의 단계를 거쳐 제작하였습니다
1. Jekyll 기본 블로그 생성(현 KMU_Blog)
2. Lanyon 테마 적용 및 댓글 기능 추가(현 KMU_Blog)
3. Memoirs 테마 재적용 및 한글화, 각종 기능 추가(현 yubin221.github.io)

# Jekyll 기본 블로그 생성(현 KMU_Blog)

## Github Page 시작하기
1. Github에서 yubin221.github.io 이름의 Repo 생성함(현재 KMU_Blog로 이름 변경됨)
2. Repository 주소를 복사한 뒤 Git에서 ```git clone <repo_name> blog```실행
3. 로컬 blog폴더에 yubin221.github.io 레포지토리 연동 완료

## Jekyll 설치하기 및 블로그 생성
1. https://jekyllrb-ko.github.io/docs/installation/windows/ 의 방법에 따라 Jekyll을 설치함
2. blog 디렉토리에서 ```jekyll new . --force```을 실행하여 blog 디렉토에 Jekyll을 설치
3. ```bundle exec jekyll serve```실행하여 서버 실행, localhost:4000 에서 제작된 블로그 확인
4. ```git add *```실행하여 변경 파일 지정 후 ```git commit -m "add: jekyll on repository"```로 커밋
5. ```git push origin main```을 통해 지금까지 변경사항을 Github에 Push
6. 지금 단계까지의 커밋 기록은 [여기](https://github.com/yubin221/KMU_Blog/commit/ddf58ae842ede206168a216665626c76d896807f)에서 확인할 수 있습니다

## Post Upload
1. _posts 폴더에 YYYY-MM-DD-TITLE.md 형태로 Markdown 문서 생성
2. 다음과 같은 형태로 Post 문서 시작부분 작성후 Markdown 형식으로 내용 작성
```markdown
---
layout: post
title: "MongoDB 정리"
date: 2021-11-10 20:34:09 +0900
categories: jekyll update
---
```
3. Commit및 Push
4. 지금 단계까지의 커밋 기록은 [여기](https://github.com/yubin221/KMU_Blog/commit/ea457a40db1871350081b3b2fab2b72172f9e5d0)에서 확인할 수 있습니다

# Lanyon 테마 적용 및 댓글 기능 추가(현 KMU_Blog)

## Lanyon 테마 적용
1. Lanyon 테마를 git clone하여 로컬에 받아옴
2. 의존성을 감안하여 _post를 제외하고 테마를 blog폴더에 덮어씌움
3. 변경된 파일들을 Git에 Add 및 Commit, Github에 Push함
4. 지금 단계까지의 커밋 기록은 [여기](https://github.com/yubin221/KMU_Blog/commit/6909571562d3dea4ca88306fffe1f661bb1b850b)에서 확인할 수 있습니다

## 댓글 기능 추가
1. Disqus 가입 및 새팅 진행
2. _config.yml에 key-value추가
3. Universal Code복사 후 _layouts/post.html에 해당 코드 붙여넣기 후 코드 양 끝에 ```{% if page.comments %}```와 ```{% endif %}```추가
4. 주석 해제 후, PAGE_URL과 PAHE_IDENTIFIER설정
5. _posts/에 있는 Markdown파일들에 다음과 같이 comments: True로 지정
```markdown
---
layout: post
title: "MongoDB 정리"
date: 2021-11-10 20:34:09 +0900
categories: jekyll update
comments: true
---
```
6. 댓글 기능 추가 완료!
7. 지금 단계까지의 커밋 기록은 [여기](https://github.com/yubin221/KMU_Blog/commit/3a2484773c69d6d53754bdc87cee2ce41f6dd58e)부터 [여기](https://github.com/yubin221/KMU_Blog/commit/cef3308e421cbaa9c18a6cdfe240992c898738b6)까지 사이의 커밋 기록에서 확인할 수 있습니다. (오타 발견 못하고 여러번 시도한 흔적...)

# Memoirs 테마 재적용 및 한글화, 각종 기능 추가(현 yubin221.github.io)

## 테마 재적용 이유
***덮어 씌웠던 Lanyon 테마가 맘에 안들어서***(ㅎ..)

## 테마 재적용 과정
1. 기존 yubin221.github.io 레포지토리 이름을 KMU_Blog로 수정
2. 새 yubin221.github.io 레포지토리 생성
3. Repository 주소를 복사한 뒤 Git에서 ```git clone <repo_name> 블로그```실행하여 로컬 저장소와 Github 연동
3. https://bootstrapstarter.com/jekyll-theme-memoirs/ 에서 테마 다운로드 후 ```gem install bundler``` ```bundle install``` ```bundle exec jekyll serve```실행
4. ***수많은 오류와의 만남과 구글링***
5. 오류 해결 완료 및 사이트 작동 확인
6. 404 페이지, _config.yml 등 일부정보 수정 후 깃허브에 커밋 및 푸시
7. 지금 단계까지의 커밋 기록은 [여기](https://github.com/yubin221/yubin221.github.io/commit/3241b5a4c0c5d333ddd4a7f4bd4f4bf9a1a477a0)에서 확인할 수 있습니다.

## 이후 주요 커밋 기록들에 대한 요약
1. [_config.yml 수정 및 Disqus 기능 추가 시도(Universal Code), 포스트 작성자 수정](https://github.com/yubin221/yubin221.github.io/commit/2801c4fbf4d46ec52e95db13dac1e6b9358db78f)
2. [로컬호스트에서는 홈페이지가 정상적으로 나타나지만, Github에서는 나오지 않는 오류 수정(config.yml의 baseurl 삭제)](https://github.com/yubin221/yubin221.github.io/commit/461f1a0208b86b618c156108c18dd2ff4cc748a7)
3. [댓글기능 업데이트 (_config.yml의 disqus란에 닉네임 기록하면 '{{site.disqus}}'로 전달 되는것을 확인하였음. 그로 인해 _includes/disqus.html에 수정했던 내용 롤백)](https://github.com/yubin221/yubin221.github.io/commit/838a4d00cdd7746e2bdf2b629ceb77d697c1fc05)
4. [블로그 한글화, _config.yml 설명 변경, 로고 제작 및 로고 변경(favicon추가)](https://github.com/yubin221/yubin221.github.io/commit/17b7cf0c5f05c9bb22c6da8b8cd93ba1cc088ecd)
5. [한글화](https://github.com/yubin221/yubin221.github.io/commit/a5c72356187e9b45e01a14bc116e54b7610a516c) 그리고 [한글화](https://github.com/yubin221/yubin221.github.io/commit/28b9bf06a37018de4e6b8e085df5a9c46c8366a5)의 [반복](https://github.com/yubin221/yubin221.github.io/commit/32fb4afea1f7fe9b83c50e9e5ff35697e5f400ec)
6. [메일 문의와 뉴스레터 구독 기능 추가(formspree, mailchimp)](https://github.com/yubin221/yubin221.github.io/commit/f9598b5f2bdd98932c394be4f8b10c6d3b23424a)
이에 대한 자세한 내용은 [다음](https://yubin221.github.io/%EC%9D%B4%EB%A9%94%EC%9D%BC-%EB%AC%B8%EC%9D%98-%EA%B8%B0%EB%8A%A5%EA%B3%BC-%EB%89%B4%EC%8A%A4%EB%A0%88%ED%84%B0-%ED%99%9C%EC%84%B1%ED%99%94/)글에서 확인할 수 있습니다.
7. [데모 포스트와 필요없는 이미지 삭제 및 신규포스트(타 과목 스터디 내용)추가](https://github.com/yubin221/yubin221.github.io/commit/7df1ebec6b8713326ccec53a615d89f0a2c85d00)
8. [마크다운과 관련된 설명 포스트 추가](https://github.com/yubin221/yubin221.github.io/commit/dafee069ee3785a842930675c11846592216fd7a)
9. [이메일 문의 기능과 뉴스레터 활성화 포스트 추가](https://github.com/yubin221/yubin221.github.io/commit/c9655c48a56a658e39161fe1514cc7660d49a402)
