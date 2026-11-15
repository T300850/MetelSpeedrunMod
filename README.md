# 🏁 Metel — Speedrun Mod

### v1.11.0

**A speedrunning & practice toolkit for _Metel_**

[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Unity-black?logo=unity)](https://unity.com/)
[![Loader](https://img.shields.io/badge/Loader-MelonLoader-orange)](https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.3)
![Game](https://img.shields.io/badge/Metel-0.921-blue)
![Version](https://img.shields.io/badge/Mod%20version-1.11.0-00a9e0)
![Status](https://img.shields.io/badge/Status-Unofficial%20mod-lightgrey)

**Made by:** `TL12 Mods` · **Creators:** `t300850` & `Lol_official1`

---

## 🌐 Language / Язык

- [🇬🇧 English](#english)
- [🇷🇺 Русский](#русский)

---

<a id="english"></a>
## 🇬🇧 ENGLISH

A modification for **Metel 0.921 PC**, created for **speedrunning and practice**. Choose when the timer stops, change item presets, set an FPS limit and configure a restart key — all from the in-game menu.

| | |
|---|---|
| **Made by** | TL12 Mods |
| **Creators** | t300850, Lol_official1 |
| **Game** | Metel 0.921 PC (Windows, Unity Mono) |
| **Loader** | [MelonLoader 0.7.3](https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.3) |
| **Mod version** | 1.11.0 |

---

## 📥 Installation

### Requirements

- **Metel 0.921 PC** on Windows and **MelonLoader 0.7.3** installed for the game.
- The original `Metel_Data\Managed\Assembly-CSharp.dll`, not a replacement from another mod.
- Back up your saves before installing or changing codes.

### 🛠️ Using the installer

1. Extract the **entire** mod archive.
2. Run `Install-Mod.bat` and select the game's `.exe`.
3. If an older mod DLL is present, confirm its replacement.
4. Launch the game and press **F2** to open or hide the mod menu.

Keep `Install-Mod.ps1` and the archive's `Mods` folder next to the batch file. The installer copies the mod **only**; it does not install MelonLoader.

### 📁 Manual installation

Copy `Mods\MetelTimerModes.dll` from the archive to the `Mods` folder next to the game executable. Replace the previous version; do not keep multiple copies of the mod.

**Logs:** `...\MelonLoader\Latest.log`

---

## ⌨️ Hotkeys & Controls

| Key / action | What it does |
|:---|:---|
| `F2` | Show / hide the mod menu |
| `X` | Close the menu; press `F2` to reopen it |
| Drag the top bar | Move the menu; its position is saved |
| Restart key | No default key; set it in **Timer → Change key** |
| `Esc` | Cancel restart-key assignment |

⚠️ Restarting immediately ends the current attempt. The game uses its normal Restart screen; you may need to press **Continue**. The mod unlocks the cursor on that screen.

⚠️ Opening the mod menu releases the cursor but **does not pause the game**. Inputs can still reach the game; pause first when adjusting settings.

---

## ⏱️ Timer Modes

Choose a mode in the **Timer** tab:

| Mode | Stops the timer on |
|:---|:---|
| **Finish / win** | The game's normal finish event |
| **Death** | Death; in Adele's chapter, when the loss screen appears |
| **Alert** | The corresponding alert timer starting |
| **Food** | The cooked sausage disappearing in Eugene's chapter or the rainbow cereal disappearing from Adele's bowl |

The game's normal timer-stop events remain active in every mode. Changing modes does not reset or start a stopped timer. The timer uses game time and pauses with the game.

---

## 🗂️ Mod Menu Tabs (`F2`)

### 1️⃣ Timer
- Select the timer mode.
- Set or clear the restart key. The key used to bind does not immediately restart the game.
- `F2` is reserved for the menu; **Esc** cancels assignment.

### 2️⃣ Presets

| Chapter | Preset range |
|:---|:---:|
| Alan / Emily | `0–5` |
| Eugene | `0–4` |
| Adele | `0–5` |

Restart the level to apply a new preset. If a generator has fewer available positions than the chosen index, the last available position is used. Adele's overall variation still follows the game's random selection.

### 3️⃣ FPS
- Set a limit from **30 to 240 FPS** with the slider or the `−` / `+` buttons.
- **Unlock FPS** removes the software limit; **Lock FPS** applies the selected limit again.
- After selecting the slider, use arrow keys for fine adjustment or **Home / End** for the endpoints.
- The mod disables VSync. Monitor, graphics-driver or Windows settings may still limit actual FPS.

### 4️⃣ Codes

| Code | Length |
|:---|:---:|
| LockBox | 3 digits |
| Terminal | 4 digits |
| Eugene chest | 3 digits |

Enter the code and press **Save**. Leading zeros and repeated digits are allowed. Restart the level after changing LockBox or Terminal. On Eugene's level the mod attempts to update his chest immediately; restart if prompted. Eugene's chest has a separate code and stays random until one is set.

### 5️⃣ About
- Creators and sponsors.
- Links to speedrun.com, GitHub, Telegram and DonationAlerts.

---

## 💾 Settings & Files

The mod saves its settings through Unity **PlayerPrefs**. On Windows, game preferences are normally stored under `HKEY_CURRENT_USER\Software\Linked Squad\Metel`; Unity may add hashes to registry value names. Use the mod menu rather than editing the registry when possible.

```text
Game folder/
├── Metel.exe
├── MelonLoader/
└── Mods/
    └── MetelTimerModes.dll
```

---

## ⚙️ Build from Source

Install a .NET SDK and make the .NET Framework 4.7.2 reference assemblies available through NuGet. Set the game and MelonLoader managed-assembly paths in PowerShell:

```powershell
$env:METEL_MANAGED = 'C:\path\to\Metel\Metel_Data\Managed'
$env:MELON_MANAGED = 'C:\path\to\Metel\MelonLoader\net35'
cd Source
dotnet build -c Release
```

The output is `Source\bin\Release\net472\MetelTimerModes.dll`. Keep `Source\Assets\tl12.rgba` with the project: it is the embedded logo.

---

## 🧪 Testing & Support

The DLL was compiled, but version 1.11 and the installer have **not been tested in the running game or on Windows**. If something goes wrong, provide `MelonLoader\Latest.log`, the chapter, mode or preset, and the steps that caused the issue.

---

<a id="русский"></a>
## 🇷🇺 РУССКИЙ

Модификация для **Metel 0.921 PC**, созданная для **спидрана и тренировок**. Выбирайте момент остановки таймера, меняйте пресеты предметов, настраивайте FPS и бинд рестарта прямо в меню игры.

| | |
|---|---|
| **Создано** | TL12 Mods |
| **Создатели** | t300850, Lol_official1 |
| **Игра** | Metel 0.921 PC (Windows, Unity Mono) |
| **Загрузчик** | [MelonLoader 0.7.3](https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.3) |
| **Версия мода** | 1.11.0 |

---

## 📥 Установка

### Требования

- **Metel 0.921 PC** на Windows и установленный для игры **MelonLoader 0.7.3**.
- Оригинальный `Metel_Data\Managed\Assembly-CSharp.dll`, не заменённый другим модом.
- Перед установкой или изменением кодов сделайте резервную копию сохранений.

### 🛠️ Через установщик

1. Распакуйте архив мода **целиком**.
2. Запустите `Install-Mod.bat` и выберите `.exe` игры.
3. Если старая DLL мода уже установлена, подтвердите её замену.
4. Запустите игру и нажмите **F2**, чтобы открыть или скрыть меню мода.

`Install-Mod.ps1` и папка `Mods` из архива должны находиться рядом с батником. Установщик копирует **только мод** и не устанавливает MelonLoader.

### 📁 Установка вручную

Скопируйте `Mods\MetelTimerModes.dll` из архива в папку `Mods` рядом с EXE игры. Замените предыдущую версию; не оставляйте несколько копий мода.

**Логи:** `...\MelonLoader\Latest.log`

---

## ⌨️ Горячие клавиши и управление

| Клавиша / действие | Что делает |
|:---|:---|
| `F2` | Показать / скрыть меню мода |
| `X` | Закрыть меню; `F2` открывает его снова |
| Перетаскивание верхней строки | Переместить меню; положение сохраняется |
| Клавиша рестарта | По умолчанию не назначена; настройка в **Timer → Change key** |
| `Esc` | Отменить назначение клавиши рестарта |

⚠️ Рестарт сразу завершает текущую попытку. Используется штатный экран Restart; может понадобиться нажать **Continue**. На этом экране мод разблокирует курсор.

⚠️ Меню мода освобождает курсор, но **не ставит игру на паузу**. Нажатия могут попадать в игру — при настройке лучше сначала включить паузу.

---

## ⏱️ Режимы таймера

Выбираются во вкладке **Timer**:

| Режим | Когда останавливается таймер |
|:---|:---|
| **Finish / win** | При штатном завершении игры |
| **Death** | При смерти; в главе Адель — при появлении экрана проигрыша |
| **Alert** | При запуске соответствующего таймера тревоги |
| **Food** | При исчезновении приготовленной колбасы у Юджина или радужных колечек из миски у Адель |

Штатные события остановки таймера работают во всех режимах. Смена режима не сбрасывает и не запускает остановленный таймер. Таймер использует игровое время и останавливается на паузе.

---

## 🗂️ Вкладки меню (`F2`)

### 1️⃣ Timer — таймер и рестарт
- Выбор режима таймера.
- Назначение или удаление клавиши рестарта. Нажатие клавиши при назначении не перезапускает игру.
- `F2` зарезервирована для меню; **Esc** отменяет назначение.

### 2️⃣ Presets — пресеты предметов

| Глава | Варианты |
|:---|:---:|
| Алан / Эмили | `0–5` |
| Юджин | `0–4` |
| Адель | `0–5` |

Для применения нового пресета перезапустите уровень. Если у генератора доступно меньше позиций, чем выбранный индекс, используется последняя доступная позиция. Общая вариация Адель по-прежнему выбирается игрой случайно.

### 3️⃣ FPS
- Ограничение от **30 до 240 FPS** настраивается ползунком или кнопками `−` / `+`.
- **Unlock FPS** снимает программное ограничение; **Lock FPS** возвращает выбранный лимит.
- После выбора ползунка стрелки позволяют менять значение, а **Home / End** — выбрать крайние значения.
- Мод отключает VSync. Монитор, драйвер видеокарты и Windows всё равно могут ограничивать FPS.

### 4️⃣ Codes — коды

| Код | Длина |
|:---|:---:|
| LockBox | 3 цифры |
| Terminal | 4 цифры |
| Сундук Юджина | 3 цифры |

Введите код и нажмите **Save**. Начальные нули и повторяющиеся цифры разрешены. После изменения LockBox или Terminal перезапустите уровень. На уровне Юджина мод пытается обновить его сундук сразу; если появится соответствующее сообщение, перезапустите уровень. Код сундука отдельный и остаётся случайным, пока его не задали.

### 5️⃣ About — о моде
- Создатели и спонсоры.
- Ссылки на speedrun.com, GitHub, Telegram и DonationAlerts.

---

## 💾 Настройки и файлы

Мод сохраняет настройки через Unity **PlayerPrefs**. В Windows настройки игры обычно находятся в `HKEY_CURRENT_USER\Software\Linked Squad\Metel`; Unity может добавлять хеши к именам значений. По возможности используйте меню мода вместо редактирования реестра.

```text
Папка игры/
├── Metel.exe
├── MelonLoader/
└── Mods/
    └── MetelTimerModes.dll
```

---

## ⚙️ Сборка из исходников

Установите .NET SDK и обеспечьте доступ к справочным сборкам .NET Framework 4.7.2 через NuGet. Укажите пути к библиотекам игры и MelonLoader в PowerShell:

```powershell
$env:METEL_MANAGED = 'C:\path\to\Metel\Metel_Data\Managed'
$env:MELON_MANAGED = 'C:\path\to\Metel\MelonLoader\net35'
cd Source
dotnet build -c Release
```

Готовый файл: `Source\bin\Release\net472\MetelTimerModes.dll`. Файл `Source\Assets\tl12.rgba` должен находиться вместе с проектом — это встроенный логотип.

---

## 🧪 Проверка и поддержка

DLL собрана, но версия 1.11 и установщик **не проверялись в запущенной игре и на Windows**. При проблеме приложите `MelonLoader\Latest.log`, укажите главу, режим или пресет и опишите действия, после которых появилась ошибка.

---

## 👥 Creators / Создатели

- **t300850** — [speedrun.com](https://www.speedrun.com/users/t300850) · [GitHub](https://github.com/T300850)
- **Lol_official1**

## 💙 Sponsors / Спонсоры

- **zup130**
- **mistiz**

---

## 💬 Community & Support / Сообщество и поддержка

[![Telegram](https://img.shields.io/badge/Telegram-TL12%20Mods-26A5E4?logo=telegram&logoColor=white)](https://t.me/TL12Mods)
[![DonationAlerts](https://img.shields.io/badge/Support-DonationAlerts-ff7a00)](https://www.donationalerts.com/r/cyberfoxspeedrunner)

Found a bug or have a suggestion? Contact **TL12 Mods**.  
Нашли баг или есть предложение? Свяжитесь с **TL12 Mods**.

---

**Made by TL12 Mods**

*This is an unofficial fan-made modification. Not affiliated with Linked Squad.*  
*Это неофициальная модификация, созданная фанатами. Не связана с Linked Squad.*
