# Metel Timer Modes

A Windows speedrun mod for **Metel 0.921 PC**, built with MelonLoader. It adds configurable timer modes, item presets, FPS controls, code settings and a restart keybind.

[English](#english) · [Русский](#русский)

---

## English

### Features

- **Timer modes:** Finish / win, Death, Alert and Food. In Adele's chapter, Death waits for the loss screen and Food stops when the rainbow cereal disappears from the bowl. In Eugene's chapter, Food also supports the cooked sausage.
- **Item presets:** independent layouts for Alan / Emily (0–5), Eugene (0–4) and Adele (0–5). Restart the level to apply changes.
- **FPS:** choose a limit from 30 to 240, adjust it with the slider or +/- buttons, or unlock FPS. The mod disables VSync; your monitor, driver or Windows may still impose a limit.
- **Codes:** set a three-digit LockBox code, four-digit Terminal code and separate three-digit Eugene chest code. LockBox and Terminal changes require a level restart. The mod attempts to update Eugene's chest immediately when you save its code on his level.
- **Restart keybind:** assign or clear a key in the Timer tab. Restart uses the game's normal restart flow and unlocks the cursor on the Restart screen.
- **Compact menu:** press **F2** to show or hide it, or close it with **X**. Drag the top bar to move it; the position is saved. The timer stays visible when the menu is hidden.

### Requirements

- Windows version of **Metel 0.921 PC** (Unity Mono).
- [MelonLoader 0.7.3](https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.3), installed for the game.
- The original `Metel_Data\Managed\Assembly-CSharp.dll` from the game, not a replacement DLL from another mod.

Back up your saves before installing or changing codes. Do not install multiple versions of `MetelTimerModes.dll` at the same time.

### Installation

1. Install MelonLoader 0.7.3 for the game's executable.
2. Extract the entire mod archive.
3. Run `Install-Mod.bat` and select the game's `.exe`. The installer creates `Mods` if needed and asks before replacing an existing mod DLL. Keep `Install-Mod.ps1` and the archive's `Mods` folder next to the batch file.
4. Launch the game and press **F2** to open or hide the mod menu.

The installer copies the mod only; it does **not** install MelonLoader. Alternatively, copy `Mods\MetelTimerModes.dll` from the archive into the `Mods` folder next to the game executable, replacing the previous version.

### Usage notes

- Select a timer mode in **Timer**. Changing modes does not reset or restart a stopped timer. The timer uses game time and pauses with the game. The game's normal timer-stop events remain active in every mode.
- Assign a restart key with **Timer → Change key**. Press the desired key; **Esc** cancels and **Clear binding** removes it. **F2** is reserved for the menu. Restarting immediately ends the current attempt and may require pressing Continue on the Restart screen.
- With the mod menu open, the cursor is released, but the game is **not paused** and inputs can still reach it. Pause the game before changing settings if needed.
- In **Codes**, enter the exact number of digits and press **Save**. Leading zeros and repeated digits are allowed. The Eugene chest uses a separate code from LockBox; until set, it retains the game's random behavior.
- The FPS slider can also be adjusted with arrow keys after selecting it; **Home** and **End** select the endpoints. Unlocking FPS removes the software cap, not hardware or driver limits.

### Building from source

The `Source` folder contains the C# source, project file and embedded logo asset. Install the .NET SDK and make the .NET Framework 4.7.2 reference assemblies available through NuGet. In PowerShell, set the paths to your game and MelonLoader managed assemblies:

```powershell
$env:METEL_MANAGED = 'C:\path\to\Metel\Metel_Data\Managed'
$env:MELON_MANAGED = 'C:\path\to\Metel\MelonLoader\net35'
cd Source
dotnet build -c Release
```

The output is `Source\bin\Release\net472\MetelTimerModes.dll`.

### Testing and support

The mod DLL was compiled, but version 1.11 and the installer have not been tested in the running game or on Windows. If something fails, include `MelonLoader\Latest.log`, the chapter, selected mode or preset, and the steps that caused the issue.

---

## Русский

### Возможности

- **Режимы таймера:** Finish / win, Death, Alert и Food. В главе Адель Death ждёт появления экрана проигрыша, а Food останавливается, когда радужные колечки исчезают из миски. В главе Юджина Food также работает с приготовленной колбасой.
- **Пресеты предметов:** отдельные варианты для Алана / Эмили (0–5), Юджина (0–4) и Адель (0–5). Для применения перезапусти уровень.
- **FPS:** ограничение от 30 до 240 с настройкой ползунком или кнопками +/−, а также снятие ограничения. Мод отключает VSync; монитор, драйвер или Windows всё равно могут ограничивать частоту кадров.
- **Коды:** трёхзначный код LockBox, четырёхзначный код Terminal и отдельный трёхзначный код сундука Юджина. После изменения LockBox или Terminal перезапусти уровень. При сохранении кода на уровне Юджина мод пытается обновить сундук сразу.
- **Бинд рестарта:** назначение или удаление клавиши во вкладке Timer. Используется штатный рестарт игры; на экране Restart курсор разблокируется.
- **Компактное меню:** **F2** показывает и скрывает меню, **X** закрывает его. Окно можно перетащить за верхнюю строку; положение сохраняется. При закрытии меню таймер остаётся видимым.

### Требования

- Windows-версия **Metel 0.921 PC** (Unity Mono).
- [MelonLoader 0.7.3](https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.3), установленный для игры.
- Оригинальный `Metel_Data\Managed\Assembly-CSharp.dll` из игры, а не DLL, подменённая другим модом.

Перед установкой или изменением кодов сделай резервную копию сохранений. Не устанавливай несколько версий `MetelTimerModes.dll` одновременно.

### Установка

1. Установи MelonLoader 0.7.3 для EXE игры.
2. Распакуй архив мода целиком.
3. Запусти `Install-Mod.bat` и выбери `.exe` игры. Установщик создаст папку `Mods`, если её нет, и спросит перед заменой существующей DLL мода. `Install-Mod.ps1` и папка `Mods` из архива должны находиться рядом с батником.
4. Запусти игру и нажми **F2**, чтобы открыть или скрыть меню мода.

Установщик копирует только мод и **не устанавливает MelonLoader**. Также можно вручную скопировать `Mods\MetelTimerModes.dll` из архива в папку `Mods` рядом с EXE игры, заменив предыдущую версию.

### Как пользоваться

- Выбери режим во вкладке **Timer**. Смена режима не сбрасывает и не запускает остановленный таймер. Таймер использует игровое время и останавливается на паузе. Штатные события остановки таймера работают во всех режимах.
- Чтобы назначить рестарт, выбери **Timer → Change key** и нажми нужную клавишу. **Esc** отменяет назначение, **Clear binding** удаляет бинд. **F2** зарезервирована для меню. Рестарт сразу завершает текущую попытку; на экране Restart может понадобиться нажать Continue.
- При открытом меню курсор освобождается, но игра **не ставится на паузу** и нажатия могут попадать в игру. При необходимости сначала поставь её на паузу.
- Во вкладке **Codes** введи нужное количество цифр и нажми **Save**. Начальные нули и повторяющиеся цифры разрешены. Код сундука Юджина не связан с LockBox; пока он не задан, игра использует случайный код.
- Выбрав ползунок FPS, можно управлять им стрелками; **Home** и **End** выбирают крайние значения. Unlock снимает программное ограничение, но не ограничения оборудования и драйвера.

### Сборка из исходников

В папке `Source` находятся исходный код C#, файл проекта и встроенный логотип. Установи .NET SDK и обеспечь доступ к справочным сборкам .NET Framework 4.7.2 через NuGet. В PowerShell укажи пути к библиотекам игры и MelonLoader:

```powershell
$env:METEL_MANAGED = 'C:\path\to\Metel\Metel_Data\Managed'
$env:MELON_MANAGED = 'C:\path\to\Metel\MelonLoader\net35'
cd Source
dotnet build -c Release
```

Готовая DLL появится в `Source\bin\Release\net472\MetelTimerModes.dll`.

### Проверка и помощь

DLL мода собрана, но версия 1.11 и установщик не проверялись в запущенной игре и на Windows. Если возникнет проблема, приложи `MelonLoader\Latest.log`, название главы, выбранный режим или пресет и опиши действия, после которых появилась ошибка.

---

## Creators / Создатели

- **t300850** — [speedrun.com](https://www.speedrun.com/users/t300850) · [GitHub](https://github.com/T300850)
- **Lol_official1**

## Sponsors / Спонсоры

- **zup130**
- **mistiz**

[TL12 Mods on Telegram](https://t.me/TL12Mods) · [DonationAlerts](https://www.donationalerts.com/r/cyberfoxspeedrunner)
