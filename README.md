## 기능 요구사항
- username 중복 불가
  - MemberService에서 중복 확인 및 예외처리
- 토큰 발급하는 API 생성
  - JwtTokenProvider.createToken 수정
    - username을 통해 jwt 생성 
- 내 정보 조회하기
  - 토큰을 이용하여 본인 정보 응답하기
  - AuthService에 getUserByToken 생성
  - MemberController가
    - AuthService.getUsernameByToken -> getPrincipal()
    - MemberService.getMemberByUsername

## 프로그래밍 요구사항
인증 로직은 Controller에서 구현하기 보다는 재사용이 용이하도록 분리하여 구현하다.
가능하면 Controller와 인증 로직을 분리한다.
토큰을 이용한 인증 프로세스에 대해 이해가 어려운 경우 페어와 함께 추가학습을 진행한다.
