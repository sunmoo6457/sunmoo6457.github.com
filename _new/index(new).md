---
layout: page
tite: 테스트
tags: [new, Jekyll, theme, moon]
date: 2021-07-24
comments: false
---
<center><a href="http://taylantatli.github.io/Moon"><b>Moon</b></a> is a minimal, one column jekyll theme.</center>


## 글자크기 조정
# 매우 큰크기(#1개)
## 조금 큰크기(#2개)
### 보통(#3개)
#### 조금 작은 크기(#4개)
##### 아주 작은 크기(#5개)

## 기초 문법(파이썬)

{% highlight css %}
a = input("입력하세요:")
print(a)
#print(a+1)
b = int(a) + 1
print(b)

c = int(input("입력하세요:"))
print(c+5)
{% endhighlight %}

## 네이버 랭킹(오픈소스)

{% highlight css %}
'''requests을 import''' 
'''from random import randint 처럼 BeautifulSoup을 import'''
import requests
from bs4 import BeautifulSoup

'''naver영화랭킹 사이트에 접속하여 정보를 얻기, response는 객체(클래스로부터 만들어지는 변수를 객체라고하며, 여러 개의 값을 가짐)'''
response = requests.get('https://movie.naver.com/movie/sdb/rank/rmovie.nhn')
'''얻어진 정보인 response에서 text정보만 얻기(디버깅으로 확인)'''
html = response.text

'''얻은 text정보를 BeautifulSoup의 html.parser를 사용해서 html문서로 해석'''
'''soup는 BeautifulSoup로부터 얻어진 객체'''
soup = BeautifulSoup(html, 'html.parser')
ranking = 1

'''html문서인 soup을 패턴을 분석하여 정보를 얻음'''
for tag in soup.select('div[class=tit3]'):
    url = tag.get('href')
    '''strip함수는 문자열의 양쪽에 빈칸 제거'''
    print("\n" + str(ranking) + '위 : ' + tag.text.strip())	
    ranking = ranking + 1
{% endhighlight %}

## Getting Started

To learn how to install and use this theme check out the [Setup Guide](http://taylantatli.me/Moon/moon-theme/) for more information.
      
[Install Moon](https://github.com/TaylanTatli/Moon){: .btn}

