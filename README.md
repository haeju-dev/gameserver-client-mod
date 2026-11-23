# 게임 서버에 들어가기

마인크래프트 게임 서버에 들어가는 방법입니다. 설치는 처음 한 번만 합니다. 그 뒤에는 Prism Launcher에서 게임을 켜기만 하면 됩니다. 모드는 게임을 켤 때마다 알아서 새 버전으로 바뀝니다.

## 준비할 것

- 마인크래프트 Java 에디션을 산 Microsoft 계정이 있어야 합니다.
- 관리자에게 내 마인크래프트 이름을 알려 줍니다. 관리자가 허락해야 서버에 들어갈 수 있습니다.
- 서버 주소는 관리자가 알려 줍니다.

## Windows에서 설치하기

1. 아래 주소를 눌러 설치 파일을 받습니다.
   https://github.com/haeju-dev/gameserver-client-mod/releases/download/installer-v1/gameserver-windows-install.cmd
2. 브라우저가 받은 파일을 막을 수 있습니다. Edge에서는 아래처럼 합니다.
   1. 받기 목록에서 파일 옆의 "..." 단추를 누르고 "유지"를 누릅니다.
   2. 경고 창에서 "자세히 표시"를 누릅니다.
   3. "그래도 계속"을 누릅니다.
   Chrome은 "계속" 또는 "유지"를 누릅니다.
3. 받은 파일 `gameserver-windows-install.cmd`를 두 번 누릅니다.
4. "Windows의 PC 보호" 창이 뜨면 "추가 정보"를 누르고 "실행"을 누릅니다. "보안 경고" 창이 뜨면 "실행"을 누릅니다.
5. 검은 창이 뜨고 Prism Launcher를 설치합니다. 1~2분 걸립니다. 이미 설치되어 있으면 이 단계는 건너뜁니다.
6. Prism Launcher 창이 열립니다. 처음이면 언어와 테마를 고르는 화면이 나옵니다. 언어는 한국어를 고르고 "다음"을 누릅니다.
7. Microsoft 로그인 화면이 나오면 마인크래프트를 산 계정으로 로그인합니다.
8. "새 인스턴스"(New Instance) 창이 뜹니다. 이름이 `gameserver`인지 보고 "확인"(OK)을 누릅니다. 이 창이 뜨지 않으면 Prism Launcher를 닫고 설치 파일을 한 번 더 실행합니다.
9. 목록에 `gameserver`가 생깁니다. 검은 창은 아무 키나 눌러 닫습니다.

이제 아래 "게임 켜기"로 갑니다.

## macOS에서 설치하기

1. 아래 주소를 눌러 Prism Launcher를 받습니다.
   https://github.com/PrismLauncher/PrismLauncher/releases/download/11.1.1/PrismLauncher-macOS-11.1.1.dmg
2. 받은 파일을 엽니다. 열린 창에서 Prism Launcher 아이콘을 "응용 프로그램" 폴더로 끌어 놓습니다.
3. "응용 프로그램" 폴더에서 Prism Launcher를 엽니다. "인터넷에서 다운로드한 앱" 창이 뜨면 "열기"를 누릅니다.
4. 처음이면 언어와 테마를 고르는 화면이 나옵니다. 언어는 한국어를 고르고 "다음"을 누릅니다.
5. Microsoft 로그인 화면이 나오면 마인크래프트를 산 계정으로 로그인합니다.
6. 왼쪽 위의 "인스턴스 추가"(Add Instance)를 누릅니다.
7. 왼쪽 목록에서 "불러오기"(Import)를 누릅니다.
8. 주소 칸에 아래 주소를 그대로 붙여 넣습니다.
   https://github.com/haeju-dev/gameserver-client-mod/releases/download/installer-v1/gameserver.zip
9. 이름이 `gameserver`인지 보고 "확인"(OK)을 누릅니다. 목록에 `gameserver`가 생깁니다.

## 게임 켜기

1. Prism Launcher에서 `gameserver`를 고르고 "실행"(Launch)을 누릅니다.
2. 처음에는 Java와 모드를 받느라 1~2분 걸립니다. 작은 창이 떠서 모드를 받습니다.
3. 마인크래프트가 켜지면 "멀티플레이"를 누르고 "서버 추가"를 누릅니다.
4. "서버 주소" 칸에 관리자에게 받은 주소를 적고 "완료"를 누릅니다.
5. 목록의 서버를 두 번 누르면 들어갑니다.

다음부터는 Prism Launcher에서 `gameserver`를 고르고 "실행"만 누르면 됩니다.

## 안 될 때

- 설치 창에 빨간 글이 뜨면 설치 파일을 한 번 더 실행합니다. 같은 파일을 다시 실행해도 `gameserver`가 두 개 생기지 않습니다.
- 서버에 들어갈 때 "화이트리스트" 이야기가 나오면 관리자에게 마인크래프트 이름을 알려 줍니다.
- 모드를 받는 작은 창에 오류가 뜨면 인터넷 연결을 확인하고 다시 "실행"을 누릅니다.
- 로그인 화면을 건너뛰었으면 Prism Launcher 오른쪽 위의 계정 메뉴에서 Microsoft 계정을 더합니다.
- 전부터 Prism Launcher를 쓰던 사람은 게임이 바로 꺼질 수 있습니다. 이 게임은 Java 25가 필요합니다. 아래처럼 Java 25를 고릅니다.
  1. `gameserver`를 오른쪽 클릭하고 "편집"(Edit)을 누릅니다.
  2. 왼쪽 목록에서 "설정"(Settings)을 누르고 "Java" 탭을 엽니다.
  3. "Java 설치"(Java installation) 칸을 켭니다.
  4. "감지"(Detect)를 눌러 버전이 25로 시작하는 것을 고릅니다. 목록에 없으면 "다운로드"(Download)를 눌러 Java 25를 받습니다.
  5. 창을 닫고 다시 "실행"을 누릅니다.
- 전부터 Prism Launcher를 Scoop이나 압축 파일(포터블)로 쓰던 사람은 설치 파일이 그것을 찾지 못합니다. 그러면 Prism Launcher가 하나 더 설치됩니다. 새로 설치된 것을 쓰면 됩니다.
- 그래도 안 되면 화면을 사진으로 찍어 관리자에게 보냅니다. 설치 창이면 그 창을, 게임 문제면 Prism Launcher의 로그 화면을 찍습니다.
- 설치 파일을 쓰지 않고 직접 설치하는 방법도 있습니다. https://github.com/haeju-dev/gameserver-client-mod/blob/main/modpack/README.md

## 이 저장소에 있는 것

- `modpack/`: 게임 서버 모드팩입니다. 설치한 인스턴스가 게임을 켤 때마다 여기서 새 버전을 받습니다. 직접 설치하는 방법은 `modpack/README.md`에 있습니다.
- Releases의 `installer-v1`: 위 설치 파일과 인스턴스 zip입니다.
- `fire-mod.md`: 예전 Paper 서버에서 쓰던 연사 모드 안내입니다.
