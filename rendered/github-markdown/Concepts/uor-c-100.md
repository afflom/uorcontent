# Compression Metrics

The quantitative measures and evaluation criteria used to assess the performance and effectiveness of signal compression in the UOR framework.

## Definition

The effectiveness of UOR compression can be quantified using several metrics:

- Compression Ratio - The ratio of the original representation size to the compressed representation size
- Coherence Preservation - The degree to which essential structural relationships are maintained, measured by the coherence distance metric
- Semantic Fidelity - The preservation of semantic meaning and utility for downstream applications
- Computational Efficiency - The computational resources required to perform compression and decompression operations
- Cross-Domain Consistency - The consistency of compression performance across different types of signals and application domains

## Mathematical Formulation

$$
\text{UOR compression performance is evaluated using several key metrics:}
$$

$$
\text{1. Compression Ratio: Measures size reduction achieved:}
$$

$$
r = \frac{|\phi(S)|}{|\phi'(S)|} \quad \text{or} \quad r_{\text{percent}} = \left(1 - \frac{|\phi'(S)|}{|\phi(S)|} \right) \times 100\%
$$

$$
\text{2. Coherence Preservation: Quantifies structural integrity:}
$$

$$
C_p = 1 - \frac{d(\phi(S), \phi'(S))}{d_{\max}(S)}
$$

$$
\text{where } d_{\max}(S) \text{ is the maximum possible coherence distance for signal } S.
$$

$$
\text{3. Semantic Fidelity: Evaluates meaning preservation:}
$$

$$
F_s = \frac{1}{|\mathcal{F}|} \sum_{f \in \mathcal{F}} \left( 1 - \frac{|f(\phi(S)) - f(\phi'(S))|}{\Delta_f} \right)
$$

$$
\text{where } \mathcal{F} \text{ is the set of semantic features and } \Delta_f \text{ is the normalization factor.}
$$

$$
\text{4. Computational Efficiency: Measures computational resources required:}
$$

$$
E_c = \frac{T_{\text{original}}}{T_{\text{compressed}}} \quad \text{and} \quad E_s = \frac{M_{\text{original}}}{M_{\text{compressed}}}
$$

$$
\text{where } T \text{ and } M \text{ represent processing time and memory requirements.}
$$

$$
\text{5. Cross-Domain Consistency: Evaluates performance across domains:}
$$

$$
C_d = 1 - \frac{\sigma(\{r_i\})}{\mu(\{r_i\})}
$$

$$
\text{where } \{r_i\} \text{ is the set of compression ratios across domains, and}
$$

$$
\sigma \text{ and } \mu \text{ are the standard deviation and mean.}
$$

$$
\text{6. Rate-Distortion Performance: Assesses rate-distortion tradeoff:}
$$

$$
RD(\lambda) = \min_{\phi'} \{d(\phi(S), \phi') + \lambda|\phi'|\}
$$

$$
\text{where } \lambda \text{ is the rate-distortion parameter.}
$$

$$
\text{7. Compression-Decompression Accuracy: Measures reconstruction fidelity:}
$$

$$
A_{cd} = 1 - \frac{d(S, D(K(S)))}{d_{\max}(S, S_{\text{null}})}
$$

$$
\text{where } K \text{ is the compression operator, } D \text{ is the decompression operator,}
$$

$$
\text{and } d_{\max}(S, S_{\text{null}}) \text{ is the maximum possible distance between } S \text{ and a null signal.}
$$

## Related Concepts

- [compression-definition](./compression-definition.md)
- [coherence-norm](./coherence-norm.md)
- [information-preservation](./information-preservation.md)

## Metadata

- **ID:** urn:uor:concept:compression-metrics
- **Type:** concept
- **Code:** UOR-C-100
- **Related Concepts:**
  - [compression-definition](./compression-definition.md)
  - [coherence-norm](./coherence-norm.md)
  - [information-preservation](./information-preservation.md)
