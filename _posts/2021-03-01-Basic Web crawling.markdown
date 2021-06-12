---
title:  "Basic Web crawling "
date:   2021-03-05 15:04:23
categories: [Web_crawling]
tags: [Web_crawling]
---
In [31]:
import requests
from bs4 import BeautifulSoup
#라이브러리 임포트 
#requests : 웹페이지 가져오기 라이브러리
#bs4(beautifulsoup) : 웹페이지 분석 라이브러리

res = requests.get('https://v.media.daum.net/v/20170615203441266')
#웹페이지 가져오기

soup = BeautifulSoup(res.content,'html.parser')
#웹페이지 파싱하기

mydata = soup.find('title')
#필요한 데이터 추출하기

print(mydata.get_text())
#추출한 데이터 활용하기
# res.content
print(mydata)
