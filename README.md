# Brane in outgoing AdS5–Vaidya: junction-closure cross-check

Independent verification notebook (symbolic + numerical). **It does not claim new physics.** The energy-exchange law
for a Z2 FRW brane with bulk matter is known (e.g. Apostolopoulos & Tetradis, hep-th/0412246, Eq. 29). The notebook checks, with explicit
conventions, that the Vaidya source, the brane embedding, both Israel equations and the Codazzi projection are mutually consistent, and that the
exchange current is

    Q = -3 mu'(u) udot^2 / (kappa^2 a^3)      [= -3 mu' L^2 / (kappa^2 a^5 (1 + rho/lambda + H L)^2) for RS-tuned branes]

A version without the udot^2 factor fails the independent acceleration equation (≈27% relative residual in the included test).

## Run it

```bash
python -m venv .venv
# Windows:  .venv\Scripts\activate        macOS/Linux:  source .venv/bin/activate
pip install -r requirements.txt
jupyter lab brane_outgoing_vaidya_junction_check.ipynb      # run all cells (about 5-10 s)
# or, non-interactively:
jupyter nbconvert --to notebook --execute --inplace brane_outgoing_vaidya_junction_check.ipynb
```

Expected key outputs: all symbolic checks `True`; residual ≈ 1e-14 (correct Q), ≈ 2.7e-1 (no udot^2), ≈ 2.6e-3 (half Q).

## Status and limits
Not established here: novelty vs. the braneworld literature; the physical origin of mu(u) (an outgoing positive-energy flux extended to the
horizon is white-hole-like; evaporation needs ingoing negative-energy flux near the horizon, Hiscock-type); asymmetric (non-Z2) branes; stability.

## Authorship and AI-assistance statement
[AUTHOR NAME] ran and checked this notebook on [DATE] ([OS / Python version]). It was drafted with the assistance of an AI assistant (Perplexity);
the author is responsible for the content. [State what you personally verified.]

## Cite
See `CITATION.cff`. DOI: [add after the first Zenodo release].
