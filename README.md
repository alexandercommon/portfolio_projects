# Portfolio Projects

This "portfolio" is a work-in-progress. The entirety of my career has been with closed-source technology, so I'm actively working on cleaning up my personal projects for demonstration.

## Projects

### [End-to-End AWS ETL Pipeline for SPX Options Data](data_engineering_pipeline.ipynb)

A distributed cloud ETL pipeline that filters a ~115 TB SPX/SPXW options quote feed down to roughly 80,000 five-minute snapshots, then fits arbitrage-free SVI volatility surfaces and derives greeks for each one.

**Stack:** AWS Lambda, Step Functions, SQS, EC2 spot fleet, S3, Athena · Python, PyArrow, DuckDB, `sanos`

**Covers:** fan-out orchestration at ~80,000 invocations, a validation-and-requeue loop for corrupt and empty output, the dependency-size constraint that forced greek fitting off Lambda and onto a spot fleet, and a retrospective on what would be built differently.
