# 📷 Smart Witness - Configuración BLE

**Interfaz web para configuración avanzada del Smart Witness ESP32-CAM via Bluetooth LE**

🌐 **Sitio web**: [https://arielzubigaray.github.io/smart-witness-ble-config/](https://arielzubigaray.github.io/smart-witness-ble-config/)

## 🎯 Descripción

Esta página web permite configurar dispositivos Smart Witness ESP32-CAM utilizando tecnología Bluetooth LE (BLE) de forma intuitiva y segura. La interfaz guía al usuario paso a paso para establecer la configuración completa del dispositivo sin necesidad de conocimientos técnicos.

## ✨ Características Principales

### 🔧 Configuración Completa
- **Información del dispositivo**: Nombre personalizado y mensaje de alerta
- **Usuario de Telegram**: Validación automática de formato y permisos
- **Conectividad WiFi**: Configuración de red principal
- **Chat vecinal**: Configuración opcional para alertas comunitarias
- **Integración Telegram**: Auto-configuración del bot @SmartWitnessBot

### 🛡️ Seguridad y Validación
- **Validación en tiempo real** de campos requeridos
- **Verificación de formato** de usuario Telegram (@usuario)
- **Conexión segura BLE** con UUIDs únicos
- **Validación de credenciales WiFi** antes de guardar

### 🎨 Experiencia de Usuario
- **Interfaz progresiva** con pasos claros numerados
- **Validación visual** con iconos y mensajes informativos
- **Responsivo** optimizado para dispositivos móviles
- **Feedback en tiempo real** del estado de configuración

## 🚀 Tecnologías Utilizadas

- **HTML5 + CSS3**: Interfaz moderna y responsiva
- **JavaScript ES6+**: Lógica de aplicación y validaciones
- **Web Bluetooth API**: Comunicación BLE nativa del navegador
- **Progressive Web App**: Funcionalidades nativas

## 📱 Compatibilidad

### ✅ Navegadores Soportados
- **Chrome/Chromium** 56+ (Android/Desktop)
- **Edge** 79+ (Windows/Android)
- **Opera** 43+ (Android/Desktop)
- **Samsung Internet** 6.0+

### 📵 Limitaciones
- **iOS Safari**: No soporta Web Bluetooth API
- **Firefox**: Soporte experimental (requiere flags)
- **Conexión HTTPS**: Requerida para BLE

## 🔌 Protocolo de Comunicación BLE

### Service UUID
```
12345678-1234-1234-1234-123456789abc
```

### Características Principales
- **Config**: `87654321-4321-4321-4321-cba987654321` (Write)
- **Status**: `11111111-2222-3333-4444-555555555555` (Notify)
- **Device ID**: `aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee` (Notify)
- **Chat ID**: `ffffffff-eeee-dddd-cccc-bbbbbbbbbbbb` (Write)
- **Fields**: `12121212-3434-5656-7878-909090909090` (Notify)
- **Step**: `34343434-5656-7878-9090-121212121212` (Read/Write/Notify)

### Formato de Configuración JSON
```json
{
  "deviceName": "Casa Juan - Entrada",
  "telegramUser": "@juan_perez",
  "ssid": "MiWiFi_Principal",
  "password": "miPasswordWiFi",
  "alertMsg": "ALERTA DE SEGURIDAD ACTIVADA",
  "vecinoChatId": "-1001234567890"
}
```

## 🔄 Flujo de Configuración

### 1. Detección de Dispositivo
- Busca dispositivos con nombre `SmartWitness_*`
- Establece conexión GATT segura
- Suscripción a notificaciones BLE

### 2. Configuración de Campos
- **Paso 1**: Información del dispositivo
- **Paso 2**: Usuario de Telegram (con validación)
- **Paso 3**: Credenciales WiFi
- **Paso 4**: Chat vecinal (opcional)

### 3. Prueba y Validación
- Envío de configuración via BLE
- Prueba de conectividad WiFi en dispositivo
- Generación de Device ID único

### 4. Integración Telegram
- Apertura automática de @SmartWitnessBot
- Auto-configuración de Chat ID
- Envío de foto de prueba

### 5. Confirmación
- Pantalla de éxito con instrucciones finales
- Dispositivo listo para operación

## 🛠️ Desarrollo Local

### Prerequisitos
- Navegador compatible con Web Bluetooth
- Servidor HTTPS local (requerido para BLE)
- Dispositivo ESP32-CAM con firmware Smart Witness

### Instalación
```bash
# Clonar repositorio
git clone https://github.com/ArielZubigaray/smart-witness-ble-config.git
cd smart-witness-ble-config

# Servir localmente con HTTPS
python -m http.server 8000 --bind localhost
# O usar cualquier servidor HTTPS local
```

## 📋 Roadmap

### Versión Actual (1.0)
- ✅ Configuración BLE completa
- ✅ Validación de usuario Telegram
- ✅ Auto-configuración de Chat ID
- ✅ Interfaz responsive

### Próximas Versiones
- 🔄 **v1.1**: Multi-idioma (EN/ES)
- 🔄 **v1.2**: Configuración de múltiples redes WiFi
- 🔄 **v1.3**: Historial de dispositivos configurados
- 🔄 **v1.4**: Modo offline con sincronización posterior

## 🤝 Contribución

### Reportar Issues
1. Usa el [sistema de issues](https://github.com/ArielZubigaray/smart-witness-ble-config/issues)
2. Incluye información del navegador y dispositivo
3. Describe pasos para reproducir el problema

## 📄 Licencia

Este proyecto está bajo la licencia MIT.

## 🔗 Enlaces Relacionados

- **Firmware ESP32-CAM**: [smart-witness-esp32cam](https://github.com/ArielZubigaray/smart-witness-esp32cam)
- **Bot de Telegram**: [@SmartWitnessBot](https://t.me/SmartWitnessBot)

---

**Smart Witness** - Sistema de seguridad inteligente con alertas comunitarias automáticas

📧 **Contacto**: [Issues en GitHub](https://github.com/ArielZubigaray/smart-witness-ble-config/issues) | 🌐 **Web**: [Smart Witness Config](https://arielzubigaray.github.io/smart-witness-ble-config/)