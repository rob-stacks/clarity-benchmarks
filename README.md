# clarity-benchmarks

CLARITY_BENCHMARK=clarityN_YYYYMMDD.json CLARITY_BENCHMARK_ITERATIONS=1000 cargo test --lib --package clarity --features profiler -- vm::test::test_native_functions_benchmark --exact --nocapture --include-ignored
