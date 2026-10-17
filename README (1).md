# 🌾 Complejo Arrocero Sabana Dorada · Recorrido virtual 3D

> *Del campo llanero a su mesa*

Recorrido virtual 3D en primera persona de una planta arrocera colombiana completa, ambientada en los Llanos Orientales. Corre en el navegador, sin instalación. Se hizo para enseñar **cómo funciona la agroindustria del arroz**: el proceso se ve ocurrir. Los camiones llegan, se pesan, descargan y regresan al campo, las cosechadoras dejan rastrojo por donde pasan y los bultos avanzan por las bandas.

**Cadena que se recorre:** cultivo → cosecha → recepción y báscula → secado → silos → molino de trilla → empaque → bodega → despacho → punto de venta.

<!-- Reemplaza con una captura o GIF propio -->
<!-- ![Vista aérea del complejo](docs/captura.jpg) -->

---

## 🚀 Cómo usarlo

### Opción 1: abrir directamente
Descarga `planta_arrocera_3d.html` y ábrelo con doble clic en **Chrome** o **Edge** (versión reciente).

### Opción 2: servidor local (recomendado)
```bash
# Con Python
python -m http.server 8000
# o con Node
npx serve .
```
Luego abre `http://localhost:8000/planta_arrocera_3d.html`.

### Opción 3: GitHub Pages
1. Sube el archivo al repositorio (puedes renombrarlo a `index.html`).
2. En **Settings → Pages**, elige la rama `main` y la carpeta raíz.
3. Comparte el enlace `https://TU_USUARIO.github.io/TU_REPOSITORIO/`.

> **Requiere internet la primera vez** para cargar Three.js y la fuente Inter desde CDN. Las texturas y modelos reales son opcionales. Si no cargan, el mundo se arma completo con texturas generadas por código.

---

## 🎮 Controles

| Tecla | Acción |
|---|---|
| `W A S D` / flechas | Moverse |
| Mouse | Mirar (clic en la escena para capturar el puntero) |
| `Shift` | Correr (caminando) o volar rápido (dron) |
| `Espacio` | Saltar |
| `Q` / `E` | Bajar / subir (modo dron) |
| `1` | Modo **caminar** |
| `2` | Modo **dron** |
| `3` | **Recorrido guiado** |
| `M` | Lista "Ir a zona" |
| `N` | Activar / silenciar sonido |
| `H` | Ocultar / mostrar ayuda |
| `F` | Contador de FPS, llamadas de dibujo y triángulos |

**Minimapa:** haz clic en cualquier punto para ir allá.
**Celular o tableta:** la mitad izquierda de la pantalla es una palanca virtual para moverse. Arrastrar en la mitad derecha mueve la mirada.

---

## 🧭 Modos de visita

- **Caminar:** a la altura de los ojos (1,68 m), entre trabajadores, camiones y máquinas. Se choca con muros, máquinas, cercas, árboles y vehículos, y se entra a los edificios por sus puertas.
- **Dron:** vuelo libre con inercia entre 1,8 m y 900 m de altura.
- **Recorrido guiado:** la cámara viaja sola por 15 paradas explicadas. Entra al molino por el portón y termina en modo dron.

---

## 🏭 Qué contiene

### Zonas de la planta
| Zona | Contenido |
|---|---|
| Portería y báscula | Dos básculas camioneras de 80 t, semáforos, talanqueras y patio de espera |
| Recepción y muestreo | Calador neumático, caseta de análisis y tolvas de recibo bajo cobertizo |
| Prelimpieza y secado | Tres secadoras de torre y horno de cascarilla con chimenea |
| Almacenamiento en silos | 10 silos metálicos con aireación y torre de elevadores de 44 m |
| Molino de trilla | Interior recorrible: descascaradoras, mesas separadoras, pulidoras, trieur, seleccionadoras ópticas, plansifter y cuarto de control |
| Cascarilla y caldera | Caldera, chimenea de 34 m y patio de cascarilla con cargador frontal |
| Empaque | Ensacadoras de 50 kg, empacadoras de libra, robot paletizador y envolvedora |
| Bodega de producto terminado | Estantería selectiva, arrume en piso, montacargas y 6 muelles de despacho |
| Bodega de subproductos | Salvado, granza y arrocillo |
| Administración y laboratorio | Oficinas, laboratorio, casino, vestieres, cancha, tanque elevado y subestación |
| Taller y combustible | Taller de mantenimiento y surtidor de ACPM |
| Punto de venta | Local comercial sobre la vía nacional, con valla publicitaria |
| PTAR | Planta de tratamiento de aguas residuales |
| Patio de maquinaria agrícola | Tractores, cosechadora y oficina de campo |
| Estación de bombeo | Captación del río para el riego |
| Cultivo de arroz | Unas 140 hectáreas de lotes en cuatro etapas: plántula, macollamiento, listo para cosecha y barbecho |

