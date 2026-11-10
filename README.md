# Discrete Walk-Jump Sampling

A study implementation of energy-based antibody sequence generation with
Langevin sampling and one-step denoising, based on
[Protein Discovery with Discrete Walk-Jump Sampling](https://arxiv.org/abs/2306.12360)
(Frey et al., 2023).

## Run

With Python and [uv](https://docs.astral.sh/uv/):

```sh
git clone https://github.com/stochi0/discrete-walk-jump-sampling.git
cd discrete-walk-jump-sampling
uv venv
uv pip install -r requirements.txt
uv run --no-project python main.py
```

The entrypoint trains the energy model and denoiser on synthetic, randomly
generated amino-acid sequences, then samples and plots results. It does not
reproduce the paper's biological dataset or demonstrate experimentally validated
antibodies. Settings live in [config.py](config.py), including `DATA`, `TRAINING`,
and `SAMPLING`.

## Implementation

- [models.py](models.py), [training.py](training.py): energy and denoising networks.
- [sampling.py](sampling.py): Langevin exploration and denoising.
- [evaluation.py](evaluation.py), [visualisations.py](visualisations.py): metrics and plots.
- [data_processing.py](data_processing.py): sequence preprocessing.

Cite the original paper for the method; the citation below identifies this implementation.

## Citation

<!-- BEGIN generated citations -->

```bibtex
@software{bodadeprojectdiscretewalkjumpsampling,
  author = {Bodade, Ayush},
  title = {{Discrete Walk-Jump Sampling}},
  url = {https://github.com/stochi0/discrete-walk-jump-sampling},
  note = {Software implementation; cite the original research separately. Specify the commit or version used.}
}
```

<!-- END generated citations -->
