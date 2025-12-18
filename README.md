# Chat App JS Only

Una aplicación de chat en tiempo real construida completamente con JavaScript vanilla, sin frameworks ni dependencias externas.

## 🌟 Características

### Funcionalidades Principales
- **Chat en tiempo real**: Actualización automática de mensajes cada 5 segundos
- **Envío de mensajes**: Límite de 140 caracteres por mensaje
- **Identificación de usuario**: Los mensajes del usuario "Osman" se marcan como propios
- **Tema claro/oscuro**: Cambio entre modos con persistencia en localStorage

### Características Visuales
- **Burbujas de chat diferenciadas**: 
  - Mensajes propios alineados a la derecha en azul
  - Mensajes de otros usuarios alineados a la izquierda
- **Detección automática de contenido**:
  - Imágenes (jpg, jpeg, gif, png, webp) se muestran como previsualizaciones
  - Enlaces se muestran con tarjetas de vista previa
- **Animaciones suaves**: Transiciones al mostrar mensajes
- **Contador de caracteres**: Indicador visual del límite de 140 caracteres

### Optimizaciones de UX
- **Scroll inteligente**: 
  - Auto-scroll al final cuando llegas al fondo
  - Preserva posición cuando estás viendo mensajes antiguos
- **Envío con Enter**: Presiona Enter para enviar mensajes rápidamente
- **Diseño responsivo**: Se adapta a diferentes tamaños de pantalla

## 🛠️ Tecnologías

- **HTML5**: Estructura básica
- **JavaScript Vanilla**: Lógica completa de la aplicación
- **CSS en JS**: Estilos aplicados dinámicamente
- **Fetch API**: Comunicación con el servidor
- **localStorage**: Persistencia de preferencias de tema

## 📡 API

La aplicación se conecta a: `https://chat.nrywhite.lat/chats`

### Endpoints utilizados:
- **GET**: Obtiene todos los mensajes
- **POST**: Envía un nuevo mensaje

### Estructura de mensaje:
```json
{
  "username": "Osman",
  "message": "Texto del mensaje"
}
```

## 🎨 Temas

### Modo Claro
- Fondo blanco
- Texto negro
- Burbujas de mensajes ajenos en gris claro

### Modo Oscuro
- Fondo negro (#121212)
- Texto blanco
- Burbujas de mensajes ajenos en gris oscuro (#333)

## 🚀 Uso

1. Abre el archivo HTML en un navegador
2. Escribe tu mensaje en el campo de texto
3. Presiona "Send" o Enter para enviar
4. Cambia entre tema claro/oscuro con el botón en la esquina superior derecha

## 📝 Limitaciones

- Límite de 140 caracteres por mensaje
- Usuario fijo como "Osman" (hardcodeado)
- Actualización cada 5 segundos (no WebSockets)
- Sin sistema de autenticación
- Sin edición o eliminación de mensajes

## 🔧 Configuración

Puedes modificar estos valores en el código:

```javascript
const API_URL = 'https://chat.nrywhite.lat/chats'; // URL del servidor
const MAX_MESSAGE_LENGTH = 140; // Límite de caracteres
const REFRESH_INTERVAL = 5000; // Intervalo de actualización (ms)
```

## 💡 Características Técnicas

- **Sin dependencias**: 100% JavaScript vanilla
- **Manejo de errores**: Try-catch en todas las operaciones asíncronas
- **Validación de datos**: Sanitización de mensajes recibidos
- **Optimización de renders**: Uso de DocumentFragment y requestAnimationFrame
- **Detección de URLs**: Expresiones regulares para enlaces e imágenes
- **Gestión de estado**: Variables globales para manejo de mensajes y scroll

## 📄 Licencia

Código de ejemplo educativo - Uso libre
