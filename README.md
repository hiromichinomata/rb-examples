# rb examples

## basic

```bash
> ls
a.md  b.md  c.md

## bulk
> ls |rb  'reverse'
c.md
b.md
a.md

## line by line
> ls |rb -l 'reverse'
dm.a
dm.b
dm.c
```