### Lo que se ve en movimiento
- **7 volquetas** en el ciclo completo: campo → báscula de entrada → calador → descargue con volco basculante → glorieta → báscula de salida → campo. Hacen cola real.
- **4 furgones** que llegan por la vía nacional, retroceden a su muelle, abren puertas, cargan y salen.
- **2 cosechadoras** que cortan el arroz dejando rastrojo, cada una acompañada por un tractor con tolva.
- **5 montacargas**, un cargador frontal, un dron fumigador y tránsito en la vía nacional.
- **Hasta 260 personas** animadas en sus puestos: operarios, coteros, supervisores, visitantes, sembradores, fumigadores y clientes.
- Robot paletizador, bandas con bultos, máquinas vibrando, banderas, humo, vapor, polvo y paja.
- Ganado cebú y, si cargan los modelos, garzas, loros y caballos.
- Sonido ambiente generado con Web Audio: viento, zumbido de planta, motores y pito de reversa.

---

## ⚙️ Calidad gráfica

Se elige en la pantalla de inicio y se puede cambiar durante el recorrido con el botón **Calidad**.

| Nivel | Pixel ratio | Sombras | Radio de sombra | Pasto | Árboles |
|---|---|---|---|---|---|
| Alta | hasta 2 | 4096 | 150 m | 3 celdas · 0,60 m | 100 % |
| Media *(escritorio)* | hasta 1,25 | 2048 | 115 m | 2 celdas · 0,72 m | 80 % |
| Baja *(móvil)* | hasta 0,9 | 1024 | 80 m | 1 celda · 0,95 m | 45 % |

Si el recorrido va lento, baja la calidad o usa la tecla `F` para ver el rendimiento.

---

## 🛠️ Detalles técnicos

- **Un solo archivo HTML**, sin compilación ni dependencias locales. Todo el CSS y el JavaScript están dentro.
- **[Three.js](https://threejs.org/) r169** cargado desde jsDelivr mediante *import map*. Usa los addons `GLTFLoader`, `RGBELoader`, `Sky` y `BufferGeometryUtils`.
- **Mundo procedural:** edificios, máquinas, vehículos, personas, árboles y terreno se construyen por código a partir de primitivas.
- **Azar repetible** con semilla fija (`20261006`): el mundo sale idéntico cada vez.
- **Optimización:**
  - Geometría estática fusionada por material y por celda de 380 m.
  - `InstancedMesh` para árboles, pasto, pallets, ganado y personas.
  - Colisiones 2D en rejilla y una sola luz con sombras que sigue al espectador.
- **Personas** sin esqueleto: piezas rígidas instanciadas con cinemática directa calculada en cada cuadro.
- **Vehículos** con rutas Catmull-Rom, aceleración y frenado suaves, detección del vehículo de adelante y remolques articulados.

### Estructura del código (orden dentro del archivo)
1. HTML, CSS e interfaz
2. Configuración, calidades, renderer, cámara, matemáticas y ruido
3. Carga de recursos, texturas de respaldo y materiales
4. Lote de geometría estática, primitivas, letreros y colisiones
5. Luces, cielo, HDRI y terreno
6. Piezas reutilizables de edificio y de planta
7. Distribución de la planta e interiores
8. Oclusión ambiental falsa
9. Cultivos, pasto y arroz instanciados
10. Árboles, palmas y ganado
11. Personas
12. Vehículos, rutas, partículas, bandas y talanqueras
13. Rutas de vehículos, vehículos estacionados y personal
14. Aves, jugador, recorrido guiado, minimapa, sonido y bucle principal

---

## ⚠️ Limitaciones conocidas

- Pensado para Chrome y Edge de escritorio. En Firefox y Safari puede comportarse distinto.
- La primera carga tarda unos segundos mientras se construye el mundo y se compilan los shaders.
- Los modelos animados de aves y caballos dependen de servidores externos. Si no responden, simplemente no aparecen.
- En celulares de gama baja conviene usar la calidad **baja**.

¿Encontraste un error? Abre un *issue* con el navegador, el sistema operativo y el mensaje de la consola (`F12`).

---

## 🙏 Créditos

- **Motor 3D:** [Three.js](https://github.com/mrdoob/three.js) (licencia MIT).
- **Texturas PBR y cielo HDRI:** [Poly Haven](https://polyhaven.com/) (CC0). Se descargan en tiempo de ejecución.
- **Textura de pasto, mapa de normales de agua y modelos de garza, loro y caballo:** ejemplos oficiales de Three.js.
- **Fuente:** [Inter](https://fonts.google.com/specimen/Inter) (SIL Open Font License).

La empresa *Arrocera Sabana Dorada* es **ficticia** y se creó con fines educativos.

---

## 👤 Autor

**Luis Fernando Delgado Muñoz**
Universidad de San Buenaventura Cali
📧 lfdelgadom@usbcali.edu.co

---

## 📄 Licencia

<!-- Elige la licencia que prefieras; MIT es una opción común para material educativo -->
Este proyecto se distribuye bajo la licencia **MIT**. Consulta el archivo [`LICENSE`](LICENSE).
