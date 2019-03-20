---
layout: post
title: "코드 하이라이터 적용"
date: 2019-01-06 01:11:00 -0400
author: Shawn Choi
categories: git_pages
---


코드 하이라이터 임베딩 방법 (범용)
---

블로그에 소스코드를 올리는 방법에 대해 잠깐 찾아보았다.  
몇가지 방법이 있는 것 같은데, 그 중 가장 쉬운 방법은 [gist](https://gist.github.com/)를 사용하는 것.
(광주과학기술원 말하는 거 아님.)

사용법은 매우 간단하다.<br>

1. 깃허브 아이디가 없을 시, 가입한 후 로그인.
2. 파일 제목으로 `<이름.확장자>`를 적는다. (예, helloworld.py)
3. 소스코드를 붙여 넣는다.
4. `Create public gist` 클릭
5. Embed 스크립트 복사
6. 해당 포스트에 붙여넣기



Embed할 스크립트는 다음의 형식을 띄고있다.<br>
```
<script src="https://gist.github.com/YOURID/*********.js"></script>
```

**결과**
<script src="https://gist.github.com/ChoiSeongWoo/6b00e535009963b6d24d84ac79825979.js"></script>

<br>
<br>
<br>


추가(Github Pages용)
---
Github Pages에 `Rouge`라는 Highlighter가 있다는 것을 알게 되었고,
내가 지금 사용하고 있는 Jekyll 테마에 이미 구현되어 있다는 것을 확인했다..
위의 방법은 하나도 필요가 없었다는 것.

xml을 지원하는 다른 플랫폼(네이버 블로그,티스토리 등)에서 코드를 적을 일이 생긴다면 위의 방법을 사용하고,
그렇지 않다면 아래의 `Rouge` 를 사용하자.  

코드 Highlighting 방법은 다음과 같다.

1. 첫 째 줄에 `물결 3개+사용언어`
2. 중간 줄에 `코드 내용`
3. 마지막줄에 `물결 3 개`로 마무리

```
~~~python
import numpy
print("hello world")
~~~
```
<br><br>
**결과**

~~~python
import numpy
print("hello world")
~~~
<br><br><br>


훨씬 편하다.
지금이라도 알았으면 됐지 뭐.
그나마 Github Pages를 사용하는 의미를 찾은 듯 하다.
