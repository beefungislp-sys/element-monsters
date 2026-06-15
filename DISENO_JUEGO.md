# ⚗️ ELEMENT MONSTERS — Documento de Diseño

> Juego de cartas tipo Yu-Gi-Oh, educativo, de química con la tabla periódica.
> Cada elemento es un monstruo. Une ganchos, forma compuestos, gana.

---

## 1. Lo que ya decidimos

| Tema | Decisión |
|------|----------|
| **Jugador** | Niños 8-12 años |
| **Plataforma** | Web (HTML + JavaScript). Se comparte con link. |
| **Cómo ganas** | Formando compuestos químicos |
| **Química** | Valencia real, mostrada como "ganchos" visuales |
| **Elementos** | Primeros 36 (Hidrógeno hasta Kriptón) |
| **Modos** | 1vPC · 1v1 local · 2vPC (equipo, más adelante) |
| **Pelea** | Algunos compuestos (ácidos, etc.) pueden atacar al rival |
| **Online** | NO por ahora. Tal vez después. |

---

## 2. La idea en una frase

> Junta cartas de elementos llenando sus "ganchos" para formar compuestos reales.
> Cada compuesto te da puntos. Algunos compuestos atacan al rival. El primero en
> llegar a la meta de puntos, gana.

---

## 3. Los "ganchos" (así enseñamos valencia sin números)

Cada elemento tiene ganchos = su valencia. Para formar un compuesto, **todos los
ganchos deben quedar unidos, ninguno suelto.**

```
   H  = 1 gancho      ─o
   O  = 2 ganchos     o─ ─o
   Cl = 1 gancho      ─o
   Na = 1 gancho      o─
   C  = 4 ganchos     más ganchos
```

**Ejemplo Agua (H₂O):**
```
   H ─o   o─ ─o   o─ H
            O
   Dos H (1 gancho cada uno) llenan los 2 ganchos del O. ✅ ¡Listo!
```

**Ejemplo Sal (NaCl):**
```
   Na o─   ─o Cl     ✅ Un gancho con un gancho.
```

Si sobra o falta un gancho → el compuesto NO sirve. Así el niño aprende valencia
**tocando y uniendo**, sin memorizar números. (Más adelante: modo difícil que sí
muestra los números, para los de 12.)

---

## 4. Cómo se juega (ACTUALIZADO — más simple para niños)

**No se enseñan los ganchos.** El juego guía: eliges un elemento y te muestra
**con quién SÍ se combina**. Eliges al amigo y el compuesto se forma solo (el juego
pone las cantidades). Nunca hay combinaciones fallidas.

**Dos modos:**

- 🔬 **Laboratorio (aprender):** tocas cualquier monstruo → su ficha (nombre, dato
  curioso, qué es) + sus amigos para combinar. Libre, sin presión. *(Etapa 1 ✅)*

- ⚔️ **Batalla por turnos (1 vs Compu):** tipo Yu-Gi-Oh/Magic pero simple. Formas
  compuestos que son cartas con efecto (monstruo, escudo, hechizo). Bajas la vida del
  rival a 0. Lento, para pensar. *(Ver Sección 12 — reemplaza a la "carrera".)*

**Elementos que no se combinan:**
- ⭐ **Gases nobles** (He, Ne, Ar, Kr) = **cartas estrella**. No se mezclan, pero
  valen puntos solos (son estables). Química real.
- ➕ Los demás elementos tienen al menos un amigo (agregamos mezclas simples).

---

## 4.5 Monstruos (la cara de cada elemento) 🐉

Cada elemento tiene un **monstruo** como cara de la carta — estilo Pokémon/Yu-Gi-Oh.
El monstruo **refleja una propiedad real** del elemento (¡así enseña química sin
esfuerzo!), pero **NO cambia las reglas**: el juego sigue siendo puro ganchos.
El monstruo es la personalidad, no poderes nuevos.

**Dibujos:** hechos con código (formas/SVG simples, estilo "feo-lindo"). Gratis y
rápido. Si después queremos arte IA bonito, se cambia fácil.

Ejemplos:

