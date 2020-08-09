# plum

**plum** is an umbrella library for various probabilistic data structures for rust :crab:.

Currently, it only contains a fast standard [bloom filter implementation](https://onatm.dev/2020/08/10/let-s-implement-a-bloom-filter/).

## Usage

```rust
use plum::{StandardBloomFilter};

let items_count = 1_000_000;
let fp_rate = 0.01;

let mut bloom = StandarBloomFilter::new(items_count, fp_rate);
bloom.insert("item1");
bloom.contains("item1"); /* true */
bloom.contains("item2"); /* false */
```

## Installation

```toml
[dependencies]
plum="0.1.0"
```

## Documentation

See [docs.rs/plum](https://docs.rs/plum)

## License

Licensed under MIT license ([LICENSE](LICENSE) or <http://opensource.org/licenses/MIT>)
