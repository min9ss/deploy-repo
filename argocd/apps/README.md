# Applications & ApplicationSets

이 디렉토리는 실제 워크로드를 생성하는 **ApplicationSet 및 Application 정의**를 담습니다.

## 포함 파일
- `appset-fastapi.yaml`
  - ApplicationSet
  - dev/prod 환경에 따라 `charts/fastapi + envs/<env>/values.yaml`을 매핑
  - 결과: `fastapi-dev`, `fastapi-prod` Application이 자동 생성됨

## 특징
- 환경(dev/prod) 추가/삭제는 `elements` 목록 수정 후 Git push
- 각 Application은 Helm/Kustomize로 배포되며, root.yaml을 통해 전체 관리
