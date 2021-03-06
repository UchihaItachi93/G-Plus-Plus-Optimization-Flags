# G-Plus-Plus-Optimization-Flags
This is the repo where I will try to share whatever (little) knowledge I gain about the g++ optimization flags . There are four main flags or levels that we use for optimizatios ie -O0 , -O1 , -O2 , -O3 .


There are ways to check the optimization flags of each level in 
 `g++ -Q -O{level} --help=optimizers`
 example
 `g++ -Q -O1 --help=optimizers` 
 If you want to see a short description of each optimization flag 
 `g++ --help=optimizers`
 
 
The different optimizations on each level are as follows :

`
| FLAG                                  | O0       | O1       | O2       | O3       |
| ------------------------------------- | -------- | -------- | -------- | -------- |
| -faggressive-loop-optimizations       | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -falign-functions                     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -falign-jumps                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -falign-labels                        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -falign-loops                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fassociative-math                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fasynchronous-unwind-tables          | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fauto-inc-dec                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fbranch-count-reg                    | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fbranch-probabilities                | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fbranch-target-load-optimize         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fbranch-target-load-optimize2        | &#x274C; | &#x274C; | &#x274C; | &#x274C; |`
| -fbtr-bb-exclusive                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fcaller-saves                        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fcode-hoisting                       | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fcombine-stack-adjustments           | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fcompare-elim                        | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fconserve-stack                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fcprop-registers                     | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fcrossjumping                        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fcse-follow-jumps                    | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fcx-fortran-rules                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fcx-limited-range                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fdce                                 | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fdefer-pop                           | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fdelayed-branch                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fdelete-dead-exceptions              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fdelete-null-pointer-checks          | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fdevirtualize                        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fdevirtualize-speculatively          | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fdse                                 | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fearly-inlining                      | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fexceptions                          | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fexpensive-optimizations             | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -ffinite-math-only                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ffloat-store                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fforward-propagate                   | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ffp-int-builtin-inexact              | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ffunction-cse                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fgcse                                | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fgcse-after-reload                   | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fgcse-las                            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fgcse-lm                             | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fgcse-sm                             | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fgraphite                            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fgraphite-identity                   | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fguess-branch-probability            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fhoist-adjacent-loads                | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fif-conversion                       | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fif-conversion2                      | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -findirect-inlining                   | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -finline                              | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -finline-atomics                      | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -finline-functions                    | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -finline-functions-called-once        | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -finline-small-functions              | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-bit-cp                          | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-cp                              | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-cp-clone                        | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fipa-icf                             | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-icf-functions                   | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-icf-variables                   | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-profile                         | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fipa-pta                             | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fipa-pure-const                      | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fipa-ra                              | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-reference                       | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fipa-sra                             | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fipa-vrp                             | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fira-hoist-pressure                  | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fira-loop-pressure                   | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fira-share-save-slots                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fira-share-spill-slots               | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fisolate-erroneous-paths-attribute   | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fisolate-erroneous-paths-dereference | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fivopts                              | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fjump-tables                         | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fkeep-gc-roots-live                  | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -flifetime-dse                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -flimit-function-alignment            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -flive-range-shrinkage                | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -floop-nest-optimize                  | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -floop-parallelize-all                | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -flra-remat                           | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fmath-errno                          | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fmodulo-sched                        | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fmodulo-sched-allow-regmoves         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fmove-loop-invariants                | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fnon-call-exceptions                 | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fnothrow-opt                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fomit-frame-pointer                  | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fopt-info                            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -foptimize-sibling-calls              | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -foptimize-strlen                     | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fpack-struct                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fpartial-inlining                    | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fpeel-loops                          | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fpeephole                            | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fpeephole2                           | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fplt                                 | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fpredictive-commoning                | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fprefetch-loop-arrays                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fprintf-return-value                 | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -freciprocal-math                     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -freg-struct-return                   | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -frename-registers                    | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -freorder-blocks                      | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -freorder-blocks-and-partition        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -freorder-functions                   | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -frerun-cse-after-loop                | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -freschedule-modulo-scheduled-loops   | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -frounding-math                       | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -frtti                                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-critical-path-heuristic       | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-dep-count-heuristic           | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-group-heuristic               | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-interblock                    | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-last-insn-heuristic           | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-pressure                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsched-rank-heuristic                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-spec                          | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-spec-insn-heuristic           | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched-spec-load                     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsched-spec-load-dangerous           | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsched-stalled-insns                 | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsched-stalled-insns-dep             | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsched2-use-superblocks              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fschedule-fusion                     | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fschedule-insns                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fschedule-insns2                     | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fsection-anchors                     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsel-sched-pipelining                | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsel-sched-pipelining-outer-loops    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsel-sched-reschedule-pipelined      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fselective-scheduling                | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fselective-scheduling2               | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fshort-enums                         | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fshort-wchar                         | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fshrink-wrap                         | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fshrink-wrap-separate                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsignaling-nans                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsigned-zeros                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsingle-precision-constant           | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fsplit-ivs-in-unroller               | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fsplit-loops                         | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fsplit-paths                         | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -fsplit-wide-types                    | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fssa-backprop                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fssa-phiopt                          | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -fstack-clash-protection              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstack-protector                     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstack-protector-all                 | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstack-protector-explicit            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstack-protector-strong              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstdarg-opt                          | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fstore-merging                       | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fstrict-aliasing                     | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fstrict-enums                        | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fstrict-overflow                     | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fstrict-volatile-bitfields           | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fthread-jumps                        | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -fno-threadsafe-statics               | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftracer                              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ftrapping-math                       | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftrapv                               | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ftree-bit-ccp                        | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-builtin-call-dce               | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-ccp                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-ch                             | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-coalesce-vars                  | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-copy-prop                      | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-cselim                         | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-dce                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-dominator-opts                 | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-dse                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-forwprop                       | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-fre                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-loop-distribute-patterns       | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -ftree-loop-distribution              | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ftree-loop-if-convert                | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-loop-im                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-loop-ivcanon                   | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-loop-optimize                  | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-loop-vectorize                 | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -ftree-lrs                            | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ftree-partial-pre                    | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -ftree-phiprop                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-pre                            | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -ftree-pta                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-reassoc                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-scev-cprop                     | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-sink                           | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-slp-vectorize                  | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -ftree-slsr                           | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-sra                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-switch-conversion              | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -ftree-tail-merge                     | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -ftree-ter                            | &#x274C; | &#x2705; | &#x2705; | &#x2705; |
| -ftree-vectorize                      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -ftree-vrp                            | &#x274C; | &#x274C; | &#x2705; | &#x2705; |
| -funconstrained-commons               | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -funroll-all-loops                    | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -funroll-loops                        | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -funsafe-math-optimizations           | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -funswitch-loops                      | &#x274C; | &#x274C; | &#x274C; | &#x2705; |
| -funwind-tables                       | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fvar-tracking                        | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fvar-tracking-assignments            | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fvar-tracking-assignments-toggle     | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fvar-tracking-uninit                 | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fvariable-expansion-in-unroller      | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fvpt                                 | &#x274C; | &#x274C; | &#x274C; | &#x274C; |
| -fweb                                 | &#x2705; | &#x2705; | &#x2705; | &#x2705; |
| -fwrapv                               | &#x274C; | &#x274C; | &#x274C; | &#x274C; |


