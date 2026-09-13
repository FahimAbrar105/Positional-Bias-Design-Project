# Positional Bias Design Project

## Overview

The **Positional Bias Design Project** investigates how the ordering and position of questionnaire items influence Large Language Model (LLM) responses. The project evaluates whether changing item positions affects model-generated measurements across psychological, moral, and political assessment frameworks.

The study uses controlled experiments where the same instruments are presented under different ordering conditions to measure position-dependent response variations.

## Research Objective

The primary objective is to analyze whether item placement introduces systematic bias in AI-generated responses and to evaluate the reliability of LLM-based assessments under different presentation structures.

The project focuses on:

- Measuring response changes caused by item ordering.
- Evaluating consistency across different instrument formats.
- Identifying potential positional effects in AI-based psychological and political measurements.

## Methodology

All instruments follow a unified experimental pipeline:

1. **Item Ordering**
   - Baseline published order.
   - Full item shuffle.
   - Full item reversal.

   Item ordering is the main experimental variable used to test positional bias.

2. **Prompt Construction**
   - Standardized instructions define the response scale and required format.
   - Items are displayed with sequential numbering to prevent models from identifying internal item information.

3. **Model Query and Response Repair**
   - The model response is collected automatically.
   - Missing responses are detected and repaired through follow-up prompts.

4. **Response Parsing**
   - Generated responses are extracted and validated.
   - Only valid numerical responses within the instrument scale range are accepted.

5. **Scoring**
   - Responses are converted into instrument-specific scores using appropriate scoring methods, including reverse coding where required.

## Evaluated Instruments

The project evaluates positional bias across six assessment frameworks:

### 1. Big Five Inventory (BFI-44)
Measures five major personality dimensions:

- Extraversion
- Agreeableness
- Conscientiousness
- Neuroticism
- Openness

### 2. Short Dark Triad (SD3)
Evaluates three dark personality traits:

- Machiavellianism
- Narcissism
- Psychopathy

### 3. Moral Foundations Questionnaire (MFQ-30)
Measures moral preferences across:

- Harm/Care
- Fairness
- Loyalty
- Authority
- Purity

### 4. Moral Foundations Vignettes (MFV)
Evaluates moral judgment patterns using scenario-based measurements:

- Care
- Fairness
- Loyalty
- Authority
- Sanctity
- Liberty
- Social Norms

### 5. Self-Reported Political Dimensions (SRPD)
A custom instrument designed to measure:

- Political positions
- Salience and clarity of political views
- Contemporary political dimensions inspired by European political positioning frameworks

### 6. Political Compass Test
Evaluates political orientation through:

- Economic Left/Right dimension
- Social Libertarian/Authoritarian dimension

## Technology Stack

- Python
- Automated experiment pipeline
- Data processing and analysis tools
- Statistical evaluation methods
- Visualization frameworks

## Project Structure
├── app/
│ ├── core/
│ │ ├── engine.py
│ │ └── latin_square.py
│ │
│ └── instruments/
│ ├── bfi44.py
│ ├── sd3.py
│ ├── mfq30.py
│ ├── mfv.py
│ ├── srpd.py
│ └── political_compass.py
│
├── data/
├── results/
└── README.md


## Expected Outcome

This project provides a systematic framework for studying positional bias in LLM responses and helps understand how information ordering can influence AI-generated measurements.

The findings can contribute to improving the reliability, fairness, and robustness of AI evaluation methodologies.