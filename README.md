# CSE 240c Run Instructions

## Download:

Download/copy the competition traces https://groups.google.com/forum/#!forum/champsim <br>
Places the traces in dpc3_traces/ folder <br>

## Build:

Build each prefetcher using the build command

```
$ ./build_champsim.sh bimodal no no no no lru 1

$ ./build_champsim.sh ${BRANCH} ${L1I_PREFETCHER} ${L1D_PREFETCHER} ${L2C_PREFETCHER} ${LLC_PREFETCHER} ${LLC_REPLACEMENT} ${NUM_CORE}
```

## All Prefetchers:

D_JOLT - default D_JOLT <br>
D_JOLT_distance_double - D_JOLT doubling the distance parameter <br>
D_JOLT_distance_half - D_JOLT halving the distance parameter <br>
D_JOLT_histlen - D_JOLT doubling the histlen parameter <br>
D_JOLT_histlen2 - D_JOLT halving the histlen parameter <br>
D_JOLT_incmem - D_JOLT doubling the hardware budget <br>
D_JOLT_decmem - D_JOLT halving the hardware budget <br>

TAP - default TAP <br>
TAP_threshold_double - TAP doubling the threshold parameter <br>
TAP_threshold_half - TAP halving the threshold parameter <br>
TAP_table_anc - TAP increasing ancestors but decreasing descendants <br>
TAP_table_dec - TAP decreasing ancestors but increasing descendants <br>
TAP_incmem - TAP doubling the hardware budget <br>
TAP_decmem - TAP halving the hardware budget <br>

## Run:

```
$ ./run_default.sh D_JOLT      (runs on D_JOLT prefetcher)

$ ./run_default.sh ${L1I_PREFETCHER}
```
