
# Local fluent-bit configuration testing

## usage

    docker run --rm -v $(pwd):/var/vc -v $(pwd)/output:/output -ti fluent/fluent-bit:latest /fluent-bit/bin/fluent-bit --config /var/vc/fluent-bit.conf --verbose

## output

* Modify order of output rules in fluebt-bit.conf
* Count lines in input/output.file

### Fwd to another fluentbit/fluentd instance

Run docker with `--net host` and update `Host` in the proper `[OUTPUT]` section.


## Performance

### For better performance during testing use:

`SERVICE`:
```yaml
    Log_Level     info
```

`INPUT/tail`:
```yaml
    Mem_Buf_Limit     10M
```
