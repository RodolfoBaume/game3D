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

---

