Bootstrap: docker
From: ubuntu:bionic


%post
    mkdir -p /tmp/cellranger-build \
    && cd /tmp/cellranger-build \
    && apt-get update \
    && apt-get install -y wget \
    && wget -O cellranger-6.0.0.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.0.tar.gz?Expires=1617136743&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMC50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MTcxMzY3NDN9fX1dfQ__&Signature=ky58W6OdDZ-kIRhJD5kvdWaZDJlXgIXw0Dzna8Ks5~208ZoG-ORCLHouQVzwB-5qjaPV-hDtH3ZrjkpUf7Yh6dgUFZnlzKLBc-GTq-22-SZt03-RUpZJ2nsZdrm~AW7uY~X~1xaoSzRmX6lyZgatcPVLh3gPh1JsDX~z~jwMuu7wvo7iY5dZnOqHGbzRZ-YGiVekP7VsxXG2JcCI0V3mnsd6mrm6iwJ3FIRrLymo9YRZ5tpQLCfLhHSLKsM1m-oOjZctzE5Y0hobV-T~msb2yI24UmgsccZq-NCSftEHwfeXW899aPBY9Shq0hXfJdhCHsWYGg3bvMegYpFw84s9kQ__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" \
    && mv cellranger-6.0.0.tar.gz /apps/ \
    && mkdir /apps \
    && cd /apps \
    && tar -xzvf cellranger-6.0.0.tar.gz \
    && rm -f cellranger-6.0.0.tar.gz \
    && rm -rf /tmp/cellranger-build

%environment
    export PATH=/apps/cellranger-6.0.0:$PATH

%labels
    Michela Dell'Alma
    Version v0.0.1
