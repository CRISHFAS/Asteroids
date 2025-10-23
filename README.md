# Asteroids

Una versión mejorada del clásico juego Asteroids utilizando física realista con **p2.js**. Desarrollado con JavaScript vanilla y HTML5 Canvas.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![p2.js](https://img.shields.io/badge/p2.js-Physics-blue)

## Demo

[Jugar Ahora](https://asteroides-phisics.netlify.app/) 

## Características
- **Física realista** con motor p2.js
- **Sistema de niveles progresivos** - Más asteroides cada nivel
- **Sistema de puntuación** - Diferentes puntos según tamaño del asteroide
- **Sistema de vidas** con respawn e invulnerabilidad temporal
- **Pausa** - Presiona `P` en cualquier momento

### Visualización
- **Estilo clásico** - Fondo negro y gráficos vectoriales blancos
- **Efectos visuales** - Llama del motor al acelerar
- **HUD informativo** - Nivel, vidas y puntuación
- **Responsive** - Se adapta a cualquier tamaño de pantalla

### Controles
- **Desktop**: Teclas de flecha + Espacio + P
- **Mobile**: Controles táctiles optimizados en las esquinas
- **Interfaz no intrusiva** - Los controles no obstruyen el juego

## Cómo Jugar

### Controles Desktop
```
← →     Girar la nave
↑       Impulso
ESPACIO Disparar
P       Pausa
```

### Controles Mobile
- **Esquina inferior izquierda**: Botones de rotación (◄ ►)
- **Esquina inferior derecha**: Impulso (▲) y Disparo (●)

### Objetivo
1. Destruye todos los asteroides para avanzar de nivel
2. Los asteroides grandes se dividen en asteroides más pequeños
3. Evita colisiones o perderás una vida
4. ¡Sobrevive el mayor tiempo posible!

### Sistema de Puntos
| Tamaño de Asteroide | Puntos |
|---------------------|---------|
| Extra Grande (Nivel 1) | 100 pts |
| Grande (Nivel 2) | 50 pts |
| Mediano (Nivel 3) | 25 pts |
| Pequeño (Nivel 4) | 10 pts |

## Instalación

### Opción 1: Usar directamente
1. Descarga el archivo `index.html`
2. Ábrelo en tu navegador
3. ¡Juega!

### Opción 2: Servidor local
```bash
# Con Python
python -m http.server 8000

# Con Node.js
npx serve

# Luego abre: http://localhost:8000
```

## Estructura del Código

```javascript
// Configuración centralizada
CONFIG = {
    ship: { ... },
    bullet: { ... },
    asteroid: { ... },
    space: { ... },
    collision: { ... }
}

// Gestor principal del juego
gameManager = {
    init()           // Inicialización
    start()          // Comenzar juego
    updatePhysics()  // Actualizar física
    render()         // Dibujar escena
    // ... más métodos
}
```

## Características Técnicas

### Física Realista
- Detección de colisiones con p2.js
- Inercia y momentum conservado
- Sistema de "warp" en los bordes (teletransporte)
- Sin fricción espacial

### Optimizaciones
- Límite de balas simultáneas (20 máximo)
- Limpieza automática de entidades antiguas
- RequestAnimationFrame para 60 FPS
- Gestión eficiente de memoria

### Responsive
- Canvas que se ajusta al viewport
- Zoom automático según espacio disponible
- Controles táctiles para dispositivos móviles
- Media queries para diferentes tamaños

## Mejoras sobre el Original

| Característica | Original | Mejorado |
|----------------|----------|----------|
| Sistema de puntos | ❌ | ✅ |
| Controles móviles | ❌ | ✅ |
| Pausa | ❌ | ✅ |
| Pantallas de menú | ❌ | ✅ |
| Invulnerabilidad temporal | ❌ | ✅ |
| Límite de balas | ❌ | ✅ |
| Efectos visuales | ❌ | ✅ (motor) |
| Responsive | ❌ | ✅ |
| Arquitectura modular | ❌ | ✅ |

## Mejoras Futuras

- [ ] Sistema de audio (explosiones, disparos, motor)
- [ ] Partículas de explosión animadas
- [ ] Power-ups (escudo, disparo triple, vida extra)
- [ ] Enemigos adicionales (platillos voladores)
- [ ] LocalStorage para guardar high scores
- [ ] Campo de estrellas animado en el fondo
- [ ] Música de fondo
- [ ] Tabla de clasificación global
- [ ] Soporte para gamepad
- [ ] Estadísticas detalladas

## Contribuir

¿Tienes ideas para mejorar el juego? ¡Las contribuciones son bienvenidas!

1. Fork el proyecto
2. Crea una rama (`git checkout -b feature/MiMejora`)
3. Commit tus cambios (`git commit -m 'Agregar nueva característica'`)
4. Push a la rama (`git push origin feature/MiMejora`)
5. Abre un Pull Request

## Referencias

- [p2.js Documentation](https://schteppe.github.io/p2.js/)
- [Asteroids Original (Atari, 1979)](https://en.wikipedia.org/wiki/Asteroids_(video_game))
- [Ejemplo original de p2.js](https://schteppe.github.io/p2.js/examples/canvas/asteroids.html)


---

## Controles Rápidos

```
Desktop: ← → ↑ ESPACIO P
Mobile:  Toca los botones en las esquinas
```

**¡Que la suerte te acompañe en el espacio! 🚀**

---

<div align="center">

**Si te gustó este proyecto, dale una estrella**

*Hecho con ❤️ y JavaScript*

</div>
