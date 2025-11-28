# Pricing Turbo Options on Bitcoin

A portfolio-ready analysis notebook that prices deep-in-the-money barrier ("turbo") options on Bitcoin and explores Greek behavior across models. The project mixes practical market data ingestion with multiple option pricing engines.

## Repository contents
- `IEDA_4331_PROJECT_BARRIER.ipynb`: Colab-friendly research notebook containing data ingestion, pricing functions, experiments, and validation checks.
- `Turbo - Options Crypto.docx`: Supporting write-up/notes for the project (for reference alongside the notebook).

## Project highlights recruiters care about
- **Real market data**: Pulls BTC price history from Yahoo Finance and computes annualized log-return volatility to drive scenarios.
- **Multiple pricing engines**: Implements Black-Scholes closed-form formulas plus binomial and trinomial tree pricers for European and American-style options.
- **Barrier/turbo coverage**: Extends the trees to handle barrier-style turbo structures and runs parity/convergence checks to benchmark accuracy.
- **Model validation**: Includes convergence sweeps, put-call parity tests, and accuracy comparisons against vanilla prices to show rigor.

## Quick start
1. **Set up a virtual environment (recommended):**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows use .venv\Scripts\activate
   ```
2. **Install dependencies:**
   ```bash
   pip install yfinance numpy pandas scipy matplotlib seaborn
   ```
3. **Run the notebook locally:**
   ```bash
   jupyter notebook IEDA_4331_PROJECT_BARRIER.ipynb
   ```
   Or click the "Open in Colab" badge at the top of the notebook to run it in the cloud.


## Next steps
- Add parameterized widgets (e.g., `ipywidgets`) for interactive scenario analysis or demos.
- Export selected experiments as static plots for a short portfolio PDF or slide deck.
- Package core pricers into a lightweight module for reuse in other crypto derivatives analyses.
