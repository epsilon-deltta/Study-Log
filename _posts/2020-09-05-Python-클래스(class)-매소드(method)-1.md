---
title: Python 클래스(class) & 매소드(method) - 1
author: JONGSKY
date: 2020-09-05 3:00:00
categories: [Python]
tags: [python, class, method]
toc: false
---

## 클래스 기반 개발 설명

    - 절차 지향 vs 객체 지향
    - 객체 지향 프로그래밍 장점
    - 클래스 기반 코딩 실습

# 절차 지향 VS 객체 지향

## 절차지향(Procedural Programming)이란

**절차지향 프로그래밍**이란 물이 위에서 아래로 흐르는 것 처럼 순차적인 처리가 중요시 되며 프로그램 전체가 유기적으로 연결되도록 만드는 프로그래밍 기법입니다. 대표적인 **절차지향 언어**에는 **C언어**가 있습니다. 이는 컴퓨터의 작업 처리 방식과 유사하기 때문에 객체지향 언어를 사용하는 것에 비해 더 빨리 처리되어 시간적으로 유리합니다. 옛날에는 하드웨어와 소프트웨어의 개발 속도차이가 크지 않았지만 소프트웨어 언어의 발달과 컴파일러의 발달로 **하드웨어가 소프트웨어의 발달을 따라오지 못하는 상황**이 발생했습니다. 이는 객체지향언어가 등장하는 계기가 되었습니다. 객체지향 프로그래밍은 개발하려는 것을 **기능별로 묶어 모듈화** 함으로써 하드웨어가 같은 기능을 중복으로 연산하지 않도록 하고, 모듈을 재활용하기 때문에 하드웨어의 처리량을 획기적으로 줄여주었습니다.

## 객체지향(Object Oriented Programming)이란

**객체지향**이란 **실제 세계를 모델링하여 소프트웨어를 개발하는 방법**입니다. 객체지향 프로그래밍에서는 데이터와 절차를 하나의 덩어리로 묶어 생각합니다. 이는 마치 컴퓨터 부품들을 따로 구매하여 컴퓨를 조립하는 것과 비슷한 방법입니다.

## 객체 지향 프로그램(OOP)인 파이썬에는 어떤 장점이 있을까?

- 코드의 재사용
- 코드 중복 방지
- 유지보수
- 대형프로젝트

## 클래스 기반 코딩 실습

```
# 차량 1
car_company_1 = 'Ferrari'
car_detail_1 = [
    {'color':'White'},
    {'horsepower':400},
    {'price':8000}
]
# 차량 2
car_company_2 = 'Bmw'
car_detail_2 = [
    {'color':'Black'},
    {'horsepower':270},
    {'price':5000}
]
# 차량 3
car_company_3 = 'Audi'
car_detail_3 = [
    {'color':'Silver'},
    {'horsepower':300},
    {'price':6000}
]
```
```
# 리스트 구조
# 관리하기가 불편하다
# 인덱스 접근 시 실수 가능성, 삭제 불편
car_company_list = ['Ferrari','Bmw','Audi']
car_detail_list = [
    {'color':'White','horsepower':400,'price':8000},
    {'color':'Black','horsepower':270,'price':5000},
    {'color':'Silver','horsepower':300,'price':6000}
]
```
```
# 딕셔너리 구조
# 코드 반복 지속, 중첩 문제(키), 키 조회 예외 처리 등
car_dicts = [
    {'car_company':'Ferrai','car_detail': {'color':'White','horsepower':400,'price':8000}},
    {'car_company':'Bmw','car_detail': {'color':'Black','horsepower':270,'price':5000}},
    {'car_company':'Audi','car_detail': {'color':'Silver','horsepower':300,'price':6000}}
]
```
```
# 클래스 구조
# 구조 설계 후 재사용성 증가, 코드 반복 최소화, 메소드 활용
class Car():
    def __init__(self, company, details):
        self._company = company
        self._details = details
        
    # 비공식적인, 사용자입장의 출력문      
    def __str__(self):
        return 'str : {} - {}'.format(self._company, self._details)
    
    # 객체를 그대로 사용할 때, 개발자입장의 출력문
    def __repr__(self):
        return 'repr : {} - {}'.format(self._company, self._details)
```


## 출처

- [위키백과 - 절차적 프로그래밍](https://ko.wikipedia.org/wiki/%EC%A0%88%EC%B0%A8%EC%A0%81_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)
- [위키백과 - 객체지향프로그래밍](https://ko.wikipedia.org/wiki/%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)
- [절차지향VS객체지향](https://brownbears.tistory.com/407)
- [우리를 위한 프로그래밍:파이썬 중급](https://www.inflearn.com/course/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%A4%91%EA%B8%89-%EC%9D%B8%ED%94%84%EB%9F%B0-%EC%98%A4%EB%A6%AC%EC%A7%80%EB%84%90)