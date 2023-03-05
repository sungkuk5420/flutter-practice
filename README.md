# toonflix

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## flutter 설치
```
1. 니꼬쌤이 추천해주시는 Chocolatey를 다운 설치해야 합니다.
https://chocolatey.org/install
해당 사이트를 방문하고
다음 매뉴얼을 따라 설치하거나
A를 제외한 나머지부터 시작해주시면 됩니다.
A. Choose How to Install Chocolatey: Individual 선택
B. 작업 표시줄에 있는 윈도우 아이콘에서 우클릭 - 파워쉘 작업 관리자 실행
C. Get-ExecutionPolicy 명령어를 입력 하고 Restricted 해당 메시지가 반환 되는지 확인
D. Set-ExecutionPolicy AllSigned 혹은 Set-ExecutionPolicy Bypass -Scope Process
명령어 둘중 택1을 쉘에 입력해줍니다.
그 다음
E.
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
해당 명령줄을 복붙하거나 입력 후 실행합니다.
선택창이 출력 된다면 y를 입력해 설치해줍니다.
F. 설치가 끝나면 쉘에 choco 혹은 choco -?를 입력해 정상 설치 되었는지 확인합니다.
G. 에러 메시지 제외 다른 메시지가 출력 된다면 다음 작업을 이어 진행합니다.

2. Flutter 설치
A. 파워쉘을 닫지 말고 그대로 choco install flutter 를 입력해 설치해줍니다.
이때 선택창이 출력 된다면 y를 입력해줍니다.
B. 설치가 끝나면 flutter 명령어를 입력해 에러 메시지 제외 다른 메시지가 출력 되면 성공입니다.


3. 안드로이드 연결
- https://docs.flutter.dev/get-started/install/windows#android-setup
해당 사이트를 방문해 가이드대로 진행하시면 됩니다. 제가 한 방법은 아래 기술하겠습니다.
A. https://developer.android.com/studio 안드로이드 스튜디오를 설치합니다.
설치 방법 및 가이드는 따로 없습니다. 에러 관련 메시지는 해당 에러 메시지를 복사해 구글에 검색해보시면 쉽게 해결 방법을 찾을 수 있습니다.
B. 자바 8버전 이상이 필요하고 환경 변수 설정이 필요합니다.
[있으신 분들은 스킵, 없으신 분들은 설치해주시면 됩니다.]
C. 안드로이드 스튜디오를 실행하고 우측 상단 점3개 혹은 Device Manager를 찾아주시면 됩니다.
그 후 Create Device를 클릭해 애뮬레이터를 설정해주시면 됩니다.
[사용자마다 원하는 기기가 다르므로 원하시는 기기를 선택해주시면 됩니다.
저는 Pixel 3 XL 모델을 선택했습니다. ]
D. 기기를 선택했다면 Next를 누르고 릴리즈 버전을 골라주시면 되는데
ABI를 x86을 선택 하는 걸 권장하고 있습니다.
버전까지 선택했다면 Next를 누릅니다.
E. Verify Configuration 에서 하단에 Emulated Performance에서
Graphics를 Hardware-GLES 2.0으로 선택 후 Finish를 누릅니다.
안드로이드 설정까지는 끝났습니다. 다음 과정을 진행하시면 됩니다.

4. 콘솔 혹은 파워쉘에서 flutter doctor --android-licenses 명령어를 입력합니다.
특별한 메시지 없이 넘어가시면 좋지만 저는 이슈가 발생해 공유합니다.
빨간 메시지로
Android sdkmanager not found. Update to the latest Android SDK and ensure that the cmdline-tools are installed to resolve this.
해당 메시지가 출력된다면
안드로이드 스튜디오에서 SDK Manager를 실행합니다.
좌측의 System Settings 에서 Android SDK를 선택
화면에서 SDK Tools를 선택합니다
하단에 Hide Obsolete Packages 의 체크를 해제합니다.

저의 경우 command-line 이 없어 오류가 생겼는데
이런 경우
Android SDK Command-line Tools(latest)의 Status 부분을 확인해
Not Installed 인지 확인합니다.
Not Installed 라면 설치해주면 됩니다.
혹은 다른 메시지가 출력될 수 있는데
Android SDK Tools (Obsolete)가 Installed 상태인지 확인해주시면 됩니다.
선택 후 설치를 진행합니다.
설치가 완료되었다면 Finish를 클릭하고
flutter doctor --android-licenses를 쉘에서 다시 입력해
에러 메시지가 아닌 설치되는 듯한 화면이 출력 되면 됩니다.
이때 동의에 대해 묻는데 y 입력해주시면 됩니다.
All SDK package licenses accepted 메시지가 출력 되면 라이센스 동의가 끝났습니다.

쉘에 flutter doctor를 입력합니다.
뭔가 검사가 진행됩니다.
이슈가 없다고 뜨면 끝! 인데 저는 두 개 떴습니다..
하단에 공유합니다.
Windows 10 SDK이 없다고 출력 되면
https://visualstudio.microsoft.com/ko/downloads/
해당 사이트에서 Visual Studio 2022 무료 다운로드를 설치해줍니다.
설치 창이 열리면 데스크톱 및 모바일에서 C++를 이용한 데스크톱 개발을 선택 후 설치합니다.

Unable to find bundled Java version 해당 메시지가 출력되면
안드로이드 스튜디오가 설치된 위치로 갑니다.
[따로 안 바꾸셨다면 아마 설치 위치는 C:\Program Files\Android\Android Studio 여기
일 껍니다.]
해당 파일에 jbr폴더 내용을 그대로 복사해 jre파일에 붙여넣기 합니다.

쉘이나 명령프롬트롬을 닫고
다시 열어 flutter doctor를 입력합니다.

No issues found!가 출력 되면 다 됐습니다
```


## flutter doctor 
```
flutter doctor
```

## flutter start
```
flutter create <project name>
cd <project name> 
flutter run 
```

