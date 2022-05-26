Implementation of algorithm to efficiently verify QCSAT instance with s total Quantum gates, of which t are T-gates and the rest are Clifford gates. We aim to demonstrate the paper's theoretical result of exponential runtime scaling only in the number of T-gates.


**Step 1: Compute Sum of Paulis**
* Methodology:
    - Construct circuit of the form $\bra{0^m}U^{\dag}ZU\ket{0^m}$

**Step 2: Perform Optimal Basis Change of Paulis**
