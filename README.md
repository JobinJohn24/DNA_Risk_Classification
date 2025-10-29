# Secondary Structure Predictor: DNA Risk Classification via Knot Theory

This bioinformatics pipeline brings together knot theory and genomic analysis. It aims to classify synthetic DNA sequences based on their structural and biological risks. The setup relies on five complementary metrics. Those metrics offer a thorough risk assessment for use in genetic engineering projects.

## Overview

This project looks twenty diverse DNA sequences. They cover risk profiles from low to medium-high. It draws on knot invariants and biophysical properties to predict secondary structure formation. The approach mixes topological analysis with standard bioinformatics methods. In that way, it offers a fresh take on risk stratification for synthetic biology.

## Dataset Profile

- **Sequences Analyzed**: 20 diverse DNA sequences
- **Risk Distribution**: 35 low-risk, 27 medium-risk, 0 high-risk, 0 critical-risk
- **Structural Variety**: Simple repeats, GC-rich, hairpin-prone, inverted structures, triplex-forming, palindromic, complex topologies

## Five Core Metrics


## Results & Visualizations
### Test 1: GC Content Distribution
![Test 1: GC Content](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/test1_gc_content.png)
*Figure 1.1 - Represents the distribution of guanine-cytosine content in DNA structures.*
  
### Test 2: Melting Temperature Distribution
![Test 2: Melting Temperature](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/test2_tm_analysis.png)
*Figure 1.2 - Represents the temperature at which half of the hydrogen bonds of the double helix are broken and separated.*

### Test 3: Homopolymer vs Complexity
![Test 3: Homopolymer](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/test3_homopolymer.png)
*Figure 1.3 - Represents the comparisons between being long runs of the same nucleotide or a varied sequence.*

### Test 4: Shannon Entropy Distribution
![Test 4: Entropy](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/test4_entropy.png)
*Figure 1.4 - Represents how entropy valleys aligns with knots, risky hotspots, and fragile sites.*

### Test 5: Codon Usage Bias
![Test 5: Codon Bias](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/test5_codon_bias.png)
*Figure 1.5 - Represents the likelihood of synonymous condons are used, which indicate translational risk & evolutionary pressure.*

### Integrated Risk Assessment
![Risk Landscape](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/knot_risk_landscape.png)
*Figure 1.6 - Represents the overlaying map of stability, entropy, condon bias, and topology, which reveal genomic 'hotspots' of biological & structural risk.* 

![Risk Distribution](https://github.com/JobinJohn24/Secondary-Structure-Predictor/blob/main/analysis/risk_distribution.png)
*Figure 1.7 - Represents the distribution of clusters of high-risk regions versus broadly stable zones.*

## Results Interpretation

The five-metric approach worked well for stratifying things. It classified sequences right across the risk spectrum in an effective way. Topological features had a strong correlation. They showed high predictive value when it came to structural stability. The GC content sweet spot sits in the 50 to 60 percent range. That turns out optimal for applications in synthetic biology. Entropy plays a real role here. Sequences with lower entropy demonstrated significantly higher propensity for secondary structure. Codon choices matter too. The dominance of GAT and GAC points to considerations in design at the expression level.

## Quick Start

```bash
python main.py
```

## Technical Stack

- **Language**: Python 3.x
- **Libraries**: NumPy, Pandas, Matplotlib, Seaborn
- **Methods**: Knot invariant computation, thermodynamic modeling, statistical analysis

## Project Structure
```
secondary_structure_predictor/
├── config.py                      # Configuration & thresholds
├── knot_analyzer.py               # Knot theory calculations
├── bioinformatics_analyzer.py      # Metric computation
├── main.py                        # Pipeline orchestration
├── sequence_parser.py             # FASTA parsing
├── structure_predictor.py         # Secondary structure prediction
├── visualization.py               # Visualization generation
├── example_sequences.fasta         # Test data
├── requirements.txt               # Dependencies
├── README.md                      # This file
├── QUICKSTART.md                  # Quick reference
└── results/
    ├── test1_gc_content.png
    ├── test2_tm_analysis.png
    ├── test3_homopolymer.png
    ├── test4_entropy.png
    ├── test5_codon_bias.png
    ├── knot_risk_landscape.png
    ├── risk_distribution.png
    └── sequence_*.png             # 20 individual analyses
```
## Workflow
```
FASTA Input
    ↓
Parse DNA Sequences
    ↓
Extract Biophysical Metrics (GC, Tm, Homopolymers, Entropy, Codons)
    ↓
Analyze Topological Properties (Knot Theory)
    ↓
Predict Secondary Structure & Classify Risk
    ↓
Generate Visualizations (7 plots)
    ↓
Execute Pipeline & Generate Report
    ↓
20 Sequence Analyses + Comprehensive Visualizations + Summary Statistics
```
