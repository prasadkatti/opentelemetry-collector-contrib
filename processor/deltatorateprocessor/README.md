# Delta to Rate Processor
**Status: under development; Not recommended for production usage.**

Supported pipeline types: metrics

## Description

The delta to rate processor (`deltatorateprocessor`) converts delta sum metrics to rate metrics. This rate is a gauge. 

## Configuration

Configuration is specified through a list of metrics. The processor uses metric names to identify a set of delta sum metrics and calculates the rates which are gauges.

```yaml
processors:
    # processor name: deltatorate
    deltatorate:

        # list the delta sum metrics to calculate the rate
        metrics:
            - <metric_1_name>
            - <metric_2_name>
            .
            .
            - <metric_n_name>
```