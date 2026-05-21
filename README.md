# conservation-mdps

A collection of Markov Decision Process (MDP) papers from the **conservation and environmental protection** domain, paired with their natural-language (NL) problem descriptions and corresponding **RDDL** code.

## What each entry contains

For each paper:

- **PDF** — the original paper that formulates a conservation problem as an MDP.
- **NL description** — a natural-language write-up of the MDP (states, actions, transitions, reward, horizon).
- **RDDL code** — split into:
  - `domain.rddl` — types, fluents, action schemas, transition dynamics, reward;
  - `instance.rddl` — objects, initial state, non-fluents, horizon, discount.

## Naming

Each entry lives in a directory named after the **problem**, in lowercase kebab-case — e.g. `wildfire-suppression/`, `tiger-poaching-patrol/`, `coral-reef-restoration/`. Pick a short, descriptive name; don't use the paper's citation key or arbitrary IDs.

## Layout

```
conservation-mdps/
├── <problem-name>/
│   ├── paper.pdf
│   ├── description.md
│   ├── domain.rddl
│   └── instance.rddl
└── ...
```

## Contributing

To add a paper, create a new `<problem-name>/` directory containing all four files (`paper.pdf`, `description.md`, `domain.rddl`, `instance.rddl`) following the layout above, then open a PR:

```bash
git clone https://github.com/<your-user>/conservation-mdps.git
cd conservation-mdps

# create the entry (use a short, descriptive kebab-case name)
mkdir <problem-name>
cp /path/to/paper.pdf       <problem-name>/paper.pdf
cp /path/to/description.md  <problem-name>/description.md
cp /path/to/domain.rddl     <problem-name>/domain.rddl
cp /path/to/instance.rddl   <problem-name>/instance.rddl

# commit and push on a new branch
git checkout -b add-<problem-name>
git add <problem-name>/
git commit -m "Add <problem-name>"
git push -u origin add-<problem-name>

# then open a pull request on GitHub
```
