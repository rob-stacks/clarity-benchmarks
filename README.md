# clarity-benchmarks

CLARITY_BENCHMARK=clarityN_YYYYMMDD.json CLARITY_BENCHMARK_ITERATIONS=1000 cargo test --lib --package clarity --features profiler -- vm::test::test_native_functions_benchmark --exact --nocapture --include-ignored

remember to patch clarity/Cargo.toml:

```
+profiler = ["perf-event2"]
+
+[target.'cfg(all(target_os = "linux", target_arch = "x86_64"))'.dependencies]
+perf-event2 = { version = "0.7.4", optional = true }
```
