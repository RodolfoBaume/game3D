# 🚀 Prompt Engineering en Acción: Crea tu primer videojuego 3D

¡Bienvenido al taller de la **Semana de TICS del Tecnológico de Pachuca**! 🎓

En este curso no solo aprenderás a programar, sino a colaborar con una Inteligencia Artificial para construir un proyecto desde cero. El objetivo es aprender a redactar instrucciones (**Prompts**) precisas para que la IA actúe como tu programador senior.

---

## 🛠️ Requisitos Previos

Para que el juego funcione, necesitas tener instalado **Python** y la librería **Ursina Engine**. 

Abre tu terminal o consola y ejecuta el siguiente comando:
```bash
pip install ursina
```

---

## 🎯 Dinámica del Taller: El Camino del Desarrollador

No copiaremos y pegaremos código. Tu misión es actuar como el **Director de Proyecto**. Usarás los prompts sugeridos para guiar a la IA (ChatGPT, Claude o Gemini) hacia la meta.

### 🟢 Fase 1: El Mundo Base (El "Hola Mundo" 3D)
**Misión:** Crear el espacio mínimo viable donde podamos movernos.

**Prompt sugerido:**
> "Actúa como un desarrollador experto en Python y Ursina Engine. Escribe un script que:
> 1. Importe todo de `ursina` y el `FirstPersonController` de `ursina.prefabs.first_person_controller`.
> 2. Inicialice la aplicación.
> 3. Cree un suelo usando la clase `Entity` con modelo `'plane'`, escala 100x100, color gris y un collider `'box'`.
> 4. Añada un cielo usando `Sky()`.
> 5. Instancie el `FirstPersonController` y asígnelo a la variable `jugador`.
> 6. Ejecute `app.run()`."

---

### 🔵 Fase 2: Generación Procedural (Aleatoriedad)
**Misión:** Poblar el mundo con obstáculos dinámicos.

**Prompt sugerido:**
> "Modifica el código anterior. Importa la librería `random`. Antes de instanciar al jugador, crea un bucle que genere 30 cubos aleatorios. Cada cubo debe tener: modelo `'cube'`, color cyan, collider `'box'` y una posición X, Y, Z aleatoria (X y Z entre -20 y 20, Y entre 1 y 8)."

---

### 🟡 Fase 3: Interacción y Feedback (Mecánica de Disparo)
**Misión:** Hacer que el juego sea interactivo y tenga sensaciones visuales ("Game Juice").

**Prompt sugerido:**
> "Agrega una mecánica de destrucción. Define la función `input(key)`. Si la tecla es `'left mouse down'`, verifica si el ratón apunta a una entidad (que no sea el suelo) y destrúyela usando `destroy()`. 
> Además, añade un efecto visual de retroceso: cuando se dispare, la cámara del jugador debe subir ligeramente y el campo de visión (`fov`) debe cambiar a 95 y regresar a 90 rápidamente usando la función `invoke()`."

---

### 🔴 Fase 4: Inteligencia Artificial (El Enemigo)
**Misión:** Crear una amenaza autónoma que persiga al jugador.

**Prompt sugerido:**
> "Crea una clase llamada `Enemigo` que herede de `Entity`. 
> 1. En el `__init__`, asígnale un modelo `'cube'`, color rojo, collider `'box'` y que reciba la posición X y Z como parámetros.
> 2. En el método `update()`, haz que el enemigo siempre mire al jugador usando `self.look_at(jugador)` y se mueva hacia él sumando `self.forward * 1.2 * time.dt` a su posición.
> 3. Fuera de la clase, crea un bucle que instancie 5 enemigos en posiciones aleatorias."

---

### 🔥 Reto Final: Condición de Derrota (Game Over)
**Misión:** Implementar la lógica para perder la partida.

**Instrucción para el alumno:** 
Intenta redactar tu propio prompt para lograr esto. **Pista:** Dile a la IA que en el método `update` del enemigo, calcule la distancia entre el enemigo y el jugador. Si la distancia es menor a 1.5, debe imprimir `'¡GAME OVER!'` y cerrar la aplicación con `application.quit()`.

---

## 🏆 Tips de Oro para Prompt Engineering

Para obtener los mejores resultados de la IA, recuerda:

1.  **Asigna un Rol**: Empieza con *"Actúa como un experto en..."*
2.  **Sé Específico**: En lugar de *"haz que se mueva"*, usa *"suma la posición actual más la dirección forward multiplicada por el tiempo"*.
3.  **Itera y Corrige**: Si el código lanza un error, no te rindas. Copia el error exacto y dile a la IA: *"Me salió este error: [PEGA EL ERROR AQUÍ], ¿cómo lo soluciono?"*.

---

## 📂 Estructura del Repositorio
- `game_final.py`: La solución maestra completa (¡No la abras hasta terminar el reto!).
- `images/`: Carpeta con texturas para quienes quieran mejorar el aspecto visual del juego.

**¡Buena suerte, desarrollador! 🚀**