| Elemento | Monstruo | Propiedad real que muestra |
|----------|----------|----------------------------|
| O (oxígeno) | Espíritu de gas flotante, ligero | Es un gas |
| C (carbono) | Golem negro robusto y duro | Sólido, forma el diamante |
| Fe (hierro) | Caballero de armadura metálica | Metal fuerte, se oxida |
| He (helio) | Globito flotador risueño | Gas muy ligero, no reacciona |
| Na (sodio) | Bicho explosivo nervioso | Reacciona violento con agua |
| Au (oro) | Rey brillante presumido | Metal precioso, no se oxida |

(Cada uno de los 36 elementos tendrá su monstruo. Los diseñamos al codear.)

---

## 5. Tipos de carta

- **Cartas Elemento** → H, O, Na, Cl... cada una con su **monstruo**, sus ganchos y su símbolo.
- **Cartas Compuesto** (se forman, no se roban) → Agua, Sal, CO₂, HCl...
  - Cada una vale puntos.
  - Algunas son de ataque.
- **(Futuro) Cartas Reacción** → bonus, energía, sorpresas. Por ahora NO, para no complicar.

---

## 6. Ganchos de cada elemento (los 36)

Cada elemento tiene un número fijo de ganchos (su valencia más común). Lo fijamos en
UNO solo para que sea simple para los niños. La química de verdad a veces da más de
una opción, pero aquí elegimos la más famosa.

| # | Elemento | Símbolo | Ganchos | | # | Elemento | Símbolo | Ganchos |
|---|----------|---------|---------|-|---|----------|---------|---------|
| 1 | Hidrógeno | H | 1 | | 19 | Potasio | K | 1 |
| 2 | Helio | He | **0** 🚫 | | 20 | Calcio | Ca | 2 |
| 3 | Litio | Li | 1 | | 21 | Escandio | Sc | 3 |
| 4 | Berilio | Be | 2 | | 22 | Titanio | Ti | 4 |
| 5 | Boro | B | 3 | | 23 | Vanadio | V | 5 |
| 6 | Carbono | C | 4 | | 24 | Cromo | Cr | 3 |
| 7 | Nitrógeno | N | 3 | | 25 | Manganeso | Mn | 2 |
| 8 | Oxígeno | O | 2 | | 26 | Hierro | Fe | 3 |
| 9 | Flúor | F | 1 | | 27 | Cobalto | Co | 2 |
| 10 | Neón | Ne | **0** 🚫 | | 28 | Níquel | Ni | 2 |
| 11 | Sodio | Na | 1 | | 29 | Cobre | Cu | 2 |
| 12 | Magnesio | Mg | 2 | | 30 | Zinc | Zn | 2 |
| 13 | Aluminio | Al | 3 | | 31 | Galio | Ga | 3 |
| 14 | Silicio | Si | 4 | | 32 | Germanio | Ge | 4 |
| 15 | Fósforo | P | 3 | | 33 | Arsénico | As | 3 |
| 16 | Azufre | S | 2 | | 34 | Selenio | Se | 2 |
| 17 | Cloro | Cl | 1 | | 35 | Bromo | Br | 1 |
| 18 | Argón | Ar | **0** 🚫 | | 36 | Kriptón | Kr | **0** 🚫 |

**🚫 Gases nobles (He, Ne, Ar, Kr) = 0 ganchos = NO se combinan.** Son los "lobos
solitarios". Esto es química real: no reaccionan con nada. En el juego son cartas
especiales (idea: úsalas como **escudo** que bloquea 1 ataque, porque "no reaccionan").
*(Esa regla del escudo es opcional — la podemos quitar si complica.)*

---

## 6.5 Lista de compuestos que el juego acepta

Diseñada para que **los ganchos siempre cuadren** (ningún gancho suelto). Cada
compuesto da puntos. ⚔️ = compuesto de ataque (quita vida al rival).

### 🟢 Nivel Fácil (2 elementos, pocos ganchos)

| Compuesto | Fórmula | Ganchos cuadran | Puntos | ⚔️ | Dato curioso |
|-----------|---------|-----------------|:------:|:--:|--------------|
| Agua | H₂O | 1+1 = 2 (=O) | 10 | | La bebes todos los días |
| Sal de mesa | NaCl | 1 = 1 | 10 | | La sal de la comida |
| Gas hidrógeno | H₂ | 1 = 1 | 5 | | El gas más ligero |
| Gas oxígeno | O₂ | 2 = 2 | 5 | | El que respiras |
| Óxido de magnesio | MgO | 2 = 2 | 10 | | Polvo blanco |
| Cal | CaO | 2 = 2 | 10 | | Para construir casas |
| Fluoruro de sodio | NaF | 1 = 1 | 10 | | ¡En tu pasta de dientes! |
| Cloruro de potasio | KCl | 1 = 1 | 10 | | Sal sin sodio |

