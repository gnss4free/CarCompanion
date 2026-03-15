# 🚗 CarCompanion - Проект GNSS4Free

[Русский](#-carcompanion---проект-gnss4free) | [English](#-carcompanion---gnss4free-project)

---

## CarCompanion - Проект GNSS4Free

### 📱 Описание проекта

**CarCompanion** — это мобильное приложение на базе Android, которое преобразует смартфон в цифрового ассистента (компаньона) для автомобильных информационных систем на базе Android по образу и подобию Android Auto.

### 🎯 Текущая функциональность

1. **Автоматическая раздача интернета**
   - Активируется при подключении автомобиля через Bluetooth
   - Автоматически включает точку доступа (HotSpot) на телефоне
   - Обеспечивает интернет-соединение для автомобильной информационной системы

2. **Передача геокоординат**
   - Активируется при наличии в сети системы-потребителя (в остальных случаях не тратится энергия на передачу данных "вхолостую")
   - Система-провайдер(как правило, телефон с GNSS-чипом) отправляет геоданные (геолокацию) по локальной сети системам-потребителям (автомобилю без GNSS-чипа)
   - Система-получатель получая данные о геолокации делает их доступными Android-приложениям через функциональность ОС "Приложение для фиктивных положений"

3. **Передача буфера обмена и текста**
   - Активируется выделение текста в любом приложении и выбором в диалоге "Поделиться/Share" приложения Car Companion
   - Активируется выбором в шторке уведомления команды "Отправить буфер" при условии, что в буфере обмена есть текст
   - Система-потребитель получает переданный текст (отражается в карточке "Сообщения") и автоматически размещает его в буфере обмена своей системы

### Предпосылки проекта

Китайские автомобили для глобального рынка, в особенности для рынка СНГ, часто поставляются без полной функциональности в информационно-развлекательной области (Infotainment). Большинство таких автомобилей лишены:
- **Телематического блока** (подключение к интернету, управление и контроль)
- **Встроенного GPS-модуля** и блока навигации

### Преимущества CarCompanion

#### 1. **Простой и лаконичный интерфейс**
   - Минималистичный дизайн
   - Интуитивно понятная настройка, не требующая вводить IP-адреса, названия сетевых интерфейсов и тому подобного

#### 2. **Надежная логика работы**
   - Использование **FSM** (Finite State Machine — конечный автомат) для управления состоянием приложения
   - Эффективный и предсказуемый алгоритм установления связи "Провайдер ↔ Потребитель"

#### 3. **Максимальная производительность**
   - Эффективный **Бинарный протокол**
   - Минимальная задержка при передаче данных

#### 4. **Не требует вложений**
   - Программа бесплатна для частного использования
   - Не требуется преобретать дополнительные устройства/модули, выполнять аппаратную доработку автомобиля
   - Идеально, чтобы "попробовать"

### Технические требования
- **Платформа для Провайдера:** система на базе Android 6.0 и выше (API 23), для управления HotSpot требуется программа Macrodroid Connectivity Helper
- **Платформа для Потребителя:** система на базе Android 6.0 и выше (API 23), открытый доступ к настройкам разработчика
- **Статус:** Публичная бета-версия
- **Репозиторий:** https://github.com/gnss4free/CarCompanion

---

## CarCompanion - GNSS4Free Project

### Project Description

**CarCompanion** is an Android mobile application that transforms a smartphone into a digital assistant (companion) for Android-based car information systems on Android Auto manner.

### Current Functionality

1. **Automatic Internet Sharing**
   - Triggered upon Bluetooth connection with the vehicle
   - Automatically activates the HotSpot (Wi-Fi access point) on the phone
   - Provides internet connectivity for the car's information system

2. **GNSS Coordinates Broadcasting**
   - Activated only when a consumer system is present in the network (no wasted energy on idle data transmission)
   - Provider system (typically a phone with GNSS chip) sends geolocation data over the local network to consumer systems (vehicle without GNSS chip)
   - Consumer system receives geolocation data and makes it available to Android applications through the OS functionality "Mock Location Provider"

3. **Clipboard and plain Text sending/receiving**
   - Activates when user share Text via "Share" functionality of Android OS
   - Activate wher user use action "Send Clipboard" via Notification action of Car Companion app
   - System-consumer receive this message and copy it into system Clipboard for late use

### Project Motivation

Chinese vehicles for the global market, particularly for the CIS region, are often shipped without full functionality in the infotainment area. Most such vehicles lack:
- **Telematics module** (internet connectivity, management and control)
- **Built-in GPS module** and navigation unit

### Key Advantages of CarCompanion

#### 1. **Simple and Concise Interface**
   - Minimalist design
   - Intuitive setup that doesn't require entering IP addresses, network interface names, and the like

#### 2. **Reliable Operation Logic**
   - Uses **FSM** (Finite State Machine) for managing application state
   - Efficient and predictable algorithm for establishing "Provider ↔ Consumer" connection

#### 3. **Maximum Performance**
   - Efficient **Binary protocol**
   - Minimal latency in data transmission

#### 4. **No Investment Required**
   - The application is free for personal use
   - No need to purchase additional devices/modules or perform hardware modifications to the vehicle
   - Perfect for "trying it out"

### Technical Requirements

- **Platform for Provider:** Android 6.0 (API 23), requires an additional application for HotSpot management (MacroDroid Connectivity Helper)
- **Platform for Consumer:** Android 6.0 (API 23), requires Developer options to be enabled for Mock Location management. 
- **Status:** Public beta
- **Repository:** https://github.com/gnss4free/CarCompanion

---

