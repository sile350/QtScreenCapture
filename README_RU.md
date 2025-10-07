# Screen Capture - Захват Экрана

<p align="center">
  <img src="doc/images/screencapture.jpg" alt="Screen Capture Application" width="800"/>
</p>

<p align="center">
  <a href="README.md">English</a> | <strong>Русский</strong>
</p>

## 📝 О проекте

**Screen Capture** — кроссплатформенное приложение на Qt 6 для захвата экрана и окон в режиме реального времени. Приложение демонстрирует использование современного Qt Multimedia API для создания мощного инструмента захвата с интуитивным интерфейсом.

## ✨ Возможности

- 🖥️ **Захват экрана** — выбор и захват любого подключенного монитора
- 🪟 **Захват окон** — захват конкретных окон приложений
- 📺 **Предварительный просмотр** — мгновенное отображение в реальном времени
- 🎯 **Простой интерфейс** — интуитивное управление одним кликом
- 🔄 **Динамическое обновление** — автоматическое обновление списка источников
- ⚠️ **Обработка ошибок** — понятные сообщения о проблемах
- 🌍 **Кроссплатформенность** — Windows, macOS, Linux, Android, iOS

## 🛠️ Технологии

- **Qt 6** (Qt 5 также поддерживается)
- **C++17**
- **CMake** / **qmake**
- Qt Widgets, Qt Multimedia, Qt Multimedia Widgets

## 📋 Требования

### Минимальные требования

- Qt 6.x или Qt 5.x
- CMake 3.16+ или qmake
- C++17 совместимый компилятор (GCC 7+, Clang 5+, MSVC 2017+)

### Поддерживаемые платформы

- ✅ Windows 10/11
- ✅ macOS 10.14+
- ✅ Linux (X11/Wayland)
- ✅ Android
- ✅ iOS

## 🚀 Быстрый старт

### Сборка

```bash
# Клонирование
git clone https://github.com/sile350/QtScreenCapture.git
cd screencapture

# Сборка с CMake
mkdir build && cd build
cmake ..
cmake --build .

# Или с qmake
qmake screencapture.pro
make
```

### Запуск

```bash
./screencapture         # Linux/macOS
screencapture.exe       # Windows
```

## 📖 Использование

1. **Выберите источник** — экран или окно из списка
2. **Нажмите "Start"** — начните захват
3. **Наблюдайте** — видео появится справа
4. **Остановите** — нажмите "Stop" когда закончите

### Советы

- 💡 Правый клик на списке окон → "Update Windows List" для обновления
- 💡 Выбор автоматически переключает режим захвата
- 💡 Приложение уведомит, если окно стало недоступным

## 🏗️ Структура проекта

```
screencapture/
├── main.cpp                      # Точка входа
├── screencapturepreview.h/cpp    # Главный класс UI
├── screenlistmodel.h/cpp         # Модель списка экранов
├── windowlistmodel.h/cpp         # Модель списка окон
├── CMakeLists.txt                # CMake
├── screencapture.pro             # qmake
├── android/                      # Android конфигурация
├── doc/                          # Документация
└── .github/                      # GitHub конфигурация
```

## 🤝 Участие в разработке

Мы рады любому вкладу! Пожалуйста, прочитайте [CONTRIBUTING.md](CONTRIBUTING.md) для подробностей.

### Быстрый старт для разработчиков

1. Форкните репозиторий
2. Создайте ветку (`git checkout -b feature/amazing`)
3. Зафиксируйте изменения (`git commit -m 'feat: добавить функцию'`)
4. Отправьте в ветку (`git push origin feature/amazing`)
5. Откройте Pull Request

## 📄 Лицензия

BSD-3-Clause License. См. [LICENSE](LICENSE) для подробностей.

Части кода основаны на официальных примерах Qt.

## 🙏 Благодарности

- [Qt Project](https://www.qt.io/) — за замечательный фреймворк
- Сообщество Qt — за поддержку и документацию
- Всем контрибьюторам проекта

## 📞 Связь

- **Issues:** [GitHub Issues](https://github.com/yourusername/screencapture/issues)
- **Обсуждения:** [GitHub Discussions](https://github.com/yourusername/screencapture/discussions)

## 🗺️ Дорожная карта

- [ ] Сохранение видео в файл (MP4, AVI, MKV)
- [ ] Захват аудио
- [ ] Настройки качества и разрешения
- [ ] Горячие клавиши
- [ ] Захват выбранной области
- [ ] Аннотации и рисование

## 📊 Статус сборки

| Платформа | Статус |
|-----------|--------|
| Windows   | [![Windows](https://github.com/yourusername/screencapture/workflows/Build%20and%20Test/badge.svg)](https://github.com/yourusername/screencapture/actions) |
| macOS     | [![macOS](https://github.com/yourusername/screencapture/workflows/Build%20and%20Test/badge.svg)](https://github.com/yourusername/screencapture/actions) |
| Linux     | [![Linux](https://github.com/yourusername/screencapture/workflows/Build%20and%20Test/badge.svg)](https://github.com/yourusername/screencapture/actions) |

## 🔧 Решение проблем

### Проблема: Черный экран при захвате

**Решение:** Проверьте разрешения приложения в настройках системы (особенно на macOS/Windows 10+).

### Проблема: Не видны некоторые окна

**Решение:** Используйте контекстное меню для обновления списка окон.

### Проблема: Ошибка компиляции

**Решение:** Убедитесь, что установлены все модули Qt (Widgets, Multimedia, MultimediaWidgets).

## 📚 Дополнительные ресурсы

- [Документация Qt Multimedia](https://doc.qt.io/qt-6/qtmultimedia-index.html)
- [QScreenCapture Class](https://doc.qt.io/qt-6/qscreencapture.html)
- [QWindowCapture Class](https://doc.qt.io/qt-6/qwindowcapture.html)

---

<p align="center">
  Сделано с ❤️ с использованием Qt
</p>

