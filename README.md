# dbt-junitxml

Convert your dbt test results into jUnit XML format so that CI/CD platforms (such as Jenkins, CircleCI, etc.)
can better report on tests in their UI.

## Installation

```shell
pip install dbt-junitxml
```


## Usage

When you run your dbt test suite, the output is saved under `target/run_results.json`. Run the following command
to parse your run results and output a jUnit XML formatted report named `report.xml`.

```shell
dbt-junitxml parse target/run_results.json report.xml
```

## Notes

Currently, v4 and v5 of the [Run Results](https://docs.getdbt.com/reference/artifacts/run-results-json) specifications are both supported.
