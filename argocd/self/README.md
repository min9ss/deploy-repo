
# Argo CD Self-Manage

이 디렉토리는 **Argo CD 자기 자신을 GitOps로 관리(Self-manage)** 하기 위한 매니페스트를 담고 있습니다.

## 포함 파일
- `install.yaml`
  - Argo CD 공식 매니페스트 (버전 고정, pinned)
  - Argo CD를 설치/업그레이드할 때 Git에서 이 파일을 수정 → Argo CD가 스스로 동기화
- `kustomization.yaml` (옵션)
  - 필요 시 ConfigMap/RBAC/알림 등 추가 패치를 관리

## 특징
- Argo CD 업그레이드 = install.yaml 버전 변경 후 Git push
- 클러스터에서 수동 수정이 있더라도 Git 상태로 자동 복원(Self-heal)
