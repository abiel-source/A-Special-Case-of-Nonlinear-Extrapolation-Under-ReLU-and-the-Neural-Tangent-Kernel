**A Special Case of Nonlinear Extrapolation Under ReLU and the Neural Tangent Kernel**
[Click here to view the paper (PDF)](A_Special_Case_of_Nonlinear_Extrapolation_Under_ReLU_and_the_Neural_Tangent_Kernel.pdf)

*Author(s)*: Abiel J. Kim

*Date*: November 2025

*Keywords*: Machine Learning, Neural Network, Extrapolation, Neural Tangent Kernel, Pseudo-Inverse, Moore-Penrose Inverse, Asymptotic Analysis, Distributional Derivative, Tikhonov Regularization, Ridge Regression, Training Data, ReLU Activation, Squared Loss Error

**ABSTRACT**

It has been demonstrated both theoretically and empirically that the ReLU MLP tends to extrapolate linearly for an out-of-distribution evaluation point. The machine learning literature provides ample analysis with respect to the mechanisms to which linearity is induced. However, the analysis of extrapolation at the origin under the NTK regime remains a more unexplored special case. In particular, the infinite-dimensional feature map induced by the neural tangent kernel is not translationally invariant. This means that the study of an out-of-distribution evaluation point very far from the origin is not equivalent to the evaluation of a point very near the origin. And since the feature map is rotation invariant, these two special cases may represent the most canonically extreme bounds of ReLU NTK extrapolation. Ultimately, it is this loose recognition of the two special cases of extrapolation that motivate the discovery of quadratic extrapolation for an evaluation close to the origin.

**INTRODUCTION**

The work of Xu et al. [11] proves that an over-parameterized ReLU-activated multilayer perceptron (MLP) will extrapolate linearly when evaluated along any direction very distant from the origin. They formally prove extrapolative linearity by analysis of the learned regressor's functional form in the *neural tangent kernel* (NTK) *reproducing kernel hilbert space* (RKHS) [3]. And, since the infinite dimensional feature map induced by the neural tangent kernel is rotation invariant, the analysis covers the generalizable case of an evaluation point very distant from the origin. However, it is not difficult to recognize that the same feature map is not translation invariant. It is by a geometric reasoning that the origin of the RKHS must be a distinct special case whose analysis departs from Theorem 1 of Xu et al. [11]. That is, in the limit of a large relative distance between the training point set and the evaluation point, one observes that there must be two special locations of the evaluation point with respect to the NTK induced feature map: A location casted along a singular feature direction, and a location which intersects all feature directions.

It is this recognition of the distinguishable cases that motivates the extrapolative analysis at the origin location. The non translation invariance of the feature map implies that the extrapolative analysis at the origin and far from origin are not equivalent problems. It can be reasoned that they are two canonical cases of a more complete analysis of extrapolation. However, inducing extrapolation at the origin must be done carefully to ensure that the evaluation data is pushed out of the support of the training distribution space. This is achieved by this paper's definition of a labeled training set, which is formally presented in the problem setup of section 2. The desired effect of said definition is to induce a problem setup where all members of the training set are sent infinitely far away from the origin whilst fixing the evaluation data at the origin. Under this variant setting, we state Theorem 1, which discovers that an over-parameterized neural network extrapolates quadratically when evaluated near the origin. This finding contrasts, but does not conflict with, Xu et al. [11], which contrastingly concerns itself an evaluation point far from the origin.

The paper is organized as follows. The proof of Theorem 1 is presented in §A.4 and will depend on the results of Lemmas 1 and 2, which are proven with continuity in §A.2 and §A.3 respectively. Our problem setup induces a special case of the NTK gram matrix which must be studied in §A.1 to set the stage for the remainder of the mathematics.

**THEORETICAL CONTRIBUTIONS**

<img width="1868" height="520" alt="image" src="https://github.com/user-attachments/assets/f6f5ef7b-6577-4b06-8efa-de597345933d" />

> The closed-form of the asymptotic pseudo-inverse of the NTK gram matrix forms the basis of the manuscript and is induced from how I define the training set as being infinitely distant from the origin, along any direction

<img width="1842" height="160" alt="image" src="https://github.com/user-attachments/assets/741d4349-cce1-4363-98bf-d46a7412df1c" />

Theorem 1 Proof Sketch:
Theorem 1 is the main contribution of this paper and states that an extremely wide NTK predictor with ReLU activations that is trained on a dataset which is extremely distant from the origin will converge to a quadratic extrapolator when evaluated near the origin. That is, Theorem 1 states that the predictor's first and second directional derivatives exist and all higher-order derivatives are $0$. And the proof of Theorem 1, which is presented in §A.4, depends on the results of Lemmas 1 and 2. Lemma 1 is a generalized algebraic manipulation and states that the directional derivative of the NTK predictor can be expressed in terms of the derivatives of the indicator. The significance of Lemma 1 is most clear when we leverage the Dirac-delta's so-called sifting property, also known as the sampling property. We note that the derivative of the Heaviside indicator is the Dirac-delta, and applies itself nicely when viewing the predictor's derivative as an integral. Lemma 2 completes the second half of Theorem 1's proof by stating that the partial derivatives of the beta components with respect to the bias component of a feature direction $\mathbf{w}{d+1}$ are always $0$ for any order derivative past the second. The significance of Lemma 2 is clear when we see in §A.2 that the $z$-th derivative of the predictor depends on the $(z-1)$-th and $(z-2)$-th partial derivatives of the beta components. It is not difficult to see that the quadratic-order persists when taking the $z$-th derivative of $f{NTK}$.

<img width="1780" height="482" alt="image" src="https://github.com/user-attachments/assets/2b5f508d-7290-4d69-a78f-d8529afe48fa" />

[Click here to view the paper (PDF)](A_Special_Case_of_Nonlinear_Extrapolation_Under_ReLU_and_the_Neural_Tangent_Kernel.pdf)

> **Status:** This manuscript is a work in progress.
