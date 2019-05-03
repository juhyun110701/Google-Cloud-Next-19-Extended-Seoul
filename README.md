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

### G Suite + Playstore 

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
    
### Next 19' Extended Google Next 다녀왔어요!
