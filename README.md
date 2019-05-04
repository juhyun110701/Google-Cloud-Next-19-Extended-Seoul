# Google-Cloud-Next-19-Extended-Seoul
###### 2019.04.27 11:00-16:00 at YangJae AT center

### Track1 beyond kubernetes (Istio, spinnaker, knative, kubeflow)

* micro service  
  * 속도형 개발에 좋음
  * enterprise에는 별로
  * micro service가 항상 좋은 것은 아님
  * life of request in the mesh
* DevOps
  * developer team use the platform by developing & deployment
  * DevOps팀이 따로 있어서 개발자들이 스스로 운영할 수 있게 해줌
  * DevOps team develop self service platform
  * 보통 3-5년 내에 DevOps팀이 빠짐(이것을 목표로 함)
* kubernetes
  * sidecar pattern(다른 ip와 소통)
  * 똑같은 application server라도 다 다름
  * pheonix server pattern(immutable server)
    * snow flakes server pattern → pheonix server pattern
    * 서버 배포할 때마다 새로 만듦  
* spinnaker
  * open-source, multi-cloud, continuous delivery platform
  * container monitoring stack
  * stackdriver
    * stackdriver logging 반드시 쓰자!
      * 검색 & 필터링
      * 외부 저장소(external storage)에 log 저장 가능
* Knative
  * Knative-based products
    * Google Cloud Run
    * Pivotal Function Service
    * Red Hat OpenShift
    * IBM Cloud Kubernetes Service
    * SAP Kyma
    * TriggerMesh
  * Blue-green deployment model
  
### Track1 Knative로 서버리스 워크로드 구현
  
  * Dev
    * data center → virtual machine → container → serverless
  * Faas (Function as a service)
    * function을 수행
    * dependency 때문에 제약조건 ↑
    * event → function → services
    * multi, hybrid cloud 사용 어려움
  * Knative
    * serverless 워크로드를 빌드, 배포, 관리하기 위한 kubernetes 기반 platform
    * source 중심
    * 컨테이너 기반 application
    * kubernetes cluster가 있으면 어디서나 실행
    * Knative Stack, Knative Build, Knative Serving, Knative Eventing
  * Cloud Run
    * google computing platform services
    * +)serverless : 모든 인프라가 추상화되어 비즈니스 로직에 집중할 수 있음
  * Cloud Run on GKE
    * Seamless
    * 운영 최소화
    * simple & serverless for developers

### Track1 구글의 차세대 데이터베이스 Cloud Spanner 맛보기

  * CAP theory
    * Consistency
    * Availability
    * Partition tolerance
  * Database 비교
    * Relational (SQL)
      * MySQL, PostgreSQL, Oracle, SQL server, DB2
    * Non-Relational (NoSQL)
      * Wide Column Store, Key value store, Document store, Graph, Search
  * Cloud Spanner
    * Relational semantics + Horizontal scale
    * Google Managed/Scalable/Relational Database Service
    * Cloud Spanner Architecture
      * cpu는 cpu대로 돌고 storage는 storage대로 돎
      * cpu에서 node 추가해도 storage는 영향 X (pointer 많이 씀)
        * storage : split으로 구분되어 있음(multi master 역할에 도움을 줌)
    * Use Cases
      * Transactional Consistency
      * Scale
      * Global Data
      * Database Consolidation
    * Workload for Cloud Spanner
      * Sharded RDBMS
      * Scalable relational data
      * Manageability/HA
      * Multi-region
    * Application Types
      * Mission-critical
      * SaaS
      * Gaming
    * Not appropriate Cases
      * Lift/Shift
      * DB 내 많은 비즈니스 로직
      * 호환성이 필요한 경우
      * 앱이 매우 낮은 지연시간에 민감한 경우

### Track2 G Suite + Playstore 

  * 관리자 입장에서의 G Suite
  * 공동 작업 가능 → 공동 생산성 향상
  * G Suite DLP
    * 주민등록번호, 카드번호 등의 정보를 검출해낼 수 있는 방법
    * 사전 정의된 contents를 자동으로 검출 → 관리자에게 통보 (구글의 OCR 기능 이용)
    * 트리거, 조건, 작업
  * Google Vault
    * 하루종일 감시 - 파일 생성, 수정, 삭제 전송 등 검출 가능
    * email, groups, hangout, drive file 지원
    * 전자증거개시제도 - 법적문제 생겼을 때 증거자료로 사용 가능
    * 기능
      * 단일화된 아카이브
      * 이메일, 채팅 데이터 보관
      * 관리자 도구 등
    * 이점
      * 비용 ↓
      * 법적준수(소송에 대한 위험요소 ↓) 등
  * G Suite MDM
    * Single console to manage your entire enterprise mobility
    * 모바일 기기
      * android sync
      * ios sync
      * google sync
    * 모바일 관리
      * one click setup
      * customizing
      * 회사 사용 앱
      * monitoring & 감사
      * 실행
    * 사내 앱
      * 아이콘에 가방 모양 표시
      * 같은 application이 2개가 될 수도 있음 (가방 모양 있는 것과 없는 것)
      * 관리 : 승인해주는 형식
      * 승인하면 내 기기에 모두 설치하게끔 함 (제거할 수 없게 할 수도 있음)
  * All G Suite Beta Programs
    * G Suite Add-ons
    * Hangout Chat Accelerated Program
    * Connected Sheets(Big Query)
    * Metadata in Google Drive
    * Google data connectors for Sheets
    * Currents Beta, new Google+
    * G Suite access with Context-aware
    
