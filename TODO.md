# AIMA Haskell ToDo list

## General

- Complete reorganization. Do we want to separate:
  - core modules
  - interactivity (e.g. playing games)
  - research (e.g. collecting statistics)
  - examples
- Improve Haddock documentation, including section headings.
- Use either System.TimeIt or Criterion for timing calculations.
- Keep making improvements to ProbDist module (or use the PFP module?)

## Utils

- Extensions to table-generating code. For example:
  - Write tables to arbitrary handles.
  - More customisable table layout.
  - Use an external library?
- Improve queueing module to use a more efficient data structure for priority queues.
- Rewrite the Util.Array module to actually use arrays!
- Organize Utils module into subsections.

## Search

- Informed/uninformed search
  - More statistics, e.g. time taken.
  - Is it possible to structure backtracking search as a monad?
  - Round out the search functions by including e.g. depth-limited graph search.
  - Fill in missing search functions from AIMA
  - Round effective branching factor to a sensible number of dps.
- Local search
  - Make changes to n-queens problem so that it can be used with simulatedAnnealingsearch.
  - Include genetic algorithm
- Adversarial Search
  - Alpha-beta search that orders nodes according to some heuristic before searching.
  - Stochastic games (using probability monad?)
  - Figure out why alpha/beta search sometimes makes stupid decisions while playingConnect 4.
- Constraint Satisfaction
  - Wrapper for CSP class to allow statistics to be collected.
  - Examples - word puzzles, scheduling, n queens?
- Examples
  - Use GraphViz to draw graph problems
  - Interactive stepping through a graph problem - highlight nodes as they are explored, keep track of running cost etc.
  - GUI for graph problems?
  - GUI for interactive playing of tic-tac-toe/connect 4?
  - Finish chess example
  - Other games, e.g checkers?

## Logic

- Propositional logic:
  - Truth-table SAT
  - Local search for SAT
  - Backward chaining
- First-order logic:
  - Backward chaining
  - Reduction to normal form

## Probability

- Flesh out functionality for MDPs.
- Partially observed MDPs
- Bayes Net uses lists rather than arrays to store the conditional probability table. This is probably inefficient - profile it and check!
- Markov chain (Gibbs sampling) routines for Bayes Net
- Function to compute children of a node in a Bayes Net
- Function to compute markov blanket of a node in a Bayes Net

## Learning

- More functions to auto-fit decision trees
- Decision tree demos are really slow - can they be optimized? In particular, computing the entropy for splits takes a long time.
- Cross validation should return average validation set error rate
- Handle continuous attributes
- Compute precision, recall and f-statistic
- Function to compare multiple classifiers
- More examples - test random forest vs. pruned decision trees
- Tests for linear/logistic regression and regularized regression
- LASSO
- Linear classifiers
- Naive Bayes