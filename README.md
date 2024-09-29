# homework2.2
## 列出1.gtf文件中 XI 号染色体上的后 10 个 CDS （按照每个CDS终止位置的基因组坐标进行sort）。
```
$ cat 1.gtf | awk '$1=="XI" && $3=="CDS" { print $5 } ' | sort -n | tail -10
632798
635179
638283
639968
642501
649862
656733
657753
660464
663286

$ cat 1.gtf | awk '$1=="XI" && $3=="CDS" && $5>=632798 { print $1, $2, $3, $4, $5, $6, $7, $8, $9 } '
XI ensembl CDS 631152 632798 . + 0 gene_id
XI ensembl CDS 633029 635179 . - 0 gene_id
XI ensembl CDS 635851 638283 . + 0 gene_id
XI ensembl CDS 638904 639968 . - 0 gene_id
XI ensembl CDS 640540 642501 . + 0 gene_id
XI ensembl CDS 646356 649862 . + 0 gene_id
XI ensembl CDS 653080 656733 . + 0 gene_id
XI ensembl CDS 656836 657753 . + 0 gene_id
XI ensembl CDS 658719 660464 . - 0 gene_id
XI ensembl CDS 661442 663286 . + 0 gene_id
```

## 统计 IV 号染色体上各类 feature （1.gtf文件的第3列，有些注释文件中还应同时考虑第2列） 的数目，并按升序排列。

## 寻找不在 IV 号染色体上的所有负链上的基因中最长的2条 CDS 序列，输出他们的长度。

## 寻找 XV 号染色体上长度最长的5条基因，并输出基因 id 及对应的长度。

## 统计1.gtf列数
