# Проверка игрока на читы в Rust

## 1. Проверка отдачи оружия
- Проверить отдачу оружия в инвентаре.

## 2. Консоль
- Нажать **F1** → **info/net/items/tools/server**.

## 3. Оконный режим
- **Alt+Enter** → свернуть игру в маленькое окно.  
- Если интерфейс смещается и багуется → **бан** (признак ImGui-меню).

## 4. LastActivityView **[в крайнем случае]**
- Скачать [LastActivityView](https://www.nirsoft.net/utils/computer_activity_view.html).  
- Просмотреть **15–25 приложений от запуска Rust**.  
- Поискать `Exloader`, `.dll`.  
- Проверить, запускался ли **CCleaner** перед проверкой.

## 5. Steam
- Открыть `C:\Program Files (x86)\Steam\config\loginusers.vdf`.  
- Ctrl+F → `765`.  
- Проверить на игровые баны и блокировки.

## 6. AppData и мышь
- Win+R → `appdata`.  
- Проверить мышку:
  - **Logitech** → `lua`, `txt`.  
  - **Razer** → `.xml`.  
  - **Bloody** → `.amc`.  
- Перейти: `AppData\Local\(mouse name)\scripts`, проверить дату изменения.  
- В `AppData\Local\CrashDumps` — подозрительные файлы (читы, макросы, инжекторы).  
- В `AppData\Roaming` — искать конфиги читов.
- Если есть открыть и проверить программу мыши

## 7. Временные файлы
- Win+R → `%temp%`.

## 8. Папка игры
- Проверить папку с Rust:  
  - Подозрительные папки (например, `Skyline`).  
  - Файлы (например, `imgui.ini`).  
  - Папку `Screenshots`.

## 9. Проводник
- Win+E → быстрый доступ, загрузки, другие диски, корзина.

## 10. Браузер и ВК
- Проверить историю браузера по ключевым словам:  
  `macro`, `cheat`, `vh`, `soft`, `aim`, `lua`, `макрос`, `аим`, `вх`, `чит`.  
- Просмотреть загрузки браузера.  
- ВКонтакте:  
  - Слева снизу кнопка **файлы** → проверить подозрительные.  
  - Поиск по ключевым словам.  
  - Проверить личные сообщения.

## 11. Telegram
- Если есть — обязательно проверить.  
- Поиск: `macro`, `cheat`, `vh`, `soft`, `aim`, `макрос`, `аим`, `вх`, `чит`.

## 12. Реестр
- Win+R → `regedit`. 
- Проверить ключи:
    - HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FeatureUsage\AppSwitched
    - HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FeatureUsage\ShowJumpView
    - HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Compatibility Assistant\Store
    - HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\OpenSavePidlMRU
- искать файлы с короткими названиями [пример](https://freeimghost.net/images/2025/08/21/imageeac0b94c1a4e8534.png)

## 13. Проверка почт
- Открыть браузер.  
- Проверить почты на [oplata.info](https://oplata.info).  
- Прогнать все найденные почты через:
- [Gmail](https://mail.google.com/mail/u/0/#inbox)  
- [Яндекс](https://360.yandex.ru/mail/)  
- [Mail.ru](https://mail.ru/)
- Discord
- Steam
- Funpay
- Playerok

## 14. Торговые площадки и форумы
- Проверить авторизацию и покупки:
- FunPay  
- GGsell  
- PlayerOK  
- Форумы:
- Phoenix  
- Evil  

## 15. Process Hacker
1. Скачать [Process Hacker](https://www.softportal.com/getsoft-14593-process-hacker-3.html) 
2. Запустить от имени администратора (x64).  
3. Найти `RustClient.exe` → ПКМ → **Properties** → вкладка **Memory**.  
4. Нажать **Strings**.  
5. Ввести `4`, поставить все галочки.  
6. После загрузки → **Filter → contains (case insensitive)**.  
7. Поиск по строкам:
  - Aimbot
  - ComputeStringHash
  - facepunch.graphics
  - norecoil
  - ExternalCheat_NoRecoil
  - RustExploit_Injector
  - Injector
  - Hack
  - Facepunch.Sharp
  - BasicLand
  - f482aa25-0061-48e7-a4d0-06b8ef97a0a6
  - data-
  - plusminus
  - fake admin
