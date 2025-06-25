# 🚨 Smart Witness - Proyecto Unificado

**Sistema de seguridad inteligente con alertas comunitarias automáticas**

## 📋 Descripción del Proyecto

Smart Witness transforma alarmas domésticas tradicionales en una red de alertas comunitaria con evidencia fotográfica automática. El sistema se compone de dos componentes principales trabajando en conjunto:

## 🗂️ Componentes del Proyecto

### 📦 **Repositorios**

| Componente | Repositorio | Estado | Propósito |
|------------|-------------|--------|-----------|
| 🌐 **Web Interface** | [smart-witness-ble-config](https://github.com/ArielZubigaray/smart-witness-ble-config) | ✅ Público | Configuración BLE via navegador |
| 🔧 **Firmware** | [smart-witness-esp32cam](https://github.com/ArielZubigaray/smart-witness-esp32cam) | 🔒 Privado | Código ESP32-CAM con BLE |

### 🌐 **Servicios Externos**
- **Bot Telegram**: [@SmartWitnessBot](https://t.me/SmartWitnessBot)
- **Interfaz Live**: [smart-witness-config](https://arielzubigaray.github.io/smart-witness-ble-config/)

## 🎯 Arquitectura del Sistema

```
┌─────────────────────────────────────────────────────────────┐
│                    SMART WITNESS PROJECT                    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  🌐 Web Interface          📱 Firmware ESP32-CAM           │
│  ┌─────────────────┐      ┌─────────────────────────────┐   │
│  │ BLE Config      │◄────►│ Smart Witness Device        │   │
│  │ (Public Repo)   │ BLE  │ (Private Repo)              │   │
│  │                 │      │                             │   │
│  │ • HTML5 + JS    │      │ • Arduino C++               │   │
│  │ • Web Bluetooth │      │ • BLE Server                │   │
│  │ • GitHub Pages  │      │ • Camera Control            │   │
│  │ • User Validation│     │ • Telegram Integration      │   │
│  └─────────────────┘      └─────────────┬───────────────┘   │
│                                         │                   │
│                           ┌─────────────▼───────────────┐   │
│                           │    🤖 @SmartWitnessBot      │   │
│                           │    (Telegram Service)       │   │
│                           └─────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

## 🚀 Flujo de Operación Completo

### 1. **Configuración (Web Interface)**
```
Usuario → Navegador → BLE → ESP32-CAM → Configuración Guardada
```

### 2. **Operación Automática (Firmware)**
```
Alarma → Activación → Captura → Telegram → Notificaciones
```

### 3. **Integración Telegram (Ambos Componentes)**
```
Web Interface → Device ID → Bot → Chat Auto-Config → Foto Prueba
```

## 📊 Estado Actual del Proyecto

### ✅ **Completado (v2.0)**
- [x] Configuración BLE completa via web
- [x] Validación de usuario Telegram en tiempo real
- [x] Auto-configuración de Chat ID
- [x] Captura automática por activación de alarma
- [x] Notificaciones diferenciadas (personal/vecinal)
- [x] Protocolo BLE robusto con UUIDs únicos
- [x] Interfaz responsiva y user-friendly

### 🔄 **En Desarrollo**
- [ ] Múltiples redes WiFi con failover automático
- [ ] Grabación de video corto (5-10 segundos)
- [ ] Detección de movimiento independiente
- [ ] Geolocalización en alertas

### 🔮 **Roadmap Futuro**
- [ ] Mini App de Telegram para configuración avanzada
- [ ] Red mesh de múltiples dispositivos
- [ ] Análisis de imágenes con AI
- [ ] Integración con sistemas domóticos

## 🛠️ Tecnologías Utilizadas

### **Web Interface (BLE Config)**
- **Frontend**: HTML5, CSS3, JavaScript ES6+
- **APIs**: Web Bluetooth API, Progressive Web App
- **Hosting**: GitHub Pages
- **Protocolos**: HTTPS, BLE GATT

### **Firmware (ESP32-CAM)**
- **Platform**: Arduino Framework, ESP32 Core
- **Hardware**: ESP32-S, OV2640 Camera, BLE 4.2
- **Librerías**: UniversalTelegramBot, ArduinoJson, BLE
- **Protocolos**: WiFi, BLE, HTTPS, Telegram Bot API

## 📚 Documentación del Proyecto

### **Guías de Usuario**
- [📱 Configuración BLE](https://github.com/ArielZubigaray/smart-witness-ble-config#readme) - Setup paso a paso
- [🔧 Instalación Firmware](https://github.com/ArielZubigaray/smart-witness-esp32cam#readme) - Hardware y software

### **Documentación Técnica**
- [🔌 Protocolo BLE](https://github.com/ArielZubigaray/smart-witness-ble-config#-protocolo-de-comunicación-ble) - UUIDs y formato
- [📊 API Reference](https://github.com/ArielZubigaray/smart-witness-esp32cam#-protocolo-ble) - Características y comandos

### **Desarrollo**
- [💻 Setup Local Web](https://github.com/ArielZubigaray/smart-witness-ble-config#️-desarrollo-local) - Entorno web
- [🔧 Setup Local Firmware](https://github.com/ArielZubigaray/smart-witness-esp32cam#️-desarrollo) - Arduino IDE

## 🐛 Issues y Soporte

### **Reportar Problemas**
- **Web Interface**: [BLE Config Issues](https://github.com/ArielZubigaray/smart-witness-ble-config/issues)
- **Firmware**: [ESP32-CAM Issues](https://github.com/ArielZubigaray/smart-witness-esp32cam/issues)

### **Tipos de Issues Comunes**
- 🔵 **BLE**: Problemas de conexión Bluetooth
- 📱 **Telegram**: Configuración de bot o chats
- 📷 **Camera**: Captura de fotos o calidad
- 🌐 **WiFi**: Conectividad de red
- ⚙️ **Config**: Problemas de configuración

## 🤝 Contribución al Proyecto

### **Áreas de Contribución**
1. **UX/UI**: Mejoras en interfaz web
2. **Firmware**: Optimizaciones ESP32-CAM
3. **Documentación**: Guías y ejemplos
4. **Testing**: Pruebas en diferentes dispositivos
5. **Features**: Nuevas funcionalidades

### **Proceso de Desarrollo**
1. Fork del repositorio específico
2. Crear feature branch
3. Implementar cambios con tests
4. Submit pull request con descripción detallada
5. Review y merge

## 📄 Licencias

- **Web Interface**: MIT License
- **Firmware**: MIT License
- **Documentación**: CC BY-SA 4.0

## 🔗 Enlaces Importantes

### **Repositorios**
- 🌐 [smart-witness-ble-config](https://github.com/ArielZubigaray/smart-witness-ble-config) - Configuración web
- 🔧 [smart-witness-esp32cam](https://github.com/ArielZubigaray/smart-witness-esp32cam) - Firmware dispositivo

### **Servicios Live**
- 📱 [Configurador Web](https://arielzubigaray.github.io/smart-witness-ble-config/) - Interface BLE
- 🤖 [@SmartWitnessBot](https://t.me/SmartWitnessBot) - Bot Telegram

### **Documentación Externa**
- 📋 [Product Brief](../docs/Smart%20Witness%20-%20Product%20Brief.md) - Especificaciones completas
- 📊 [Technical Analysis](../docs/Technical%20Analysis.md) - Análisis técnico detallado

---

## 🏷️ Project Topics

`smart-witness` `esp32-cam` `ble-configuration` `telegram-bot` `security-system` `iot-device` `community-alerts` `web-bluetooth` `arduino` `surveillance`

---

**🚨 Smart Witness Project** - Convirtiendo alarmas tradicionales en redes de alerta comunitaria inteligente

📧 **Contacto**: GitHub Issues | 🌐 **Demo**: [Smart Witness Config](https://arielzubigaray.github.io/smart-witness-ble-config/) | 📱 **Bot**: [@SmartWitnessBot](https://t.me/SmartWitnessBot)
