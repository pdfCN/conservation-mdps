# conservation-mdps

A collection of Markov Decision Process (MDP) papers from the **conservation and environmental protection** domain, paired with their natural-language (NL) problem descriptions and corresponding **RDDL** code.

## What each entry contains

For each paper:

- **PDF** — the original paper that formulates a conservation problem as an MDP.
- **NL description** — a natural-language write-up of the MDP (states, actions, transitions, reward, horizon).
- **RDDL code** — split into:
  - `domain.rddl` — types, fluents, action schemas, transition dynamics, reward;
  - `instance.rddl` — objects, initial state, non-fluents, horizon, discount.

## Layout

```
conservation-mdps/
├── <paper-id>/
│   ├── paper.pdf
│   ├── description.md
│   ├── domain.rddl
│   └── instance.rddl
└── ...
```

## Contributing

To add a paper, open a PR that creates a new `<paper-id>/` directory containing all four files (`paper.pdf`, `description.md`, `domain.rddl`, `instance.rddl`) following the layout above.
