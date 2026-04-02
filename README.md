# SW-AI W06 C Programming

6주차 C 프로그래밍 자료구조 학습 저장소입니다.

## 학습 순서

1. **Linked List** — 연결 리스트 (Q1 ~ Q7)
2. **Stack & Queue** — 스택과 큐 (Q1 ~ Q7)
3. **Binary Tree** — 이진 트리 (Q1 ~ Q8)
4. **Binary Search Tree** — 이진 탐색 트리 (Q1 ~ Q5)

각 폴더의 PDF 파일에 문제 설명이 있으며, `.c` 파일에서 직접 풀이합니다.

## 개발 환경

- Docker + VSCode DevContainer 기반
- `F5`로 디버깅 실행 가능

---

## 환경 구축 가이드

<details>
<summary>펼쳐서 보기</summary>

## 1. Docker란 무엇인가요?

**Docker**는 애플리케이션을 어떤 컴퓨터에서든 **동일한 환경에서 실행**할 수 있게 도와주는 **가상화 플랫폼**입니다.  

Docker는 다음 구성요소로 이루어져 있습니다:

- **Docker Engine**: 컨테이너를 실행하는 핵심 서비스
- **Docker Image**: 컨테이너 생성에 사용되는 템플릿 (레시피)
- **Docker Container**: 이미지를 기반으로 생성된 실제 실행 환경 (요리)

### AWS EC2와의 차이점

| 구분 | EC2 같은 VM | Docker 컨테이너 |
|------|-------------|-----------------|
| 실행 단위 | OS 포함 전체 | 애플리케이션 단위 |
| 실행 속도 | 느림 (수십 초 이상) | 매우 빠름 (거의 즉시) |
| 리소스 사용 | 무거움 | 가벼움 |

---

## 2. VSCode DevContainer란 무엇인가요?

**DevContainer**는 VSCode에서 Docker 컨테이너를 **개발 환경**처럼 사용할 수 있게 해주는 기능입니다.

- 코드를 실행하거나 디버깅할 때 **컨테이너 내부 환경에서 동작**
- 팀원 간 **환경 차이 없이 동일한 개발 환경 구성** 가능
- `.devcontainer` 폴더에 정의된 설정을 VSCode가 읽어 자동 구성

---

## 3. Docker Desktop 설치하기

1. Docker 공식 사이트에서 설치 파일 다운로드:  
   https://www.docker.com/products/docker-desktop

2. 설치 후 Docker Desktop 실행  
   - Windows: Docker 아이콘이 트레이에 떠야 함  
   - macOS: 상단 메뉴바에 Docker 아이콘 확인

---

## 4. 프로젝트 파일 다운로드

터미널에서 아래 명령어로 프로젝트를 클론합니다:

```bash
git clone https://github.com/JYPark-Code/SW-AI-W06-C-Programming.git
```

### 폴더 구조

```
SW-AI-W06-C-Programming/
├── .devcontainer/
│   ├── devcontainer.json      # VSCode에서 컨테이너 환경 설정
│   └── Dockerfile             # C 개발 환경 이미지 정의
│
├── .vscode/
│   ├── launch.json            # 디버깅 설정 (F5 실행용)
│   └── tasks.json             # 컴파일 자동화 설정
│
├── Data-Structures/
│   ├── Linked_List/
│   ├── Stack_and_Queue/
│   ├── Binary_Tree/
│   └── Binary_Search_Tree/
│
└── README.md
```

---

## 5. VSCode에서 프로젝트 열기

1. VSCode를 실행
2. `파일 → 폴더 열기`로 클론한 폴더를 선택

---

## 6. 개발 컨테이너에서 열기

1. VSCode에서 `Ctrl+Shift+P` (Windows/Linux) 또는 `Cmd+Shift+P` (macOS)를 누릅니다.
2. 명령어 팔레트에서 `Dev Containers: Reopen in Container`를 선택합니다.
3. 컨테이너가 자동으로 빌드 및 실행됩니다. 처음에는 빌드 시간이 걸릴 수 있습니다.

---

## 7. 디버깅 (F5)

C 파일에 브레이크포인트를 설정한 뒤 `F5`를 눌러 디버깅을 시작할 수 있습니다.
변수, 메모리, 스택, 출력 등을 VSCode에서 확인할 수 있습니다.

</details>
