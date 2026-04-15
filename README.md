# 🎮 High Game Priority

[![Windows](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square&logo=windows)](https://www.microsoft.com/windows)
[![Registry](https://img.shields.io/badge/Edit-Registry-0078D6?style=flat-square&logo=windows)](https://learn.microsoft.com/ru-ru/windows/win32/sysinfo/registry)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

**Автоматическое назначение высокого приоритета процессора для игр в Windows.**

Этот репозиторий содержит `.reg` файлы, которые одним нажатием добавляют в реестр Windows настройку для запуска игр с **высоким приоритетом (High)**. Это позволяет игре получать больше процессорного времени, снижая количество микро-задержек (статтеров) и повышая стабильность FPS.

---

## 📦 Доступные скрипты

| Файл | Игра | Процесс |
| :--- | :--- | :--- |
| [cs2_high.reg](https://raw.githubusercontent.com/Groyz-soft/hight-game-priority/main/cs2_high.reg) | Counter-Strike 2 | cs2.exe |
| [deadlock_high.reg](https://raw.githubusercontent.com/Groyz-soft/hight-game-priority/main/deadlock_high.reg) | Deadlock | deadlock.exe |
| [dota2_high.reg](https://raw.githubusercontent.com/Groyz-soft/hight-game-priority/main/dota2_high.reg) | Dota 2 | dota2.exe |
| [hoi4_high.reg](https://raw.githubusercontent.com/Groyz-soft/hight-game-priority/main/hoi4_high.reg) | Hearts of Iron IV | hoi4.exe |

> 💡 **Хотите другую игру?** Создайте [Issue](https://github.com/Groyz-soft/hight-game-priority/issues) с названием игры и процесса, и я добавлю скрипт.

---

## 🚀 Быстрый старт

1. Нажмите на ссылку нужного `.reg` файла в таблице выше
2. Нажмите **Ctrl + S** или сохраните файл через браузер
3. **Дважды кликните** по скачанному файлу
4. Нажмите **«Да»** → **«Да»** в окнах подтверждения
5. **Перезагрузите компьютер**

Готово! После перезагрузки игра всегда будет запускаться с высоким приоритетом.

> ⚠️ Если появляется ошибка «Доступ запрещён», нажмите на файл правой кнопкой мыши и выберите **«Запуск от имени администратора»**.

---

## 🛠️ Как проверить результат

1. Запустите игру
2. Откройте **Диспетчер задач** (`Ctrl + Shift + Esc`)
3. Перейдите на вкладку **«Подробности»**
4. Найдите процесс игры (например, `cs2.exe`)
5. Нажмите правой кнопкой мыши → **«Задать приоритет»**

Напротив пункта **«Высокий»** должна стоять отметка. ✅

---

## 📊 Как это работает

```mermaid
graph LR
    A[Запуск игры] --> B{Есть настройка в реестре?}
    B -- Да --> C[Высокий приоритет High]
    B -- Нет --> D[Обычный приоритет Normal]
