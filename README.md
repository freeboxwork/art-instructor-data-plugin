# Art Instructor Data plugin for Codex

예비 미술 강사 인력풀의 등록자 및 익명 사이트 분석 데이터를 Codex에서 자연어로 조회하는 읽기 전용 플러그인입니다.

## 제공 기능

- 등록자 현황 및 조건별 집계
- 방문·페이지 조회·CTA·등록 전환 분석
- 유입 경로와 UTM 캠페인 분석
- 필요한 데이터를 스프레드시트로 정리

등록자 수정·삭제, 분석 데이터 초기화, 임의 SQL 실행은 제공하지 않습니다.

## 설치

PowerShell 또는 터미널에서 다음 명령을 실행합니다.

```powershell
codex plugin marketplace add freeboxwork/art-instructor-data-plugin
codex plugin add art-instructor-data@art-instructor-data
```

관리자에게 개인 MCP 토큰을 전달받은 뒤 Windows 사용자 환경 변수에 저장합니다.

```powershell
[Environment]::SetEnvironmentVariable(
  "ART_INSTRUCTOR_MCP_TOKEN",
  "전달받은_개인_토큰",
  "User"
)
```

Codex 앱을 완전히 종료한 뒤 다시 실행하고 새 작업에서 질문합니다.

## 질문 예시

- 최근 30일 방문과 등록 전환을 요약해 줘.
- 현재 구직 중인 강사를 지역별로 집계해 줘.
- 특정 UTM 캠페인의 방문 세션을 보여 줘.
- 조건에 맞는 등록자 목록을 스프레드시트로 만들어 줘.

## 보안

- 토큰은 사용자별로 발급되며 이 저장소에는 포함되지 않습니다.
- 토큰을 GitHub, 채팅방, 문서 또는 코드에 커밋하지 마세요.
- 토큰이 노출되면 관리자에게 폐기와 재발급을 요청하세요.
- 조회 결과의 이메일과 자유 입력 답변은 개인정보로 취급하세요.

## 서버

- MCP endpoint: `https://art-instructor-pool.vercel.app/api/mcp`
- Website: `https://art-instructor-pool.vercel.app`
- Application repository: `https://github.com/freeboxwork/art-instructor-pool`
