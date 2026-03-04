# 🚗 CarCompanion - GNSS4Free Project

[🇷🇺 Русский](#-карcompanion---проект-gnss4free) | [🇬🇧 English](#-carcompanion---gnss4free-project-1)

---

## 🇷🇺 CarCompanion - Проект GNSS4Free

### 📱 Описание проекта

**CarCompanion** — это мобильное приложение на базе Android, которое преобразует смартфон в цифрового ассистента (компаньона) для автомобильных информационных систем на базе Android.

### 🎯 Текущая функциональность (Этап 1)

Первый релиз реализует две ключевые функции:

1. **Автоматическая раздача интернета**
   - Активируется при подключении автомобиля через Bluetooth
   - Автоматически включает точку доступа (HotSpot) на телефоне
   - Обеспечивает интернет-соединение для автомобильной информационной системы

2. **Передача геокоординат**
   - Активируется при наличии в сети системы-потребителя (в остальных случаях не тратится энергия на передачу данных "вхолостую")
   - Система-провайдер(как правило, телефон с GNSS-чипом) отправляет геоданные (геолокацию) по локальной сети системам-потребителям (автомобилю)
   - Система-получатель получая данные о геолокации делает их доступными Android-приложениям через функциональность ОС "Приложение для фиктивных положений"

### 📋 Предпосылки проекта

Китайские автомобили для глобального рынка, в особенности для рынка СНГ, часто поставляются без полной функциональности в информационно-развлекательной области (Infotainment). Большинство таких автомобилей лишены:
- **Телематического блока** (подключение к интернету, управление и контроль)
- **Встроенного GPS-модуля** и блока навигации

### 🔧 Почему именно CarCompanion?

На рынке уже существуют подобные решения, однако они имеют те или иные недостатки: они либо устарели, либо имеют сложный в настройке интерфейс, либо требуют внешних систем, автоматизирующих их использование (типа Macrodroid или Tasker).  В любом случае, мне было просто интересно разработать систему, используя современные технологии программирования и которая устроила бы лично меня.

### ✨ Ключевые преимущества CarCompanion

#### 1. **Простой и лаконичный интерфейс**
   - Минималистичный дизайн
   - Интуитивно понятная настройка, не требующая вводить IP-адреса, названия сетевых интерфейсов и тому подобного

#### 2. **Надежная логика работы**
   - Использование **FSM** (Finite State Machine — конечный автомат) для управления состоянием приложения
   - Эффективный и предсказуемый алгоритм установления связи "Провайдер ↔ Потребитель"

#### 3. **Максимальная производительность**
   - Эффективный **Бинарный протокол**
   - Минимальная задержка при передаче данных

### 📊 Технические параметры

- **Платформа:** Android (минимальная версия: TBD)
- **Языки программирования:** Java/Kotlin
- **Лицензия:** GNU General Public License v3.0
- **Статус:** Активная разработка
- **Репозиторий:** https://github.com/gnss4free/CarCompanion

### 🚀 Roadmap

- [x] Этап 1: Базовая функциональность (GNSS + интернет)
- [ ] Этап 2: Расширенные функции (OBD-II интеграция, расширенная телеметрия)
- [ ] Этап 3: Веб-интерфейс и облачная синхронизация
- [ ] Этап 4: Поддержка iOS и Web-версий

### 📚 Документация

- [Архитектура проекта](docs/ARCHITECTURE.md)
- [Установка и настройка](docs/INSTALLATION.md)
- [Как контрибьютить](docs/CONTRIBUTING.md)

### 📄 Лицензия

Проект распространяется под лицензией **GNU General Public License v3.0**. Подробности в файле [LICENSE](LICENSE).

---

## 🇬🇧 CarCompanion - GNSS4Free Project

### 📱 Project Description

**CarCompanion** is an Android mobile application that transforms a smartphone into a digital assistant (companion) for Android-based car information systems.

The application is designed to make a mobile phone a full-fledged assistant to a vehicle through wireless connectivity, providing data exchange and services between the phone and the car's infotainment system.

### 🎯 Current Functionality (Phase 1)

The first release implements two key features:

1. **Automatic Internet Sharing**
   - Automatic activation of the HotSpot (Wi-Fi access point) on the phone
   - Triggered upon Bluetooth connection with the vehicle
   - Provides internet connectivity for the car's information system

2. **GNSS Coordinates Broadcasting**
   - Transmission of GNSS data (geolocation) over the local network
   - Broadcasting GPS coordinates from the phone to the consumer (vehicle system)
   - Uses local network protocol for data exchange

### 📋 Project Prerequisites

Chinese vehicles for the global market, particularly for the CIS region, are often shipped without full Infotainment functionality. Most such vehicles lack:
- **Telematics module** (internet-based management and control)
- **Built-in GPS module** and navigation unit

**CarCompanion** solves these fundamental problems:
- ✅ Shares internet from smartphone to vehicle
- ✅ Provides navigation apps with GPS coordinates from the smartphone
- ✅ Automates the entire process without complex manual configuration

### 🔧 Why CarCompanion?

Similar solutions already exist on the market, but they have the following drawbacks:

| Problem | CarCompanion |
|---------|-------------|
| **Outdated applications** | Modern code with current Android APIs |
| **Complex interface** | ✅ **Simple and concise UI** |
| **Dependency on external systems** | ✅ **No need for Tasker, Macrodroid, etc.** |
| **Connection instability** | ✅ **Reliable logic thanks to FSM** |
| **Poor performance** | ✅ **Maximum performance** |

### ✨ Key Advantages of CarCompanion

#### 1. **Simple and Concise Interface**
   - Minimalist design
   - Intuitive navigation
   - Easy to enable/disable features with a single tap

#### 2. **Reliable Operation Logic**
   - Uses **FSM** (Finite State Machine)
   - Strict state management
   - Efficient and predictable algorithm for establishing "Provider ↔ Consumer" connection
   - Eliminates race conditions and instability

#### 3. **Maximum Performance**
   - **Binary protocol** instead of text formats (less data, higher speed)
   - Modern concurrent programming methods
   - Optimized battery resource usage
   - Minimal latency in data transmission

### 📊 Technical Parameters

- **Platform:** Android (minimum version: TBD)
- **Programming Languages:** Java/Kotlin
- **License:** GNU General Public License v3.0
- **Status:** Active Development
- **Repository:** https://github.com/gnss4free/CarCompanion

### 🚀 Roadmap

- [x] Phase 1: Basic functionality (GNSS + Internet sharing)
- [ ] Phase 2: Advanced features (OBD-II integration, extended telemetry)
- [ ] Phase 3: Web interface and cloud synchronization
- [ ] Phase 4: iOS and Web version support

### 📚 Documentation

- [Project Architecture](docs/ARCHITECTURE.md)
- [Installation and Setup](docs/INSTALLATION.md)
- [Contributing Guide](docs/CONTRIBUTING.md)

### 📄 License

The project is distributed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.

---

**Made with ❤️ by the gnss4free team**
