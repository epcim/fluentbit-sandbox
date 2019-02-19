
# Local fluent-bit configuration testing

## usage

    docker run -v $(pwd):/var/vc -ti fluent/fluent-bit:latest /fluent-bit/bin/fluent-bit --config /var/vc/fluent-bit.conf --verbose