### Track2 Next 19' Extended Google Next 다녀왔어요!

  * Google Cloud Seoul Region
  * Anthos
    * 멀티 cloud platform
    * 개발, 배포, 보안, 운영 통합해줌
    * kubernetes 기반
  * Cloud Run
    * serverless environment
    * stackdriver 통한 monitoring
  * Cloud Run on GKE
    * GKE 위에서 Cloud Rung 실행
  * Cloud Data Fusion
    * 데이터 통합 solution
    * drag-and-drop으로 클릭 몇 번으로 가능
    * 별도 코드 작성하지 않아도 됨
  * Cloud Code
    * GCP 개발 플러그인
    * 앱 개발/배포 쉽게 도와줌
  * BigQuery
    * BI Engine (1초 미만 query 응답시간 + 높은 동시성 → BigQuery에 저장된 데이터를 분석)
    * Connected Sheets (새로운 모델 추가 + 전문지식 없어도 handling 가능)
    * BigQuery ML (K-Means Clustering + 행렬 인수분해 + 모델 임포트)
  * AutoML Tables
    * 모델 자동 작성/배포
  * AutoML Video Intelligence
    * 특정 tagging 통해 비디오 커스텀 모델 제작 가능
  * Document Understanding AI
    * 문서 내의 데이터 자동 분석
  * Contact Center AI
    * Google의 AI 통한 고객 관리
    * dialogflow enterprise 기술 사용해 자동 catalog화 + 분석
  * Cloud Dataflow SQL
    * 표준 sql 사용해서 일괄 처리, 스트림 데이터 처리 통합하는 파이프라인 구축 가능
  * Cloud BI Solution
    * Big Query 기반
    * 파트너사의 BI툴로 시각 분석 가능
    * BQ ML 통한 예측
    * BG GIS 통한 지리 분석
  * Open Source Project 협력
    * GCP와 오픈 소스의 협력
  * Managed Service for MS Active Directory
    * MS Active Directory 실행하는 Google Cloud Service
  * Apigee Hybrid
    * multi cloud 환경에서 api 관리
  * Google Cloud Storage ICE Cold Layer
    * 매우 저렴
  * Cloud Security Commang Center
    * GCP의 보안 중앙 센터
    * 예방 탐지 응답
    * 실시간 알림
  * Cloud SQL for PostgreSQL
  * Data Catalog
    * 통합 데이터 관리 서비스
    * serverless 환경에서 이용 가능
  * Android Built-in Security Key
    * 2차 비밀번호
  * G Suite Tool 강화
  * reCAPTCHA Enterprise
    * 사기성 호라동, 스팸으로부터 website 보호

### Track1 BQ ML CASTLE
  * GCP Services Related to AI
    * AutoML
    * BG ML
    * Cloud ML Engine
  * BQ ML Syntax
    * SQL만으로 ML 할 수 있음
  * Create Model → Evaluate Model → Prediction

<hr/>

###### 발표 자료 및 참고 자료

* [Track1 beyond kubernetes (Istio, spinnaker, knative, kubeflow)] https://bcho.tistory.com/  
* [Track1 Knative로 서버리스 워크로드 구현] https://www.slideshare.net/JinwoongKim8/knative?fbclid=IwAR1QolrNYOoVxy5DAuUGxkbfWrNHjBbudF9bZ2bD0tnhZpqX6FVqZdIXTng  
* [Track1 구글의 차세대 데이터베이스 Cloud Spanner 맛보기] https://medium.com/@jwlee98  
* [Track2 G Suite + Playstore] https://www.slideshare.net/JasonPark164/mdm-vault-dlp?fbclid=IwAR3SyZeFZVSQxEzuNd1rA8Mcc_ttlUiXiA36Iy5ByqJp8YNrE9v4z8hL7Sc  
* [Track2 Next 19' Extended Google Next 다녀왔어요!] https://drive.google.com/file/d/1iegfq0cOwxvMt_Bmia7bV5_EY7HePTE7/view?fbclid=IwAR2SzOcFs9q_f7mI-6PeeLU4873e2bDsNVW89nXelWxi2SrsCZNguvBhO3M  
* [Track1 BQ ML CASTLE] https://docs.google.com/presentation/d/10jYewv5mRoKbfgmSCYTtdxuZmDkniCcwtq5vq8NMF6c/edit?fbclid=IwAR1XwS7gAITw6kl5Z3V8pELAqdN66j1lW69xuX9RS-ONPafThfdNdPnsqIc#slide=id.g43abcd927d_0_104
