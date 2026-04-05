#  Unidad 2: Componentes y Paquetes / Librerías

> Repositorio de aprendizaje sobre el uso, creación y gestión de componentes y paquetes en el desarrollo de software.

---

##  Tabla de Contenidos

- [2.1 Definición conceptual de componentes, paquetes y librerías](#21-definición-conceptual-de-componentes-paquetes--librerías)
- [2.2 Uso de librerías proporcionadas por el lenguaje](#22-uso-de-librerías-proporcionadas-por-el-lenguaje)
- [2.3 Creación de componentes (visuales y no visuales) definidos por el usuario](#23-creación-de-componentes-visuales-y-no-visuales-definidos-por-el-usuario)
- [2.4 Creación y uso de paquetes/librerías definidas por el usuario](#24-creación-y-uso-de-paqueteslibrerías-definidas-por-el-usuario)
- [Bibliografía](#bibliografía)

---

## 2.1 Definición conceptual de componentes, paquetes / librerías

### 🔷 ¿Qué es un Componente?

Un **componente** es una unidad de software autónoma, reutilizable y con una interfaz bien definida que encapsula un conjunto de funcionalidades específicas. Los componentes pueden ser combinados con otros para construir sistemas más complejos, siguiendo el principio de separación de responsabilidades.

Características principales de un componente:

- **Encapsulamiento**: oculta su implementación interna y expone solo lo necesario mediante una interfaz pública.
- **Reutilización**: puede ser usado en múltiples contextos o aplicaciones sin modificar su código fuente.
- **Independencia**: puede ser desarrollado, probado y desplegado de forma aislada.
- **Reemplazabilidad**: puede ser sustituido por otro componente que cumpla la misma interfaz.
- **Composición**: distintos componentes pueden combinarse para formar sistemas mayores.

Los componentes se clasifican en dos grandes grupos:

| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| **Visual (UI)** | Tienen representación gráfica e interacción con el usuario | Botones, formularios, tablas, menús |
| **No visual (lógica)** | No tienen interfaz gráfica; ejecutan lógica, acceso a datos, etc. | Servicios, validadores, conexiones a BD |

---

### 🔷 ¿Qué es una Librería?

Una **librería** (también llamada biblioteca) es una colección organizada de módulos, funciones, clases o rutinas predefinidas que un desarrollador puede importar y utilizar dentro de su propio programa. Su propósito es evitar la reescritura de código que resuelve problemas comunes y acelerar el desarrollo.

A diferencia de un *framework*, la librería **no dicta la arquitectura** del proyecto; el programador la invoca cuando la necesita, manteniendo el control del flujo de ejecución.

Tipos de librerías:

- **Estándar o nativas**: incluidas con el lenguaje de programación sin instalación adicional.
- **De terceros**: desarrolladas por la comunidad y distribuidas mediante gestores de paquetes.
- **Propias o internas**: creadas por el mismo equipo de desarrollo para cubrir necesidades específicas.

---

### 🔷 ¿Qué es un Paquete?

Un **paquete** es un mecanismo de agrupamiento y distribución de código. Desde el punto de vista estructural, un paquete es un directorio o módulo que contiene uno o más archivos de código relacionados entre sí, acompañados de metadatos (nombre, versión, dependencias, autor, licencia) que permiten su gestión automatizada.

Los paquetes son gestionados mediante herramientas especializadas llamadas **gestores de paquetes**:

| Lenguaje | Gestor de Paquetes |
|----------|--------------------|
| Python   | `pip`, `conda`     |
| JavaScript / Node.js | `npm`, `yarn`, `pnpm` |
| Java     | `Maven`, `Gradle`  |
| Dart / Flutter | `pub`        |
| Rust     | `cargo`            |
| C# / .NET | `NuGet`           |

---

### 🔷 Diferencias clave: Componente vs. Librería vs. Paquete

```
┌─────────────┬──────────────────────────────────┬──────────────────────────────────┐
│  Concepto   │           Enfoque                │            Propósito             │
├─────────────┼──────────────────────────────────┼──────────────────────────────────┤
│ Componente  │ Unidad funcional reutilizable    │ Encapsular comportamiento/UI     │
│ Librería    │ Colección de utilidades/clases   │ Evitar reescritura de código     │
│ Paquete     │ Unidad de distribución/módulo    │ Organizar y compartir código     │
└─────────────┴──────────────────────────────────┴──────────────────────────────────┘
```

---

###  Espacio para ejemplos de código — 2.1

```
[Agregar aquí ejemplos de código relacionados con la definición de componentes, 
librerías y paquetes en el lenguaje de programación elegido]
```

---

## 2.2 Uso de librerías proporcionadas por el lenguaje

### 🔷 Librerías estándar (Built-in Libraries)

La **biblioteca estándar** de un lenguaje de programación es el conjunto de módulos y paquetes incluidos de forma nativa con la instalación del lenguaje, sin necesidad de instalar dependencias externas. Representan soluciones probadas y optimizadas para tareas comunes del desarrollo.

El uso de librerías estándar ofrece múltiples ventajas:

-  No requieren instalación adicional.
-  Están mantenidas y actualizadas por los creadores del lenguaje.
-  Son multiplataforma y garantizan compatibilidad.
-  Tienen documentación oficial detallada.
-  Minimizan dependencias externas en el proyecto.

---

### 🔷 Proceso general para usar una librería estándar

El proceso típico de importación y uso varía según el lenguaje, pero sigue la misma lógica:

**1. Importar el módulo o librería**
```
import <nombre_libreria>
// o
from <nombre_libreria> import <elemento>
```

**2. Utilizar los elementos del módulo**
```
resultado = nombre_libreria.funcion(argumentos)
```

**3. Gestionar posibles errores**
```
try:
    resultado = nombre_libreria.funcion(argumentos)
except ExcepcionEspecifica as e:
    manejar_error(e)
```

---

### 🔷 Categorías comunes de librerías estándar

La mayoría de los lenguajes modernos incluyen librerías para las siguientes áreas:

| Área | Descripción |
|------|-------------|
| **Matemáticas** | Operaciones aritméticas avanzadas, trigonometría, estadística |
| **Manejo de fechas y tiempo** | Formateo, diferencias, zonas horarias |
| **Entrada / Salida (I/O)** | Lectura/escritura de archivos, consola, redes |
| **Estructuras de datos** | Pilas, colas, conjuntos, diccionarios avanzados |
| **Expresiones regulares** | Búsqueda y manipulación de cadenas de texto |
| **Concurrencia / Hilos** | Manejo de procesos paralelos y asincrónicos |
| **Red y HTTP** | Comunicación por sockets, peticiones HTTP |
| **Compresión** | Manejo de archivos ZIP, GZIP, etc. |
| **Serialización** | JSON, XML, CSV, pickle |

---

### 🔷 Buenas prácticas al usar librerías estándar

1. **Preferir la librería estándar** antes de buscar alternativas de terceros.
2. **Consultar la documentación oficial** antes de implementar.
3. **Importar solo lo necesario** para mantener el código limpio.
4. **No reinventar la rueda**: si existe una función estándar, usarla.
5. **Manejar excepciones** específicas de cada módulo.

---

###  Espacio para ejemplos de código — 2.2

```
[Agregar aquí ejemplos de uso de librerías estándar del lenguaje: 
matemáticas, fechas, archivos, colecciones, etc.]
```

---

## 2.3 Creación de componentes (visuales y no visuales) definidos por el usuario

### 🔷 ¿Por qué crear componentes propios?

A medida que las aplicaciones crecen en complejidad, surge la necesidad de **abstraer lógicas repetidas** o elementos de interfaz comunes en unidades independientes y reutilizables. La creación de componentes personalizados permite:

- Reducir la duplicación de código (principio **DRY**: *Don't Repeat Yourself*).
- Mejorar la mantenibilidad y legibilidad del proyecto.
- Facilitar las pruebas unitarias al tener lógica aislada.
- Permitir el trabajo en equipo sobre módulos independientes.

---

### 🔷 Componentes Visuales (UI Components)

Los **componentes visuales** son elementos que tienen representación gráfica dentro de una aplicación. Su propósito es mostrar información al usuario o capturar interacciones.

**Características:**
- Poseen propiedades o parámetros que controlan su apariencia y comportamiento.
- Pueden emitir eventos al resto de la aplicación (clic, cambio de valor, etc.).
- Son completamente reutilizables en distintas partes de la interfaz.
- Deben ser responsivos y accesibles.

**Ejemplos de componentes visuales personalizados:**

| Componente | Descripción |
|------------|-------------|
| `<TarjetaProducto>` | Muestra imagen, nombre y precio de un producto |
| `<ModalConfirmacion>` | Ventana emergente con botones de aceptar/cancelar |
| `<BarraBusqueda>` | Campo de texto con ícono y sugerencias automáticas |
| `<TablaOrdenable>` | Tabla con ordenamiento dinámico por columnas |
| `<GraficoLineas>` | Visualización de datos estadísticos |

**Principios de diseño de componentes visuales:**

1. **Responsabilidad única**: cada componente hace una sola cosa.
2. **Configurabilidad mediante props/parámetros**.
3. **Independencia de estilos globales** (CSS encapsulado o scoped).
4. **Accesibilidad** (ARIA roles, contraste, navegación por teclado).
5. **Estado predecible**: el mismo input produce el mismo output.

---

### 🔷 Componentes No Visuales (Lógicos / de Servicio)

Los **componentes no visuales** encapsulan lógica de negocio, acceso a datos, validaciones u otras operaciones sin producir ninguna salida gráfica. Son el núcleo funcional de una aplicación.

**Ejemplos de componentes no visuales:**

| Componente | Descripción |
|------------|-------------|
| `ValidadorFormulario` | Verifica reglas de negocio en campos de entrada |
| `ServicioAutenticacion` | Maneja login, logout y gestión de sesiones |
| `ConectorBaseDatos` | Abstrae operaciones CRUD sobre la BD |
| `GestorNotificaciones` | Envía alertas, correos o mensajes push |
| `CalculadoraImpuestos` | Aplica reglas fiscales sobre montos |

**Características de los componentes no visuales:**

- No dependen de ningún framework de UI.
- Son altamente testeables (pruebas unitarias puras).
- Siguen principios SOLID, especialmente **Inversión de Dependencias**.
- Pueden ser compartidos entre proyectos sin adaptaciones.

---

### 🔷 Ciclo de vida de un componente

La mayoría de los frameworks modernos definen fases en la vida de un componente:

```
┌─────────────────────────────────────────────────────────┐
│                  CICLO DE VIDA                          │
│                                                         │
│  Creación → Montaje → Actualización → Destrucción       │
│                                                         │
│  • Creación:      Se instancia el componente            │
│  • Montaje:       Se inserta en el DOM / contexto       │
│  • Actualización: Reacciona a cambios de estado/props   │
│  • Destrucción:   Se limpia y elimina del contexto      │
└─────────────────────────────────────────────────────────┘
```

---

###  Espacio para ejemplos de código — 2.3 (Componentes Visuales)

```
[Agregar aquí ejemplos de creación de componentes visuales personalizados:
botones, tarjetas, formularios, modales, etc.]
```

---

###  Espacio para ejemplos de código — 2.3 (Componentes No Visuales)

```
[Agregar aquí ejemplos de creación de componentes no visuales:
servicios, validadores, utilidades, etc.]
```

---

## 2.4 Creación y uso de paquetes/librerías definidas por el usuario

### 🔷 Motivación para crear paquetes propios

En proyectos medianos y grandes, es frecuente que ciertas funcionalidades se repitan en múltiples módulos o incluso en distintos proyectos. Empaquetar estas funcionalidades de manera estructurada permite:

- **Versionamiento**: controlar cambios y garantizar compatibilidad.
- **Distribución**: compartir el código entre proyectos o con la comunidad.
- **Encapsulamiento**: definir claramente qué es público y qué es interno.
- **Mantenimiento centralizado**: corregir un bug en un solo lugar afecta a todos los consumidores.
- **Integración con gestores**: instalar, actualizar o eliminar con un solo comando.

---

### 🔷 Estructura típica de un paquete

Aunque varía según el lenguaje y el ecosistema, la mayoría de los paquetes siguen una estructura similar:

```
mi_paquete/
│
├── src/                        # Código fuente principal
│   ├── __init__.py / index.js  # Punto de entrada del paquete
│   ├── modulo_a.py             # Módulo A
│   └── modulo_b.py             # Módulo B
│
├── tests/                      # Pruebas unitarias e integración
│   ├── test_modulo_a.py
│   └── test_modulo_b.py
│
├── docs/                       # Documentación
│
├── examples/                   # Ejemplos de uso
│
├── README.md                   # Descripción del paquete
├── LICENSE                     # Licencia de uso
└── setup.py / package.json     # Metadatos y configuración del paquete
```

---

### 🔷 Elementos de un archivo de configuración de paquete

El archivo de metadatos (como `package.json`, `setup.py` o `pubspec.yaml`) define:

| Campo | Descripción |
|-------|-------------|
| `name` | Nombre único del paquete |
| `version` | Versión siguiendo Semántica de Versiones (SemVer) |
| `description` | Descripción breve del propósito |
| `author` | Autor o autores |
| `license` | Tipo de licencia (MIT, Apache, GPL, etc.) |
| `dependencies` | Paquetes de los que depende |
| `entry point` | Archivo principal que se expone al importar |
| `keywords` | Palabras clave para búsqueda en repositorios |

---

### 🔷 Versionamiento Semántico (SemVer)

Los paquetes siguen la convención `MAJOR.MINOR.PATCH`:

```
v  2  .  1  .  4
   │     │     │
   │     │     └── PATCH: Corrección de errores (retrocompatible)
   │     └──────── MINOR: Nueva funcionalidad (retrocompatible)
   └────────────── MAJOR: Cambio que rompe compatibilidad
```

---

### 🔷 Fases para crear y publicar un paquete

**Fase 1 — Diseño**
- Definir el alcance y responsabilidades del paquete.
- Identificar la API pública (qué funciones/clases exporta).
- Elegir la licencia adecuada.

**Fase 2 — Implementación**
- Escribir el código fuente organizado en módulos.
- Definir el punto de entrada del paquete.
- Documentar cada función/clase pública (docstrings / JSDoc).

**Fase 3 — Pruebas**
- Escribir pruebas unitarias para cada componente.
- Verificar casos borde y manejo de errores.
- Medir la cobertura de pruebas.

**Fase 4 — Empaquetado**
- Configurar el archivo de metadatos (`package.json`, `setup.py`, etc.).
- Construir el paquete distribuible.

**Fase 5 — Distribución**
- Publicar en el repositorio oficial (npm, PyPI, pub.dev, etc.) o en un registro privado.
- Etiquetar la versión en el repositorio Git.

**Fase 6 — Mantenimiento**
- Atender reportes de bugs.
- Publicar nuevas versiones siguiendo SemVer.
- Mantener el CHANGELOG actualizado.

---

### 🔷 Uso de un paquete propio en un proyecto

Una vez publicado (o referenciado localmente), el paquete se usa siguiendo el mismo proceso que cualquier librería de terceros:

```
# Instalación (ejemplo genérico)
[gestor-de-paquetes] install nombre-del-paquete

# Importación en código
import nombre_del_paquete
from nombre_del_paquete import FuncionEspecifica
```

---

### 🔷 Repositorios públicos de paquetes

| Repositorio | Ecosistema | URL |
|-------------|-----------|-----|
| npm Registry | JavaScript / Node.js | https://www.npmjs.com |
| PyPI | Python | https://pypi.org |
| Maven Central | Java | https://central.sonatype.com |
| NuGet Gallery | .NET / C# | https://www.nuget.org |
| pub.dev | Dart / Flutter | https://pub.dev |
| crates.io | Rust | https://crates.io |

---

###  Ejemplos de código — 2.4 


      import matplotlib
        matplotlib.use("Agg")
        import matplotlib.pyplot as plt
        import flet as ft
        import flet_charts as fch



    def generar_grafica_barras():
    productos = ["A", "B", "C", "D"]
    ventas = [15, 30, 45, 10]
    fig, ax = plt.subplots(figsize=(4, 3))
    ax.bar(productos, ventas, color="skyblue")
    ax.set_title("Ventas por Producto", fontsize=10, weight="bold")
    plt.tight_layout()
    return fig


    def generar_grafica_lineas():
    meses = ["Ene", "Feb", "Mar", "Abr", "May"]
    rendimiento = [10, 25, 18, 40, 35]
    fig, ax = plt.subplots(figsize=(4, 3))
    ax.plot(meses, rendimiento, color="orange", marker="o", linewidth=2)
    ax.set_title("Tendencia de Rendimiento", fontsize=10, weight="bold")
    ax.grid(True, linestyle="--", alpha=0.6)
    plt.tight_layout()
    return fig


    def generar_grafica_pastel():
    categorias = ["Electrónica", "Ropa", "Alimentos", "Hogar", "Otros"]
    valores = [35, 25, 20, 12, 8]
    colores = ["#4e79a7", "#f28e2b", "#e15759", "#76b7b2", "#59a14f"]
    fig, ax = plt.subplots(figsize=(4, 3))
    _, texts, autotexts = ax.pie(
        valores,
        labels=categorias,
        autopct="%1.1f%%",
        colors=colores,
        startangle=140,
        wedgeprops=dict(edgecolor="white", linewidth=1.5),
    )
    for t in texts:
        t.set_fontsize(7)
    for at in autotexts:
        at.set_fontsize(7)
        at.set_color("white")
        at.set_weight("bold")
    ax.set_title("Distribución por Categoría", fontsize=10, weight="bold")
    plt.tight_layout()
    return fig



        CHART_W = 420
        CHART_H = 320

    def main(page: ft.Page):
    page.title = "Dashboard TAP"
    page.theme_mode = ft.ThemeMode.LIGHT
    page.scroll = ft.ScrollMode.AUTO
    page.padding = 16

    header = ft.Text(
        "Dashboard de Visualización — Constructor Interactivo",
        size=20,
        weight=ft.FontWeight.BOLD,
    )

    
    c1 = ft.Container(
        content=fch.MatplotlibChart(figure=fig1, expand=True),
        border=ft.border.all(1, ft.Colors.BLACK12),
        border_radius=10,
        padding=5,
        width=CHART_W,
        height=CHART_H,
        clip_behavior=ft.ClipBehavior.HARD_EDGE,
    )
    plt.close(fig1)

    fig2 = generar_grafica_lineas()
    c2 = ft.Container(
        content=fch.MatplotlibChart(figure=fig2, expand=True),
        border=ft.border.all(1, ft.Colors.BLACK12),
        border_radius=10,
        padding=5,
        width=CHART_W,
        height=CHART_H,
        clip_behavior=ft.ClipBehavior.HARD_EDGE,
    )
    plt.close(fig2)

    fig3 = generar_grafica_pastel()
    c3 = ft.Container(
        content=fch.MatplotlibChart(figure=fig3, expand=True),
        border=ft.border.all(1, ft.Colors.BLACK12),
        border_radius=10,
        padding=5,
        width=CHART_W,
        height=CHART_H,
        clip_behavior=ft.ClipBehavior.HARD_EDGE,
    )
    plt.close(fig3)

  

    selector_tipo = ft.Dropdown(
        label="Tipo de gráfica",
        width=170,
        text_size=12,
        options=[
            ft.dropdown.Option("barras", "📊 Barras"),
            ft.dropdown.Option("lineas", "📈 Líneas"),
            ft.dropdown.Option("pastel", "🥧 Pastel"),
            ft.dropdown.Option("area",   "📉 Área"),
        ],
        value="barras",
    )

    campo_titulo = ft.TextField(
        label="Título",
        hint_text="Ej: Mi Gráfica",
        text_size=12,
        height=52,
    )
    campo_etiquetas = ft.TextField(
        label="Etiquetas (separadas por coma)",
        hint_text="Ej: Lun,Mar,Mié",
        text_size=12,
        height=52,
    )
    campo_valores = ft.TextField(
        label="Valores (separados por coma)",
        hint_text="Ej: 10,25,40",
        text_size=12,
        height=52,
    )
    mensaje_error = ft.Text("", color=ft.Colors.RED_400, size=11)

   
    contenedor_chart = ft.Container(
        content=ft.Text(
            "Tu gráfica aparecerá aquí",
            color=ft.Colors.GREY_400,
            size=11,
            italic=True,
        ),
        alignment=ft.Alignment(0, 0),
        width=400,
        height=230,
        border_radius=8,
        bgcolor="#f0f0f0",
        clip_behavior=ft.ClipBehavior.HARD_EDGE,
    )

    def construir_grafica(e):
        mensaje_error.value = ""

        raw_labels = campo_etiquetas.value.strip()
        raw_values = campo_valores.value.strip()
        titulo = campo_titulo.value.strip() or "Mi Gráfica"
        tipo   = selector_tipo.value or "barras"

        if not raw_labels or not raw_values:
            mensaje_error.value = "⚠️ Completa etiquetas y valores."
            page.update()
            return

        try:
            etiquetas = [x.strip() for x in raw_labels.split(",") if x.strip()]
            valores   = [float(x.strip()) for x in raw_values.split(",") if x.strip()]
        except ValueError:
            mensaje_error.value = "⚠️ Los valores deben ser números válidos."
            page.update()
            return

        if len(etiquetas) != len(valores):
            mensaje_error.value = (
                f"⚠️ {len(etiquetas)} etiquetas vs {len(valores)} valores — deben coincidir."
            )
            page.update()
            return

        paleta  = ["#4e79a7", "#f28e2b", "#e15759", "#76b7b2",
                   "#59a14f", "#edc948", "#b07aa1", "#ff9da7"]
        colores = (paleta * ((len(etiquetas) // len(paleta)) + 1))[:len(etiquetas)]

        fig, ax = plt.subplots(figsize=(4, 2.8))

        if tipo == "barras":
            ax.bar(etiquetas, valores, color=colores, edgecolor="white")
            ax.set_ylabel("Valor", fontsize=8)
            ax.tick_params(axis="x", labelsize=7)
            ax.tick_params(axis="y", labelsize=7)

        elif tipo == "lineas":
            ax.plot(etiquetas, valores, color="#4e79a7",
                    marker="o", linewidth=2, markersize=5)
            ax.fill_between(range(len(etiquetas)), valores,
                            alpha=0.1, color="#4e79a7")
            ax.set_xticks(range(len(etiquetas)))
            ax.set_xticklabels(etiquetas, fontsize=7)
            ax.tick_params(axis="y", labelsize=7)
            ax.grid(True, linestyle="--", alpha=0.5)

        elif tipo == "pastel":
            _, texts, autotexts = ax.pie(
                valores, labels=etiquetas, autopct="%1.0f%%",
                colors=colores, startangle=90,
                wedgeprops=dict(edgecolor="white", linewidth=1.2),
            )
            for t in texts:
                t.set_fontsize(7)
            for at in autotexts:
                at.set_fontsize(7)
                at.set_color("white")

        elif tipo == "area":
            idx = range(len(valores))
            ax.fill_between(idx, valores, alpha=0.4, color="#59a14f")
            ax.plot(idx, valores, color="#59a14f",
                    linewidth=2, marker="o", markersize=4)
            ax.set_xticks(list(idx))
            ax.set_xticklabels(etiquetas, fontsize=7)
            ax.tick_params(axis="y", labelsize=7)
            ax.grid(True, linestyle="--", alpha=0.4)

        ax.set_title(titulo, fontsize=9, weight="bold")
        plt.tight_layout()

        

    boton_generar = ft.ElevatedButton(
        content=ft.Row(
            [
                ft.Icon(ft.Icons.BAR_CHART, color="white", size=16),
                ft.Text("Generar", color="white", size=13,
                        weight=ft.FontWeight.W_500),
            ],
            spacing=6,
            tight=True,
        ),
        on_click=construir_grafica,
        style=ft.ButtonStyle(
            bgcolor={"": "#4e79a7"},
            shape=ft.RoundedRectangleBorder(radius=8),
            padding=ft.padding.symmetric(horizontal=16, vertical=10),
        ),
    )

    panel_controles = ft.Column(
        [
            ft.Text("🛠️ Constructor de Gráficas",
                    size=12, weight=ft.FontWeight.BOLD, color="#333"),
            ft.Row(
                [selector_tipo, boton_generar],
                spacing=10,
                alignment=ft.MainAxisAlignment.START,
            ),
            campo_titulo,
            campo_etiquetas,
            campo_valores,
            mensaje_error,
        ],
        spacing=8,
    )

    c4 = ft.Container(
        content=ft.Column(
            [
                ft.Container(
                    panel_controles,
                    padding=ft.padding.only(left=8, right=8, top=8, bottom=4),
                ),
                ft.Divider(height=1, color=ft.Colors.BLACK12),
                contenedor_chart,
            ],
            spacing=4,
            horizontal_alignment=ft.CrossAxisAlignment.CENTER,
        ),
        border=ft.border.all(1, ft.Colors.BLACK12),
        border_radius=10,
        padding=6,
        bgcolor="#fafafa",
        width=CHART_W,
    )

    fila1 = ft.Row([c1, c2], spacing=16, wrap=True)
    fila2 = ft.Row([c3, c4], spacing=16, wrap=True)

    page.add(
        header,
        ft.Divider(),
        fila1,
        fila2,
    )


    if __name__ == "__main__":
        ft.run(main)



###  Ejemplos de código

      import flet as ft
        from dataclasses import dataclass, field


    @dataclass
    class DatosUsuario:
        """
        Dataclass que almacena únicamente los DATOS del perfil.
    
        @dataclass genera automáticamente:
      - __init__(self, nombre, rol, color_borde)
      - __repr__(self)
      - __eq__(self)
    
    No contiene lógica de UI ni métodos complejos,
    solo estructura de datos pura y tipada.
    """
    nombre: str
    rol: str
    color_borde: str = field(default_factory=lambda: ft.Colors.BLUE)
    # 'field(default_factory=...)' se usa cuando el valor por defecto
    # es mutable o necesita evaluarse en tiempo de ejecución.

    @property
    def inicial(self) -> str:
        """Propiedad calculada a partir de los datos almacenados."""
        return self.nombre[0].upper()

    def __post_init__(self):
        """
        Método especial de dataclasses que se ejecuta DESPUÉS
        de que __init__ asigna todos los campos.
        Útil para validaciones o transformaciones de datos.
        """
        if not self.nombre.strip():
            raise ValueError("El nombre no puede estar vacío")
        if not self.rol.strip():
            raise ValueError("El rol no puede estar vacío")


        class ControladorTarjeta:
        """
    Clase separada que maneja la lógica del componente.
    
    Recibe un DatosUsuario y construye el widget de Flet.
    Esta separación (datos vs lógica) es el patrón que
    permite usar dataclasses con Flet correctamente.
    """

    def __init__(self, datos: DatosUsuario):
        self.datos = datos  # Referencia a la dataclass de datos

    def al_hacer_click(self, e: ft.ControlEvent):
        """Manejador de evento que usa self.datos para acceder a la info."""
        print(f"✅ [Dataclasses] Perfil de: {self.datos.nombre} | Rol: {self.datos.rol}")
        e.page.snack_bar = ft.SnackBar(
            content=ft.Text(f"Perfil de {self.datos.nombre} - {self.datos.rol}"),
            bgcolor=self.datos.color_borde,
        )
        e.page.snack_bar.open = True
        e.page.update()

    def construir(self) -> ft.Container:
        """
        Método fábrica que construye y retorna el widget de Flet.
        
        La dataclass (DatosUsuario) provee los datos,
        este método los transforma en UI.
        """
        d = self.datos  # Alias corto para legibilidad

        return ft.Container(
            content=ft.Column(
                controls=[
                    ft.CircleAvatar(
                        content=ft.Text(d.inicial, size=20, color=ft.Colors.WHITE),
                        bgcolor=d.color_borde,
                        radius=30,
                    ),
                    ft.Text(d.nombre, weight=ft.FontWeight.BOLD, size=18),
                    ft.Text(d.rol, italic=True, size=13, color=ft.Colors.GREY_600),
                    ft.ElevatedButton(
                        "Ver Perfil",
                        on_click=self.al_hacer_click,
                        style=ft.ButtonStyle(
                            bgcolor=d.color_borde,
                            color=ft.Colors.WHITE,
                        )
                    ),
                ],
                tight=True,
                horizontal_alignment=ft.CrossAxisAlignment.CENTER,
                spacing=8,
            ),
            border=ft.border.all(2, d.color_borde),
            padding=16,
            border_radius=12,
            width=200,
            bgcolor=ft.Colors.WHITE,
            shadow=ft.BoxShadow(
                spread_radius=1,
                blur_radius=8,
                color=ft.Colors.with_opacity(0.15, ft.Colors.BLACK),
            ),
        )


def main(page: ft.Page):
    page.title = "Versión: Dataclasses"
    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER
    page.bgcolor = ft.Colors.GREY_100
    page.padding = 30

    # 1. Creamos las dataclasses con los DATOS
    datos1 = DatosUsuario("Ana García", "Dev Senior", ft.Colors.GREEN)
    datos2 = DatosUsuario("Carlos Ruiz", "Arquitecto SW")
    

    # 2. Creamos los controladores pasándoles los datos
    ctrl1 = ControladorTarjeta(datos1)
    ctrl2 = ControladorTarjeta(datos2)
    

    # 3. Construimos los widgets de UI a partir de los controladores
    tarjeta1 = ctrl1.construir()
    tarjeta2 = ctrl2.construir()
   

    page.add(
        ft.Text(" Lista de Usuarios", size=28, weight="bold"),
        ft.Text("Versión: Dataclasses de Python", size=14, color=ft.Colors.GREY_600),
        ft.Divider(height=20),
        ft.Row(
            [tarjeta1, tarjeta2],
            alignment=ft.MainAxisAlignment.CENTER,
            spacing=20,
            wrap=True,
        )
    )


ft.app(target=main)


## Bibliografía

Booch, G., Maksimchuk, R. A., Engle, M. W., Young, B. J., Conallen, J., & Houston, K. A. (2007). *Object-oriented analysis and design with applications* (3.ª ed.). Addison-Wesley.

Brown, E. (2019). *Learning JavaScript: Add sparkle and life to your web pages* (3.ª ed.). O'Reilly Media.

Chacon, S., & Straub, B. (2014). *Pro Git* (2.ª ed.). Apress. https://git-scm.com/book/en/v2

Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). *Design patterns: Elements of reusable object-oriented software*. Addison-Wesley.

Larman, C. (2004). *Applying UML and patterns: An introduction to object-oriented analysis and design and iterative development* (3.ª ed.). Prentice Hall.

Lutz, M. (2013). *Learning Python* (5.ª ed.). O'Reilly Media.

Martin, R. C. (2003). *Agile software development, principles, patterns, and practices*. Prentice Hall.

Martin, R. C. (2008). *Clean code: A handbook of agile software craftsmanship*. Prentice Hall.

npm, Inc. (2023). *npm documentation*. https://docs.npmjs.com

Python Software Foundation. (2024). *Python 3 documentation: The Python standard library*. https://docs.python.org/3/library/

Smedley, T. J. (2018). *Exploring ES6: Upgrade to the next version of JavaScript*. Leanpub.

Sommerville, I. (2016). *Software engineering* (10.ª ed.). Pearson Education.

Szyperski, C. (2002). *Component software: Beyond object-oriented programming* (2.ª ed.). Addison-Wesley.

Thomas, D., & Hunt, A. (2019). *The pragmatic programmer: Your journey to mastery* (20th anniversary ed.). Addison-Wesley.

