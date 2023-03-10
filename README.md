# 나만의 커밋 메시지 가이드

Git을 사용하면서 Commit message를 적을때 항상 머뭇거리곤 합니다. 과연 잘 작성했는지 혹시라도 잘못 작성하진 않았을까 등등

영어능력이 떨어지는 저는 커밋 메세지 작성하는게 여간 힘든게 아니더군요.

그래서 이번에 많은 곳에서 사용하고 있지만 조금 더 구체화시킨 커밋 메세지 작성법을 만들어보려고 합니다.

밑의 내용은 [좋은 git 커밋 케시지를 작성하기 위한 7가지 약속 :: TOAST Meetup!](https://meetup.toast.com/posts/106)에 적혀있는 커밋 메시지 작성법입니다. 아마 대부분의 분들이 이 내용에 따라 작성하고 있을 것이라 생각합니다.

### 좋은 git 커밋 메시지를 작성하기 위한 7가지 약속

> 이하 약속은 커밋 메시지를 `English`로 작성하는 경우에 최적화되어 있습니다. 한글 커밋 메시지를 작성하는 경우에는 더 유연하게 적용하셔도 좋을 것 같네요.

1. 제목과 본문을 한 줄 띄워 분리하기
2. 제목은 영문 기준 50자 이내로
3. 제목 첫글자를 대문자로
4. 제목 끝에 `.` 금지
5. 제목은 `명령조`로
6. 본문은 영문 기준 72자마다 줄 바꾸기
7. 본문은 `어떻게`보다 `무엇을`, `왜`에 맞춰 작성하기

# 나의 커밋 메시지 작성법

저는 조금 다른 방법을 적용해보려고 합니다.

참고한 곳은 다음과 같습니다.

- [Git 사용 규칙 - Git commit 메시지 :: h3ngss0](https://tttsss77.tistory.com/58)
- [Udacity Git Commit Message Style Guide :: udacity](https://udacity.github.io/git-styleguide)
- [style-git-commit-message :: slashsbin](https://github.com/slashsbin/styleguide-git-commit-message)

## 공통 규칙

1. **유형**은 **영어 or emoji**로, **제목**은 **한글**로 작성한다.
2. **메시지 본문**에 모든 **변경 사항을 상세히 작성**한다.

## 커밋 메시지 구성

모든 커밋 메시지는 다음과 같이 **세 영역으로 구성**되며, 각 영영은 **빈 줄로 분리**된다.

- 제목 줄
- 본문 (제목 만으로 표현이 가능할 때에는 생략 가능)
- 꼬리말 (관련 이슈가 없으면 생략 가능)

```
유형: 제목

본문

꼬리말
```

## 유형

유형들이 복합적으로 포함되어 있을 경우, 되도록 커밋을 분리한다. 분리가 어려운 경우 위 순서상 상위 항목의 유형으로 작성한다. (eg. 기능과 테스트가 모두 포함된 경우 기능으로 작성)

- **feat**: 기능 추가, 삭제, 변경(or ✨ emoji) - 제품 코드 수정 발생
- **fix**: 버그 수정(or 🚑 emoji) - 제품 코드 수정 발생
- **docs**: 문서 추가, 삭제, 변경(or 📚 emoji) - 코드 수정 없음
- **style**: 코드 형식, 정렬, 주석 등의 변경, eg; 세미콜론 추가(or 🎨 emoji) - 제품 코드 수정 발생, 하지만 동작에 영향을 주는 변경은 없음
- **refactor**: 코드 리펙토링, eg. renaming a variable(or 🚜 emoji) - 제품코드 수정 발생
- **test**: 테스트 코드 추가, 삭제, 변경 등(or 🔬 emoji) - 제품 코드 수정 없음. 테스트 코드에 관련된 모든 변경에 해당
- **chore**: 위에 해당하지 않는 모든 변경, eg. 빌드 스크립트 수정, 패키지 배포 설정 변경 - 코드 수정 없음

## 제목

1. 제목 줄은 **50자 내로 작성**한다.
2. 제목은 **개조식 구문으로 작성**한다.
3. 제목 줄은 **"유형: 제목"** 의 형식으로 작성한다.
4. 제목 뒤에 특수문자는 삽입하지 않습니다. 예) . ? !

예) "feat: 로그 기능 출력 기능 추가"

> **개조식 구문**
>
> 완전한 서술형으로 문장을 종결하는 것이 아니라 간결하고 요점적인 단어로 서술되는 문장형태로서, 내용을 길게 풀어서 표현하지 않고 중요하고 핵심적인 요소만 간추려 항목별로 나열하듯이 표현하는 방식
>
> \- *국립국어원*  \-

## 본문

1. 본문은 **한 줄 당 72자 내**로 작성한다.
2. 본문 내용은 양에 구애받지 않고 **최대한 상세히 작성**한다.
3. 본문 내용은 어떻게 변경했는지 보다 **무엇을 변경했는지** 또는 **왜 변경했는지**를 설명한다.

## 꼬리말

1. 꼬리말은 optional이고 **이슈 트래커 ID**를 작성한다.
2. 꼬리말은 **"유형: #이슈번호"** 형식으로 사용한다.
3. 여러개의 이슈번호를 적을때는 쉼표로 구분합니다.
4. 이슈 트래커 유형은 다음 중 하나를 사용한다.
   - **Fixes**: 이슈 수정중 (아직 해결되지 않은 경우)
   - **Resolves**: 이슈를 해결했을 때 사용
   - **Ref**: 참고할 이슈가 있을 때 사용
   - **Related to**: 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)

예) `Fixes: #45` `Reloated to: #34, #23`

## 예시

```
feat: 패킷 송신 이벤트에 관련된 로그 출력 기능 추가

커밋에 대한 자세한 설명..

Resolves: #123
Ref: #456
Related to: #48, #45
```

## Commitlint-bot 붙히기

여러 팀원들과 같이 프로젝트를 진행할때 나말고 다른 사람들이 commitlint를 맞추지 않다면 아무런 소용이 없을 겁니다. 프로젝트에 commitlint-bot을 붙혀 이러한 문제점들을 해결해보세요.

[commitlint-bot](./commitlint-bot.md)

### Reference

[좋은 git 커밋 케시지를 작성하기 위한 7가지 약속 :: TOAST Meetup!](https://meetup.toast.com/posts/106)

[Udacity Git Commit Message Style Guide :: udacity](https://udacity.github.io/git-styleguide)

[Git 사용 규칙 - Git commit 메시지 :: h3ngss0](https://tttsss77.tistory.com/58)

[커밋 메시지 가이드 :: RomuloOliveria](https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README_ko-KR.md)

[style-git-commit-message :: slashsbin](https://github.com/slashsbin/styleguide-git-commit-message)

### License

[MIT License](./LICENSE)
