# Prerequisites & Setup Guide

## 요구사항

### 필수 소프트웨어

- **Python 3.9+**
  ```bash
  python --version
  ```

- **Docker 4.10+** (또는 Docker Desktop)
  ```bash
  docker --version
  ```

- **Docker Compose 2.0+**
  ```bash
  docker-compose --version
  ```

- **Git**
  ```bash
  git --version
  ```

### 시스템 요구사항

| 요구사항 | 최소 | 권장 |
|---------|------|------|
| CPU | 4 cores | 8 cores |
| RAM | 8GB | 16GB |
| 디스크 | 20GB free | 50GB free |
| OS | macOS/Linux/Windows WSL2 | macOS/Linux |

### 사전 지식

- SQL: SELECT, JOIN, WHERE, 기본 쿼리
- Python: 함수, 클래스, 모듈 기본
- 데이터베이스: 테이블, 인덱스, 정규화 개념
- Docker: 이미지, 컨테이너 기본
- Git: clone, add, commit, push

## 설치 가이드

### macOS

#### Python 설치 (Homebrew)
```bash
brew install python@3.11
python3 --version
```

#### Docker 설치
```bash
brew install docker
# 또는 Docker Desktop 다운로드: https://www.docker.com/products/docker-desktop
```

### Linux (Ubuntu/Debian)

#### Python 설치
```bash
sudo apt-get update
sudo apt-get install python3.11 python3-pip
python3 --version
```

#### Docker 설치
```bash
sudo apt-get install docker.io docker-compose-plugin
sudo usermod -aG docker $USER
```

### Windows

1. **WSL2 설치** (Windows Subsystem for Linux)
   ```powershell
   wsl --install
   ```

2. **Docker Desktop 설치**
   - 다운로드: https://www.docker.com/products/docker-desktop
   - WSL2 백엔드로 설정

3. **Python 설치** (WSL2 내부)
   ```bash
   sudo apt-get update
   sudo apt-get install python3.11 python3-pip
   ```

## 클론 및 초기 설정

```bash
# 1. 저장소 클론
git clone <repo-url>
cd tidb-scale-workshop

# 2. 환경 변수 설정
cp .env.example .env

# 3. Docker 환경 시작
docker-compose up -d

# 4. 상태 확인
docker-compose ps
```

## 연결 테스트

### TiDB에 연결

```bash
# MySQL 클라이언트 설치 (macOS)
brew install mysql-client

# MySQL 클라이언트 설치 (Linux)
sudo apt-get install mysql-client

# TiDB에 연결
mysql -h 127.0.0.1 -P 4000 -u root
```

---

**설정이 완료되었습니다!** ✅ Lab 01로 진행하세요.
