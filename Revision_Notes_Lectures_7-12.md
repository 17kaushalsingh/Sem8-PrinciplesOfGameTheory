# Game Theory Revision Notes
## Lectures 7-12

---

## PART IV: EXPECTED UTILITY THEORY (Class 7a)

### Decision-Making Under Uncertainty: Continuous Outcomes
- **One action → many outcomes** when outcomes are random variables.
- **Discrete outcomes**: assign a probability to each outcome.
- **Continuous outcomes**: outcomes lie on an interval; probability at a single point is **0**; use **CDF/PDF** to assign probabilities to ranges.

### Lotteries and Notation (Continuous)
- A **simple lottery** over an interval is defined by a **CDF** `F(x)`.
- **CDF**: `F(x) = P(X ≤ x)` (cumulative probability up to `x`).
- **PDF**: `f(x) = F'(x)` when differentiable.
- **Probability of a range**: `P(a ≤ X ≤ b) = ∫_a^b f(x) dx`.

### Expected Payoff (Continuous)
- **Expected payoff** is a probability-weighted average across a continuum.
- **Formula**: `E[u(X)] = ∫_a^b u(x) f(x) dx`.
- **Intuition**: sum of payoffs × probabilities becomes an **integral** for continuous outcomes.

### CDF–PDF Analogy (from slides)
- **CDF** = cumulative probability mass up to a point.
- **PDF** = slope of CDF; higher slope means higher density in that range.
- **Area under PDF** over a range equals probability of that range.

### Common Continuous Distributions (Concepts)
- **Uniform**: equal density on `[a,b]`, zero outside.
- **Triangular**: peak at a value; linear rise and fall to endpoints.
- **Normal**: bell-shaped, centered at mean; symmetric, unbounded support.

### Random Variables Summary
- **Random variable**: chance-determined variable with possible values and associated probabilities.
- **Discrete RV**: probability distribution over countable outcomes; expected value is weighted average.
- **Continuous RV**: defined by CDF/PDF; expected value computed via integration.

---

## PART V: DECISIONS OVER TIME (Classes 7b-8)

### Sequential Decision-Making
- **Multiple decisions in sequence** (not simultaneous).
- Earlier decisions depend on expectations about later decisions.
- **Forward reasoning fails** when future choices are unknown.

### Game Trees
- **Decision nodes**: player chooses an action.
- **Chance (Nature) nodes**: outcome chosen by probability distribution.
- **Terminal nodes**: payoffs are assigned only at the end of the tree.

### Backward Induction
- **Principle**: solve from the end of the tree backward.
- Compare payoffs at **terminal nodes**, infer optimal action at the preceding decision node, then step backward.
- Requires **common knowledge of rationality**.

### Example: Ten Cannibals (Eat or Be Eaten)
- Cannibals move in order; if one eats, he sleeps and can be eaten next.
- **Backward induction** produces an eat / don’t eat pattern that resolves who eats Mr. Snack.
- Core lesson: **later decisions discipline earlier choices**, and assumptions about future choices must be derived from rationality, not guesses.

### Decision Trees with Nature
- **Player nodes**: choose the best available action (max payoff).
- **Nature nodes**: outcomes realized by probability (expected payoff).
- A rational player maximizes expected payoff at their own nodes.

---

## PART VI: NORMAL-FORM REPRESENTATION (Classes 9-12)

### From Decision Problems to Games
- **Decision problem**: outcomes depend on one player’s action.
- **Game**: outcomes depend on **action profiles** (actions of all players).
- **Action profile**: ordered tuple of actions, one per player.
- **Payoff profile**: vector of payoffs resulting from an action profile.
- **Strategic interdependence**: no single player can choose the outcome alone.

### Static Games of Complete Information
- **Static**: one move per player, chosen simultaneously.
- **Complete information**: all players know actions, outcomes, payoffs, and rationality.
- **Common knowledge**: everyone knows, everyone knows that everyone knows, etc.

### Pure Strategies
- **Pure strategy**: deterministic plan of action.
- In static games: strategy = action.
- In dynamic games: strategy specifies actions at every possible decision node.
- **Strategy profile**: one pure strategy chosen by each player.

### Normal-Form Game (Formal Definition)
A normal-form game consists of:
1. A finite set of players `N`.
2. Strategy sets `S_i` for each player `i`.
3. Payoff functions `u_i(s)` for each player over strategy profiles `s ∈ S`.

### Matrix Representation (Two-Player Finite Games)
- Rows = Player 1 strategies.
- Columns = Player 2 strategies.
- Each cell contains payoff pair `(u1, u2)`.
- Useful for compactly showing **all action profiles and payoffs**.

---

## Canonical Games (Discrete Strategies)

### Prisoner’s Dilemma
- Each player prefers to defect regardless of the other’s choice (dominant strategy).
- **Mutual defection** is the outcome even though both prefer mutual cooperation.
- Examples: restaurant bill split, duopoly pricing, joint project effort.

### Battle of the Sexes
- Players want to coordinate but disagree on which coordinated outcome is best.
- **Two coordination equilibria**; disagreement is the worst outcome.
- Examples: Alex & Chris (opera vs football), unified political stance, technology integration.

### Matching Pennies
- Strictly competitive **zero-sum** game.
- One player prefers matching, the other prefers mismatching.
- **No pure-strategy solution** → motivates mixed strategies later.

### Stag Hunt
- Cooperation yields highest payoff if all cooperate.
- Defection is safer if trust is low.
- **Beliefs matter**: lack of trust can lead to hunting hare.
- Contrast with Prisoner’s Dilemma: defection here is **risk-driven**, not temptation-driven.

---

## Economic Models of Competition (Continuous Strategies)

### Monopoly vs Duopoly
- **Monopoly**: single firm chooses price or quantity; market sets the other.
- **Duopoly**: two firms choose; outcomes depend on both decisions.

### Cournot Competition (Quantity Choice)
- Firms choose quantities simultaneously.
- Market price determined by total quantity (demand curve).
- Profits depend on both firms’ outputs.
- **Static and rigid**: hard to change quantities quickly.

### Bertrand Competition (Price Choice)
- Firms set prices simultaneously.
- Market demand allocates sales to the **lower-price** firm.
- Quantities adjust based on price competition.
- **Flexible**: prices can change quickly.

### Strategy Spaces
- **Finite games**: discrete strategy sets → matrix form.
- **Continuous games**: strategies are intervals; require calculus-based analysis.

---

## Key Formulas Summary

| Concept | Formula |
|---------|---------|
| CDF | `F(x) = P(X ≤ x)` |
| PDF | `f(x) = F'(x)` |
| Continuous Expected Payoff | `E[u(X)] = ∫_a^b u(x) f(x) dx` |
| Probability of a range | `P(a ≤ X ≤ b) = ∫_a^b f(x) dx` |

---

*Last Updated: February 2026*
