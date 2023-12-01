---
title: GMS
description: API reference for qiskit.circuit.library.GMS
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.library.GMS
---

# GMS

<span id="qiskit.circuit.library.GMS" />

`GMS(num_qubits, theta)`

Bases: [`qiskit.circuit.quantumcircuit.QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.quantumcircuit.QuantumCircuit")

Global Mølmer–Sørensen gate.

**Circuit symbol:**

```python
     ┌───────────┐
q_0: ┤0          ├
     │           │
q_1: ┤1   GMS    ├
     │           │
q_2: ┤2          ├
     └───────────┘
```

**Expanded Circuit:**

The Mølmer–Sørensen gate is native to ion-trap systems. The global MS can be applied to multiple ions to entangle multiple qubits simultaneously \[1].

In the two-qubit case, this is equivalent to an XX(theta) interaction, and is thus reduced to the RXXGate. The global MS gate is a sum of XX interactions on all pairs \[2].

$$
GMS(\chi_{12}, \chi_{13}, ..., \chi_{n-1 n}) =
exp(-i \sum_{i=1}^{n} \sum_{j=i+1}^{n} X{\otimes}X \frac{\chi_{ij}}{2})
$$

**References:**

\[1] Sørensen, A. and Mølmer, K., Multi-particle entanglement of hot trapped ions. Physical Review Letters. 82 (9): 1835–1838. [arXiv:9810040](https://arxiv.org/abs/quant-ph/9810040)

\[2] Maslov, D. and Nam, Y., Use of global interactions in efficient quantum circuit constructions. New Journal of Physics, 20(3), p.033018. [arXiv:1707.06356](https://arxiv.org/abs/1707.06356)

Create a new Global Mølmer–Sørensen (GMS) gate.

**Parameters**

*   **num\_qubits** (`int`) – width of gate.
*   **theta** (`Union`\[`List`\[`List`\[`float`]], `ndarray`]) – a num\_qubits x num\_qubits symmetric matrix of interaction angles for each qubit pair. The upper triangle is considered.

## Attributes

<span id="qiskit.circuit.library.GMS.ancillas" />

### ancillas

Returns a list of ancilla bits in the order that the registers were added.

**Return type**

`List`\[[`AncillaQubit`](qiskit.circuit.AncillaQubit "qiskit.circuit.quantumregister.AncillaQubit")]

<span id="qiskit.circuit.library.GMS.calibrations" />

### calibrations

Return calibration dictionary.

**The custom pulse definition of a given gate is of the form**

\{‘gate\_name’: \{(qubits, params): schedule}}

**Return type**

`dict`

<span id="qiskit.circuit.library.GMS.clbits" />

### clbits

Returns a list of classical bits in the order that the registers were added.

**Return type**

`List`\[[`Clbit`](qiskit.circuit.Clbit "qiskit.circuit.classicalregister.Clbit")]

<span id="qiskit.circuit.library.GMS.data" />

### data

Return the circuit data (instructions and context).

**Returns**

a list-like object containing the [`CircuitInstruction`](qiskit.circuit.CircuitInstruction "qiskit.circuit.CircuitInstruction")s for each instruction.

**Return type**

QuantumCircuitData

<span id="qiskit.circuit.library.GMS.extension_lib" />

### extension\_lib

`= 'include "qelib1.inc";'`

<span id="qiskit.circuit.library.GMS.global_phase" />

### global\_phase

Return the global phase of the circuit in radians.

**Return type**

`Union`\[[`ParameterExpression`](qiskit.circuit.ParameterExpression "qiskit.circuit.parameterexpression.ParameterExpression"), `float`]

<span id="qiskit.circuit.library.GMS.header" />

### header

`= 'OPENQASM 2.0;'`

<span id="qiskit.circuit.library.GMS.instances" />

### instances

`= 87`

<span id="qiskit.circuit.library.GMS.metadata" />

### metadata

The user provided metadata associated with the circuit

The metadata for the circuit is a user provided `dict` of metadata for the circuit. It will not be used to influence the execution or operation of the circuit, but it is expected to be passed between all transforms of the circuit (ie transpilation) and that providers will associate any circuit metadata with the results it returns from execution of that circuit.

**Return type**

`dict`

<span id="qiskit.circuit.library.GMS.num_ancillas" />

### num\_ancillas

Return the number of ancilla qubits.

**Return type**

`int`

<span id="qiskit.circuit.library.GMS.num_clbits" />

### num\_clbits

Return number of classical bits.

**Return type**

`int`

<span id="qiskit.circuit.library.GMS.num_parameters" />

### num\_parameters

Convenience function to get the number of parameter objects in the circuit.

**Return type**

`int`

<span id="qiskit.circuit.library.GMS.num_qubits" />

### num\_qubits

Return number of qubits.

**Return type**

`int`

<span id="qiskit.circuit.library.GMS.op_start_times" />

### op\_start\_times

Return a list of operation start times.

This attribute is enabled once one of scheduling analysis passes runs on the quantum circuit.

**Return type**

`List`\[`int`]

**Returns**

List of integers representing instruction start times. The index corresponds to the index of instruction in `QuantumCircuit.data`.

**Raises**

**AttributeError** – When circuit is not scheduled.

<span id="qiskit.circuit.library.GMS.parameters" />

### parameters

Convenience function to get the parameters defined in the parameter table.

**Return type**

`ParameterView`

<span id="qiskit.circuit.library.GMS.prefix" />

### prefix

`= 'circuit'`

<span id="qiskit.circuit.library.GMS.qubits" />

### qubits

Returns a list of quantum bits in the order that the registers were added.

**Return type**

`List`\[[`Qubit`](qiskit.circuit.Qubit "qiskit.circuit.quantumregister.Qubit")]
