Attempt 1:
```bash
conda create -n olivar olivar=1.3.3 blast=2.13.0 numpy=1 --channel conda-forge --channel bioconda --strict-channel-priority
conda activate olivar
olivar build -f /data/user/olivar/RHCE.fasta -p 20 -t rhce
olivar build -f /data/user/olivar/RHD.fasta -p 20 -t rhd
```

Attempt 2:
```bash
conda create -n olivar2 olivar=1.2 blast numpy --channel conda-forge --channel bioconda --strict-channel-priority
conda activate olivar2
olivar build /data/rkalendar/olivar/RHCE.fasta -p 20 -t rhce2
olivar build /data/rkalendar/olivar/RHD.fasta -p 20 -t rhd2
olivar tiling ./olvr/ -o example_output --seed 10 -p 20
```

Attempt 3:
```bash
conda create -n olivar3 olivar=1.2.1 blast numpy plotly=5.13 --channel conda-forge --channel bioconda --strict-channel-priority
conda activate olivar3
olivar build /data/rkalendar/primers_making/olivar/RHCE.fasta -p 20 -t rhce
olivar build /data/rkalendar/primers_making/olivar/RHD.fasta -p 20 -t rhd
olivar tiling ./ -o example_output --seed 10 -p 20
```
