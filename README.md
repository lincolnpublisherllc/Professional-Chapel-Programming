README (requested outside the ZIP)
What you’re getting

Chapter folders: chapter-01 to chapter-15, each holding the code referenced in that chapter.

Original filenames preserved: When the book specified a path or filename, I used it (e.g., libs/metrics/src/metrics.chpl, tools/version.sh, Dockerfile, Mason.toml, YAML for CI).

Guessed filenames: If the book showed code without a filename, I created snippet-N.ext with the right extension (.chpl, .sh, .yml, .toml, etc.) based on content.

Manifest: A CSV listing every extracted file with its chapter and line count is included at:

extracted_chapel_code/MANIFEST.csv inside the ZIP directory structure.

Quick structure preview

chapter-01/ — build scripts, version/manifest tooling, CI examples, SLURM script, Dockerfile, Mason.toml, minimal app and banner modules.

chapter-02/ — generics, params, constrained shapes, iterators (serial and leader/follower), custom reductions, policy records, analytics kernel suite skeleton (analytics/src/...), and demo bench app.

chapter-03/ — memory behavior examples (SoA/AoS patterns, task-local combine, FFI boundaries).

chapter-04/ — sparse domains, graph kernels (BFS layering, SpMV-style), top-K, sketches, quantiles.

chapter-05/ — façade modules, bounded queues, capability injection, versioning and deprecation examples.

chapter-06/ — forall/coforall/cobegin/begin patterns, sync/single/atomic, bounded buffers pipeline with live snapshots.

chapter-07/ — CSV/Parquet exporters (CLI-first), curl/FFI HTTP options, Postgres upsert jobs, containerized runners, object storage workflows.

chapter-08/ — validation schemas, retry/backoff with jitter, idempotency keys, redact utilities, graceful shutdown patterns.

chapter-09/ — Time.stopwatch timings, flamegraph/profiler shells, tuning checklists, parse+reduce optimization steps.

chapter-10/ — case study snippets, windowed reduce interfaces, test strategies.

chapter-11/ — domain kernels (stencils, Monte Carlo, imaging filters, compaction) and distributed scenarios.

chapter-12/ — distributed analytics service skeleton, multi-locale exchange, runbooks/metrics/health signals, CI promotion.

chapter-13/ — test pyramid harness, GitHub Actions workflows, doc coverage checks, repo scaffolding.

chapter-14/ — contribution hygiene, PR templates, CI additions, maintainer guidance.

chapter-15/ — forward roadmap snippets, 90-day mastery plan scaffolds.

How I parsed the book

I scanned the DOCX for chapter headers, then captured code under each chapter.

When the book showed a filename or path (like tools/build.sh, libs/io/src/io.chpl, scripts/run_ana.slurm), I used that.

Otherwise, I used heuristics to detect code blocks (shebangs, Chapel keywords like module, proc, record, shell constructs, Dockerfile and YAML keys) and saved them with guessed extensions.

Notes and tips

Duplicates: If a filename was repeated with different snippets, I suffixed them to avoid overwriting (e.g., _2, _3). Check the MANIFEST.csv to see all files and locations.

Line endings & encoding: UTF-8 with Unix line endings.

Rebuilding examples: Many examples reference Chapel 1.33+ and standard tools shown in Chapter 1. Start by reviewing:

chapter-01/Mason.toml

chapter-01/tools/build.sh

chapter-01/tools/version.sh

SLURM scripts in chapter-01/scripts/

CI YAML in chapter-01/ and chapter-13/

Analytics kernel suite: Look in chapter-02/analytics/src/ for the “core/iters/policy/kernels” layout demonstrated in the book.
