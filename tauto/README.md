# Tauto Tactic

The `tauto` tactic in [tauto.mm1](https://github.com/GinoGiotto/mm1_tactics/blob/main/tauto/tauto.mm1) proves statements of classical propositional logic. It supports all primary propositional operators used in set.mm:

| Symbol | Meaning                               |
| -------- | ------------------------------------- |
| `->`     | Material implication                  |
| `~`      | Logical negation                      |
| `/\`     | Logical conjunction                   |
| `\/`     | Logical disjunction                   |
| `<->`    | Logical equivalence                   |
| `-/\`    | Alternative denial (NAND)             |
| `-\/`    | Joint denial (NOR)                    |
| `\/_`    | Exclusive disjunction (XOR)           |
| `T.`     | Constant true                         |
| `F.`     | Constant false                        |
| `ifp`    | Conditional operator for propositions |
| `had`    | Full-adder sum                        |
| `cad`    | Full-adder carry                      |

Goal theorems can be of arbitrary shape and size, provided they are propositional tautologies. Definitions should not be edited, as the tactic depends on their chosen definiens. Rules of inferences are currently not supported.

Proofs and specifications have been verified as follows:
<pre>
mm0-rs compile -W tauto.mm1 tauto.mmb
mm0-c tauto.mmb < tauto.mm0 
</pre>

No warnings or errors should appear.
