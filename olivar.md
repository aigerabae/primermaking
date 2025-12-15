```bash
conda create -n olivar olivar=1.1.5 blast=2.13.0 numpy=1 --channel conda-forge --channel bioconda --strict-channel-priority
conda activate olivar
olivar build /data/rkalendar/olivar/ucsc.hg38.fa -p 20 
```

problem: ValueError: Ambiguous bases are not supported. {'n'} found in reference fasta file.

Solution: remove all N and n symbols (except for chromosome names):
```bash
sed '/^>/! s/N//g' ucsc.hg38.fa | sed '/^>/! s/n//g' | tr -s '\n' > hg38_noN.fa
olivar build /data/rkalendar/olivar/hg38_noN.fa -p 20 
```
