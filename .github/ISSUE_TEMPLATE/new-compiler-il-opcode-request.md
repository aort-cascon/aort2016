---
name: New compiler IL opcode request
about: Describe this issue template's purpose here.

---

## Proposed IL Opcode Name(s)

Provide the name for a single IL opcode, or list each opcode in a family of IL opcodes 

## Operation

Describe the semantics, structure, and operation of the new IL opcode.  You must include:

* overall operational semantics of the IL opcode
* number of children
* data type of opcode
* data type and semantics of each child
* existing IL opcode properties required
* new IL opcode properties required and their semantics
* will the node have a symbol reference?
* aliasing semantics
* whether it is capable of producing an exception
* describe any side effects

## Scope

* Will this opcode be useful in all projects that consume OMR?  If not, please justify.

* Will this opcode be useful on all code generator backends in OMR?  If not, please justify.

## Usage Restrictions

Describe any restrictions on the use of this IL opcode.  For example, it must only appear as a treetop, it must not be commoned, etc.

## Implementation Dependencies

Describe any implementation dependencies this IL opcode incurs.  For example, does this IL opcode:

* require special support to be implemented in one or more optimizations before it can be used?
* require all backends to implement it simultaneously?
* require special backend support (e.g., an out-of-line path to handle an exceptional case)?
* require implementation in all projects consuming OMR?
* require codegen lowering, and if so, to what trees?

## Testing Considerations

Describe how this proposed IL opcode will be tested in a project-independent manner that can be automated in Eclipse OMR CI builds.  If Tril unit tests cannot be provided, please justify and propose an alternative.

## IL Validation

Describe the checks that will be added to the IL validator to test this new IL opcode.
