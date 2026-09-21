# Equipo 2 — Haskell
## Exposición: Introducción a lenguajes funcionales · Unidad 1

## Integrantes y roles

| Rol | Estudiante | Responsabilidad |
|:-:|:--|:--|
| 1 | BARBOZA CARBALLO, DIEGO ANTONIO | Contexto e historia |
| 2 | BOJORQUEZ VALDEZ, VICTOR MANUEL | Modelo de cómputo y sintaxis |
| 3 | CAMACHO OTAÑEZ, JUAN PABLO | Sistema de tipos / runtime |
| 4 | CAMARILLO MOLINA, CRISTIAN | Demo en vivo + caso real |

## Datos del lenguaje

- **Año / origen:** 1990 (comité Haskell)
- **Creador(es):** _(completar)_
- **Modelo de evaluación:** perezoso (*lazy*) por defecto
- **Sistema de tipos:** estático, inferencia Hindley-Milner, clases de tipos, `Maybe`/`Either`
- **REPL / herramienta:** `ghci` (GHC)
- **Caso real verificado (obligatorio en pantalla):** Standard Chartered — motor de valuación de derivados en Haskell. _(fuente IEEE abajo)_

## Guion (12–15 min)

1. **Contexto (2 min)** — por qué un comité crea un lenguaje "puro y perezoso".
2. **Modelo de cómputo (3 min)** — expresiones, pureza, evaluación perezosa (listas infinitas).
3. **Tipos / runtime (3 min)** — qué atrapa el compilador antes de correr; `Maybe`/`Either` frente a `null` y excepciones.
4. **Demo en vivo (4 min)** — `ghci` + "Hola Paradigma" (1..10) + 2.º ejemplo idiomático (`take 10 [1..]` o `foldr`).
5. **Caso real + cierre (2 min)** — Standard Chartered con referencia IEEE; conexión con OCaml, Elm y Gleam.

## Comandos exactos del demo

```bash
# Instalación
ghcup install ghc      # https://www.haskell.org/ghcup/

# Hola Paradigma (imprimir 1..10)
ghci
ghci> mapM_ print [1..10]

# Segundo ejemplo idiomático
ghci> take 10 [1..]              -- lista infinita, evaluación perezosa
```

Salida esperada:

```
1
2
3
4
5
6
7
8
9
10
[1,2,3,4,5,6,7,8,9,10]
```

## Grabación de respaldo (asciinema cloud)

- URL: _https://asciinema.org/a/fl0rxxHtJGfDaN7H_
- Cómo: `asciinema rec demo.cast` → `asciinema upload demo.cast`

## Diapositivas

- `slides.pdf` — 5–8 diapositivas, subir a esta carpeta **antes** de la sesión.

## Caso Real
El uso de Haskell en Standard Chartered dentro de su plataforma financiera Cortex es uno de los casos de éxito comercial más conocidos y emblemáticos de la programación funcional en la industria de la banca global.

Poseen un sistema Cortex, la cual es su plataforma central para la valoracion de derivados financieros, analisis cuantitativos y la gestion de riesgos en tiempo real. Poseen uno de los sistemas comerciales en Haskell mas grandes del mundo, con mas de 5 millones de lineas de codigo.

### ¿Por qué Standard Chartered eligió Haskell para Cortex?
- **Seguridad Teórica y Tipado Fuerte:** En el mercado de derivados financieros, un error numérico o de lógica en el código puede costar millones de dólares. El sistema de tipos de Haskell garantiza que gran parte de los errores se detecten durante la compilación y no en producción.
- **Modelado Matemático Directo:** La sintaxis de Haskell se parece mucho a las matemáticas financieras puras. Esto permite a los analistas cuantitativos (quants) y desarrolladores traducir fórmulas financieras complejas directamente a código ejecutable.
- **Mantenibilidad y Refactorización:** El sistema financiero requiere cambios constantes por regulaciones. Haskell permite refactorizar código crítico a gran escala con alta confianza de que no se romperán otras partes del sistema.

## Bibliografía (IEEE)

1. _(fuente 1)_
2. _(fuente 2)_
3. _W. T. H. Yuen, "Functional Programming in Financial Services: Industrial Haskell at Scale," IEEE Software, vol. 35, no. 6, pp. 62–68, Nov.-Dec. 2018._

---

Rúbrica, medio de presentación y reglas: [`../TEMAS-INTRO-LENGUAJES-FUNCIONALES-40.md`](../TEMAS-INTRO-LENGUAJES-FUNCIONALES-40.md)
