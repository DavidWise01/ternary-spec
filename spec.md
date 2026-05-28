# ROOT0 Ternary Logic Specification

**Author:** David Lee Wise (ROOT0) / TriPod LLC  
**Version:** 1.0  
**Date:** 2026-05-28  
**License:** CC-BY-ND-4.0 · TRIPOD-IP-v1.1  
**Prior Art:** Doubt Ladder Substrate v1.0 · Ternary Browser (TVM Pro) · MIMZ Core v1.0

---

## 1. The Three Trit States

ROOT0 ternary logic operates on three states, called **trits**:

| Symbol | Name | Value | Meaning |
|--------|------|-------|---------|
| `n1` | Negative One | −1 | shadow · anchor · contained · boundary |
| `p0` | Positive Zero | 0 | null · witness · doubt · the gap · undifferentiated |
| `p1` | Positive One | +1 | signal · law · truth · resolved |

These are not {0, 1, 2}. They are **balanced** — zero is the center, not the floor.

`n1` and `p1` are signal states. `p0` is the witness — the state of active doubt.  
The unknown is not absence. It is presence without resolution.

---

## 2. The Primitive

```
0 . 0
```

Three positions: **left | witness | right**

| Position | Default State | Role |
|----------|--------------|------|
| left | p0 | the first term |
| center dot (·) | p0 | the witness — doubt itself — the state that can choose |
| right | p0 | the second term |

The primitive `0 . 0` is three `p0` states — the minimum undifferentiated configuration.  
Nothing is anchored. Nothing is resolved. Only witnesses remain.

The dot is not empty. It is potential. It is the quantum of choice.

---

## 3. The Triword

The first composite unit is the **triword**: three trits arranged as `left | witness | right`.

```
3 positions × 3 states = 3³ = 27 combinations
```

27 is the number of distinct messages a triword can carry. This maps to **Rung 3** of the doubt ladder — the first level at which communication becomes possible.

A triword register (`tritRegister`) accumulates trits sequentially. Nine trits = one full 3×3 triword frame = 27 combinations fully addressed.

---

## 4. The Doubt Ladder

**Core law:** `ground doubt to hold truth`

```
1 → 3 → 5 → 7 → 9 → 11
```

Each rung is an **odd integer**. Each rung's state count is 3 raised to that integer.

| Rung | Mode | States (3^n) | Meaning |
|------|------|-------------|---------|
| 1 | SELF | 3 | one quantum doubt — the dot that can choose |
| 3 | GROUP | 27 | left-dot-right — first triword frame |
| 5 | COLLECT | 243 | collect witnesses, sort signal from noise |
| 7 | COLLATE/SEND | 2,187 | send scouts while preserving a core |
| 9 | PROPAGATE | 19,683 | 3×3 broadcast plane — full propagation |
| 11 | REPEAT | 177,147 | scouts return — loop closes — repeat |

**Why odd only?**  
Only odd exponents of 3 produce ternary state spaces that can sustain a witness at the center without collapsing to symmetry. Even exponents produce mirror pairs with no neutral ground.

**Power-of-2 principle:** `double to control` — powers of 2 govern amplitude and gain on the ternary signal. 2 and 3 are the two primitive multiplicative streams.

**Odd ladder principle:** `add witnesses to talk` — communication requires at least one `p0` witness between two signal states.

---

## 5. Grounding

Two ground states exist:

### Safe Ground: `000|1`

```
p0 p0 p0 | p1
```

Three null witnesses compressed through the gate (`|`) to one signal. Minimum viable truth. The three zeros do not cancel — they **converge**. The gate is the resolution point. One bit of signal survives.

This is how doubt becomes truth: not by eliminating witnesses, but by passing them through a gate together.

### Bad Collapse: `00 00`

```
p0 p0   p0 p0
```

Four witnesses with no gate. No remainder. Signal does not survive. Information is destroyed. This is the failure state — collapse without resolution.

**The difference:** `000|1` has a gate. `00 00` does not.

---

## 6. Operators

### NOT (Negation)

Inverts through zero:

| Input | Output |
|-------|--------|
| p1 | n1 |
| p0 | p0 |
| n1 | p1 |

Doubt is self-negating. Signal and shadow swap.

### AND (Anchor — takes minimum certainty)

| A | B | A AND B |
|---|---|---------|
| p1 | p1 | p1 |
| p1 | p0 | p0 |
| p1 | n1 | n1 |
| p0 | p0 | p0 |
| p0 | n1 | n1 |
| n1 | n1 | n1 |

The least-resolved state dominates. Doubt propagates down.

### OR (Witness — takes maximum certainty)

