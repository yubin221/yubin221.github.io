---
layout: post
title:  "교육은 또한 신속하고 단호하며 효과적인 사고를 위해 훈련시켜야 한다."
author: yubin
categories: [ 라이프스타일 ]
image: assets/images/3.jpg
beforetoc: "프리즘 형광펜은 매우 강력한 것입니다. 이 기사에서는 게시물을 편집하는 동안 실제로 수행할 수 있는 몇 가지 요령과 팁을 보여드리겠습니다. 요약에서 볼 수 있듯이 Tocs도 활성화됩니다."
toc: true
---
Memories 테마에는 Prism 형광펜이 통합되어 있습니다. 웹 사이트에 코드를 추가할 계획인 개발자의 경우 이 게시물에서 몇 가지 예를 보여드리겠습니다.


#### HTML

```html
<li class="ml-1 mr-1">
    <a target="_blank" href="#">
    <i class="fab fa-twitter"></i>
    </a>
</li>
```

#### CSS

```css
.highlight .c {
    color: #999988;
    font-style: italic; 
}
.highlight .err {
    color: #a61717;
    background-color: #e3d2d2; 
}
```

#### JS

```js
// alertbar later
$(document).scroll(function () {
    var y = $(this).scrollTop();
    if (y > 280) {
        $('.alertbar').fadeIn();
    } else {
        $('.alertbar').fadeOut();
    }
});
```

#### Python

```python
print("Hello World")
```

#### Ruby

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

#### C

```c
printf("Hello World");
```