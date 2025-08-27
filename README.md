# Проверка игрока на использование читов в Rust

## Шаги проверки

### 1. Rust
1. Проверить отдачу оружия в инвентаре.
2. Открыть консоль `F1` и проверить вкладки:
   - Консоль — наличие **debugcamera**.
   - Вкладка **Tools** — должна быть пустой.
   - Вкладка **Server** — должна быть пустой.
3. Нажать `Alt+Enter`, свернуть игру в маленькое окно:
   - Если интерфейс смещается и багуется → бан (признак ImGui-меню).

### 2. Windows
4. На Windows 10 нажать `Win+Tab` и прокрутить файлы вниз.
5. В **Discord**:
   - Отправить файл → стрелка у названия файла → прокрутить файлы вниз.
   - Проверить последние группы и личные чаты (за время игры на сервере).
6. В **Steam**:
   - Открыть:  
     `C:\Program Files (x86)\Steam\config\loginusers.vdf`
   - Найти по `765` (SteamID).
   - Проверить наличие игровых банов и блокировок.
7. В **AppData**:
   - `Win+R → appdata`
   - В `AppData\Local\CrashDumps` — подозрительные файлы (читы, макросы, инжекторы).
   - В `AppData\Roaming` — конфиги читов.
8. В `%temp%` — проверить временные файлы.
9. Проверить папку с Rust:
   - Дата изменения папки **Screenshots**.
10. Проверить **корзину**.

### 3. Социальные сети и мессенджеры
11. **Браузер**:
    - История по ключевым словам:  
      `macro`, `cheat`, `vh`, `soft`, `aim`, `lua`, `макрос`, `аим`, `вх`, `чит`.
    - Проверить загрузки.
12. **ВКонтакте**:
    - Слева снизу кнопка **Файлы** → проверить подозрительные.
    - Поиск по ключевым словам.
    - Проверить личные сообщения.
13. **Telegram**:
    - Проверить поиск по ключевым словам:  
      `macro`, `cheat`, `vh`, `soft`, `aim`, `макрос`, `аим`, `вх`, `чит`.
    - Проверить авторизации и покупки на:
      - FunPay
      - GGsell
      - PlayerOK

### 4. Почты
14. Проверить почтовые аккаунты:
    - Gmail
    - Яндекс
    - Mail.ru
    - Discord
    - Steam
    - FunPay
    - PlayerOK

### 5. Process Hacker
15. Скачать [Process Hacker](https://www.softportal.com/getsoft-14593-process-hacker-3.html).
16. Запустить от имени администратора (x64).
17. Найти `RustClient.exe` → ПКМ → **Properties** → вкладка **Memory**:
    - Отсортировать по весу.
    - Искать `...cheat.dll`, `loader` и т.п.
18. Нажать **Strings**:
    - Ввести `4`, поставить все галочки.
    - После загрузки → **Filter** → `contains` (case insensitive).
    - Поискать строки:
      - `Aimbot`
      - `ComputeStringHash`
      - `facepunch.graphics`
      - `norecoil`
      - `ExternalCheat_NoRecoil`
      - `RustExploit_Injector`
      - `Injector`
      - `Hack`
      - `Facepunch.Sharp`
      - `BasicLand`
      - `f482aa25-0061-48e7-a4d0-06b8ef97a0a6`
      - `data-`
      - `plusminus`
      - `fake admin`

### 6. LastActivityView (в крайнем случае)
19. Скачать [LastActivityView](https://www.nirsoft.net/utils/computer_activity_view.html).
20. Проверить 15–25 приложений, запущенных после старта Rust.
21. Ищем: **Exloader**, `.dll`.
22. Проверить, запускался ли **CCleaner** перед проверкой.
