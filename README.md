# Kubernetes in action

This repository contains all the code (and some additional files) from my [Kubernetes in Action](https://k8s.si/book) book.

# 1부 OVERVIEW
## 1장. 쿠버네티스 소개
### 1.1 쿠버네티스 시스템의 필요성 이해
1.1.1 모놀리식 애플리케이션에서 마이크로서비스로 전환하기
1.1.2 애플리케이션에 일관된 환경 제공
1.1.3 지속적 전달로 이동: 데브옵스와 노옵스
### 1.2. 컨테이너 기술 소개
1.2.1 컨테이너 이해하기
1.2.2 도커 컨테이너 플랫폼 소개
1.2.3 rkt 소개: 도커의 대안
### 1.3 쿠버네티스 소개
1.3.1 쿠버네티스 기원에 대한 이해
1.3.2 넓은 시각으로 쿠버네티스 바라보기
1.3.3 쿠버네티스 클러스터 아키텍처 이해하기
1.3.4 쿠버네티스에서 애플리케이션 실행하기
1.3.5 쿠버네티스의 이점 이해하기
1.4 요약

## 2장. 도커와 쿠버네티스의 첫걸음
### 2.1 컨테이너 이미지의 생성, 실행, 공유
2.1.1 도커를 설치하고 Hello World 컨테이너 실행하기
2.1.2 간단한 Node.js 앱 만들기
2.1.3 이미지용 도커 파일(Dockerfile) 만들기
2.1.4 컨테이너 이미지 만들기
2.1.6 실행 중인 컨테이너 내부 탐색
2.1.7 컨테이너 중지 및 제거
2.1.8 이미지 레지스트리로 이미지 푸시하기
### 2.2 쿠버네티스 클러스터 설정
2.2.1 미니큐브를 사용한 로컬의 단일 노드 쿠버네티스 클러스터 실행
2.2.2 구글 쿠버네티스 엔진(GKE)에서 호스팅된 쿠버네티스 클러스터의 사용
2.2.3 alias와 kubectl 명령행 셋업하기
### 2.3 쿠버네티스에서 첫 번째 앱 실행하기
2.3.1 Node.js 앱 배포
2.3.2 웹 애플리케이션 액세스하기
2.3.3 시스템의 논리적 부분
2.3.4 애플리케이션 수평 확장하기
2.3.5 앱이 실행되고 있는 노드 검사하기
2.3.6 쿠버네티스 대시보드 소개
### 2.4 요약

# 2부 CORE CONCEPTS

## 3장. 포드: 쿠버네티스에서 컨테이너 실행하기
### 3.1 포드 소개
3.1.2 포드의 필요성 이해하기
3.1.2 포드 이해하기
3.1.3 컨테이너를 포드 전체에 적절하게 구성하기
### 3.2 YAML 혹은 JSON 파일 디스크립터로 포드 만들기
3.2.1 기존 포드의 YAML 디스크립터 검사하기
3.2.2 포드를 위한 간단한 YAML 디스크립터 만들기
3.2.3 kubectl을 사용해 포드 만들기
3.2.4 애플리케이션 로그보기
3.2.5 포드에 요청 보내기
### 3.3 라벨로 포드 구성하기
3.3.1 라벨 소개
3.3.2 포드를 만들 때 라벨 지정하기
3.3.3 기존 포드의 라벨 수정하기
### 3.4 라벨 셀렉터를 통한 하위 집합 나열하기
3.4.1 라벨 셀렉터를 사용해 포드 나열하기
3.4.2 라벨 셀렉터에서 다중 조건 사용하기
### 3.5 포드 스케줄링 제약을 위한 라벨과 셀렉터 사용하기
3.5.1 워커노드 분류를 위해 라벨 사용하기
3.5.2 노드 지정을 위한 포드 스케줄링 하기
3.5.3 하나의 지정된 포드에 스케줄링하기
### 3.6 포드에 주석 달기
3.6.1 객체의 주석 찾아보기
3.6.2 주석 추가 및 수정하기
### 3.7 그룹 리소스의 네임스페이스 사용하기
3.7.1 네임스페이스의 필요성 이해하기
3.7.2 다른 네임스페이스와 네임스페이스의 포드 찾아보기
3.7.3 네임스페이스 만들기
3.7.4 다른 네임스페이스의 객체 관리하기
3.7.5 네임스페이스가 제공하는 격리에 대해 이해하기
### 3.8 포드를 중지하고 삭제하기
3.8.1 이름으로 포드 삭제하기
3.8.2 라벨 셀렉터로 포드 삭제하기
3.8.3 전체 네임스페이스를 삭제해서 포드 삭제하기
3.8.4 네임스페이스가 유지되는 동안 모든 포드 삭제하기
3.8.5 네임스페이스의 (거의)모든 리소스 삭제하기
### 3.9 요약

## 4장. 리플리케이션 및 기타 컨트롤러: 관리되는 포드 배포
### 4.1 포드를 안정적으로 유지하기
4.1.1 liveness probe 소개
4.1.2 HTTP 기반의 liveness probe생성
4.1.3 동작 중인 liveness probe 보기
4.1.4 liveness probe의 추가 속성 구성하기
4.1.5 효과적인 liveness probe 생성하기
### 4.2 리플리케이션컨트롤러 소개
4.2.1 리플리케이션컨트롤러의 동작
4.2.2 리플리케이션컨트롤러 생성하기
4.2.3 실행 중인 리플리케이션컨트롤러 보기
4.2.4 리플리케이션컨트롤러의 범위 안팎으로 포드 이동
4.2.5 포드 템플릿 변경
4.2.6 수평 포드 스케일링
4.2.7 리플리케이션컨트롤러 삭제하기
### 4.3 리플리케이션컨트롤러 대신 리플리카셋 사용
4.3.1 리플리카셋과 리플리케이션컨트롤러 비교
4.3.2 리플리카셋 정의
4.3.3 리플리카셋 생성 및 검사
4.3.4 리플리카셋의 더욱 풍부한 라벨 셀렉터 사용하기
4.3.5 리플리카셋 정리하기
### 4.4 데몬셋으로 각 노드에 정확히 한 개의 포드 실행하기
4.4.1 데몬셋을 사용해 모든 노드에서 포드 실행
4.4.2 데몬셋을 사용해 특정 노드에서 포드를 실행
### 4.5 완료 가능한 단일 태스크를 수행하는 포드 실행
4.5.1 잡 리소스 소개
4.5.2 잡리소스의 정의
4.5.3 포드를 실행하는 잡 보기
4.5.4 잡에서 다수의 포드 인스턴스 실행
4.5.5 잡 포드를 완료하는 데 허용되는 시간 제한
### 4.6 잡을 주기적으로 또는 한번만 실행하도록 스케줄링
4.6.1 CronJob 만들기
4.6.2 스케줄된 잡의 실행 방법 이해
### 4.7 요약

## 5장. 서비스: 클라이언트가 포드를 검색하고 대화를 가능하게 함
### 5.1 서비스 소개하기
5.1.1 서비스 생성하기
5.1.2 서비스 검색하기
### 5.2 클러스터 외부에 존재하는 서비스 연결하기
5.2.1 서비스 엔드포인트 소개
5.2.2 수동으로 서비스 엔드포인트 설정하기
5.2.3 외부 서비스를 위한 별칭 생성
### 5.3 외부 서비스에서 외부 클라이언트로
5.3.1 NodePort 서비스 사용하기
5.3.2 외부 로드 밸런서를 통해 서비스 노출하기
5.3.3 외부 연결의 특성 이해하기
### 5.4 Ingress 리소스를 통해 외부로 서비스 노출하기
5.4.1 Ingress 리소스 생성하기
5.4.2 Ingress를 통해 서비스 액세스하기
5.4.3 동일한 Ingress를 통해 다수의 서비스 노출하기
5.4.4 TLS 트래픽을 처리하기 위해 Ingress 설정하기
### 5.5 포드가 연결을 수락할 준비가 되어 있을 때 신호 보내기
5.5.1 준비 프로브 소개
5.5.2 포드로 준비 프로브 추가하기
5.5.3 실제환경에서 준비 프로브의 역할 이해하기
### 5.6 각각의 포드를 찾기 위한 헤드리스 서비스 사용하기
5.6.1 헤드리스 서비스 생성하기
5.6.2 DNS를 통해 포드 발견하기
5.6.3 모든 포드 발견하기(심지어 준비되지 않은 포드까지)
### 5.7 서비스 문제 해결하기
### 5.8 요약

## 6장. 볼륨: 컨테이너에 디스크 스토리지 연결
### 6.1 볼륨 소개
6.1.1 예제에서 볼륨 설명
6.1.2 가능한 볼륨 유형 소개
### 6.2 볼륨을 사용해 컨테이너 간에 데이터 공유하기
6.2.1 emptyDir볼륨 사용하기
### 6.3 워커노드 파일 시스템에 액세스하기
6.3.1 hostPath 볼륨 소개
6.3.2 hostPath 볼륨을 사용하는 시스템 포드 검사
### 6.4 영구 스토리지 사용하기
6.4.1 포드볼륨에서 GCE 영구 디스크 사용하기
6.4.2 기본 영구 스토리지에서 다른 볼륨의 유형 사용하기
### 6.5 기본 스토리지 기술에서 포드 분리하기
6.5.1 PersistentVolumes(영구볼륨) 및PersistentVolumeClaims(영구볼륨클레임) 소개
6.5.2 PersistentVolume 생성
6.5.3 PersistentVolumeClaim을 생성해 PersistentVolume 할당하기
6.5.4 포드에서 PersistentVolumeClaim 사용하기
6.5.5 PersistentVolumes및 클레임 사용의 이점 이해하기
6.5.6 PersistentVolumes재활용하기
### 6.6 PersistentVolumes의 동적 프로비저닝
6.6.1 스토리지 클래스리소스를 통해 사용 가능한 스토리지 유형 정의하기
6.6.2 PersistentVolumeClaim의 스토리지 클래스 요청하기
6.6.3 스토리지 클래스를 지정하지 않고 동적 프로비저닝하기
### 6.7 요약

## 7장. ConfigMaps와 Secret: 애플리케이션 설정
### 7.1 컨테이너화된 애플리케이션 설정
### 7.2 컨테이너에 명령행 인자 전달
7.2.1 도커에서 명령과 인자 정의하기
7.2.2 쿠버네티스에서 명령과 인자를 재정의하기
### 7.3 컨테이너를 위한 환경 변수 설정하기
7.3.1 컨테이너 정의에 환경 변수 지정하기
7.3.2 변수 값에서 다른 환경 변수 참조하기
7.3.3 하드코딩된 환경 변수의 단점 이해하기
### 7.4 ConfigMap을 통한 설정의 분리
7.4.1 ConfigMaps 소개
7.4.2 ConfigMap 생성하기
7.4.3 컨테이너의 환경 변수로 ConfigMap 엔트리를 전달하기
7.4.4 ConfigMap의 모든 항목을 한번에 환경 변수로 전달하기
7.4.5 ConfigMap 항목을 명령행 인자로 전달하기
7.4.6 ConfigMap 엔트리를 파일로 노출하기 위해 ConfigMap 볼륨 사용하기
7.4.7 애플리케이션 다시 시작 없이 애플리케이션 설정 업데이트하기
### 7.5 컨테이너에 민감한 데이터 전달을 위한 Secret 사용하기
7.5.1 시크릿 소개
7.5.2 기본 토큰 Secret 소개
7.5.3 Secret 생성하기
7.5.4 ConfigMaps와 Secret 비교하기
7.5.5 포드에서 Secret 사용하기
7.5.6 image pull Secrets 이해하기
### 7.6 요약

## 8장. 애플리케이션에서 포드 메타데이터와 그 외의 리소스에 접근하기
### 8.1 Downward API를 통한 메타데이터 전달하기
8.1.1 사용 가능한 메타데이터 이해하기
8.1.2 환경 변수를 통한 메타데이터 노출하기
8.1.3 Downward API 볼륨 내의 파일을 통한 메타데이터 전달하기
### 8.2 쿠버네티스 API 서버와 통신하기
8.2.1 쿠버네티스 REST API 탐색하기
8.2.2 포드 내에서 API 서버와 통신하기
8.2.3 앰배서더 컨테이너와의 API 서버 통신 간소화
8.2.4 클라이언트 라이브러리를 사용해 API 서버와 통신
### 8.3 요약

## 9장. 디플로이먼트: 애플리케이션을 선언적으로 업데이트하기
9.1 포드에서 실행 중인 애플리케이션 업데이트하기
9.1.1 오래된 포드를 삭제하고 새로운 포드로 교체하기
9.1.2 새로운 포드의 스핀 업 및 오래된 포드 삭제하기
9.2 리플리케이션 컨트롤러를 통한 자동 롤링 업데이트 수행하기
9.2.1 애플리케이션 초기 버전 실행
9.2.2 kubectl을 통해 롤링 업데이트 수행하기
9.2.3 kubectl 롤링 업데이트가 더 이상 사용되지 않는 이유 이해하기
9.3 선언적으로 애플리케이션을 업데이트하기 위한 디플로이먼트 사용하기
9.3.1 디플로이먼트 생성하기
9.3.2 디플로이먼트 업데이트하기
9.3.3 디플로이먼트 롤백하기
9.3.4 롤아웃 속도 통제
9.3.5 롤아웃 프로세스 일시 중지
9.3.6 잘못된 버전의 롤아웃 방지
9.4 요약

## 10장. 스테이트풀셋: 복제된 스테이트풀 애플리케이션 배포하기
### 10.1 스테이트풀 포드 복제
10.1.1 각각 분리된 저장소를 갖는 다수의 복제본 실행하기
10.1.2 각 포드에 안정적인 ID 제공
### 10.2 스테이트풀셋 이해하기
10.2.1 스테이트풀셋과 레플리카셋 비교
10.2.2 안정적인 네트워크 ID 제공
10.2.3 각 스테이트풀 인스턴스에 안정적인 전용 스토리지 제공
10.2.4 스테이트풀셋의 보장 이해하기
### 10.3 스테이트풀셋 사용하기
10.3.1 앱 및 컨테이너 이미지 만들기
10.3.2 스테이트풀셋을 통한 애플리케이션 배포
10.3.3 실제로 포드를 동작해보기
### 10.4 스테이트풀셋에서 피어 발견
10.4.1 DNS를 통한 피어 검색 구현
10.4.2 스테이트풀셋 업데이트
10.4.3 클러스터된 데이터 저장소 사용
### 10.5 스테이트풀셋이 노드 장애를 처리하는 방법 이해하기
10.5.1 네트워크에서 노드 연결 해제 시뮬레이션
10.5.2 수동으로 포드 삭제
10.6 요약

# 3부 BEYOND THE BASICS
## 11장. 쿠버네티스 내부 이해하기
### 11.1 아키텍처 이해하기
11.1.1 쿠버네티스 컴포넌트의 분산 특성(nature)
11.1.2 쿠버네티스가 etcd 사용하는 방법
11.1.3 API 서버가 하는 일
11.1.4 API 서버가 클라이언트의 리소스 변화를 감지하는 방법 이해하기
11.1.5 스케줄러 이해하기
11.1.6 컨트롤러 매니저에서 실행되고 있는 컨트롤러 소개하기
11.1.7 Kubelet이 하는 일
11.1.8 쿠버네티스 서비스 프록시의 역할
11.1.9 쿠버네티스 애드온 소개하기
11.1.10 모두 함께 가져오기
### 11.2 컨트롤러의 상호협력 방식
11.2.1 관련된 컴포넌트 이해하기
11.2.2 이벤트 체인
11.2.3 클러스터 이벤트 관찰하기
### 11.3 실행 중인 포드 이해하기
### 11.4 상호 포드 네트워킹
11.4.1 네트워크는 어떤 모습이어야 하는가
11.4.2 네트워크의 동작 원리 깊이 알아보기
11.4.3 컨테이너 네트워크 인터페이스 소개
### 11.5 서비스의 구현 방식
11.5.1 kube-proxy 소개하기
11.5.2 kube-proxy가 iptables을 사용하는 방식
11.6 고가용성 클러스터 실행
### 11.6.1 앱의 가용성 높이기
11.6.2 쿠버네티스 컨트롤 플레인 컴포넌트의 가용성 높이기
### 11.7 요약

## 12장. 쿠버네티스 API 서버 보안
### 12.1 인증 이해하기
12.1.1 사용자와 그룹
12.1.2 서비스어카운트 소개
12.1.3 서비스어카운트 생성하기
12.1.4 포드에 서비스어카운트 할당하기
### 12.2 역할(롤)기반 접근 제어 클러스터 보안
12.2.1 RBAC 인증 플러그인 소개
12.2.2 RBAC 리소스 소개
12.2.3 롤과 롤바인딩 사용하기
12.2.4 클러스터롤과 클러스터롤바인딩 사용하기
12.2.5 디폴트 클러스터롤과 클러스터롤바인딩 이해하기
12.2.6 인증 권한을 현명하기 부여하기
### 12.3 요약

## 13장. 클러스터 노드와 네트워크의 보안
### 13.1 포드 내에서 호스트 노드의 네임스페이스 사용하기
13.1.1 포드에서 노드의 네트워크 네임스페이스 사용하기
13.1.2 호스트 네임스페이스를 사용하지 않고 호스트 포트에 바인딩
13.1.3 노드의 PID와 IPC 네임스페이스 사용하기
### 13.2 컨테이너 보안 컨텍스트 설정
13.2.1 특정 사용자로 컨테이너 실행
13.2.2 컨테이너가 루트로 실행하는 것을 방지하기
13.2.3 권한 모드에서 포드 실행
13.2.4 컨테이너에 개별 커널 기능 추가하기
13.2.5 컨테이너에서 기능 제거
13.2.6 프로세스가 컨테이너의 파일 시스템에 쓰는 것을 방지하기
13.2.7 컨테이너가 다른 사용자로 실행될 때 볼륨 공유하기
### 13.3 포드의 보안 관련 기능 사용 제한하기
13.3.1 PodSecurityPolicy 리소스의 소개
13.3.2 runAsUser, fsGroup, supplementalGroups 정책 이해하기
13.3.3 허용, 기본 값, 허용하지 않음 설정하기
13.3.4 포드가 사용할 수 있는 볼륨의 유형 제한하기
13.3.5 다른 사용자 및 그룹에 다른 PodSecurityPolicies 할당
### 13.4 포드 네트워크 분리
13.4.1 네임스페이스에서 네트워크 격리 사용
13.4.2 네임스페이스의 일부 포드만 서버 포드에 연결하도록 허용하기
13.4.3 쿠버네티스 네임스페이스 간 네트워크 격리하기
13.4.4 CIDR 표기법을 사용해 격리하기
13.4.5 포드 세트의 아웃 바운드 트래픽 제한하기
### 13.5 요약

## 14장. 포드의 계산 리소스 관리
### 14.1 포드 컨테이너의 리소스 요청
14.1.1 리소스 요청을 포함한 포드 만들기
14.1.2 리소스 요청이 스케줄링에 미치는 영향 이해
14.1.3 CPU 요청이 CPU 시간 공유에 미치는 영향 이해
14.1.4 사용자 지정 리소스의 정의와 요청
### 14.2 컨테이너에 사용 가능한 리소스 한계
14.2.1 컨테이너가 사용 가능한 리소스 양에 대한 엄격한 한계 설정
14.2.2 한계 초과
14.2.3 컨테이너의 앱이 한계를 확인하는 방법 이해
### 14.3 포드의 QoS 클래스 이해
14.3.1 포드에 대한 QoS 클래스 정의
14.3.2 메모리가 부족할 때 어떤 프로세스가 강제 종료되는지 이해하기
### 14.4 네임스페이스당 포드에 대한 기본 요청 및 한계 설정
14.4.1 LimitRange 리소스 소개
14.4.2 LimitRange 객체 만들기
14.4.3 한계 적용
14.4.4 기본 리소스 요청 및 한계 적용
### 14.5 네임스페이스에서 사용 가능한 총 리소스 한계
14.5.1 ResourceQuota 객체 소개
14.5.2 영구 스토리지에 할당량 지정
14.5.3 생성 가능한 객체 수 제한
14.5.4 특정 포드 상태 및 / 또는 QoS 클래스의 할당량 지정
### 14.6 포드 리소스 사용 모니터링
14.6.1 실제 리소스 사용량 수집 및 검색
14.6.2 리소스 사용 통계의 히스토리 저장 및 분석
14.7 요약

## 15장. 포드와 클러스터 노드의 오토스케일링
### 15.1 포드의 수평적 오토 스케일링
15.1.1 오토스케일링 프로세스 이해하기
15.1.2 CPU 사용률에 따른 스케일링
15.1.3 메모리 소비량에 기반한 스케일링
15.1.4 기타 및 사용자 지정 메트릭을 기반으로 한 오토스케일링
15.1.5 오토스케일링에 적합한 메트릭 항목 결정하기
15.1.6 복제본을 0으로 스케일링다운
### 15.2 포드의 수직적 오토 스케일링
15.2.1 리소스 요청 자동으로 구성하기
15.2.2 포드 실행 중 리소스 요청 수정하기
### 15.3 클러스터 노드의 수평적 스케일링
15.3.1 클러스터 오토스케일러 소개
15.3.2 클러스터 오토스케일러 활성화
15.3.3 클러스터 스케일다운 시 서비스 중단 제한하기
15.4 요약

## 16장. 고급 스케줄링
### 16.1 테인트와 톨러레이션을 사용해 특정 노드에서 포드 실행 제한하기
16.1.1 테인트와 톨러레이션 소개
16.1.2 노드에 사용자 정의 테인트 추가하기
16.1.3 포드에 톨러레이션 추가하기
16.1.4 테인트와 톨러레이션의 활용 방법 이해하기
### 16.2 특정 노드로 포드를 유인하기 위해 노드 친밀성 사용하기
16.2.1 하드 노드 친밀성 룰을 지정하기
16.2.2 포드를 스케줄링할 때 노드의 우선순위 지정하기
### 16.3 포드 친밀성 및 반친밀성으로 포드를 가깝게 위치하기
16.3.1 인터포드 친밀성을 사용해 동일 노드에 포드 배포하기
16.3.2 동일한 랙, 가용 영역 또는 지리적 위치에 포드 배포하기
16.3.3 엄격한 요구 사항 대신 포드 친밀성 선호도 표현하기
16.3.4 포드 반친밀성으로 포드를 서로 멀리해 스케줄링하기
### 16.4 요약

## 17장. 애플리케이션 개발을 위한 베스트 프렉티스
### 17.1 모든 것을 함께 가져오기
### 17.2 포드의 라이프사이클 이해하기
17.2.1 애플리케이션은 종료하고 재배치 해야 한다
17.2.2 죽은 포드 또는 부분적으로 죽은 포드의 재스케줄링
17.2.3 원하는 순서로 포드 시작하기
17.2.4 라이프사이클 훅 추가하기
17.2.5 포드 셧다운 이해하기
### 17.3 모든 클라이언트 요청이 올바르게 처리되도록 보장하기
17.3.1 포드가 시작할 때 클라이언트의 연결이 끊어짐을 방지하기
17.3.2 포드 셧다운 동안 연결이 끊어짐을 방지하기
### 17.4 쿠버네티스에서 애플리케이션을 쉽게 실행하고 관리할 수 있게 만들기
17.4.1 관리 가능한 컨테이너 이미지 만들기
17.4.2 이미지에 적절히 태그하고 imagePullPolicy를 현명하게 사용하기
17.4.3 단일 차원 라벨 대신 다차원 라벨 사용하기
17.4.4 주석을 통해 각 리소스 설명하기
17.4.5 프로세스가 종료된 원인에 대한 정보 제공하기
17.4.6 애플리케이션 로그 핸들링
### 17.5 개발과 테스트의 Best Practice
17.5.1 개발 과정에서 쿠버네티스 외부에서 애플리케이션 실행하기
17.5.2 개발 중 미니큐브 사용하기
17.5.3 버전 관리 및 리소스 매니페스트 자동 배포
17.5.4 YAML / JSON 매니페스트를 작성하는 대안으로 Ksonnet을 소개
17.5.5 CI(Continuous Integration) 및 CD(Continuous Delivery) 사용하기
### 17.6 요약

## 18장. 쿠버네티스 확장하기
### 18.1 사용자 지정 API 객체 정의하기
18.1.1 CustomResourceDefinitions 소개
18.1.2 사용자 지정 컨트롤러를 사용한 사용자 지정 리소스 자동화하기
18.1.3 사용자 지정 객체 검증하기
18.1.4 사용자 지정 객체에 사용자 지정 API 서버 제공
### 18.2 쿠버네티스 서비스 카탈로그를 이용한 쿠버네티스 확장
18.2.1 서비스 카탈로그 소개
18.2.2 서비스 카탈로그 API 서버 및 컨트롤러 관리자 소개
18.2.3 서비스 브로커 및 OpenServiceBroker API소개
18.2.4 프로비저닝과 서비스 사용하기
18.2.5 바인딩 해제와 프로비저닝 해제
18.2.6 서비스 카탈로그 이해
### 18.3 쿠버네티스 기반 플랫폼
18.3.1 레드햇 오픈시프트 컨테이너 플랫폼7
18.3.2 Deis 워크플로우와 Helm
### 18.4 요약
부록 A 다중 클러스터 환경에서 kubectl 사용하기
부록 B kubeadm을 이용한 다중 노드 클러스터 설정
부록 C 다른 컨테이너 런타임 사용하기
부록 D 클러스터 페더레이션

## Reference 
 > http://acornpub.co.kr/book/k8s-in-action#toc
