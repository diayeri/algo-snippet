# Snippet

- https://github.com/paullabkorea/programmersLv0/blob/main/Solution.md

## 포크받은 REPO 관리

추후 업데이트 시 충돌을 피하기 위해, 개인적인 내용이나 변경 사항을 별도의 파일이나 폴더로 분리하는 것이 좋은 방법입니다. 이렇게 하면 원본 레포지토리와의 병합 작업이 수월해지고 충돌 가능성을 최소화할 수 있습니다. 다음은 충돌을 피하기 위한 몇 가지 팁입니다.

### 충돌을 피하기 위한 팁

1. **개인적인 파일 및 폴더 분리**:

   - 개인적인 변경 사항이나 프로젝트와 관련 없는 파일을 별도의 디렉토리로 관리합니다.
   - 예: `personal/` 또는 `custom/` 같은 폴더를 만들어 사용.

2. **브랜치 사용**:

   - 원본 레포지토리에서 가져온 업데이트는 항상 `main` 또는 `master` 브랜치에서 관리하고, 개인적인 변경 사항은 별도의 브랜치에서 작업합니다.
   - 예: `feature/my-changes`, `bugfix/my-bugfix` 등.
   - 원본 레포지토리와 동기화할 때는 `main` 또는 `master` 브랜치에서 작업하고, 개인 브랜치와 병합합니다.

3. **작은 커밋**:

   - 변경 사항을 작고 논리적인 단위로 나눠 커밋합니다. 이렇게 하면 충돌이 발생했을 때 해결하기가 더 쉬워집니다.

4. **정기적인 동기화**:

   - 원본 레포지토리와 정기적으로 동기화하여, 큰 변경이 누적되기 전에 병합하고 충돌을 해결합니다.

5. **커스텀 파일 네이밍**:

   - 개인적인 파일이나 커스텀 파일을 원본 파일과 혼동되지 않도록 명명 규칙을 사용합니다.
   - 예: `config.custom.json`, `README.custom.md` 등.

6. **충돌 해결 능력**:
   - Git에서 충돌이 발생하면 이를 해결하는 방법을 숙지합니다. Git은 충돌을 해결하기 위한 다양한 도구와 명령을 제공합니다.
   - 예: `git mergetool`을 사용하여 시각적으로 충돌을 해결.

### 예제: 개인 파일 및 폴더 분리

다음은 개인 파일을 별도의 폴더로 분리하는 예제입니다:

```
project-root/
├── src/
│   ├── original-code.js
│   └── another-file.js
├── personal/
│   ├── my-custom-script.js
│   └── my-config.json
└── README.md
```

### 예제: 브랜치 사용

1. **원본 레포지토리에서 최신 코드 가져오기**:

   ```bash
   git checkout main
   git fetch upstream
   git merge upstream/main
   git push origin main
   ```

2. **개인적인 브랜치에서 작업하기**:

   ```bash
   git checkout -b feature/my-changes
   # 작업 수행 후 커밋
   git add .
   git commit -m "Add my custom changes"
   ```

3. **원본 레포지토리와 동기화하기**:

   ```bash
   git checkout main
   git fetch upstream
   git merge upstream/main
   git push origin main
   ```

4. **개인 브랜치와 병합**:
   ```bash
   git checkout feature/my-changes
   git merge main
   ```

이 방법을 통해 원본 레포지토리와 개인 작업을 분리하여 관리할 수 있습니다. 이렇게 하면 충돌을 최소화하고, 충돌이 발생하더라도 쉽게 해결할 수 있습니다.
