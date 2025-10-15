# DETECCIÓN DE CARACTERISTICAS HTML5
# HTML5 no es una Entidad Única
HTML5 no es un solo "objeto" que se pueda detectar de una vez; es una colección de características individuales
(como Canvas, Video, Geolocalización, Web Workers, etc.). Por lo tanto, el soporte en navegadores antiguos o nuevos debe detectarse función por función.
# Técnicas de Detección de Características
La Detección de Características se basa en inspeccionar el Modelo de Objeto de Documento (DOM) con JavaScript.
Un navegador que soporta una función de HTML5 añade propiedades o métodos únicos a los objetos DOM relevantes.
# Modernizr: La Herramienta Esencial 
Modernizr es una librería JavaScript de código abierto que automatiza la detección de soporte para muchas características de HTML5 y CSS3.
Uso: Se incluye en la cabecera de la página y se ejecuta automáticamente.

Resultado: Crea un objeto global llamado Modernizr que contiene propiedades booleanas (true/false) para cada característica (Ej. Modernizr.canvas).

Propósito: Permite a los desarrolladores usar un condicional (if/else) para utilizar la función nativa si está disponible, o recurrir a una solución de reserva (fallback/polyfill) si no lo está.
# Características Clave Mencionadas
Canvas: Permite dibujar gráficos con JavaScript.

Video: El elemento nativo <video>. La detección de formato (códecs) se hace con canPlayType(), que devuelve "probably", "maybe" o una cadena vacía.

Almacenamiento Local: Permite almacenar grandes cantidades de datos del lado del cliente (window.localStorage).

Web Workers: Permite ejecutar código JavaScript en segundo plano, sin bloquear la interfaz de usuario (window.Worker).

Geolocalización: API para obtener la ubicación del usuario (navigator.geolocation).

Formularios: Nuevos tipos de entrada (ej. type="date", type="color") y atributos como placeholder y autofocus.
