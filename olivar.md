```bash
conda create -n olivar olivar=1.3.3 blast=2.13.0 numpy=1 --channel conda-forge --channel bioconda --strict-channel-priority
conda activate olivar
olivar build -f /data/rkalendar/olivar/RHCE.fasta -p 20 -t rhce
olivar build -f /data/rkalendar/olivar/RHD.fasta -p 20 -t rhd
olivar tiling /data/rkalendar/olivar/ -o example_output --seed 10 -p 1
```