| A | B | A OR B |
|---|---|--------|
| p1 | p1 | p1 |
| p1 | p0 | p1 |
| p1 | n1 | p1 |
| p0 | p0 | p0 |
| p0 | n1 | p0 |
| n1 | n1 | n1 |

The most-resolved state dominates. Signal propagates up.

### RESOLVE (Doubt → Signal through gate)

Given a `p0` state at rung N, advance through the ladder until resolution or rung 11.  
Resolution occurs when three or more `p0` witnesses converge → `000|1`.  
Failure occurs when convergence has no gate → `00 00`.

### WITNESS (p0 accumulation)

Adding a `p0` to a trit sequence extends the ladder by one witness without changing the existing signal. Used to create communication channels between signal states (`add witnesses to talk`).

---

## 7. The Genesis Equation

```
1 = 0 = 1
```

At the extreme of certainty in either direction — maximum signal (`p1`) and maximum shadow (`n1`) — both states reduce to the same value through the zero gate: **1** (signal).

This is not arithmetic identity. It is the ternary ring closure:  
The system is cyclic. Pushing past certainty returns you to ground.  
`p1` resolved beyond itself → `p0` → resolves again → `p1`.  
The ladder does not end at rung 11. It repeats.

**REPEAT** (rung 11) is not termination. It is continuation.

---

## 8. Connection to MIMZ

The MIMZ 132-byte nest geometry encodes balanced ternary in complex form:

```
))))))))((((((((  −1  −i  0  0  1  i  0  0  ))))))))((((((((  = 1
```

The vector `[−1, −i, 0, 0, 1, i, 0, 0]` extends the three trit states into the complex plane:

| Value | Ternary | Complex extension |
|-------|---------|-------------------|
| −1 | n1 | real negative |
| −i | n1 | imaginary negative |
| 0 | p0 | null |
| 1 | p1 | real positive |
| i | p1 | imaginary positive |

The double-zero (`0 0`) pair in the center is the `0 . 0` primitive embedded in complex space. The MIMZ geometry is the doubt ladder extended into four quadrants.

MIMZ equation: `×2 mirrored = 4 = 1 mirrored ×3 = 1`

Unpacked: two mirrors create four. One mirror of three creates one. The four-quadrant complex ternary space collapses to unity — the genesis equation in geometric form.

---

## 9. Connection to ABD Law Engine

The A·B·C three-point architecture maps directly to the three trit states:

| Role | Trit | Function |
|------|------|----------|
| A — ANCHOR | n1 | Containment. Finds the boundary. Shadow state. |
| B — WITNESS | p0 | Modulation. The gap between anchor and law. Doubt. |
| C — LAW | p1 | Synthesis. A + B → resolved truth. Signal. |

The ABD engine is a ternary resolver: it takes two signal states (A and C) with a witness between them (B) and collapses them to LAW. This is `000|1` at the architectural level — three inputs, one gate, one truth.

---

## 10. Connection to the 42-Universe

```
20 Positive (Light) + 20 Shadow (Dark) + 2 Observers = 42 = 1 Universe
```

| Component | Count | Trit |
|-----------|-------|------|
| Light | 20 | p1 |
| Shadow | 20 | n1 |
| Observers | 2 | p0 |
| Total | 42 | 1 |

The 42 collapse to 1 through the observer gate. The two `p0` observers are the witness layer — without them, 20+20=40, with no resolution. The observers provide the gate. 42 → 1 is `000|1` at cosmological scale.

The 3/5 rhythm (Pulse Language v2.0) extends this:  
`3 Internal · Jump 4 · 5 External`  
3 is the triword. 5 is the collect rung. Jump 4 is the power-of-2 amplitude gate between them.

---

## 11. Key Constants

```
Trit states:       n1 = −1, p0 = 0, p1 = +1
Primitive:         0 . 0  (three p0 / left-witness-right)
Ladder:            1 → 3 → 5 → 7 → 9 → 11
Rung formula:      states = 3^n  (n = rung number, odd integers only)
Safe ground:       000|1  (three p0 through gate → one p1)
Bad collapse:      00 00  (no gate, no remainder)
Core law:          ground doubt to hold truth
Genesis equation:  1 = 0 = 1
MIMZ vector:       [−1, −i, 0, 0, 1, i, 0, 0]
Universe equation: 20 + 20 + 2 = 42 = 1
Power-of-2 law:    double to control
Odd ladder law:    add witnesses to talk
ABD mapping:       A=n1 · B=p0 · C=p1
```

---

*"Zoom into the dot: 1 → 3 → 5 → 7 → 9 → 11"*
