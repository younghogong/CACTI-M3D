This is the modified version of CACTI for modeling M3D (monolithic 3D) and TSV-3D caches with 3D BLP (bitline partitioning) and 3D WLP (wordline partitioning) designs.

Our modifications include the below features.

1) 3D stacked cache design (bitline partitioning and wordline partitioning) modeling
- Partitioning strategy can be determined in config (.cfg) file using 'partitioning' variable (e.g., -partitioning 1 (BLP) or -partitioning 0 ("WLP"))
- Partitioning strategy should be used with -layers n (n>1); '-layers 1' indicates planar 2D cache.

2) Performance/power/area comparison between M3D (Monolithic 3D using Monolithic inter-tier via) and TSV-3D.
- Depending on the number of stacked layers (e.g., -layers in .cfg file), the access time/dynamic energy/leakage power of a cache are calculated.
- The transistor performance degradation by M3D can be modeled in .cfg file.
- For example, you can reflect 10% transistor performance degradation by using '-degradation 1.1' in .cfg file.
- Via models can be found in https://github.com/younghogong/CACTI3DD-for-viamodeling

For sample configurations, please refer to .cfg files in configs directory. 

Usage: ./cacti -infile [config file]

