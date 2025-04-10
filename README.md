
# 🛫 AeroReservas - Sistema de Gestión de Vuelos en Python

AeroReservas es una aplicación completa e interactiva desarrollada en Python que permite gestionar vuelos nacionales e internacionales. Integra un sistema de reservas aéreas, gestión de pasajeros, procesamiento de pagos, y una interfaz gráfica intuitiva mediante `Tkinter`.

## 🌟 Características destacadas

- 🧳 Gestión de pasajeros con datos personalizados.
- ✈️ Visualización y administración de vuelos nacionales e internacionales.
- 🛋️ Selección de clases de vuelo: económica, ejecutiva y primera clase.
- 💳 Procesamiento de pagos con múltiples métodos disponibles.
- 📜 Historial y cancelación de reservas por usuario.
- 🖼️ Visualización gráfica con imágenes de destino.
- 🎨 Interfaz moderna y funcional utilizando `Tkinter`.

---

## 🗂️ Estructura del Proyecto

El sistema está dividido en módulos, cada uno con una responsabilidad específica:

### `vuelo.py`
Define la jerarquía de clases de vuelo:

- `Vuelo`: Clase base abstracta con información general (origen, destino, fecha, precios, disponibilidad).
- `VueloNacional`: Subclase para vuelos dentro de Colombia.
- `VueloInternacional`: Subclase para vuelos hacia el exterior.

Incluye lógica para:
- Reservar o cancelar asientos.
- Obtener el tipo de vuelo.
- Mostrar información detallada.

---

### `pasajero.py`
Define la clase `Pasajero`, que contiene:
- Nombre completo.
- Documento de identidad (cédula o pasaporte).
- Correo electrónico (opcional).
  
El pasajero puede ser representado en forma de cadena para facilitar su impresión y visualización.

---

### `Reserva.py`
Encapsula la lógica de las reservas de vuelo:

- Asocia un `Pasajero` con un `Vuelo`.
- Permite definir clase de asiento, precio y medio de pago.
- Ofrece un método `mostrar_resumen()` para imprimir todos los detalles de la reserva.

---

### `Pago.py`
Simula el flujo completo del proceso de pago:

- Muestra medios disponibles (`Visa`, `MasterCard`, `American Express`, `Davivienda`, `Nequi`).
- Solicita número de tarjeta y monto a pagar.
- Valida si el monto ingresado es correcto.
- Devuelve el resultado del intento de pago.

Este módulo permite simular un entorno realista de cobro.

---

### `tkintter.py`
Este módulo actúa como **el núcleo del sistema**. Implementa la GUI y conecta todos los demás componentes.

Funciones clave:
- Inicializa vuelos por defecto (2 nacionales y 4 internacionales).
- Permite seleccionar tipo de vuelo, vuelo específico, clase, pasajero, y medio de pago.
- Realiza reservas con validación de disponibilidad y pago.
- Muestra historial por documento del pasajero.
- Cancela reservas de manera visual.
- Integra imágenes ilustrativas del destino.

Componentes gráficos:
- `AeroReservasGUI`: ventana principal.
- Botones para ver vuelos, hacer/cancelar reservas, historial, y salir.
- Cuadro de texto con scroll para mostrar resultados y mensajes.
- Área dedicada para imágenes.

---

## 🧑‍💻 Instalación y ejecución

### 🔧 Requisitos

- Python 3.8 o superior.
- Biblioteca estándar (`Tkinter` viene preinstalado en la mayoría de versiones de Python).

### 🚀 Pasos para ejecutar

1. **Clona el repositorio:**

```bash
git clone https://github.com/bellsis/Sistema-de-Reservas-APP.git
cd Sistema-de-Reservas-APP
```

2. **Ejecuta la interfaz principal:**

```bash
python tkintter.py
```

*Recomendado:* Usa un entorno virtual.

---

## 💳 Medios de pago compatibles

Los usuarios pueden elegir entre los siguientes métodos de pago simulados:

- Visa
- MasterCard
- American Express
- Davivienda
- Nequi

El sistema verifica que el monto sea el exacto, lo que permite evaluar el control del flujo de transacción de manera realista.

---

## 🧪 Ejemplo de flujo del usuario

1. El usuario ejecuta la aplicación.
2. Selecciona si desea ver vuelos nacionales o internacionales.
3. Elige un vuelo entre los disponibles.
4. Selecciona la clase (económica, ejecutiva o primera).
5. Ingresa su información personal.
6. Elige un medio de pago e introduce los datos requeridos.
7. Si el pago es válido, se confirma la reserva y se muestra el resumen.

---

## 🖼️ Detalle visual

La interfaz gráfica incluye:

- Layout dividido en secciones con botones de acción.
- Cuadro de salida con historial de interacciones.
- Panel lateral con imagen decorativa del destino (editable).
- Diálogos modales para cada paso del proceso (selección de vuelo, clase, pago).

---

## 🔄 Cancelación y seguimiento

- El usuario puede cancelar reservas usando su número de identificación.
- El sistema muestra una lista de reservas activas para esa persona.
- También es posible consultar el historial completo de vuelos reservados.

---

## 📦 Posibles mejoras futuras

- Base de datos persistente (SQLite o MySQL).
- Generación de tiquetes en PDF.
- Autenticación y perfiles de usuarios.
- Soporte multiidioma.
- Envío de correos de confirmación.
- Integración real con plataformas de pago.

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Puedes:

1. Hacer un fork del proyecto.
2. Crear una nueva rama (`feature/nueva-funcionalidad`).
3. Enviar un Pull Request explicando claramente tus cambios.

---

## 🪪 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---

## 📬 Contacto

¿Tienes dudas, sugerencias o comentarios? Escríbeme:

- ✉️ Email: luis@ejemplo.com
- 🐙 GitHub: [@bellsis](https://github.com/bellsis)

---
