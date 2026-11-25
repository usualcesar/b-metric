# B-METRIC

Plataforma de monitoreo de la calidad del agua para productores camaroneros de Sinaloa, México. Proyecto de innovación social del equipo **Enactus 2027** (Tecmilenio, Culiacán).

La idea es una boya con sensores que flota en el estanque, mide el agua y envía los datos por 4G a una aplicación en el celular, para que el productor consulte sus estanques y reciba alertas sin tener que medir a mano a cada rato.

## ⚠️ Esto es un prototipo

- Es una **demostración de la interfaz**, no una aplicación terminada.
- **Todos los datos son simulados** y así se indica en pantalla. No son mediciones reales.
- No hay servidor, API ni base de datos. No se guarda ninguna cuenta, contraseña ni pago.
- El hardware (controlador LILYGO T-SIM7600G-H, sensores Atlas Scientific, conexión 4G) sigue en validación.

## Qué incluye

- Inicio de sesión simulado (correo y Google).
- Panel principal con el estado de los estanques (vista de lista y cuadrícula).
- Monitoreo de **pH, oxígeno disuelto, temperatura y salinidad**, con gráficas en vivo, 24 horas, 7 días y 30 días.
- Niveles de estado: **Normal, Aviso, Crítico y Sin conexión**.
- Alertas con historial, alarma de pantalla completa y notificaciones simuladas en pantalla.
- Filtro de falsas alarmas: la alerta salta tras 3 lecturas seguidas fuera de rango (configurable).
- Si un dispositivo pierde conexión, la app no presenta el último valor como actual: muestra la hora de la última lectura.
- Sección de dispositivos (identificadores y batería de demostración).
- Rangos editables por estanque.
- Bitácora de registros (alimentación, siembra, mortalidad, cosecha).
- Pantallas de suscripción y pago simuladas. El precio aparece como `[PRECIO]` porque aún no está definido.
- Un **simulador de sensores** (botón «Simulador») para provocar fallas y probar alertas y alarma.

## Rangos de referencia (preliminares)

| Parámetro | Normal | Crítico |
|---|---|---|
| Oxígeno disuelto | más de 5 mg/L | menos de 4 mg/L |
| Temperatura | 26 a 32 °C | menos de 24 °C o más de 33 °C |
| pH | 7.5 a 8.5 | menos de 7.0 o más de 9.0 (propuesta de demostración) |
| Salinidad | 15 a 25 ppt | sin definir |

Estos valores son preliminares y **deben validarse con un especialista**.

## Lo que todavía no existe

- Servidor, API y base de datos.
- Notificaciones push reales.
- Control de aireadores, bombas y alimentadores (funciones futuras).
- Turbidez, amoniaco, nitritos y alcalinidad (no confirmados para la primera versión).

## Cómo abrirlo

1. Descarga o clona este repositorio.
2. Abre el archivo `index.html` con tu navegador (doble clic).

No necesita instalar nada. Está pensado para verse como celular (columna de máximo 440 px); en computadora puedes usar el modo de dispositivo móvil de las herramientas de desarrollador del navegador. Las tipografías se cargan desde Google Fonts, así que sin internet se verá con la letra del sistema.

## Tecnología

Una sola página con HTML, CSS y JavaScript, sin librerías ni backend.
