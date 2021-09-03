# ICSE Submission #2645

## Data
All the data is available in the FuzzBench Reports and will be automatically downloaded.
 * 20 trials of 23 hours with 15 programs and 10 fuzzers.
   * Experiment name: 2021-02-17-bug-paper
   * Report: https://www.fuzzbench.com/reports/2021-02-17-bug-paper/index.html
   * Data: https://www.fuzzbench.com/reports/2021-02-17-bug-paper/data.csv.gz
   * Fuzzbench Commit: [38e344fef2f1079579391a0d9dcb52319f7051f2](https://github.com/google/fuzzbench/commits/38e344fef2f1079579391a0d9dcb52319f7051f2)
 * 30 trials of 23 hours with 11 programs and 10 fuzzers.
   * Experiment name: 2021-08-19-crash-s
   * Report: https://www.fuzzbench.com/reports/2021-08-19-crash-s/index.html and 
   * Data: https://www.fuzzbench.com/reports/2021-08-19-crash-s/data.csv.gz
   * Fuzzbench Commit: db192b60815ac87f69ee0f7f3e37aeac71949e1b
 * 30 trials of 23 hours with 11 programs and 10 fuzzers.
   * Experiment name: 2021-08-19-crash-s2
   * Report: https://www.fuzzbench.com/reports/2021-08-19-crash-s2/index.html and 
   * Data: https://www.fuzzbench.com/reports/2021-08-19-crash-s2/data.csv.gz
   * Fuzzbench Commit: db192b60815ac87f69ee0f7f3e37aeac71949e1b

## Data Analysis
The Jupyter notebook generate all tables and figures.

## Reproducibility

```
# Download the precise version of FuzzBench used for the experiment
git clone https://github.com/google/fuzzbench.git
cd fuzzbench
git checkout <Fuzzbench Commit>
# Download the internal config file.
curl https://storage.googleapis.com/[experiment-name]/config/experiment.yaml > /tmp/experiment-config.yaml
make install-dependencies
# Launch the experiment using paramters from the internal config file.
PYTHONPATH=. python experiment/reproduce_experiment.py -c /tmp/experiment-config.yaml -e <new_experiment_name>
```


