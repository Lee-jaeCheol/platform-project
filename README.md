# 소셜 네트워킹 & 일정 관리 플랫폼

## 프로젝트 설명
이 프로젝트는 **Spring Boot**와 **React**를 기반으로 구축된 소셜 네트워킹 및 일정 관리 플랫폼입니다. 주요 기능으로는 비정형 데이터 저장, 실시간 알림, 일정 기반 알림 및 이미지 업로드 기능 등이 포함됩니다. 아래는 기술 스택과 주요 설정에 대한 설명입니다.

---

## 기술 스택

### **백엔드**
- **Spring Boot**: 백엔드 프레임워크
- **Thymeleaf/React**: 템플릿 엔진 및 프론트엔드 라이브러리
- **Spring Security + JWT**: 인증 및 권한 관리
- **Quartz Scheduler**: 일정 기반 알림 처리
- **WebSocket/STOMP**: 실시간 알림 기능 구현

### **데이터베이스**
- **MongoDB**: 비정형 데이터 저장
- **Elasticsearch**: 검색 기능 강화

### **이미지 관리**
- **AWS S3** 또는 **Cloudinary**: 이미지 업로드 및 관리

### **배포 및 관리**
- **Docker**: 컨테이너화
- **Kubernetes**: 컨테이너 오케스트레이션

---

## 기능 개요
- **소셜 네트워킹 기능**: 사용자 프로필, 친구 추가, 게시물 작성
- **일정 관리**: 개인 일정 및 알림 관리
- **실시간 알림**: WebSocket/STOMP 기반 알림 시스템
- **이미지 업로드 및 관리**: AWS S3 또는 Cloudinary 활용
- **검색 기능**: Elasticsearch로 게시물 및 사용자 검색

---

## 프로젝트 구조
```plaintext
src
├── main
│   ├── java
│   │   └── com.example.platform
│   │       ├── controller
│   │       ├── model
│   │       ├── repository
│   │       ├── service
│   │       └── security
│   ├── resources
│   │   ├── static
│   │   ├── templates
│   │   └── application.yml
├── test
└── Dockerfile
```

---

## 설치 및 실행

### **1. 환경 설정**
1. **Java 17** 이상 설치
2. **Node.js 18** 이상 설치
3. **MongoDB**, **Elasticsearch** 서버 실행
4. **Docker** 및 **Kubernetes** 설정 완료

### **2. 프로젝트 실행**

#### **백엔드**
```bash
./mvnw spring-boot:run
```

#### **프론트엔드**
```bash
cd frontend
npm install
npm start
```

#### **Docker 실행**
```bash
docker-compose up
```