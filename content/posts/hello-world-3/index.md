---
title: "Hello, world! 3"
category: "Development"
tag: "Hugo"
author: "breeze256"
date: "2025-01-22"
---

test


```
"hw.module"() ({
^bb0(%arg15: i1, %arg16: !seq.clock, %arg17: i1, %arg18: i64):
%32 = "hw.constant"() {value = true} : () -> i1
%33 = "hw.constant"() {value = 0 : i64} : () -> i64
%34 = "hw.constant"() {value = false} : () -> i1
%35 = "seq.firreg"(%39, %arg16, %arg17, %34) <{name = "working"}> {firrtl.random_init_start = 128 : ui64} : (i1, !seq.clock, i1, i1) -> i1
%36 = "comb.icmp"(%arg18, %33) <{predicate = 0 : i64, twoState}> : (i64, i64) -> i1
%37 = "comb.and"(%36, %35) <{twoState}> {sv.namehint = "done"} : (i1, i1) -> i1
%38 = "comb.xor"(%37, %32) <{twoState}> : (i1, i1) -> i1
%39 = "comb.mux"(%35, %38, %arg15) <{twoState}> {sv.namehint = "nworking"} : (i1, i1, i1) -> i1
%40 = "comb.xor"(%35, %32) <{twoState}> : (i1, i1) -> i1
"hw.output"(%40, %35) : (i1, i1) -> ()
}) {comment = "", module_type = !hw.modty<input in_valid : i1, input clk : !seq.clock, input rst : i1, input reg_smaller : i64, output in_ready : i1, output reg_working : i1>, parameters = [], per_port_attrs = [], result_locs = [#loc, #loc1], sym_name = "GCD_P0"} : () -> ()
"hw.module"() ({
^bb0(%arg10: i64, %arg11: i64, %arg12: !seq.clock, %arg13: i1, %arg14: i64):
%20 = "hw.constant"() {value = false} : () -> i1
%21 = "comb.concat"(%20, %31) : (i1, i64) -> i65
%22 = "comb.concat"(%20, %arg14) : (i1, i64) -> i65
%23 = "comb.sub"(%21, %22) <{twoState}> : (i65, i65) -> i65
%24 = "comb.concat"(%20, %arg10) : (i1, i64) -> i65
%25 = "comb.mux"(%arg13, %23, %24) <{twoState}> {sv.namehint = "na"} : (i1, i65, i65) -> i65
%26 = "comb.mux"(%arg13, %arg14, %arg11) <{twoState}> {sv.namehint = "nb"} : (i1, i64, i64) -> i64
%27 = "comb.concat"(%20, %26) : (i1, i64) -> i65
%28 = "comb.icmp"(%25, %27) <{predicate = 8 : i64, twoState}> : (i65, i65) -> i1
%29 = "comb.extract"(%25) <{lowBit = 0 : i32}> : (i65) -> i64
%30 = "comb.mux"(%28, %29, %26) {sv.namehint = "nlarger"} : (i1, i64, i64) -> i64
%31 = "seq.firreg"(%30, %arg12) <{name = "larger"}> {firrtl.random_init_start = 64 : ui64} : (i64, !seq.clock) -> i64
"hw.output"(%31, %31) : (i64, i64) -> ()
}) {comment = "", module_type = !hw.modty<input in_a : i64, input in_b : i64, input clk : !seq.clock, input reg_working : i1, input reg_smaller : i64, output out : i64, output reg_larger : i64>, parameters = [], per_port_attrs = [], result_locs = [#loc2, #loc1], sym_name = "GCD_P1"} : () -> ()
"hw.module"() ({
^bb0(%arg5: i64, %arg6: i64, %arg7: !seq.clock, %arg8: i1, %arg9: i64):
%3 = "hw.constant"() {value = 0 : i63} : () -> i63
%4 = "hw.constant"() {value = 0 : i64} : () -> i64
%5 = "hw.constant"() {value = false} : () -> i1
%6 = "seq.firreg"(%18, %arg7) <{name = "smaller"}> {firrtl.random_init_start = 0 : ui64} : (i64, !seq.clock) -> i64
%7 = "comb.icmp"(%6, %4) <{predicate = 0 : i64, twoState}> : (i64, i64) -> i1
%8 = "comb.and"(%7, %arg8) <{twoState}> {sv.namehint = "done"} : (i1, i1) -> i1
%9 = "comb.concat"(%5, %arg9) : (i1, i64) -> i65
%10 = "comb.concat"(%5, %6) : (i1, i64) -> i65
%11 = "comb.sub"(%9, %10) <{twoState}> : (i65, i65) -> i65
%12 = "comb.concat"(%5, %arg5) : (i1, i64) -> i65
%13 = "comb.mux"(%arg8, %11, %12) <{twoState}> {sv.namehint = "na"} : (i1, i65, i65) -> i65
%14 = "comb.mux"(%arg8, %6, %arg6) <{twoState}> {sv.namehint = "nb"} : (i1, i64, i64) -> i64
%15 = "comb.concat"(%5, %14) : (i1, i64) -> i65
%16 = "comb.icmp"(%13, %15) <{predicate = 8 : i64, twoState}> : (i65, i65) -> i1
%17 = "comb.extract"(%13) <{lowBit = 0 : i32}> : (i65) -> i64
%18 = "comb.mux"(%16, %14, %17) {sv.namehint = "nsmaller"} : (i1, i64, i64) -> i64
%19 = "comb.concat"(%3, %8) : (i63, i1) -> i64
"hw.output"(%19, %6) : (i64, i64) -> ()
}) {comment = "", module_type = !hw.modty<input in_a : i64, input in_b : i64, input clk : !seq.clock, input reg_working : i1, input reg_larger : i64, output out_valid : i64, output reg_smaller : i64>, parameters = [], per_port_attrs = [], result_locs = [#loc3, #loc1], sym_name = "GCD_P2"} : () -> ()
```