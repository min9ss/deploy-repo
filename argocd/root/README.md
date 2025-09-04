# Root Application (App-of-Apps)

이 디렉토리는 **App-of-Apps 루트 Application**을 정의합니다.

## 포함 파일
- `root.yaml`
  - Argo CD Application
  - `path: argocd/apps` 를 바라보며, 해당 경로 아래 정의된 모든 ApplicationSet 및 Application을 한 번에 동기화

## 특징
- UI에서 `root` 앱 하나로 전체 구조 관리
- 개별 서비스(Applications)는 `apps/` 아래 정의된 ApplicationSet에 의해 자동 생성됨
