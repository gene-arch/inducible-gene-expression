
# Inducible Gene Expression Model using Tellurium

This project simulates a simple **inducible gene circuit** using [Tellurium](http://tellurium.analogmachine.org/), a Python-based modeling environment for systems and synthetic biology.

---

## Project Overview

An inducible system allows gene expression to be turned **on or off** in the presence of an **inducer molecule**. These are common in natural and engineered systems and form the basis of many logic-based synthetic biology designs.

This model captures the following biological processes:
- Transcription of mRNA from DNA
- Translation of protein from mRNA
- Degradation of mRNA and protein
- Repression of transcription by a **repressor protein**
- Repressor binding with an **inducer**, forming a complex that prevents repression

---

## Biological Components

| Component | Description |
|----------|-------------|
| `DNA` | Contains the gene to be expressed |
| `mRNA` | Transcribed message from DNA |
| `Protein` | The final translated product |
| `Repressor` | Protein that inhibits transcription |
| `Inducer` | Small molecule that inactivates the repressor |
| `Complex` | Inducer-Repressor complex (inactive) |

---

## Model Reactions

```text
1. Inducer + Repressor -> Complex
2. DNA -> mRNA      (inhibited by Repressor)
3. mRNA -> Protein
4. mRNA degradation
5. Protein degradation
```

Transcription is modeled with **simple inhibition** logic:  
When `Repressor` concentration is high, transcription slows down.

---

## Output

The simulation produces time-course plots showing the concentrations of:
- mRNA
- Protein
- Inducer-Repressor Complex

These help visualize **system behavior over time** under the influence of the inducer.

---

## Technologies Used

- [Tellurium](http://tellurium.analogmachine.org/)
- [Python](https://www.python.org/)
- [Antimony](https://antimony.sourceforge.net/)
- [Jupyter Notebook](https://jupyter.org/)
- `matplotlib` for plotting results

---

## How to Run

1. **Install Tellurium** in a virtual environment:
   ```bash
   conda create -n synbio-env python=3.10
   conda activate synbio-env
   pip install tellurium
   ```

2. **Run the code** using Jupyter Notebook or directly in Python:
   ```bash
   jupyter notebook
   ```

3. Open the `.ipynb` file and run the simulation cells.

---

## Files Included

- `inducible_gene_expression.ipynb` -> Simulation notebook
- `README.md` -> This documentation
- `requirements.txt`

---

## Author Notes

This is a **learning project** built before the start of formal undergraduate studies, as part of my preparation for a future career in **synthetic biology and genetic circuit design**. It forms part of a growing collection of small, focused models to build intuition in modeling and simulation.

---

## References

- *Engineering Genetic Circuits*, University of Colorado Boulder, Coursera
- Alon, U. (2006). *An Introduction to Systems Biology*. Chapman & Hall/CRC.
- [Tellurium Documentation](https://tellurium.readthedocs.io/)
- [SBOL Visual](https://sbolstandard.org/visual/)

---

> This project is part of a personal initiative to build **mini synthetic biology models** before formal coursework begins.
