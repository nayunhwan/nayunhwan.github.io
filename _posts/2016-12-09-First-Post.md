---
layout: post
title: 블로그를 처음 시작하며
category: Dev
summary: Jekyll, Markdown과 친해지기, 개발자에게 있어서 Github 블로그란?
---

처음으로 기술 블로그를 만들어 보았다.

### Jekyll 블로그를 시작하기

Jekyll을 이용하는 것은 쉽지 않았다.

지금까지 기업에서 운영하는 블로그나 워드프레스와 같은 설치형 블로그 서비스만을 이용하다, 직접 블로그 시스템을 구축하는 것은 결코 쉬운 일은 아니였다.

현재 많은 기업들의 Tech 블로그가 Jekyll과 [Github Pages](http://github.com)로 운영되고 있다.
처음에 사용하기 어려운 대신, 엄청난 확장성의 자유도와 무료라는 강력한 장점을 가지고 있다.

이제 이 Tech 블로그를 어떻게 시작하냐가 큰 관건이다.

1.  [Kakao 기술 블로그](kakao.github.io)
2.  [우아한형제들 기술 블로그](http://woowabros.github.io/)
3.  [스포카 기술 블로그](https://spoqa.github.io/)

> Markdown 문법은 어떻게 써야할까?

가장 처음 나를 당황스럽게 한 것은 바로 글을 쓸 때 `Markdown` 이라는 문법을 사용해서 써야한다는 것이였다.

기껏 힘들게 블로그를 만들어 놨더니, 글을 올리는 것도 코딩의 연속이다.

나도 아직 `Markdown` 문법은 아직 나도 많이 생소해서 기본적으로 담겨 있던 문서를 참고해봤다.

- **To bold text**, use `<strong>`.
- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.

이렇게 써있다.. 나도 아직 다 외우질 못해서 계속 이 글을 읽으러 찾아 들어올 것같다. 첫 글이 의미있게 되는 것일지도 모르겠다.

> Code를 자동으로 Highlight 해준다고? 신세계잖아?

### Code Highlighting

사실 Jekyll 블로그를 시작하게 된 가장 큰 계기는 바로 `Code Highlight` 기능이다. 개발을 하다보면 자신이 짠 코드를 [Github](http://github.com) 뿐 만아니라 다른 곳에도 올려두고, 여러 사람들과 공유하고 싶을 때가 많다.

하지만 일반적으로 사람들이 많이 쓰는 [네이버 블로그](http://blog.naver.com)나 [티스토리](http://www.tistory.com/) 그리고 요즘 따끈따끈하게 오픈한 [브런치](http://brunch.co.kr)을 쓰려고하니, `Code Highlight` 기능이 없어서 코드를 올려도 가독성이 떨어지게 올라가 더 이상 읽고싶지 않게 만들었다.

Jekyll은 달랐다. 무슨 언어로 쓰여져있는지만 정해주면 자동으로 `Code Highlight`를 해준다. 바로 아래와 같이 말이다.

{% highlight js %}
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
{% endhighlight %}

아주 간단하고, 기본적으로 지원하는 색상 스키마도 매우 마음에 든다. 이 기능 하나 때문에 Jekyll 블로그를 선택하게 됐다고 봐도 무방할 정도로 정말 쉽고 간편하게 코드를 하이라이팅해준다.

### Lists

`Markdown` 문법을 이용하면 쉽게 List도 만들 수 있다. `<ul>` List를 만들고 싶을 땐 간단하게 문장 앞에 `*` 을 붙여주면 된다.

* Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
* Donec id elit non mi porta gravida at eget metus.
* Nulla vitae elit libero, a pharetra augue.

그리고 `<ol>` 를 만들고 싶을 때는 문장 앞에 `1.` 과 같이 숫자와 마침표를 써주면 된다. 정말 간단하다.

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

사전의 용어를 설명하는 `<dl>`, `<dt>`, `<dd>` 태그들은 `HTML` 문법과 똑같이 그대로 태그를 써주면 된다.

<dl>
  <dt>HyperText Markup Language (HTML)</dt>
  <dd>The language used to describe and define the content of a Web page</dd>

  <dt>Cascading Style Sheets (CSS)</dt>
  <dd>Used to describe the appearance of Web content</dd>

  <dt>JavaScript (JS)</dt>
  <dd>The programming language used to build advanced Web sites and applications</dd>
</dl>

> Markdown의 한계, 이미지 삽업하기

### Images

`Markdown` 문법으로 블로그를 만들 때 가장 아쉬운 점은 이미지 삽입이다. 기존 기업에서 운영하는 블로그들은 이미지를 드래그앤 드롭이나 파일 첨부를 통하여 쉽게 본문에 이미지를 삽입할 수 있는데, Jekyll 블로그에서는 따로 이미지를 `asset` 폴더에 분류해서 넣어주거나, [Google Photo](https://photos.google.com/?hl=ko) 와 같은 이미지 클라우드 서비스에 업로드를 한 뒤에, 이미지 경로를 잡아줘야한다. 개인적으로 가장 아쉬운 점이다.

![placeholder](http://placehold.it/800x400 "Large example image")
![placeholder](http://placehold.it/400x200 "Medium example image")
![placeholder](http://placehold.it/200x200 "Small example image")


### Tables

마지막으로 표를 만드는 방법이다. 표를 만드는 것은 일반 `HTML` 문법과 동일하다.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

`<table>` `<tr>` `<td>` `<thead>` `<tbody>` 와 같이, `HTML`에서 사용하던 모든 태그들이 사용 가능하다.

> Jekyll 블로그의 첫 느낌은?

첫 포스팅은 `Jekyll`, `Markdown` 에 대해서 적어보았다.

이 글을 적으면서 느낀 점은 `Jekyll` 은 정말 개발자에 최적화 되어있다는 점이다.

포스트를 `Git` 을 통해서 업로드하고, 기존 블로그처럼 따로 에디터가 있는 것이 아니라, `Markdown` 이라는 문법으로 글을 써야한다.
Code Editor에서 바로 글을 작성하고 `Git` 을 통해서 바로 업로드가 가능하기 때문에, 코딩의 흐름이 깨지지 않는다는 큰 장점이 있다.

아직 블로그의 모든 기능이 완성되지 않았다. `Jekyll` 과 약 3일간의 삽질 끝에 이제 어느정도 블로그다운 모습을 갖추기 시작했다.
앞으로 글 검색 기능과 카테고리별로 분류하는 기능을 구현해야한다.

산 넘어 산..
