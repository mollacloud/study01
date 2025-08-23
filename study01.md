# 예상문제

1. **Azure Resource RBAC Policy: 관리그룹 및 구도에 계층형 구조에 따른 사용자권한 제어**
    - [https://learn.microsoft.com/ko-kr/azure/role-based-access-control/scope-overview](https://learn.microsoft.com/ko-kr/azure/role-based-access-control/scope-overview)
    - Tip) Azure RBAC 이해도와 Build-in Policy 조사 및 검증

1. **Azure Storage Account(Object Storage) Tier 별 특성**
    - [https://learn.microsoft.com/ko-kr/azure/storage/blobs/access-tiers-overview](https://learn.microsoft.com/ko-kr/azure/storage/blobs/access-tiers-overview)
- Tip) Storage Account
    - Disk, File, Object
    - Ojbect Tier, SKU 특징
    - 상황에 맞춰서 어떤게 괜찮은지?
    - LifeCycle Event
    - Object 컨테이너에 붙이면 1주일이상 삭제, webhook 구조

1. Azure Storage Account Life Cycle Event 활용법: Event 처리를 위한 구성방법, 데이터 유지관리 등 자동화 기능에 대한 이해
    - ○([https://learn.microsoft.com/ko-kr/azure/storage/blobs/lifecycle-management-overview](https://learn.microsoft.com/ko-kr/azure/storage/blobs/lifecycle-management-overview))
    - ○([https://learn.microsoft.com/ko-kr/azure/storage/blobs/storage-blob-event-overview](https://learn.microsoft.com/ko-kr/azure/storage/blobs/storage-blob-event-overview))
- Tip_구성할때 DMZ 외부 트래픽 받고, web-was 연결하고 외부 연결하려면 어떻게해야하는지? NAT 설정, 이런 구조 서비스가 어떻게 되는지?

1. VNet 구성시 Inbound(LB), Outbound(NAT)구성방법과 기술구조/네트웍 흐름 이해
    - ○([https://learn.microsoft.com/en-us/azure/nat-gateway/nat-gateway-design](https://learn.microsoft.com/en-us/azure/nat-gateway/nat-gateway-design))

1. Saving Plan, Reserved Instance을 활용한 비용절감 방안 이해
- ○([https://learn.microsoft.com/ko-kr/azure/cost-management-billing/savings-plan/savings-plan-compute-overview](https://learn.microsoft.com/ko-kr/azure/cost-management-billing/savings-plan/savings-plan-compute-overview))

비용 절감
- 계약 방식 RI/SP
- SP, RI 에 따른 Azure service 신청 가능한 서비스 정류

1. **Azure Storage Account 특징과 차이**
    - ○([https://learn.microsoft.com/ko-kr/azure/storage/common/storage-introduction?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json](https://learn.microsoft.com/ko-kr/azure/storage/common/storage-introduction?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json))
    - ○([https://learn.microsoft.com/ko-kr/azure/storage/blobs/storage-feature-support-in-storage-accounts](https://learn.microsoft.com/ko-kr/azure/storage/blobs/storage-feature-support-in-storage-accounts))
- 저장 용량, 추가/삭제, 기능차이
    - 상품에 따른 용도, 언제 쓰이는지 (ex_ blob , disk 는 언제?)

1. VMSS 특성에 대한 이해
    - ○([https://learn.microsoft.com/ko-kr/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-orchestration-modes](https://learn.microsoft.com/ko-kr/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-orchestration-modes))
- vmss 처리방식 흐름, 오토스케일 구현시에 어떻게? 주의점? 어떤건 지원? 어떤건 미지원?
    - build 배포 흐름도 등
    - VM 스킬셋, 로드밸랜서 연결 어떻게 되는지?
    - 디테일x

1. DNS Resolver 구성법: AWS/Azure/Onpremise DNS동기화를 위한 구성과 필요한 Network 구성
    - ○([https://learn.microsoft.com/ko-kr/azure/dns/dns-private-resolver-overview](https://learn.microsoft.com/ko-kr/azure/dns/dns-private-resolver-overview))
    - ○([https://learn.microsoft.com/ko-kr/azure/dns/dns-private-resolver-get-started-portal](https://learn.microsoft.com/ko-kr/azure/dns/dns-private-resolver-get-started-portal))

DNS reSolver
- op prem, Azure 간의 dns Sync 방법
- 방화벽 어떻게? 등

1. AKS Monitoring를 활용한 자원/Workload 모니터링 이해
    - ○([https://learn.microsoft.com/ko-kr/azure/azure-monitor/autoscale/autoscale-overview](https://learn.microsoft.com/ko-kr/azure/azure-monitor/autoscale/autoscale-overview))
    - ○([https://learn.microsoft.com/ko-kr/azure/azure-monitor/platform/monitor-azure-resource](https://learn.microsoft.com/ko-kr/azure/azure-monitor/platform/monitor-azure-resource))

AKS Monitoring 구성법
- Azure motnitor 내 세부적인 서비스, VM/컨테이너/네트워크
- Agent 설치 어떻게? 등

1. Azure 기반 Messaging 구성법 및 필요로 하는 Azure 서비스
    - ○([https://learn.microsoft.com/ko-kr/azure/messaging-services/](https://learn.microsoft.com/ko-kr/azure/messaging-services/))

Azure 메시징, 필요로하는 서비스
- Azure bus 등 4개의 특징 이해
- 요구사항에 따라 어떤거 선택해야하는지? 개념적인 문제

1. AKS Autoscale 이해: POD, Node(Node Group)
    - ○([https://learn.microsoft.com/ko-kr/azure/aks/cluster-autoscaler?tabs=azure-cli](https://learn.microsoft.com/ko-kr/azure/aks/cluster-autoscaler?tabs=azure-cli))
    - ○([https://kubernetes.io/ko/docs/tasks/run-application/horizontal-pod-autoscale/](https://kubernetes.io/ko/docs/tasks/run-application/horizontal-pod-autoscale/))

AKS AUtoscailng
- 컨테이너레벨
- Node 레벨
- 이벤트 발생하고 어떤 일이 되는 지?
- scale -in/out 둘다

1. AKS 설치 구성에 대한 이해: Ingress Controller, CNI, CSI (최근 업데이트 된 내용 확인 필요)
    - ○([https://learn.microsoft.com/ko-kr/azure/aks/learn/quick-kubernetes-deploy-terraform?pivots=development-environment-azure-cli](https://learn.microsoft.com/ko-kr/azure/aks/learn/quick-kubernetes-deploy-terraform?pivots=development-environment-azure-cli))
    - ○([https://learn.microsoft.com/ko-kr/azure/aks/concepts-network-cni-overview](https://learn.microsoft.com/ko-kr/azure/aks/concepts-network-cni-overview))
    - ○([https://learn.microsoft.com/ko-kr/azure/aks/concepts-network-ingress](https://learn.microsoft.com/ko-kr/azure/aks/concepts-network-ingress))
    - ○([https://learn.microsoft.com/ko-kr/azure/aks/concepts-storage](https://learn.microsoft.com/ko-kr/azure/aks/concepts-storage))

AKS Add-on
- Ingress Controller, CNI, CSI 이해도
- 최근 내용 확인, 설치에 대한 용어 이해

1. AKS PV/PVC 사용법 및 CSI구성에 따른 Azure Files 특성 이해
- 데이터 보관주기, lifecycle
    - azure files, 맵핑 어떻게?

1. AKS Overlaynetwork 구성에 대한 이해: POD IP 할당과 특징
- Pod IP 어떻게 할당?
    - 안썼을때 어떻게 할당되는 지?

1. Github Action의 의 기술구조 이해(Trigger Event 등)
    - ○([https://docs.github.com/ko/actions/reference/workflow-syntax-for-github-actions](https://docs.github.com/ko/actions/reference/workflow-syntax-for-github-actions))
- yaml file
    - evnet, task, 구조 워크플로 구문
    - 언제 트리거 되는지? 어떤 Action 을 하는지?

> CICD 기본 개념
> 
> - ○([https://docs.github.com/ko/actions/how-tos/security-for-github-actions/security-guides/using-secrets-in-github-actions](https://docs.github.com/ko/actions/how-tos/security-for-github-actions/security-guides/using-secrets-in-github-actions))

- 접근 부여, 언디까지 권한 줘야하는지

> Azure RBAC 이해: Built in Role/Role Group 활용법
> 

- Build Policy 알아야함

> Azure Loadbalancer 이해: 가용성, 분산처리 특징과 Coverage
> 
> - ○([https://learn.microsoft.com/ko-kr/azure/load-balancer/skus](https://learn.microsoft.com/ko-kr/azure/load-balancer/skus))

Azure LB 이해
- 글로벌, 리전, zone 서비스
- 도메인을 사면 어느 범위까지만 사용 가능하지
- 저널 서비스, 리쥬널 서비스 내에서만 가능
- ex) 글로벌인경우 비싼거 전체 다, 어떤건 리전만 아시아만
- 글로벌하려면 어떻게 주문해야하는지?

> AKS권한 관리 방식: K8S의 IAM처리 방식의 이해 Entra ID, Service Account 등 이해와 차이점
> 
> - ○([https://learn.microsoft.com/ko-kr/azure/aks/enable-authentication-microsoft-entra-id](https://learn.microsoft.com/ko-kr/azure/aks/enable-authentication-microsoft-entra-id))

AKS 권한관리
- Entra ID 바인딩 처리
- SA 명시적으로 토큰

> Container 기본 개념 및 Dockerfile 이해
> 

컨테이너 이해
- DockerFile 이해
- Run apt update & apt install nginx
run apt update
apt install nignx
이렇게 연결하는지와 따로 쓰는거에 대한 차이점    
- 도커파일은 이미지형태로 계층으로 올라감
- 어떻게 하느냐에따라 속도가 달라짐

> Support VM OS SKU 및 Migration 방법(제약사항)
> 
> - ○([https://learn.microsoft.com/en-us/azure/migrate/server-migrate-overview?view=migrate-classic](https://learn.microsoft.com/en-us/azure/migrate/server-migrate-overview?view=migrate-classic))

Support VM OS SKU 및 마이그레이션 방법(제약사항
- VMware 마이글이션할때 방법

> ●AKS 장애 대응:Node Not Ready,POD Pending 등 이슈 원인 파악 및 대응방법 이해
> 

AKS 장애(Node net Ready, Pod Pending등)
- 원인에 대한 이해

> ●Azure Network의 암호화 방식 단답식
> 

검색 잘해라

- ●AKS의 이슈상황 원인과 대응방안 역량: POD Faile, FackOff, POD Schedule Design, Nodegroup scale in 시 고래해야할 POD Life Cycle 설정

서술형) 

- Pod 줄인
    - 스케일 -in /out 서비스에 503 504 안나오게 하는 방법
    - Node group 개수 변경에 따라 taint 등 policy 골고루 배분방법

- ●용도에 따른 Azure Storage Account 선택

- ●RAG를 위한 저장소/DBMS Azure 서비스 선택

RAG를 위한 DBMS
- 문제 그대로 답

- ●Azure Function Tier 특징이해와 선택(대용량 Batch를 위한 Function Tier)
    - ○([https://learn.microsoft.com/ko-kr/azure/azure-functions/durable/](https://learn.microsoft.com/ko-kr/azure/azure-functions/durable/))

Azure Function Tier
- 용도 신뢰성을 위한 어떤 fucniotn 사용?

- ●Azure Disk 관리 운영 상의 특징: 크기 조절방법 및 제약 사항, OS Reboot 필요 등

VM DISK
- 운용상 제한적

- ●Terraform 내용 이해

테라폼
- 프로비저닝 코드에 따라 구성이 잘 못된건?
- 테라폼 씬텍스
- Azure 와 테라폼 간의 구조가 다름

- ●비용 최적화 방안: Saving Plan, RI, Size 조절, VM Schedule 방안에 대한 이해와 적용법

비용최적화
- 계약(RI/SP)
- 사이징  줄이기
- 저녁에 끄기
이중에 효율적인 거 순서대로

- ●PV, PVC 운영상의 특징(Azure File)

PV, VPC(Azure Files)
- Private 하게 private  endpotin

- ●Express Route 개념 및 SKU Tier 특징 이해
- 3가지
    - 커버리지 , 글로벌 , 가용성 등 특징

- ●DNS Resolver 방법 및 개념

- ●Istio Service Mesh 개념과 각 자원/서비스 용어와 이해

Istio service mesh
- 문서에 gw, virtual host 냐 이런 용어를 알면 문제 풀수 있음

- ●AKS 성능 개선에 대한 이해

- Size , 리소스 컨트롤, 워크로드 어떻게 배분해야하는ㄴ지?

- ●Node Pool 개념 이해와 운영 방안 특징
- System pool
    - User nodepool
    - 용도에 따라 배치하는 방법

- ●CICD Pipeline 구성시 Credential관리 주의 사항에 대한 이해와 방법

- 크레덴셜 관리 이해

- ●Github Action의 기본구성 이해와 기본 Task명에 대한 이해

- 실행해야하는 TASK / event, Triger

- ●Storage의 암호화 방식에 대한 이해
- 검색 잘하면됨 (함정문제)
    - db 컬럼 암호화/ 내용에 섞어놓음

- ●Azure Native 보안 서비스 이해

- ●Azure Monitoring 서비스 활용시 비용적인 측면의 Log Data 관리 방법에 대한 이해
- ●Migration From VMWare VM: 제약조건, 구성법 등
- ●PV/PVC with Azure File 구성시 필요한 Network 설정

- ●Data Platform 구축시 요구사항정의와 그에 따른 Cloud특징(잘 읽어보면됨)

- 기술적인 것보다 작 읽고 Data Platform 특징 잘읽어보기

- ●구독 할당 및 관리에 대한 이해

구독 할당
- 구독 Policy 에따라 A가 할수 있냐 없냐 
하려면 어떤게 필요?

- ●Vnet Flow log 서비스 종류와 특징 이행

- 새로운 제품이 나왔는데 기존/ 새로운제품 차이

- ●AKS with GPU 구성시, 자원을 효율적으로 사용하기 위한 방안
- 컨테이너에대한 request/limit 차이
    - QoS Request vs Limit
    
    burst Best Effors Gaurantee 이런거 이해
    
    - GPU Shared는 안됨
    - Request GPU: 500m
    
    옛날거는 저렇게해도 점유해버림
    
    이럴거면 어떻게?
    
    Shared 지원하는건? nvidia plugin  등 이런거 어떻게? 종류에 따라
    

[문제 힌트]
- Azure Durable Function
- GSLB
- 컨테이너의 qos 컨트롤
- Scale In/Out 시 Ingress 연결 끊김 해결방법 (서술형)
- Docker Image 나누는거 합치는거
- Attched DIsk 의 용량 변경 시 OS 재기동 여부 등
- File Share 관련 PE 붙히는 보기가 정답인 문제도 있음
- 큐 테이블 파일 등등은 안봐도 됨

[출제 비율]
Storage Account - 1/3
컨테이너/k8s - 1/3