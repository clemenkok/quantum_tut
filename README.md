161024 Tutorial

$$A = \Sigma_{xy}\ket{x}\bra{y} A_{xy}$$

So,

$$Z = \begin{bmatrix} 1&0\\0&-1\end{bmatrix}=1\cdot\ket{0}\bra{0}-1\ket{1}\bra{1}$$

$$X = \begin{bmatrix} 0&1\\1&0\end{bmatrix}=1\cdot\ket{0}\bra{1}-1\ket{1}\bra{0}$$

Inversion of order


$$U_1 \ket{\psi} \rightarrow U_2 U_1 \ket{\psi} = \alpha_2\ket{0} +\beta_2\ket{1}$$

$$e^{i\varphi}U_1 \ket{\psi} \rightarrow e^{i\varphi}U_2 U_1 \ket{\psi} = e^{i\varphi}\alpha_2\ket{0} +e^{i\varphi}\beta_2\ket{1}$$
Apply $e^{i\varphi}$ to $\ket{\psi}$ - $e^{i\varphi}$ will apply to $\alpha_2$ and $\beta_2$ 

Linear operations - phase can be pulled out. Not going to affect absolute values

Multiplying by a phase - generalised to $N$ qubits

Unitary preserves the norm

#### Control

$$C_{10}\ket{x_1x_0} \text{ (equivalent to } \ket{x_1}\otimes\ket{x_0} ) = \ket{x_1}\ket{x_0 \oplus x_1}$$
C subscript Control Target. $\oplus$ XOR

$$C_{10}\ket{10} = \ket{1}\ket{1}$$


$$C_{10} = \Sigma_{x,y \in \{ 00, 01, 10, 11\}} \mathcal{c}_{xy} \ket{x} \bra{y}$$

$$C_{10} \ket{00} = \Sigma_{xy} \mathcal{c}_{xy} \ket{x} \langle y|00 \rangle = \Sigma_x \mathcal{c}_{x, 00} \ket{x} = \ket{00}$$

$\mathcal{c}_{x,00} = \delta_{x,00}$



$$C_{10} \ket{01} = \Sigma_{xy} \mathcal{c}_{xy} \ket{x} \langle y|01 \rangle = \Sigma_x \mathcal{c}_{x, 01} \ket{x} = \ket{01}$$

$$C_{10} \ket{10} =  \Sigma_x \mathcal{c}_{x, 10} \ket{x} = \ket{11}$$

$$C_{10} \ket{11} =  \Sigma_x \mathcal{c}_{x, 11} \ket{x} = \ket{10}$$

- We can convert this to a matrix using $c_{x,11} = \delta_{x,10}$

So we get

$$\begin{bmatrix} 1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{bmatrix}$$

Ex 1 Test 1 020224

#### Exercises

##### 3.1.4
Given a qubit state in the Bloch sphere parametrisation, $\ket{\varphi} = cos\frac{\theta}{2} \ket{0} + sin \frac{\theta}{2}\ket{1}e^{i\varphi}$ compute the action of $X = \ket{0}\bra{1} + \ket{1} \bra{0}$ and $Z=\ket{0}\bra{0} - \ket{1} \bra{1}$ on the qubit and show what effect they have on the parameters $\theta, \varphi$ that parametrise a qubit in the Bloch sphere parametrisation.

$X$ is the Pauli-X Operator. It flips 1 to 0 and 0 to 1. Represented by a $180 \degree$ rotation on the X-axis of the Bloch sphere. $(\theta, \varphi) \rightarrow (\pi - \theta , \varphi)$

So, $X \ket{\varphi} = cos\frac{\theta}{2} \ket{1} + sin \frac{\theta}{2}\ket{0}e^{i\varphi}$

$Z$ is the Pauli-Z Operator. Phase shift on $\ket{1}$ but not $\ket{0}$. Represented by a $180\degree$ rotation on the Z-axis of the Bloch sphere. $(\theta, \varphi) \rightarrow (\theta , \varphi + \pi)$

$X \ket{\varphi} = cos\frac{\theta}{2} \ket{0} - sin \frac{\theta}{2}\ket{1}e^{i\varphi}$

##### 3.2.3
Compute the expected value of the random variable corresponding to the measurement on a qubit state $\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$. Show that if we relabel 0, 1 as 1, −1, this expected value equals $\langle \psi | Z | \psi \rangle$



##### 3.2.5 
Verify the output, up to a global phase, of the following quantum network.

##### 3.3.6
Compute the matrix corresponding to the CNOT gate C01 and compare against C10.

##### 3.3.8
Verify that $S_{01} = C_{01}C_{10}C_{01}$

##### 3.3.9
Introduced B = |1⟩ ⟨1| , B ̃ = 1 − B = |0⟩ ⟨0|, projectors

onto 1 and 0 bit, prove (i) BX = XB ̃

(ii) Sij = BiBj + B ̃iB ̃j + (XiXj)(BiB ̃j + B ̃iBj) (iii) Cij =B ̃i+XjBi

##### 3.3.10
Recalling the Hadamard gate H = √1 (X + Y ), prove 

$Cji = HiHjCijHiHj$

##### 3.3.11
Recalling the Pauli matrices X,Y,Z prove Sij = 21(1+

XiXj +YiYj +ZiZj).
