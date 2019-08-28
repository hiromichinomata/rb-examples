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

# simple csv
extract one column from csv

```bash
> cat example.csv
id,name,age,sex
1,Taro,17,male
2,Hanako,29,female
3,Ken,35,male
4,Ai,7,female

> cat example.csv |rb -l 'split(",")[2]'
age
17
29
35
7
```

drop header from csv

```bash
> cat example.csv |rb 'drop(1)'
1,Taro,17,male
2,Hanako,29,female
3,Ken,35,male
4,Ai,7,female
```

sort by column

```bash
> cat example.csv |rb 'drop(1).sort_by{|l| l.split(",")[2].to_i}'
4,Ai,7,female
1,Taro,17,male
2,Hanako,29,female
3,Ken,35,male
```
