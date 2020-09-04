---
title: Elasticsearch 기본 개념 잡기
author: JONGSKY
date: 2020-09-04 23:00:00
categories: [Elasticsearch]
tags: [elasticsearch, 검색엔진]
toc: false
---

이전에 했던 특허검색 프로젝트에서 Django에서 제공해주는 것을 이용해 사용했었습니다. 특허 검색의 속도문제 등을 해결하기 위해 elasticsearch를 활용해 검색엔진을 구축하려고 합니다. 이에 앞서 ```elasticsearch```란 무엇이고 왜 사용하는지에 대해서 알아보려고 합니다.

# Elasticsearch

## Elasticsearch는 무엇인가

- Java 오픈 소스 분산 검색 엔진
- 방대한 양의 데이터를 신속하게 (거의 실시간, NRT)
    - NRT : Near Real Time
    - 저장, 검색, 분석 가능

- 단독사용 가능 또는 ELK 스택으로 사용
    - ELK : Elasticsearch / Logstash / Kibana

```Elasticsearh```는 텍스트 ,숫자, 위치 기반 정보, 정형 및 비정형데이터 등 모든 유형의 데이터를 위한 분산형 오픈 소스 검색 및 분석 엔진입니다.

## ELK 스택이란 무엇인가

![image](https://user-images.githubusercontent.com/40276516/92246430-b1306a00-ef00-11ea-80d5-93eacdb534bb.png)

- Logstash : 다양한 소스( DB, csv파일 등 )의 로그 또는 트랜잭션 데이터를 수집, 집계, 파싱하여 Elasticsearch로 전달
- Elasticsearch : Logstash로부터 받은 데이터를 검색 및 집계를 하여 필요한 관심 있는 정보를 획득
- Kibana : Elasticsearch의 빠른 검색을 통해 데이터를 시각화 및 모니터링

## 어디에 사용될까?

- 애플리케이션 검색
- 웹사이트 검색
- 엔터프라이즈 검색
- 로깅과 로그 분석
- 인프라 메트릭과 컨테이너 모니터링
- 애플리케이션 성능 모니터링
- 위치 기반 정보 데이터 분석 및 시각화
- 보안 분석
- 비즈니스 분석

## 왜 사용하는가?

- 빠르다
- 본질상 분산적입니다.
- 광범위한 기능 세트와 함께 제공됩니다.

## 왜 빠른가?

- 역색인 때문이다.

예를 들어 ```Python```이란 단어가 포함된 문서를 찾는다고 가정합니다. 일반적으로는 처음부터 끝까지 문서를 읽어야만 원하는 결과를 얻을 수 있습니다. 하지만 역색인 구조는 해당 단어만 찾으면 단어가 포함된 모든 문서를 알 수 있기 때문에 빠르게 찾을 수 있습니다.

## RDB와 Elasticsearch의 차이점

![image](https://user-images.githubusercontent.com/40276516/92245947-0ae46480-ef00-11ea-84a0-cd5e132a9976.png)

## 어떤 프로그랭 언어를 지원하는가?
```Elasticsearch```는 다양한 언어를 지원하며, 다음을 위한 공식 클라이언트가 제공됩니다.

- 자바
- 자바스크립트(Node.js)
- Go
- .NET(C#)
- PHP
- Perl
- Python
- Ruby


# 출처

- [elastic-kr](https://www.elastic.co/kr/what-is/elasticsearch)
- [[2D1]Elasticsearch 성능 최적화](https://www.slideshare.net/deview/2d1elasticsearch)
- [[Elasticsearch] 기본 개념잡기](https://victorydntmd.tistory.com/308)
- [ELK stack tutorial](https://www.edureka.co/blog/elk-stack-tutorial/)