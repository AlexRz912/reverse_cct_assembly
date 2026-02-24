# Reverse CCT Assembly - Manual x86 Annotation

## Objective

Manually annotate C code with hypothetical x86 assembly to understand how compilers translate high-level code to low-level instructions.

## Challenge

Self-imposed exercise to:
- Understand assembly fundamentals (registers, stack, calling conventions)
- Trace how control flow (if/else, loops) becomes jumps and branches
- Learn function call mechanics and stack frame management
- Improve reverse engineering intuition

## Structure

`reverse_cct_assembly_guess.c` contains:
- **C code** from the Reverse CCT game main function : `https://github.com/AlexRz912/reverse_cct`
- **Inline assembly comments** showing hypothetical compiled output
- **Annotations** explaining memory access and control flow

Example:
```c
int previousAnswerCorrect = 1;
// mov dword ptr [ebp-4], 1
```

## Key Learning Areas

1. Function prologue/epilogue and stack frames
2. Local variable access via stack offsets
3. cdecl calling convention (arguments, return values)
4. Condition translation to jumps
5. Complex multi-condition logic evaluation

## Limitations

- Only covers `-O0` (no compiler optimizations)
- x86 32-bit architecture only
- Windows calling conventions
- Not validated against actual compiler output (PLEASE, this is MACHINE code, give me some time to sleep)

*An exercise in understanding the bridge between C and assembly.*
