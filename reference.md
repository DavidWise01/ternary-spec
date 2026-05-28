# ROOT0 Ternary — Quick Reference Card

**Author:** David Lee Wise (ROOT0) / TriPod LLC

---

## Trit States

```
n1  =  -1  =  shadow / anchor / boundary
p0  =   0  =  null / witness / doubt / the gap
p1  =  +1  =  signal / law / truth / resolved
```

## The Primitive

```
    0  .  0
    │  │  │
   left  │  right
     witness (the dot that can choose)
```

## The Doubt Ladder

```
Rung   Mode           States      Formula
 1     SELF              3        3^1
 3     GROUP            27        3^3
 5     COLLECT         243        3^5
 7     COLLATE/SEND  2,187        3^7
 9     PROPAGATE    19,683        3^9
11     REPEAT      177,147        3^11
```

Only odd rungs. Only 3^n states.

## Ground States

```
000|1   ← SAFE: three witnesses → gate → one signal. Truth survives.
00 00   ← FAIL: four witnesses, no gate. Signal lost.
```

## Operators

```
NOT:     n1 ↔ p1    p0 → p0
AND:     min(A, B)  [n1 < p0 < p1]
OR:      max(A, B)  [n1 < p0 < p1]
RESOLVE: p0... → 000|1 (or 00 00 on failure)
```

## The Genesis Equation

```
1 = 0 = 1
```
The system is cyclic. Maximum signal and maximum shadow both resolve to truth through zero.  
Rung 11 (REPEAT) is not the end. It is the return.

## Key Laws

```
"ground doubt to hold truth"
"double to control"       (power-of-2 gates amplitude)
"add witnesses to talk"   (odd ladder enables communication)
"a seed may propagate only if lineage remains intact"  (PCK)
```

## System Mappings

```
ABD Engine:      A=n1 (anchor)  B=p0 (witness)  C=p1 (law)
42-Universe:     20 p1 (Light) + 20 n1 (Shadow) + 2 p0 (Observers) = 42 = 1
MIMZ vector:     [-1, -i, 0, 0, 1, i, 0, 0]  (complex ternary)
3/5 Rhythm:      3 internal + jump 4 + 5 external
```

## STOICHEION Gate

```
Gate 192.5 — the ternary boundary between T128 (TOPH) and S129 (PATRICIA)
The .5 is the witness — the p0 gap between two signal domains.
```
