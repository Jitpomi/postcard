# Maintained compatibility branch

Base: upstream `postcard/v1.1.3`. All upstream source, history and licenses are retained.

Move default heapless buffers from 0.7 to 0.8 and use portable-atomic support. Serde wire encoding stays unchanged; heapless return values now use the maintained 0.8 public type. Preserve fixed-capacity APIs, allocation-free operation, feature names and overflow errors.

This is an explicit JITPOMI-maintained source branch, not a claim that upstream released this change. Applications must pin the reviewed commit. No advisory ignores, renamed copies of the obsolete dependencies, TLS bypasses or target filters are used.

Validation: `cargo test -p postcard --features use-std,experimental-derive && cargo test -p postcard --no-default-features` plus DogRS/Business integration and audit checks. On upstream release, verify the source/API and stored-format compatibility, rerun the same checks, and replace the source pin with the maintained registry release.
