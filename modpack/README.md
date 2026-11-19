# 게임 서버 모드팩 설치

서버가 NeoForge로 바뀌면 모든 접속자가 모드팩을 깔아야 합니다. 설정은 처음 한 번만 합니다. 그 뒤에는 게임을 켤 때마다 새 버전을 자동으로 받습니다.

## 필요한 것

- Prism Launcher. https://prismlauncher.org/download/ 에서 받습니다. 무료입니다.
- Prism Launcher에 Microsoft 계정으로 로그인합니다.
- 자동 업데이트 도구(packwiz-installer) 파일 두 개. 아래 표의 주소에서 받습니다.

| 파일 | 버전 | 받는 주소 |
|:---|:---|:---|
| `packwiz-installer-bootstrap.jar` | v0.0.3 | https://github.com/packwiz/packwiz-installer-bootstrap/releases/download/v0.0.3/packwiz-installer-bootstrap.jar |
| `packwiz-installer.jar` | v0.5.14 | https://github.com/packwiz/packwiz-installer/releases/download/v0.5.14/packwiz-installer.jar |

받은 파일은 아래 "파일 확인"으로 sha256을 맞춰 봅니다.

## 1. 인스턴스 만들기

1. Prism Launcher에서 "Add Instance"를 누릅니다.
2. 이름에 `gameserver`를 적습니다.
3. 게임 버전 목록에서 26.1.2를 고릅니다.
4. 아래쪽 Mod loader에서 NeoForge를 고르고, 버전 26.1.2.127을 고릅니다.
5. OK를 누릅니다.

게임 26.1.2는 Java 25가 필요합니다. 인스턴스 설정의 Java 화면에서 Java 25를 고르거나 받습니다.

## 2. 자동 업데이트 도구 넣기

1. 만든 인스턴스를 고르고 오른쪽의 "Folder"를 누릅니다.
2. 열린 폴더에 `mmc-pack.json`이 없으면 한 단계 위 폴더로 갑니다. `mmc-pack.json`이 있는 폴더가 인스턴스 폴더입니다.
3. 받은 jar 두 개를 인스턴스 폴더에 넣습니다.

## 3. 실행 전 명령 걸기

1. 인스턴스를 오른쪽 클릭하고 "Edit"를 누릅니다.
2. 왼쪽의 "Settings"를 누르고 "Custom commands" 탭으로 갑니다.
3. "Custom Commands" 칸을 체크합니다.
4. "Pre-launch command" 칸에 아래 한 줄을 그대로 붙여 넣습니다.

```text
"$INST_JAVA" -jar "$INST_DIR/packwiz-installer-bootstrap.jar" --bootstrap-no-update --bootstrap-main-jar "$INST_DIR/packwiz-installer.jar" --pack-folder "$INST_MC_DIR" --multimc-folder "$INST_DIR" https://raw.githubusercontent.com/haeju-dev/gameserver-client-mod/main/modpack/pack.toml
```

- `$INST_JAVA`, `$INST_DIR`, `$INST_MC_DIR`는 Prism Launcher가 이 인스턴스의 Java와 폴더로 바꿔 줍니다. 고치지 않습니다.
- `--bootstrap-no-update`는 도구가 스스로 새 버전을 받지 않게 합니다. 위에서 확인한 파일만 씁니다.
- 마지막 주소가 모드팩 주소입니다.

## 4. 처음 켜기

1. 인스턴스를 고르고 "Launch"를 누릅니다.
2. 작은 창이 떠서 모드를 받습니다. 처음에는 1~2분 걸릴 수 있습니다.
3. 다 받으면 게임이 켜집니다.
4. 멀티플레이에서 서버를 더하고 들어갑니다. 서버 주소는 관리자에게 받습니다.

## 업데이트

