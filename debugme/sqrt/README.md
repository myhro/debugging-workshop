
This program returns the square root of a number you provide via the command
line. It is supposed to work on negative numbers but it crashes for some
reason. Can you find out why?

<details>
  <summary>Hint</summary>

  Try setting a breakpoint before the panic happens, then `restart` and
  `continue` to the breakpoint. You can then step through the program with
  `next` and inspect state with `print`.
</details>

<details>
  <summary>Solution</summary>

  The variable `r` inside the `sqrt` function is being shadowed by an
  additional declaration in the negative case. We should use the assignment
  operator `=` vs the declare and assign operator `:=` on line 52.
</details>
