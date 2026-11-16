# 🎯 Marcador de Bocha Offline — SCBP

**Marcador digital completo para partidos de Bocha Paralímpica (Boccia), 100% offline.**

Una réplica fiel del marcador en vivo del [SCBP](https://scboccia.com) (Sistema de Campeonatos de Bocha Paralímpica), funcionando en un único archivo HTML sin necesidad de servidor, internet ni instalación. Ideal para árbitros, organizadores de competiciones y entrenadores que necesitan registrar partidos en cualquier lugar.

---

## 🌐 Idiomas / Languages / Idiomes

- 🇧🇷 **Português (BR)** — [README.md](README.md)
- 🇺🇸 **English** — [README.en.md](README.en.md)
- 🇪🇸 **Español** — [README.es.md](README.es.md) ← estás aquí

El propio marcador incluye un **selector de idioma** en la parte superior (PT | EN | ES).

---

## ✨ Funcionalidades

### ⚽ Durante el partido
- **Marcador gigante** rojo × azul, idéntico al diseño oficial del SCBP
- **Temporizador individual por atleta** con play/pause (cuenta regresiva separada para cada lado)
- **Parciales (Ends)**: P1, P2, P3, P4 + Tiebreak (TB1, TB2) con puntuación separada
- **Bolas por end** con contadores clicables (+/−)
- **Sistema completo de violaciones** basado en el Artículo 16 de las Reglas World Boccia 2025-2028:
 - Retracción (Art. 16.5)
 - Bola de Penalización (Art. 16.6)
 - Retracción + Penalización (Art. 16.7)
 - Penalización + Tarjeta Amarilla (Art. 16.8)
 - Tarjeta Amarilla (Art. 16.9)
 - Tarjeta Roja (Art. 16.11)
 - Forfeit (Art. 16.12)
- **Contador de bolas de penalización (1P)** con chip amarillo
- **Tiebreak automático** cuando hay empate al final del último end
- **Guardado automático** en `localStorage` — cierra el navegador y continúa donde lo dejaste

### 📺 Pantalla gigante / Scoreboard
- El botón **"Pantalla"** en el menú abre una nueva pestaña con diseño para TV en la cancha
- Actualización automática cada 2 segundos (lee el `localStorage`)
- Ideal para televisores, proyectores o tablets al lado de la cancha

### 📄 Acta oficial
- Modal con acta **idéntica** al modelo World Boccia / ANDE utilizado en el SCBP
- Tabla de parciales con tiempos individuales de cada atleta
- Violaciones agrupadas (con contador "N × 1 Bola de Penalización")
- Cuadro del ganador con borde destacado
- **Botón "Imprimir / Guardar PDF"** — usa la impresión nativa del navegador, funciona offline

### 🏅 Clases oficiales soportadas
| Clase | Modalidad | Ends | Bolas/atleta | Tiempo/parcial |
|-------|-----------|------|--------------|----------------|
| BC1 | Individual | 4 | 6 | 4:30 min |
| BC2 | Individual | 4 | 6 | 3:30 min |
| BC3 | Individual (c/ RO) | 4 | 6 | 6 min |
| BC4 | Individual | 4 | 6 | 3:30 min |
| Parejas BC3 | Dobles | 4 | 3 | 7 min |
| Parejas BC4 | Dobles | 4 | 3 | 4 min |
| Equipo | Trío (BC1+BC2) | 6 | 2 | 5 min |
| ⚙️ Personalizado | Custom | 1-10 | 1-6 | 60-900s |

### 💻 Desktop
- Aplicación de escritorio (Windows, Mac, Linux)
- Modo pantalla completa (F11) disponible en el menú

---

## 🚀 Cómo usar

### Opción 1 — Descarga directa (recomendado)
1. Descarga el archivo [`index.html`](./index.html) de este repositorio
2. Abre con doble clic en cualquier navegador moderno (Chrome, Edge, Firefox, Safari)
3. ¡Listo! No necesita instalación, servidor ni internet

### Opción 2 — Clonar el repositorio
```bash
git clone https://github.com/gabrielrdesousa123/Placar_offline.git
cd Placar_offline
# Abre index.html en tu navegador
```

### Opción 3 — Usar como PWA
En Chrome/Edge, haz clic en el icono "Instalar" de la barra de direcciones para tener el marcador como aplicación en tu escritorio o móvil.

---

## 🎮 Guía rápida

1. **Selecciona la clase** (BC1, BC2, BC3, BC4, Parejas, Equipo o Personalizado)
2. **Introduce los nombres** (opcional — si se deja vacío, asume "ROJO" y "AZUL")
3. **Añade clubes/equipos** (opcional)
4. Haz clic en **▶ INICIAR PARTIDO**
5. Usa los botones ▶ junto a cada temporizador para controlar el tiempo de cada atleta
6. Haz clic en los números del marcador para añadir puntos (+1)
7. Usa los botones **−** y **+** para controlar las bolas lanzadas
8. Haz clic en **⚠️ Añadir Violación** para registrar infracciones
9. Haz clic en **SIGUIENTE END ▶** para avanzar
10. Al finalizar, haz clic en **☰ Menú → Ver Acta → Imprimir / Guardar PDF**

---

## 💾 Almacenamiento

- Todos los datos se guardan en el `localStorage` del navegador
- Al reabrir la página, el partido continúa donde se quedó
- Para empezar un nuevo juego: **☰ Menú → Reiniciar Juego Completo**

---

## 📂 Estructura del proyecto

```
Placar_offline/
├── index.html ← Marcador completo (HTML + CSS + JS en un solo archivo)
├── README.md ← Portugués
├── README.en.md ← Inglés
├── README.es.md ← Este archivo (Español)
└── LICENSE ← Licencia MIT
```

**Cero dependencias externas.** Todo está integrado en `index.html` (~55 KB).

---

## 🧠 Reglas implementadas

Este marcador sigue las **Reglas Oficiales de World Boccia (BISFed) 2025-2028**, en especial:

- **Art. 10.16** — Criterios de desempate (Tiebreak)
- **Art. 16** — Violaciones y penalizaciones (16.5 a 16.12)
- **Sección 2.1.5.1** — Puntuación de W.O. (6-0 o mayor diferencia)

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Abre un issue o pull request.

---

## 📜 Licencia

[Licencia MIT](LICENSE) — libre para uso personal, comercial y modificaciones.

---

## 🔗 Enlaces

- **SCBP (sistema online):** [scboccia.com](https://scboccia.com)
- **World Boccia:** [worldboccia.com](https://worldboccia.com)
- **Autor:** Gabriel R. de Sousa

---

## ❓ Preguntas frecuentes

**¿Funciona sin internet?**
Sí, 100%. Es un archivo HTML autocontenido.

**¿Se envían datos a algún servidor?**
No. Todo queda en tu navegador (localStorage). Ningún dato sale del dispositivo.

**¿Puedo usarlo en competiciones oficiales?**
Sí. El diseño y las reglas son idénticos a los usados en el SCBP, sistema adoptado por la ANDE y diversas competiciones brasileñas de Bocha Paralímpica.

**¿Dónde está el acta?**
En el menú ☰ lateral, opción "Ver Acta". Puedes imprimir o guardar como PDF.

**¿Cómo abro la pantalla gigante?**
En el menú ☰ lateral, opción "Pantalla / Scoreboard". Se abre una nueva pestaña con el marcador ampliado, ideal para TVs en la cancha.