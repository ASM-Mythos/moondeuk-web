# moondeuk-web

문득(Moondeuk) 공개 웹 — Google Play 계정 삭제 정책·개인정보처리방침 게시용 정적 페이지.

GitHub Pages(`main` 루트)로 서빙한다. 빌드 없음 — HTML/CSS 만.

| 페이지 | 용도 |
|--------|------|
| `index.html` | 인덱스(앱 소개 + 문서 링크) |
| `account-deletion.html` | **계정 삭제 안내** — Play Console 데이터 보안 폼의 "계정 삭제 요청 URL"에 기재 |
| `privacy.html` | **개인정보처리방침** — Play Console 앱 정보의 처리방침 URL에 기재 |

## 내용 유지보수 규칙

- 서버 삭제 정책의 정본은 `moondeuk-api` `MemberWithdrawalController`·`AuthService.restoreIfWithdrawn`(소프트 삭제 → **30일 유예 중 재로그인 시 복구** → 30일 뒤 배치 영구 파기). 정책이 바뀌면 두 페이지의 보관·복구 문구를 함께 바꾼다.
- 앱 쪽 대응 문서: `moondeuk-android/docs/2026-07-30-account-deletion-play-policy.md`, 탈퇴 화면 스펙 `.claude/design/10e_withdraw.md`.
- 색상은 앱 팔레트(`moondeuk-android` `ui/theme/Color.kt`)와 동일 값(`style.css` `:root`).
- 문구는 한국어, 앱 내 문구(10e 화면)와 어긋나지 않게 유지한다.

## 미확정(후속)

- 커스텀 도메인(moondeuk.kr) CNAME — DNS 등록 후 Pages 설정에 추가. URL 이 바뀌면 Play Console 폼도 갱신.
- 개인정보처리방침 법적 검토.
