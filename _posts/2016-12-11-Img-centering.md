---
layout: post
title: Markdown에서 Image 다루기
category: Dev
summary: Markdown을 이용해 Image를 리사이즈하고 가운데 정렬하는 방법을 알아보자
---

Jekyll 블로그를 하면서 이미지를 삽입해야할 때가 있었는데, 이미지 사이즈를 줄이고 본문에 가운데 정렬을 하고싶었다.
맨 처음 `Jekyll` 블로그를 만들 때 써있던 `Markdown` 문법 가이드에는 이런 부분이 설명되지 않아서 직접 찾고 해결한 부분을 포스트하려한다.

<hr>

### Image 사이즈 조절하기

[Google](http://google.com)에서 `Markdown` 문법으로 이미지를 리사이즈하는 방법을 찾아보니 가장 위에 뜬 [Stack Overflow](http://stackoverflow.com/questions/14675913/how-to-change-image-size-markdown) 글에서는 아래와 같은 방법이 적혀있다.

{% highlight md %}
![Image](./pic/pic1_50.png =100x20)
{% endhighlight %}

하지만, 위와 같은 방법으로는 `Jekyll` 에서 이미지 리사이즈가 되지 않았다. 자세히 찾아보진 않았지만, `Jekyll` 의 버전이 업그레이드 되면서 발생한 문제같았다.

좀 더 검색을 해보고 다양한 방법들을 해외 개발자분들이 많이 답변을 해놨지만, 대부분 `Jekyll` 에서는 작동하지 않았다.

왜 이럴까 고민하던 중, [이 글](http://stackoverflow.com/questions/24383700/resize-image-in-the-wiki-of-github-using-markdown)의 맨 마지막 답변에서 해답을 찾을 수 있었다.

{% highlight md %}
![Image](./pic/pic1_50.png){: width="100px" height="20px"}
{% endhighlight %}

위와 같이 선언해주면, 내가 선언한 너비와 높이만큼 이미지가 리사이즈된다. `px` 뿐만 아니라 `%` 도 작동한다.

<hr>

### Image 가운데 정렬하기

[Google](http://google.com)에서 검색을 해본 결과, `Markdown` 에서는 기본적으로 이미지 가운데 정렬은 지원하지 않는 듯하다. <del>내가 못 찾은 것일 수도 있다.</del>

내가 찾은 [방법](https://thornelabs.net/2014/11/30/centering-images-with-jekyll-and-markdown.html)은 `CSS`에서 가운데를 정렬하는 `class` 를 만든 뒤, `Markdown` 에서 가운데 정렬 `class` 를 적용시켜 가운데 정렬을 하는 방법이다.

`1.` 아래와 같은 `CSS` `class` 를 만든다.

{% highlight css %}
.center-image{
    margin: 0 auto;
    display: block;
}
{% endhighlight %}

`2.` `Markdown` 에서 `class` 를 적용한다.
{% highlight md %}
![Picture description](/link/to/picture.jpg){: .center-image }
{% endhighlight %}

이 두 과정을 거치면, 가운데 정렬된 이미지를 확인할 수 있다.


> Markdown과 언제쯤 친해질 수 있을까?

저는 이제 갓 `Markdown` 문법에 입문한 초보자입니다. 위에 기술한 내용보다 훨씬 훌륭하고 간단한 방법이 있을지도 모릅니다.
혹시 위에 기술된 내용보다 더욱 좋은 방법을 알고 있는 사람이 계시다면, 아래 댓글 창에 남겨주시면 추가하도록 하겠습니다!
