---
layout: single
title : ElasticSearch 개념 정리
categories: project
author_profile: false
---

## 1. Elasticsearch
#### 1.1. Elasticsearch란  
<div class="contents_box">
  Elasticsearch는 Apache Lucene 기반으로 만들어진 검색 엔진이며 Elasticsearch 개별적으로 사용 가능하고<br/>‘ELK Stack’ 으로 사용 되기도 한다
</div>

#### 1.2. ELK Stack
<div class="contents_box">
  <div style="text-align:centerl">
    <table class="inner_table_font">
      <th>명칭</th>
      <th>역할</th>
      <tr>
        <td>Elasticsearch</td>
        <td>Logstash 에서 받은 데이터를 색인 및 조회</td>
      </tr>
      <tr>
        <td>Logstash</td>
        <td>다양한 Resource (DB, File 등) 데이터를 수집, 집계, Parsing 하여 Elasticsearch에 수집한 데이터 전달</td>
      </tr>
      <tr>
        <td>Kibana</td>
        <td>Elasticsearch 검색 결과를 바탕으로 데이터 시각화 및 모니터링 지원</td>
      </tr>
    </table>
  </div>
</div>

#### 1.3. Elasticsearch 구성
<div class="contents_box">
  <div class="minimal_contents_box">
    (Elasticsearch 7.0 이후 버전을 기준으로 함)
  </div>
  <table>
    <tr>
      <td>클러스터 (Cluster)</td>
      <td>하나 이상의 Node(서버)가 모인 집합. 이를 통해 전체 데이터를 저장하고 모든 노드를 포괄하는 통합 색인화 및 검색 기능을 제공</td>
    </tr>
    <tr>
      <td>노드 (Node)</td>
      <td>클러스터에 포함된 단일 서버</td>
    </tr>
    <tr>
      <td></td>
      <td>
        <table class="inner_table_font">
          <tr>
            <td>마스터 노드</td>
            <td>인덱스 생성/삭제 등 클러스터 전반적 관리</td>
          </tr>
          <tr>
            <td>데이터 노드</td>
            <td>실질적인 데이터를 저장하며 검색,통계와 같은 데이터 관련 작업 관리</td>
          </tr>
        </table>
      </td>
    </tr>
    <tr>
      <td>도큐먼트 (Document)</td>
      <td>문서를 색인화 할 수 있는 기본 정보 단위, 단일 데이터 단위이며 JSON 형식</td>
    </tr>
    <tr>
      <td>인덱스 (Index)</td>
      <td>도큐먼트를 저장하는 논리적 구분</td>
    </tr>
    <tr>
      <td>샤드 (Shard)</td>
      <td>인덱스를 분산 저장하기 위해 쪼개 놓은 단위 저장소</td>
    </tr>
  </table>


<div class="ref_contents">
  <span>참고자료</span>
  <div class="ref_list">
  https://pearlluck.tistory.com/695 , https://the-dev.tistory.com/30 , https://twofootdog.tistory.com/53 ,<br/>https://needjarvis.tistory.com/579 , https://cornswrold.tistory.com/556 ,https://choseongho93.tistory.com/231 ,<br/>https://www.elastic.co/guide/kr/elasticsearch/reference/current/gs-basic-concepts.html
  </div>
</div>