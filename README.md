Implementation of algorithm to efficiently verify QCSAT instance with s total Quantum gates, of which t are T-gates and the rest are Clifford gates. We aim to demonstrate the paper's theoretical result of exponential runtime scaling only in the number of T-gates.


**Step 1: Compute Sum of Paulis**
* Methodology:
    - Construct circuit of the form $\bra{0^m}U^{\dagger}ZU\ket{0^m}$, where $U$ is our QCSAT instance
        * We want to find minimum eigenvalues of the above operator
    - Convert this quantum circuit into a tensor network
        * Deciding between Google's tensornetwork framework vs Xanadu's quantum-jet framework for 
        quantum circuit simulation using tensor networks (leaning towards latter)
    - Contract tensor network (functionality built into both frameworks) so what we should be left with is tensor representing our sum of Paulis
    - Extracting out sum of Paulis from contracted tensor (trying to figure this out)

**Step 2: Perform Optimal Basis Change of Paulis**
