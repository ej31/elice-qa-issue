---
name: Custom issue template
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

name: 🐞 Bug Report
description: 버그 발생 시 신고해주세요.
title: "[BUG] "
labels: ["bug"]
body:
  - type: textarea
    id: description
    attributes:
      label: 📝 버그 설명
      description: 어떤 문제가 발생했는지 알려주세요.
      placeholder: |
        예) 로그인 버튼을 눌러도 반응이 없음
    validations:
      required: true

  - type: dropdown
    id: bug-type
    attributes:
      label: 🧭 버그 유형
      description: 어떤 종류의 버그인가요?
      options:
        - 기능적 버그 (Functional Bug)
        - 비기능적 버그 (Non-functional Bug)
    validations:
      required: true

  - type: dropdown
    id: severity
    attributes:
      label: 🚨 버그 심각도
      description: 영향을 고려해 심각도를 선택해주세요.
      options:
        - 치명적 (Critical) — 기능 완전 차단, 시스템 사용 불가
        - 중요한 (Major) — 주요 기능 오작동, 우회 가능
        - 사소한 (Minor) — UI/UX 문제 또는 경미한 오류
    validations:
      required: true

  - type: textarea
    id: reproduce
    attributes:
      label: 🔁 재현 방법
      description: 동일 문제를 재현할 수 있는 단계를 알려주세요.
      placeholder: |
        1. 로그인 페이지로 이동
        2. 이메일/비밀번호 입력
        3. 로그인 버튼 클릭
        4. 반응 없음
    validations:
      required: true

  - type: textarea
    id: expected
    attributes:
      label: ✅ 기대 동작
      placeholder: 예) 로그인 버튼 클릭 시 대시보드로 이동

  - type: textarea
    id: screenshot
    attributes:
      label: 📸 스크린샷 / 로그 (선택)
      description: 참고할 자료가 있다면 첨부해주세요.

  - type: input
    id: browser
    attributes:
      label: 🌐 환경 정보 (브라우저/OS)
      placeholder: 예) Chrome 120 / macOS 14.2
