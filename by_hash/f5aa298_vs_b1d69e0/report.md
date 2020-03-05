# Benchmark Report

## Job Properties

*Commit(s):* [TuringLang/Turing.jl@f5aa2986551f66ce7c57f282f5260031e375df01](https://github.com/TuringLang/Turing.jl/commit/f5aa2986551f66ce7c57f282f5260031e375df01) vs [TuringLang/Turing.jl@b1d69e0db225542c0370b6b8f171bfae33b82048](https://github.com/TuringLang/Turing.jl/commit/b1d69e0db225542c0370b6b8f171bfae33b82048)

*Triggered By:* [link](https://github.com/TuringLang/Turing.jl/pull/1146#issuecomment-595004588)

*Tag Predicate:* `ALL`

## Error

The build could not finish due to an error:

```
NanosoldierError: failed to run benchmarks against primary commit: failed process: Process(`/opt/hostedtoolcache/julia/1.3.1/x64/bin/julia --project -e 'using Pkg;
pkg"instantiate; add JSON GitHub DataFrames BenchmarkTools;"
Pkg.build(verbose=true)
push!(LOAD_PATH, joinpath(".", "benchmarks"))
using BenchmarkTools
using BenchmarkHelper
BenchmarkHelper.set_benchmark_info("f5aa2986551f66ce7c57f282f5260031e375df01_primary", "f5aa2986551f66ce7c57f282f5260031e375df01_primary")
for bm in BenchmarkHelper.benchmark_files()
    include(joinpath("benchmarks", bm))
end

benchmarks = BenchmarkHelper.BenchmarkSuite[@tagged(ALL)]
println("WARMING UP BENCHMARKS...")
warmup(benchmarks)

println("RUNNING BENCHMARKS...")
results = run(benchmarks; verbose=true)

println("SAVING RESULT...")
BenchmarkTools.save("/home/runner/test_workdir/tmpresults/data/f5aa2986551f66ce7c57f282f5260031e375df01_primary.json", results)

println("DONE!")

'`, ProcessExited(1)) [1]

Stacktrace:
 [1] pipeline_error at ./process.jl:525 [inlined]
 [2] #run#565(::Bool, ::typeof(run), ::Cmd) at ./process.jl:440
 [3] run at ./process.jl:438 [inlined]
 [4] execute_benchmarks!(::Nanosoldier.BenchmarkJob, ::Symbol) at /home/runner/work/Turing.jl/Turing.jl/Nanosoldier.jl/src/jobs/BenchmarkJob.jl:520
 [5] run(::Nanosoldier.BenchmarkJob) at /home/runner/work/Turing.jl/Turing.jl/Nanosoldier.jl/src/jobs/BenchmarkJob.jl:197
 [6] run_as_github_action(::Nanosoldier.Server) at /home/runner/work/Turing.jl/Turing.jl/Nanosoldier.jl/src/server.jl:113
 [7] top-level scope at /home/runner/work/Turing.jl/Turing.jl/Nanosoldier.jl/bin/turing_benchmark.jl:31
 [8] include at ./boot.jl:328 [inlined]
 [9] include_relative(::Module, ::String) at ./loading.jl:1105
 [10] include(::Module, ::String) at ./Base.jl:31
 [11] exec_options(::Base.JLOptions) at ./client.jl:287
 [12] _start() at ./client.jl:460
```

Check the logs folder in this directory for more detailed output.

