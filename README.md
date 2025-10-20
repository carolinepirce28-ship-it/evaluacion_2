# Evaluacion_2
 App Android: Interacción Avanzada con Intents y Servicios

---
Caroline Pirce



## **Descripción del Proyecto**

Este prototipo consiste en una aplicación Android que integra **intents explícitos e implícitos**, **servicios en segundo plano**, **BroadcastReceivers** y el manejo de **Threads** para mejorar la experiencia de usuario.  

El objetivo principal fue **practicar la navegación entre pantallas internas**, **interactuar con aplicaciones del sistema** y **gestionar tareas en background sin bloquear la interfaz**, logrando una estructura modular y eficiente.

---

### 🔹 Implícitos (5)

| Nº | Acción | Descripción |
|----|--------|-------------|
| 1 | 🌍 Abrir ubicación en Google Maps | Muestra un marcador en la ubicación de Santo Tomás. |
| 2 | 🌐 Abrir sitio web | Navega hacia [santotomas.cl](https://www.santotomas.cl) desde el navegador. |
| 3 | 📧 Enviar correo | Prellena destinatario, asunto y cuerpo en la app de correo. |
| 4 | 📞 Llamar (marcador) | Abre la app de teléfono con número prellenado. |
| 5 | 📶 Abrir configuración Wi-Fi | Redirige al menú de ajustes de Wi-Fi del dispositivo. |

### 🔹 Explícitos (3)

| Nº | Acción | Descripción |
|----|--------|-------------|
| 1 | 👤 Home → PerfilActivity | Envía el correo del usuario y recibe el nombre editado usando `ActivityResultLauncher`. |
| 2 | ⚙️ Home → MiService | Inicia o detiene un servicio en **segundo plano** para ejecutar tareas sin bloquear la UI. |
| 3 | 📷 Home → CamaraActivity | Abre la cámara interna de la app para capturar imágenes y mostrarlas. |

---

## 🛠 Servicios y BroadcastReceivers

- **MiService:** ejecuta tareas de fondo mientras la app está abierta o minimizada.  
- **BroadcastReceiver interno:** permite recibir mensajes desde el servicio o desde el sistema, demostrando comunicación interna sin interrumpir al usuario.  
- **Threads:** aseguran que las acciones del servicio y la linterna no bloqueen la interfaz principal.

---

## 🔐 Manejo de Permisos

- La **linterna** y la **cámara** requieren permisos (`CAMERA`).  
- Se verifica el permiso antes de ejecutar acciones, siguiendo las políticas de seguridad de Android.  
- Uso de `ActivityResultLauncher` para manejar resultados y permisos de forma segura.

---

Capturas de Pantalla

![Pantalla Home](![WhatsApp Image 2025-10-19 at 23 40 35](https://github.com/user-attachments/assets/7668a82c-48a3-4ef9-9b91-55669ff9acce)
)  

![Intent Maps](![WhatsApp Image 2025-10-19 at 23 40 36 (2)](https://github.com/user-attachments/assets/a903ed24-2a0c-47ac-86fe-5ece1c7ceaf3)
)  

<img width="1260" height="466" alt="image" src="https://github.com/user-attachments/assets/6020b8db-7a93-4b13-9e83-ac79fa07388a" />
<img width="1093" height="505" alt="image" src="https://github.com/user-attachments/assets/dd632a4e-00eb-4937-9ee2-2ec217e7ba55" />



Lecciones Aprendidas

Comprendimos la diferencia entre intents explícitos (internos) y implícitos (apps/sistema).

Aprendimos a usar Services para ejecutar tareas en segundo plano sin bloquear la UI.

Integración de BroadcastReceivers para comunicación interna y externa.

Manejo de Threads y permisos de usuario para optimizar la experiencia.

Mejora en la estructura modular y UX del proyecto.