- 게임을 켤 때마다 새 버전이 있는지 봅니다. 있으면 받고, 모드팩에서 빠진 jar는 지웁니다.
- 서버와 모드 버전이 다르면 접속이 안 됩니다. 그때는 게임을 끄고 다시 켭니다.
- 모드팩이 NeoForge 버전을 바꾸면 도구가 인스턴스 설정도 고칩니다. 게임이 켜지지 않거나 접속이 안 되면 한 번 더 켭니다.
- 새 버전이 나온 직후 몇 분 동안은 옛 파일과 새 파일이 섞여 받아질 수 있습니다. 도구 창에 오류가 뜨면 몇 분 뒤 다시 켭니다.
- `mods` 폴더에 직접 넣은 jar는 도구가 지우지 않습니다.
- 모드팩에 든 모드의 다른 버전(예: Cloth Config)을 `mods` 폴더에 넣지 않습니다. 같은 모드가 둘이 되어 게임이 바로 꺼집니다.

## 들어 있는 모드

| 모드 | 하는 일 |
|:---|:---|
| 게임 서버 기본 | 워프 이름 바꾸기, 블록 보호, 나뭇잎 빨리 사라지기, 숫돌 인챈트 옮기기, 투명 아이템 액자 |
| 게임 서버 장치 | 경험치 상자, 경험치 호퍼, 분류 호퍼, 무선 레드스톤, 가짜 플레이어 블록 |
| 게임 서버 총 | 총, 탄, 부착물, 작업대, 연사, 조준 확대와 조준경 화면 |
| GraveStone Mod | 죽은 자리에 무덤을 남기고 아이템을 담습니다 |
| Inventory Sorting | 인벤토리와 상자를 정리합니다 |
| Cloth Config API | Inventory Sorting이 설정 화면에 씁니다 |

- 연사와 조준경 확대는 총 모드에 들어 있습니다. 옛 Fabric 연사 모드는 이 인스턴스에 넣지 않습니다.

## 파일 확인

받은 파일의 sha256이 아래 값과 같아야 합니다.

| 파일 | sha256 |
|:---|:---|
| `packwiz-installer-bootstrap.jar` | `a8fbb24dc604278e97f4688e82d3d91a318b98efc08d5dbfcbcbcab6443d116c` |
| `packwiz-installer.jar` | `c9f646908d340d84773948a9a7d98bc1dae250d35e1016dc6e2b8459760b5598` |

macOS 터미널. 받은 파일이 "다운로드" 폴더에 있다고 보고 그 폴더로 옮겨 가서 실행합니다:

```zsh
cd ~/Downloads
shasum -a 256 packwiz-installer-bootstrap.jar packwiz-installer.jar
```

Windows PowerShell. 같은 방법으로 "다운로드" 폴더에서 실행합니다:

```powershell
cd $HOME\Downloads
Get-FileHash packwiz-installer-bootstrap.jar, packwiz-installer.jar -Algorithm SHA256
```

- 출력의 긴 16진수가 sha256입니다. PowerShell은 대문자로 보여 줍니다. 대소문자는 달라도 됩니다.
- 이미 인스턴스 폴더에 넣었으면 첫 줄의 `cd` 뒤를 인스턴스 폴더로 바꿉니다.
- 값이 다르면 넣지 말고 다시 받습니다.
- 모드 파일은 도구가 받을 때 sha256이나 sha512를 맞춰 봅니다. 따로 확인하지 않아도 됩니다.

## 문제가 생기면

- 도구 창에 오류가 뜨면 인터넷 연결을 확인하고 다시 켭니다.
- 모드팩은 GitHub에서 받습니다. GitHub에 접속이 안 되면 모드팩을 받지 못합니다. 몇 분 뒤 다시 켭니다.
- 게임이 바로 꺼지면 인스턴스의 Java가 25인지 봅니다.
- 실행 전 명령이 돌지 않으면 "Custom Commands" 칸이 체크됐는지 봅니다.
- 그래도 안 되면 Prism Launcher의 로그 화면을 찍어 관리자에게 보냅니다.

## 지우기

Prism Launcher에서 인스턴스를 지웁니다. 다른 인스턴스와 공식 런처는 그대로입니다.
