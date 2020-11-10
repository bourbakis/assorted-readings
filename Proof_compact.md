**Proof.** We will show by contradiction. Suppose we cannot find such finite cover which means that for each finite $x_i$, $i=1,2,\cdots, n$, there exits an $x_{n+1}$ such that 
$$
x_i\notin \mathcal B_{\epsilon}(x_{n+1}).
$$
Given that we can construct an infinite sequence $\{x_n\}$ such that 
$$
(\ddagger)\qquad d(x_i,x_j)\geq\epsilon.
$$
for each $i\neq j$.

Since $X$ is sequentially compact, we can find a convergent subsequence $\{x_{n_k}\}$of $\{x_n\}$ which means that the subsequence $\{x_{n_k}\}$ is a Cauchy sequence. Then , there exits a $K\in\mathbb{N}$ such that
$$
d(x_{n_p},x_{n_q})<\epsilon
$$
whenever $p,q> K$.



It contradicts with $(\ddagger)$. Hence our assumption is problematic. Thus, we have shown that we can a finite $\mathcal B_{\epsilon}(x_i)$s which covers space $X$ if $X$ is sequentially compact.