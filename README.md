# Pac-Man Game 👾

## Descripción

Implementación clásica del juego arcade **Pac-Man** en Python utilizando la librería `turtle` y `freegames`. Controla a Pac-Man para comer todos los puntos del laberinto mientras evitas a los fantasmas enemigos.

## Requisitos

- **Python** 3.7+
- **turtle** (incluido en la instalación estándar de Python)
- **freegames** (librería personalizada)

## Instalación

### 1. Clonar o descargar el repositorio
```bash
git clone https://github.com/tu-usuario/pacman-game.git
cd pacman-game
```

### 2. Instalar dependencias
```bash
pip install freegames
```

## Uso

Ejecuta el juego con:
```bash
python pacman.py
```

### Controles del Juego

| Tecla | Acción |
|-------|--------|
| `↑` | Mover arriba |
| `↓` | Mover abajo |
| `←` | Mover izquierda |
| `→` | Mover derecha |

## Características

✅ **Laberinto dinámico** - Tablero diseñado con sistema de tiles  
✅ **Sistema de puntuación** - Acumula puntos al comer  
✅ **4 Fantasmas inteligentes** - IA básica con movimiento aleatorio  
✅ **Colisión** - Detección de colisiones con fantasmas  
✅ **Gráficos retro** - Estilo arcade clásico con Turtle Graphics  

## Estructura del Código

```
pacman.py
├── Variables Globales
│   ├── state          # Estado del juego (puntuación)
│   ├── pacman         # Posición de Pac-Man
│   ├── ghosts         # Array de fantasmas [posición, dirección]
│   └── tiles          # Mapa del laberinto (20x20)
├── Funciones Gráficas
│   ├── square()       # Dibuja un cuadrado
│   ├── world()        # Renderiza el laberinto
│   └── offset()       # Calcula índice en el grid
├── Lógica del Juego
│   ├── valid()        # Valida posiciones
│   ├── move()         # Loop principal de movimiento
│   └── change()       # Cambia dirección de Pac-Man
└── Configuración
    └── setup(), listen(), done()
```

## Ejercicios de Mejora

El código incluye 5 ejercicios sugeridos:

1. **Cambiar el tablero** - Modifica el array `tiles` para crear nuevos laberintos
2. **Cambiar número de fantasmas** - Añade/elimina elementos en la lista `ghosts`
3. **Cambiar posición inicial de Pac-Man** - Edita el vector `pacman`
4. **Fantasmas más rápidos/lentos** - Ajusta el parámetro `ontimer(move, 100)`
5. **Fantasmas más inteligentes** - Reemplaza la lógica `choice(options)` con algoritmo de búsqueda

## Posibles Mejoras

- 🎯 Implementar algoritmo A* para IA de fantasmas
- 💾 Sistema de niveles
- 🎵 Efectos de sonido y música
- 👻 Fantasmas con comportamientos diferenciados
- 📊 Tabla de puntuaciones
- 🎨 Temas personalizables

## Ejemplo de Extensión: Fantasmas Más Inteligentes

```python
def smart_ghost(point, pacman):
    """IA mejorada: fantasma persigue a Pac-Man."""
    options = [
        vector(5, 0),
        vector(-5, 0),
        vector(0, 5),
        vector(0, -5),
    ]
    
    # Elige la dirección más cercana a Pac-Man
    best = min(options, key=lambda v: abs(point + v - pacman))
    return best
```

## Licencia

Este proyecto utiliza la librería `freegames` de [Giles Thomas](https://github.com/giles/freegames).

## Autor

Creado como práctica de programación con Turtle Graphics.

---

**¿Listo para jugar?** 🕹️ Ejecuta `python pacman.py` y ¡que disfrutes!
