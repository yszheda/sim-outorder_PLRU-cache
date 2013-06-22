SimpleScalar sim-outorder simulator with PLRU policy cache
===

We implement the 
**Tree-based Pseudo LRU** (PLRU) from 
in the _SimpleScalar_(http://www.simplescalar.com/) sim-outorder simulator.

## Configuration ##

Format:

```
<name> <nsets>:<bsize>:<assoc>:<repl>
```

Cache replacement policy:
```
l: LRU;
p: PLRU;
d: DIP;
r: Random;
f: FIFO;
```

Example:

```
 # l2 data cache config, 256KB, 64-byte line, 8-way, PLRU
-cache:dl2             ul2:512:64:8:p
```

## Compilation ##

```bash
make config-alpha
make clean
make sim-outorder
```
