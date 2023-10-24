# AWS_IAM
IAM에 관한 교육 자료입니다

# AWS IAM CLI를 사용하여 사용자 목록 가져오기

## 내용

AWS IAM CLI를 사용하여 사용자 목록을 가져오는 방법을 알아보겠습니다.

## 준비

* AWS 계정 및 IAM 사용자
* AWS CLI 설치 및 구성

## 실행

1. AWS CLI를 사용하여 IAM에 로그인합니다.


알겠습니다. 다음과 같이 작성하시면 됩니다.

Markdown
# AWS IAM CLI를 사용하여 사용자 목록 가져오기

## 내용

AWS IAM CLI를 사용하여 사용자 목록을 가져오는 방법을 알아보겠습니다.

## 준비

* AWS 계정 및 IAM 사용자
* AWS CLI 설치 및 구성

## 실행

1. AWS CLI를 사용하여 IAM에 로그인합니다.

코드를 사용할 때는 주의하시기 바랍니다. 자세히 알아보기


2. AWS Access Key ID, AWS Secret Access Key, Default region name, Default output format을 입력합니다.

```markdown
AWS Access Key ID [None]: xxxxxxxxxxxxxxxxxxxxx
AWS Secret Access Key [None]: xxxxxxxxxxxxxx
Default region name [None]: ap-northeast-2
Default output format [None]:
```

3. aws iam list-users 명령을 사용하여 사용자 목록을 가져옵니다.

```
aws iam list-users
```

출력

```
{
    "Users": [
        {
            "Path": "/",
            "UserName": "plint",
            "UserId": "XXXXXXXXXXXXXX",
            "Arn": "arn:aws:iam::803785241427:user/plint",
            "CreateDate": "2023-10-23T12:38:25+00:00",
            "PasswordLastUsed": "2023-10-24T10:15:56+00:00"
        }
    ]
}
```

## 해석

출력은 다음과 같은 정보를 포함한다

* `Path`: 사용자의 계정 경로
* `UserName`: 사용자 이름
* `UserId`: 사용자 ID
* `Arn`: 사용자 ARN
* `CreateDate`: 사용자 생성 날짜
* `PasswordLastUsed`: 사용자 비밀번호가 마지막으로 사용된 날짜

## 참고

* `aws iam list-users` 명령은 IAM 사용자 목록을 가져온다
* `Path`는 사용자의 계정 경로를 나타냅니다.
* `UserName`은 사용자 이름을 나타냅니다.
* `UserId`는 사용자 ID를 나타냅니다.
* `Arn`은 사용자 ARN을 나타냅니다.
* `CreateDate`는 사용자 생성 날짜를 나타냅니다.
* `PasswordLastUsed`는 사용자 비밀번호가 마지막으로 사용된 날짜를 나타낸다


IAM Section – Summary

Users
단계별 설명:

IAM 콘솔에 로그인합니다.
Users 탭을 클릭합니다.
Add user 버튼을 클릭합니다.
사용자 이름, 이메일 주소, 액세스 유형을 입력합니다.
Create user 버튼을 클릭합니다.
생성된 사용자에게 임시 액세스 키를 할당합니다.
사용자에게 영구 액세스 키를 할당하거나 IAM 역할을 지정합니다.
Groups
단계별 설명:

IAM 콘솔에 로그인합니다.
Groups 탭을 클릭합니다.
Create group 버튼을 클릭합니다.
그룹 이름과 설명을 입력합니다.
Create group 버튼을 클릭합니다.
그룹에 사용자를 추가합니다.
그룹에 IAM 폴리시를 할당합니다.
Policies
단계별 설명:

IAM 콘솔에 로그인합니다.
Policies 탭을 클릭합니다.
Create policy 버튼을 클릭합니다.
폴리시 문서를 작성하거나 기존 폴리시를 복사하여 사용합니다.
Review policy 버튼을 클릭하여 폴리시를 검토합니다.
Create policy 버튼을 클릭하여 폴리시를 생성합니다.
사용자 또는 그룹에 폴리시를 할당합니다.
Roles
단계별 설명:

IAM 콘솔에 로그인합니다.
Roles 탭을 클릭합니다.
Create role 버튼을 클릭합니다.
역할 이름과 설명을 입력합니다.
역할의 트러스트 관계를 설정합니다.
역할에 IAM 폴리시를 할당합니다.
Create role 버튼을 클릭하여 역할을 생성합니다.
EC2 인스턴스 또는 AWS 서비스에 역할을 할당합니다.
Security
단계별 설명:

IAM 콘솔에 로그인합니다.
Users 탭을 클릭합니다.
사용자를 선택하고 Edit user 버튼을 클릭합니다.
Require MFA 체크박스를 선택합니다.
Password policy 섹션에서 비밀번호 정책을 설정합니다.
Save changes 버튼을 클릭하여 변경 사항을 저장합니다.
AWS CLI
단계별 설명:

AWS CLI를 설치 및 구성합니다.
IAM 콘솔에 로그인합니다.
My Security Credentials 탭을 클릭합니다.
Download Your Credentials 버튼을 클릭하여 액세스 키를 다운로드합니다.
액세스 키를 사용하여 AWS CLI에 로그인합니다.
AWS CLI 명령어를 사용하여 AWS 서비스를 관리합니다.
AWS SDK
단계별 설명:

AWS SDK를 설치 및 구성합니다.
IAM 콘솔에 로그인합니다.
My Security Credentials 탭을 클릭합니다.
Access Keys 섹션에서 액세스 키를 복사합니다.
액세스 키를 사용하여 AWS SDK에 로그인합니다.
AWS SDK를 사용하여 AWS 서비스를 관리합니다.
Access Keys
단계별 설명:

IAM 콘솔에 로그인합니다.
My Security Credentials 탭을 클릭합니다.
Access Keys 섹션에서 액세스 키를 복사합니다.
액세스 키를 사용하여 AWS CLI 또는 AWS SDK에 로그인합니다.
액세스 키를 사용하여 AWS 서비스를 관리합니다.
Audit
단계별 설명:

IAM 콘솔에 로그인합니다.
Reports 탭을 클릭합니다.
User activity report 또는 IAM credential report를 선택합니다.
보고서를 생성합니다.
보고서를 검토하여 IAM 사용자 및 역할의 활동을 확인합니다.
참고:

IAM 사용자, 그룹, 폴리시, 역할은 AWS 리소스에 대한 액세스를 제어하는 데 사용됩니다





