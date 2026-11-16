# RDGate — выпуски

**Русский** · [English](#english)

Здесь лежат готовые сборки [RDGate](https://github.com/DQuest/RDGate) — лаунчера RDP для macOS с UDP
через RD Gateway. Исходники, описание и вопросы — в основном репозитории.

## Первая установка

Нужен Mac на Apple Silicon.

1. Скачайте `RDGate-<версия>-macos-arm64.zip` из последнего выпуска и распакуйте его.
2. Снимите карантин:

   ```bash
   xattr -dr com.apple.quarantine RDGate.app
   ```

   Приложение подписано «для себя» и не нотаризовано Apple: без этой команды Gatekeeper его не
   запустит.
3. Перенесите `RDGate.app` в «Программы» и откройте.

Если macOS слишком старая для этой сборки, она скажет об этом при запуске: минимальная версия
записана в приложении.

## Обновления

Дальше RDGate обновляется сам. Раз в сутки он проверяет этот репозиторий и, если вышла новая
версия, показывает плашку над списком подключений: «Что нового», «Установить», «Пропустить эту
версию». Новая версия ставится, когда вы выходите из RDGate, или сразу по кнопке «Перезапустить
сейчас». Галочки «Проверять обновления» и «Устанавливать автоматически» — в настройках, в разделе
«Обновления».

Рядом с каждым архивом лежит его подпись (`.sig`): RDGate ставит только архив, подписанный ключом
выпусков, и проверяет подпись самого приложения.

После каждого обновления macOS один раз спросит, можно ли RDGate брать пароли из связки ключей:
нажмите «Разрешать всегда».

## Что внутри

Клиент FreeRDP `sdl-freerdp` с правками для RDP-UDP и библиотеки, от которых он зависит, каждая под
своей лицензией. Тексты лицензий и их перечень — в `RDGate.app/Contents/Resources/Licenses`.
RDGate распространяется по лицензии GPL-3.0-or-later.

---

<a id="english"></a>

# RDGate releases

Ready-made builds of [RDGate](https://github.com/DQuest/RDGate), an RDP launcher for macOS with UDP
through RD Gateway. The source code, the documentation and issues are in the main repository.

## First install

You need a Mac with Apple Silicon.

1. Download `RDGate-<version>-macos-arm64.zip` from the latest release and unpack it.
2. Remove the quarantine flag:

   ```bash
   xattr -dr com.apple.quarantine RDGate.app
   ```

   The app is signed for local use and not notarized by Apple: without this command Gatekeeper will
   not start it.
3. Move `RDGate.app` to Applications and open it.

If your macOS is too old for this build, it says so at launch: the minimum version is recorded in the
app.

## Updates

From then on RDGate updates itself. Once a day it checks this repository and, when a new version is
out, shows a banner above the connection list: What’s New, Install, Skip This Version. The new version
is installed when you quit RDGate, or right away with Restart Now. The Check for updates and Install
automatically switches are in Settings, under Updates.

Every archive has its signature next to it (`.sig`): RDGate installs only an archive signed with the
release key, and checks the app's own code signature as well.

After every update macOS asks once whether RDGate may read passwords from the keychain: click
“Always Allow”.

## What is inside

The FreeRDP client `sdl-freerdp` with the RDP-UDP changes and the libraries it depends on, each under
its own license. The license texts and their list are in `RDGate.app/Contents/Resources/Licenses`.
RDGate is distributed under GPL-3.0-or-later.
