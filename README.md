# AAE4203 GNSS Lab — Group 10

GPS single point positioning using elevation-weighted least squares, Sagnac correction and Huber-type residual reweighting.

## Requirements

Python 3 and NumPy:

```bash
pip install numpy
```

## Reproduce the Results

Run the following commands from the repository root.

Own-data solution:

```bash
python WLSE-spp.py --mode gps --input-dir own_data --output-dir outputs/own_data --submission G10_owndata.csv
```

Benchmark solution:

```bash
python WLSE-spp.py --mode gps --input-dir benchmark/gps_csv --output-dir outputs/benchmark --submission G10_benchmark.csv
```

Keep `tools/legacy_solver.py` and `COM14___9600_261030_081046.obs` in their original locations. The own-data run reads timestamps from this observation file.

## Outputs

The submission files are saved as:

- `outputs/own_data/G10_owndata.csv`
- `outputs/benchmark/G10_benchmark.csv`

Each output folder also contains detailed solutions, omitted epochs and a summary. Unsolved epochs are omitted rather than filled with previous positions.

The benchmark solution-output rate is not a measure of positioning accuracy; benchmark ground truth and official scores were unavailable.
