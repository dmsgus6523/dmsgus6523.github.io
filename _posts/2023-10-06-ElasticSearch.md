---
layout: single
title : ElasticSearch 개념 정리
---

## Elasticsearch

참고 : https://pearlluck.tistory.com/695 , https://the-dev.tistory.com/30, https://twofootdog.tistory.com/53, https://needjarvis.tistory.com/579,  https://cornswrold.tistory.com/556, https://choseongho93.tistory.com/231 , https://www.elastic.co/guide/kr/elasticsearch/reference/current/gs-basic-concepts.html
<br/><br/>


> Elasticsearch란  

Elasticsearch는 Apache Lucene 기반으로 만들어진 검색 엔진이며 Elasticsearch 개별적으로 사용 가능하고 아니면 ‘ELK Stack’ 으로 사용 되기도 한다
<br/><br/>

#### - ELK Stack
<div style="text-align:centerl">

|제목|내용|설명|
|------|---|---|
|테스트1|테스트2|테스트3|
|테스트1|테스트2|테스트3|
|테스트1|테스트2|테스트3|

|명칭|역할|
|:---|:---|
|Elasticsearch|Logstash 에서 받은 데이터를 색인 및 조회|
|Logstash|다양한 Resource (DB, File 등) 데이터를 수집, 집계, Parsing 하여 Elasticsearch에 수집한 데이터 전달|
|Kibana|Elasticsearch 검색 결과를 바탕으로 데이터 시각화 및 모니터링 지원|

</div>
<br/><br/>

#### - Elasticsearch 구성 &nbsp;(Elasticsearch 7.0 이후 기준)
- 클러스터 (Cluster)
  > 하나 이상의 Node(서버)가 모인 집합. 이를 통해 전체 데이터를 저장하고 모든 노드를 포괄하는 통합 색인화 및 검색 기능을 제공


- 노드 (Node) : 클러스터에 포함된 단일 서버
  >마스터 노드 : 인덱스 생성/삭제 등 클러스터 전반적 관리

  >데이터 노드 : 실질적인 데이터를 저장하며 검색,통계와 같은 데이터 관련 작업 관리


- 도큐먼트 (Document)
  >문서를 색인화 할 수 있는 기본 정보 단위, 단일 데이터 단위이며 JSON 형식

- 인덱스 (Index)
  >도큐먼트를 저장하는 논리적 구분

- 샤드 (Shard)
  >인덱스를 분산 저장하기 위해 쪼개 놓은 단위 저장소