### 🟡 Nivel Medio

| Compuesto | Fórmula | Ganchos cuadran | Puntos | ⚔️ | Dato curioso |
|-----------|---------|-----------------|:------:|:--:|--------------|
| Ácido clorhídrico | HCl | 1 = 1 | 15 | ⚔️ | El ácido de tu estómago |
| Dióxido de carbono | CO₂ | 4 = 2+2 | 15 | | El gas que exhalas |
| Metano | CH₄ | 4 = 1+1+1+1 | 15 | | El gas de las vacas 🐄 |
| Amoníaco | NH₃ | 3 = 1+1+1 | 15 | | Para limpiar |
| Cloruro de calcio | CaCl₂ | 2 = 1+1 | 15 | | Derrite el hielo |
| Óxido de zinc | ZnO | 2 = 2 | 15 | | El bloqueador solar |
| Sulfuro de hidrógeno | H₂S | 1+1 = 2 | 15 | ⚔️ | Huele a huevo podrido 🥚 |
| Ácido fluorhídrico | HF | 1 = 1 | 15 | ⚔️ | ¡Disuelve el vidrio! |
| Dióxido de silicio | SiO₂ | 4 = 2+2 | 20 | | La arena y el vidrio |

### 🔴 Nivel Difícil (muchos ganchos / 3+ elementos)

| Compuesto | Fórmula | Ganchos cuadran | Puntos | ⚔️ | Dato curioso |
|-----------|---------|-----------------|:------:|:--:|--------------|
| Óxido de hierro (herrumbre) | Fe₂O₃ | 3+3 = 2+2+2 | 25 | | El óxido naranja |
| Óxido de aluminio | Al₂O₃ | 3+3 = 2+2+2 | 25 | | Protege el aluminio |
| Cloruro de aluminio | AlCl₃ | 3 = 1+1+1 | 20 | | |
| Tetracloruro de carbono | CCl₄ | 4 = 1+1+1+1 | 20 | | |
| Dióxido de titanio | TiO₂ | 4 = 2+2 | 20 | | La pintura blanca |
| Trifluoruro de boro | BF₃ | 3 = 1+1+1 | 20 | | |
| Arsina | AsH₃ | 3 = 1+1+1 | 25 | ⚔️ | ¡Gas muy venenoso! ☠️ |
| Nitruro de aluminio | AlN | 3 = 3 | 20 | | |
| Nitruro de magnesio | Mg₃N₂ | 2+2+2 = 3+3 | 30 | | El más difícil de armar |

**Total inicial: ~26 compuestos.** Es una buena cantidad para empezar. Se pueden
agregar más fácil después (la lista vive en un solo archivo de datos).

> Nota de química: algunos elementos (Fe, Cu, S, P...) en la vida real tienen varias
> valencias. Para no confundir a los niños, en el juego cada uno usa UNA sola. Por eso
> no metimos cosas como SO₂ o FeS todavía. Si más adelante hacemos "modo experto",
> ahí abrimos las valencias múltiples.

---

## 7. Qué hace que sea EDUCATIVO

- Aprende **símbolos** de los elementos (H, O, Na...).
- Aprende **valencia** uniendo ganchos.
- Aprende **fórmulas reales** (H₂O, NaCl).
- Mini-dato al formar cada compuesto: "¡El agua es H₂O! La tomas todos los días."

---

## 8. Cómo se ve (estilo)

- Colorido, amigable, cartas grandes y claras (para niños).
- Animación suave al unir ganchos y al formar compuesto.
- Sonido de "¡click!" al encajar, fanfarria al ganar.
- Se ve profesional, NO "HTML viejo y feo".

---

## 9. Plan por etapas (para no morir construyendo todo de golpe)

- **Etapa 1 — Laboratorio (aprender):** tabla de 36 monstruos + fichas + combinar guiado. ✅ HECHO
- **Etapa 2 — Carrera vs Compu:** menú, mano de 5 cartas, puntos, barra a 100, robot rival. ✅ HECHO
- **Etapa 3 — (libre):** pulir, sonidos, dificultad del robot.
- **Etapa 4 — Pelea:** compuestos de ataque + vida.
- **Etapa 5 — Multijugador:** 1v1 local, luego 2vPC (equipo).
- **Etapa 6 — Bonito:** animación, sonido, datos educativos.
- **Futuro:** online, más elementos, cartas reacción.

