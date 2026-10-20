# 김진우 · Jinwoo Kim

**AI 백엔드 · 모바일·웹 개발**

서비스에 필요한 기능이라면 익숙하지 않은 영역도 직접 배우고 구현해 보는 개발자입니다.  
프론트엔드 개발로 시작해 AI 백엔드와 배포까지 맡으며, 각 기능이 연결되는 전체 흐름에 관심을 가져 왔습니다.

[대표 프로젝트](#대표-프로젝트) · [최근 작업](#최근-작업)

## 대표 프로젝트

| 프로젝트 | 담당한 개발 | 코드 |
| --- | --- | --- |
| **HEAPY**<br>개인 건강관리 AI 서비스 | FastAPI 기반 AI 백엔드와 RAG 챗봇, 질문 의도 분류 모델, 앱–서버 API 연동, Docker·EC2 배포 | [AI](https://github.com/Heapy-AI/heapy-ai-health) · [서버](https://github.com/Heapy-AI/heapy-backend) · [앱](https://github.com/Heapy-AI/heapy-frontend) |
| **After Buy**<br>전자기기 구매·보증 관리 앱 | React Native 앱, OCR 결과 반영과 입력 상태 보존, 토큰 갱신·재요청, OCR 수정 필드 기록 API 연동 | [앱](https://github.com/After-Buy/after-buy-app/tree/develop) |
| **Gachon Bridge**<br>교내 프로젝트 공유 웹 | 24시간 해커톤에서 Codex로 React·TypeScript 프론트엔드 개발, 공통 API 모듈과 서버 연동 점검 | [웹](https://github.com/AI-Hackerthon-2026/frontend) |

<details>
<summary><b>구현 코드와 문제 해결 기록 살펴보기</b></summary>

### HEAPY
- [AI API 인터페이스](https://github.com/Heapy-AI/heapy-ai-health/blob/dev/app/internal.py): 요청·응답 스키마, 서버 간 인증, SSE 스트리밍
- [RAG 검색](https://github.com/Heapy-AI/heapy-ai-health/blob/dev/app/services/vector_search.py): 여러 컬렉션 병렬 검색과 검색 결과 정리
- [질문 의도 분류](https://github.com/Heapy-AI/heapy-ai-health/tree/dev/model/classifier): 의도 기준과 학습 데이터 검토, 문장 임베딩 기반 분류기 학습·평가

### After Buy
- [제품 상세 화면](https://github.com/After-Buy/after-buy-app/blob/develop/src/screens/item/ItemDetailScreen.tsx): OCR 촬영 후에도 작성 중인 입력값을 유지하고, 원본 인식값과 최종 입력을 비교해 변경된 필드명을 서버에 전달
- [공통 API 클라이언트](https://github.com/After-Buy/after-buy-app/blob/develop/src/services/api/api.ts): 동시 401 응답의 토큰 갱신을 한 번으로 모으고 대기 요청을 재시도

### Gachon Bridge
- [공통 API 클라이언트](https://github.com/AI-Hackerthon-2026/frontend/blob/develop/src/services/api.ts): 세션 쿠키, 요청·응답 타입, 오류 처리
- [서버 API 연동 점검](https://github.com/AI-Hackerthon-2026/frontend/blob/develop/서버_API_연동_점검.md): CORS 응답 확인, Vite 개발 프록시 적용, 실제 서버 응답과 빌드·린트 검증 기록

</details>

## 최근 작업

**[바로핏 자세 분석 모듈](https://github.com/Barofit-team/barofit-pose) · 개발 중**

MediaPipe 관절 좌표를 이용한 푸시업·플랭크 판정 모듈을 개발하고 있습니다. Python으로 영상과 판정 결과를 비교하고, 앱에서 사용할 JavaScript 모듈의 입출력과 운동별 확장 방법을 정리하고 있습니다.

[입출력 규격](https://github.com/Barofit-team/barofit-pose/blob/main/docs/IO_CONTRACT.md) · [판정 기준](https://github.com/Barofit-team/barofit-pose/blob/main/docs/RULES.md) · [검증 기록](https://github.com/Barofit-team/barofit-pose/blob/main/docs/VALIDATION.md)

## 사용하는 기술

| 영역 | 기술 |
| --- | --- |
| AI · 백엔드 | Python · FastAPI · PyTorch · Sentence Transformers · RAG · Spring Boot |
| 모바일 · 웹 | TypeScript · React Native · Expo · React |
| 데이터 · 배포 | PostgreSQL · Redis · Pinecone · Docker · AWS EC2 / ECR / SSM · GitHub Actions |

## 일하는 방식

- 새로운 기술은 해결하려는 문제에 맞는지 살펴보고, 작은 구현을 실행하며 익힙니다.
- 결과가 나온 이유와 오류가 생기는 조건을 확인하면서 보완합니다. Codex로 작성한 코드도 구현 원리와 실제 동작을 검토합니다.
- 화면과 API 명세를 일찍 공유하고, 팀원들의 의견을 구현에 반영한 뒤 변경 내용을 다시 공유합니다.
