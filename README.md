<h3>🐤 Todo</h3>

- 팀별 branching/merge 가이드를 작성
- 브랜치를 자유롭게 생성하고, 커밋을 한 후 push, pull
- 오전 수업의 4가지 merge를 혼용
- 작업 시나리오, 가이드와 함께 원격저장소 주소를 DM으로 제출

---

### 1. 브랜치 규칙

- **`main`** : 제품에 배포되는 안정적인 코드만 포함
- **`작업 브랜치`** : 개인 작업 브랜치
  - `hyejeong`
  - `yourim`
  - `yunseo`

### 2. Merge 방식

- **`Fast-Forward merge`** : 다른 브랜치에서 작업한 후, 머지할 때 main 브랜치에는 변화가 없는 경우
- **`3-Way merge`** : 여러 명이 각자 다른 브랜치에서 비슷한 수준의 기능을 작업하고, 한번에 합칠 때 각자의 히스토리를 남기고자 할 때 사용한다.
- **`rebase`** : 히스토리 유지보다 히스토리를 깔끔하게 남기고자 할 때 사용한다. 다른 브랜치의 이력들이 중요하지 않고 순차적으로 작업한 것처럼 보이고 싶을 때 사용한다.
- **`squash & merge`** : 기능 구현 중 자잘한 커밋들을 한줄로 축약하고자 할 때 사용한다.

**🐳 Merge 방식별 사용 목적 요약**

| **Merge 방식**         | 사용 시점                   | 목적                              |
| ---------------------- | --------------------------- | --------------------------------- |
| **Fast-Forward merge** | 단독 작업 후 develop에 병합 | 불필요한 merge 커밋 없이 깔끔하게 |
| **3-Way merge**        | 병렬 작업 병합 시 충돌 추적 | 팀 개발 흐름 보존, 충돌 해결 용이 |
| **rebase**             | 본인 브랜치 최신화 시       | 커밋 기록 정리, 충돌 최소화       |
| **squash & merge**     | PR 병합 시                  | 여러 커밋을 하나로, 리뷰 후 정리  |

<hr/>

<h3>🙊 4가지 머지 방식 실습해 보기!</h3>

**`Fast-forward`**

- yunseo, hyejeong : 3-Way
- yurim : fast-forward

![Image](https://github.com/user-attachments/assets/8056fbcc-39d0-4106-b3fd-1fee61846886)

**`rebase`**

- main에서 commit 작성된 후 yurim2 브랜치로 분기, 분기한 브랜치에서 커밋 작성 후 main 브랜치에 rebase하여 커밋 시점이 옮겨진 것을 확인할 수 있다.

![Image](https://github.com/user-attachments/assets/72e037bb-b1ed-433c-954d-0a022f6cfa0c)

**`squash`**

- hyejeong2 브랜치에서 작업 후 두 개의 커밋을 남긴다. 이후 메인 브랜치로 squash merge를 하여 feat: squash merge hyejeong2 커밋만 남아 있는 것을 확인할 수 있다.

![Image](https://github.com/user-attachments/assets/26e1ae53-2256-4197-86a2-5facf2b6c944)