---

## 10. Números del juego (decididos — se pueden balancear después)

- **Puntos para ganar:** 100
- **Cartas en la mano:** 5
- **Vida en modo ataque:** 50
- *(Si el juego sale muy suave o muy duro, movemos estos números. Por eso van en un
  solo lugar fácil de cambiar.)*

## 11. Nombre

**ELEMENT MONSTERS** 🐉⚗️

---

## 12. SISTEMA DE BATALLA (reemplaza la "carrera")

Turnos lentos, tipo Yu-Gi-Oh/Magic pero simple. Cada compuesto es una CARTA con
efecto. Los gases nobles también tienen efecto (usados solos).

### 12.1 Tipos de carta (solo 4)
- 🐉 **MONSTRUO** — se queda en tu zona; cada turno hace su **Ataque** a la vida rival.
- 🛡️ **ESCUDO** — se queda; **bloquea** daño; se gasta al usarse.
- ✨ **HECHIZO** — efecto inmediato (daño/curar/robar/destruir); se descarta.
- ⭐ **ESTRELLA** — gas noble, usado solo; efecto especial (casi siempre defensivo).

### 12.2 Reglas
- Vida inicial **30** cada uno. Mano de **5**. (Números ajustables.)
- Turno: **roba 1 → forma 1 compuesto (o usa 1 noble) → resuélvelo → tus monstruos
  atacan → pasa turno.**
- Máximo **3 monstruos** en tu zona (para que el ataque no crezca infinito).
- Escudos bloquean el daño entrante; algunos hechizos destruyen monstruos/escudos.
- **Gana** quien deje al rival en 0 de vida.
- **COMBATE = SIMPLE (decidido):** los monstruos tienen SOLO Ataque y pegan directo
  a la vida del rival. NO pelean entre sí, NO tienen vida propia. Para destruir un
  monstruo se usa un hechizo (ej: NH₃). *(Monstruos con vida propia = posible mejora
  futura, no ahora.)*

### 12.3 Tabla de efectos

**🐉 Monstruos (Ataque):** Mg₃N₂=8 (jefe) · Fe₂O₃=6 · TiO₂=5 · V₂O₅=5 ·
CuO/AlCl₃/Cr₂O₃/Ga₂O₃/GeO₂/Sc₂O₃/CCl₄=4 · Li₂O/MgO/CaO/MnO/CoO/NiO=3 ·
NaCl/KCl/NaBr/LiCl=2

**🛡️ Escudos (Bloquea):** Al₂O₃=5 · AlN=5 · SiO₂=4 · BeO=4 · ZnO=3 · NaF=2 (+cura 2)

**✨ Hechizos:** AsH₃=daño 6 · HF=daño 5 (ignora escudo) · HCl=daño 4 ·
HBr/PH₃/H₂Se=daño 4 · BF₃=daño 4 · H₂S=daño 3 · H₂/CH₄=daño 3 ·
H₂O=cura 4 · O₂=roba 2 · CaCl₂=derrite un escudo · NH₃=destruye un monstruo ·
CO₂=el monstruo rival no ataca 1 turno

**⭐ Estrellas (gases nobles):** Ar=bloquea próximo ataque completo · Kr=bloquea 5 ·
He=esquivas el próximo ataque · Ne=roba 1 carta y espías la mano rival

### 12.4 Balance del mazo
Cada elemento aparece **tantas veces como reacciones tenga** (mínimo 1):
- O=21, H=11, Cl=7, Na/C/N/F/Al=3, Br/Li/Mg/Ca=2, resto=1
- Gases nobles=2 cada uno
- **Mazo total ≈ 90 cartas.** Así las que más reaccionan (O, H) salen más seguido.

### 12.5 Estado
- Etapa 1 (Laboratorio) ✅ · Carrera ❌ eliminada · **Batalla ✅ CONSTRUIDA**.
- Combate: **simple** (monstruos solo Ataque). Vida 30, mano 5 (cap 7), draw 2/turno.
- Robot rival con IA simple (elige la mejor carta cada turno).
- Pendiente de pruebas/balance del usuario.
