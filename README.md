Для работы нужен загрузчик модов MelonLoader (проверено на версии 0.7.3).
Его установщик лежит в архиве — это официальный файл с GitHub, без изменений.

## Установка (Windows)

1. Запустите `MelonLoader.Installer.exe`, выберите в списке Volcano Princess (или укажите `VolcanoPrincess.exe` вручную) и нажмите **Install**.
2. Откройте папку игры: Steam → ПКМ по Volcano Princess → Управление → Просмотреть локальные файлы.
3. Скопируйте туда папку `Mods` из архива. Должно получиться так:

   ```
   VolcanoPrincess/
     VolcanoPrincess.exe
     version.dll
     MelonLoader/
     Mods/VPLocalization.dll
   ```

4. Установите шрифт из папки `Шрифт`: ПКМ по каждому `.ttf` → **Установить для всех пользователей**.
4. Запустите игру. Первый запуск дольше обычного, появится консоль MelonLoader — так и должно быть.
5. В настройках игры выберите язык «Русский».

## Linux / Steam Deck (Proton)

1. Скачайте установщик для Linux: <https://github.com/LavaGang/MelonLoader.Installer/releases/latest> (файл `MelonLoader.Installer.Linux`), сделайте его исполняемым и запустите.
2. Дальше как в Windows, с шага 2.
3. В Steam: ПКМ по игре → Свойства → Параметры запуска:

   ```
   WINEDLLOVERRIDES="version=n,b" %command%
   ```

   Без этой строки Proton не загрузит MelonLoader, и мод не запустится.

## Не хотите запускать exe из архива?

Скачайте установщик сами с официальной страницы MelonLoader:
<https://github.com/LavaGang/MelonLoader.Installer/releases/latest>

## Что внутри

- Полный русский перевод: сюжет, диалоги, интерфейс, предметы, обучение.
- Текст подгоняется под рамки интерфейса, чтобы не вылезал за края.
- Шрифт PT Sans Narrow с полной кириллицей.
- Имена дочери, отца и персонажей склоняются по падежам
- Даты и месяцы по-русски.

## Настройки

После первого запуска появится файл `UserData/MelonPreferences.cfg`, раздел `[VPLocalization]`: размер шрифта, минимальный размер, склонение имён и т.д. Клавиша **F5** в игре — перечитать настройки без перезапуска.

Если какой-то текст всё равно не влезает, он записывается в `UserData/VPLocalization/overflow.log`. В `overrides.json` рядом можно вписать свой короткий вариант фразы.

## Как удалить

- Только перевод — удалите `Mods/VPLocalization.dll` и `UserData/VPLocalization`.
- Вместе с MelonLoader — запустите `MelonLoader.Installer.exe` и нажмите **Uninstall**, или в Steam: Свойства → Установленные файлы → Проверить целостность.
