To reproduce the issue run `lake build` in the `reference-manual`
directory on macOS. The Lean compiler segfaults while building `Manual.lean`.

Here's the backtrace:
```
  * frame #0: 0x000000010c4b932c libleanshared.dylib`lean_mark_persistent + 148
    frame #1: 0x0000000101005fcc libLake_shared.dylib`initialize_Lake_DSL_Config + 488
    frame #2: 0x000000010c2e6238 libleanshared.dylib`lean_run_mod_init + 56
    frame #3: 0x000000010754efdc libleanshared.dylib`l_Array_forIn_x27Unsafe_loop___at_Lean_registerInitAttrUnsafe___spec__7 + 748
    frame #4: 0x0000000107552838 libleanshared.dylib`l_Lean_registerInitAttrUnsafe___lambda__3 + 380
    frame #5: 0x0000000107552cb0 libleanshared.dylib`l_Lean_registerInitAttrUnsafe___lambda__3___boxed + 76
    frame #6: 0x000000010c4c7690 libleanshared.dylib`lean_apply_3 + 1456
    frame #7: 0x00000001072eda24 libleanshared.dylib`l_Lean_registerParametricAttribute___rarg___lambda__1 + 36
    frame #8: 0x000000010c4c76f4 libleanshared.dylib`lean_apply_3 + 1556
    frame #9: 0x00000001095ca0c0 libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop + 3416
    frame #10: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #11: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #12: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #13: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #14: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #15: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #16: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #17: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #18: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #19: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #20: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #21: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #22: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #23: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #24: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #25: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #26: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #27: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #28: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #29: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #30: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #31: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #32: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #33: 0x00000001095c930c libleanshared.dylib`l___private_Lean_Environment_0__Lean_finalizePersistentExtensions_loop___lambda__1 + 84
    frame #34: 0x00000001095d4ff0 libleanshared.dylib`l_Lean_finalizeImport___lambda__2 + 36
    frame #35: 0x00000001095d6ce4 libleanshared.dylib`l_Lean_importModules___lambda__1___boxed + 124
    frame #36: 0x000000010c4c5804 libleanshared.dylib`lean_apply_2 + 896
    frame #37: 0x000000010c4c3c08 libleanshared.dylib`lean_apply_1 + 536
    frame #38: 0x000000010962a244 libleanshared.dylib`l_Lean_withImporting___rarg + 112
    frame #39: 0x00000001095d71f8 libleanshared.dylib`l_Lean_importModules___lambda__2___boxed + 176
    frame #40: 0x000000010c4c5844 libleanshared.dylib`lean_apply_2 + 960
    frame #41: 0x000000010c4c3c08 libleanshared.dylib`lean_apply_1 + 536
    frame #42: 0x000000010c0534f0 libleanshared.dylib`l_Lean_profileitIOUnsafe___rarg___lambda__1 + 24
    frame #43: 0x000000010c053760 libleanshared.dylib`l_Lean_profileitIOUnsafe___rarg___lambda__1___boxed + 20
    frame #44: 0x000000010c4c3bf4 libleanshared.dylib`lean_apply_1 + 516
    frame #45: 0x000000010c25c81c libleanshared.dylib`lean_profileit + 128
    frame #46: 0x000000010c053654 libleanshared.dylib`l_Lean_profileitIOUnsafe___rarg + 112
    frame #47: 0x00000001095d6f98 libleanshared.dylib`lean_import_modules + 372
    frame #48: 0x00000001082c3700 libleanshared.dylib`l_Lean_Elab_processHeader + 88
    frame #49: 0x00000001096750d0 libleanshared.dylib`l_Lean_Language_Lean_process_processHeader___lambda__5 + 360
    frame #50: 0x00000001096761e4 libleanshared.dylib`l_Lean_Language_Lean_process_processHeader___lambda__6___boxed + 20
    frame #51: 0x000000010c4c7814 libleanshared.dylib`lean_apply_3 + 1844
    frame #52: 0x000000010c4c5a68 libleanshared.dylib`lean_apply_2 + 1508
    frame #53: 0x0000000109650524 libleanshared.dylib`l___private_Lean_Language_Lean_0__Lean_Language_Lean_withHeaderExceptions___rarg + 80
    frame #54: 0x000000010c4c3f3c libleanshared.dylib`lean_apply_1 + 1356
    frame #55: 0x000000010c4dceec libleanshared.dylib`lean::lean_io_as_task_fn(lean_object*, lean_object*) + 24
    frame #56: 0x000000010c4c3e68 libleanshared.dylib`lean_apply_1 + 1144
    frame #57: 0x000000010c4c25e8 libleanshared.dylib`lean::task_manager::run_task(std::__1::unique_lock<std::__1::mutex>&, lean_task*) + 148
    frame #58: 0x000000010c4c3680 libleanshared.dylib`lean::task_manager::spawn_worker()::'lambda'()::operator()() const + 304
    frame #59: 0x000000010c4b5d80 libleanshared.dylib`lean::lthread::imp::_main(void*) + 56
    frame #60: 0x0000000180d8df94 libsystem_pthread.dylib`_pthread_start + 136
```


Any of the following changes make it disappear:
 1. Remove the `precompileModules` line from `lakefile.toml` in `verso`
 2. Remove either of the imports in `reference-manual/Manual.lean`
 3. Replace the toolchain with `leanprover/lean4:nightly-2025-02-26`
