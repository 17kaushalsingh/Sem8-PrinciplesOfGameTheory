# Game Theory Revision Notes
## Lectures 1-6

---

## PART I: INTRODUCTION TO GAME THEORY (Classes 1-2)

### What is Game Theory?
- **Game Theory** is the study of making decisions in strategic settings where the outcome depends not only on your own choices but also on the choices of others
- A **Game** is a mathematical model of a strategic interaction
- Distinct from single-person decision problems because outcomes depend on multiple participants

### Core Components of a Game
1. **Players** - The decision-makers (individuals, corporations, nation-states, etc.)
2. **Actions** - The choices available to each player
3. **Outcomes** - The results that depend on combinations of actions by all players
4. **Preferences/Payoffs** - How players rank outcomes

### The Jungle Treasure Game (Prisoner's Dilemma)
A classic example demonstrating strategic interaction:

**Setup:**
- Two players secretly choose either SHARE or TAKE
- Payoff Matrix:

|           | Friend: SHARE | Friend: TAKE |
|-----------|---------------|--------------|
| Me: SHARE | Half, Half    | Nothing, Whole |
| Me: TAKE  | Whole, Nothing | Quarter, Quarter |

**Key Insights:**
- **Strategic Thinking**: No matter what my friend selects, I get a better outcome by selecting TAKE (dominant strategy)
- **Suboptimal Outcome**: When both players think strategically, they end up at (TAKE, TAKE) = (Quarter, Quarter), which is worse for both than (SHARE, SHARE) = (Half, Half)
- This demonstrates the tension between individual rationality and collective welfare

### Why Select TAKE? (Strategic Reasoning)
1. Hoping for the best outcome (chance to get whole treasure)
2. Distrust of the other player
3. Short-term gain over cooperation
4. Fear of worst outcome (SHARE while friend TAKEs = Nothing)
5. **Dominant Strategy**: TAKE guarantees at least a quarter

### Why Select SHARE? (Behavioral Considerations)
1. Fairness - found treasure together
2. Trust in friendship
3. Social norms
4. Guilt avoidance

### Approaches to Resolve Suboptimal Outcomes
1. **Communication** - Talk and make a pact (but may not always work)
2. **Mechanism Design** - Change the payoffs/incentives
3. **Enforcement** - Binding contracts with third-party enforcement

### Types of Games
| Dimension | Types |
|-----------|-------|
| **Time** | Simultaneous (one-move) vs. Sequential moves |
| **Information** | Full knowledge vs. Uncertainty about preferences/actions |

---

## PART II: THE RATIONAL CHOICE PARADIGM (Classes 3-4)

### The Single-Person Decision Problem
Three components:
1. **Actions (A)** - All alternatives the player can choose from
2. **Outcomes (X)** - Possible consequences of actions
3. **Preferences** - How the player ranks outcomes

**Example**: Friday evening decision
- Actions: A = {Study (S), Play Games (G), Socialize with Friends (F)}
- Outcomes: X = {Better prepared for exam (s), Immediate relaxation (g), Build relationships (f)}
- Preference: s ≻ f ≻ g

### Preference Relations

| Notation | Meaning |
|----------|---------|
| x ≻ y | x is strictly preferred to y |
| x ≿ y | x is at least as good as y (weak preference) |
| x ~ y | Indifference between x and y |

### Axioms of Rational Preferences

**Axiom 1: Completeness**
- Any two outcomes x, y ∈ X can be ranked
- Either x ≿ y OR y ≿ x (or both, meaning indifference)
- The decision-maker is decisive (avoids Buridan's donkey paradox)

**Axiom 2: Transitivity**
- For any x, y, z ∈ X: if x ≿ y and y ≿ z, then x ≿ z
- No "loopy" preferences
- Rankings are consistent without contradictions

**Result**: A preference relation that is complete and transitive guarantees at least one best outcome exists.

### The Payoff Function

**Definition**: A function u(X) that assigns a number to each outcome such that outcomes with higher numbers are preferred.

u(x) ≥ u(y) if and only if x ≿ y

**Key Properties:**
- Provides a convenient, quantitative way to model preferences
- Payoffs can be compared within a person, NOT between people
- Same outcomes with different payoff numbers can represent the same preferences (ordinal nature)

**Example:**
| Preference | Possible Payoff Functions |
|------------|--------------------------|
| s ≻ f ≻ g | u(s)=10, u(f)=7, u(g)=3 |
| s ≻ f ≻ g | u(s)=97, u(f)=72, u(g)=31 |

### Action Spaces

**Discrete Action Spaces:**
- Finite number of distinct actions
- Example: A = {S, G, F}

**Continuous Action Spaces:**
- Infinitely many actions in a range
- Example: A = [0, 500] for "how much juice to drink"
- Notation: a ∈ [0, 500] means "a belongs to the set"

### Solving Continuous Decision Problems

**Example**: Optimal coffee consumption
- Action space: A = [0, 1] (liters)
- Payoff function: v(a) = 2a - 4a²
- Too little = sleepy, Too much = sick

**First-Order Condition (FOC):**
1. Set derivative to zero: d/da[2a - 4a²] = 0
2. Solve: 2 - 8a = 0 → a* = 0.25
3. Check second-order condition: d²/da² = -8 < 0 (confirms maximum)

### Decision Trees
A graphical approach to modeling decision problems:

**Components:**
- **Root/Decision Node** - Where decision-maker chooses
- **Branches** - Represent actions
- **Terminal Nodes** - Outcomes with associated payoffs

**Reading**: Left to right

### The Rational Player (Homo Economicus)

**Key Assumptions:**
1. **Rationality** - Chooses actions that maximize well-being based on payoff function
2. **All-knowing** - Understands the decision problem completely
3. **Self-interested** - Maximizes own payoff (not absolute selfishness)
4. **Predictable** - Given preferences, behavior is consistent

**Contrast: Homo Erraticus** (Irrational Man)
- Makes inconsistent choices
- Violates transitivity or completeness

### Cognitive Biases

**The Decoy Effect:**
- Introducing a third, less appealing option (decoy) can shift preferences between two original options
- Decoy is asymmetrically dominated - worse than one option in all aspects, partially worse than the other
- Used in marketing to push consumers toward a target product

**The Anchoring Effect:**
- Decisions heavily influenced by the first piece of information (anchor)
- Example: Real estate agent shows overpriced house first to make subsequent options seem cheaper

---

## PART III: EXPECTED UTILITY THEORY (Classes 5-6)

### Decision-Making Under Uncertainty

**The Problem:**
- One action can lead to multiple possible outcomes
- The decision-maker chooses the action, but "Nature" determines which outcome occurs
- Need to incorporate probability and intensity of preferences

### Nature as a Pseudo Decision-Maker

In decision trees with uncertainty:
- **Nature (N)** represents randomness/chance
- Nature "moves" after the decision-maker chooses an action
- Nature's "actions" have probabilities (not strategic choices)

**Properties of Nature's probabilities:**
- Each probability is non-negative: p(xₖ) ≥ 0
- Probabilities sum to 1: Σp(xₖ) = 1

### Lotteries

**Simple Lottery:**
A probability distribution over outcomes X = {x₁, x₂, ..., xₙ}

p = (p(x₁), p(x₂), ..., p(xₙ))

where p(xₖ) ≥ 0 and Σp(xₖ) = 1

**Compound Lottery:**
When Nature moves multiple times (sequential uncertainty)

**Example - Drug Development Decision:**

| Action | Outcome | Probability | Payoff (Rs. Crores) |
|--------|---------|-------------|---------------------|
| Conventional (C) | Approved | 0.7 | 100 |
| | Not Approved | 0.3 | -20 |
| Innovative (I) | Breakthrough | 0.3 | 200 |
| | Standard Success | 0.3 | 80 |
| | Failure | 0.4 | -40 |

### Expected Payoff

**Definition:**
E[u(x)|p] = Σ pₖ · u(xₖ) = p₁u(x₁) + p₂u(x₂) + ... + pₙu(xₙ)

This is a weighted average of payoffs, weighted by probabilities.

**Example Calculation:**
- v(C) = 0.7 × 100 + 0.3 × (-20) = 70 - 6 = **64**
- v(I) = 0.3 × 200 + 0.3 × 80 + 0.4 × (-40) = 60 + 24 - 16 = **68**

**Rational Choice:** Select Innovative method (higher expected payoff)

### Ordinal vs. Cardinal Payoffs

**Ordinal Payoffs (Certain Outcomes):**
- Only order/ranking matters
- Multiple payoff functions can represent the same preferences
- Example: u(s)=10, u(f)=7, u(g)=3 AND u(s)=97, u(f)=72, u(g)=31 both represent s ≻ f ≻ g

**Cardinal Payoffs (Uncertain Outcomes):**
- Intensity of preferences matters, not just order
- The specific numerical values affect expected payoff calculations
- Different numbers can lead to different optimal decisions

**Example showing intensity matters:**
- Original: v(I) = 0.3×200 + 0.3×80 + 0.4×(-40) = 68 > v(C) = 64 → Choose I
- Changed: v(I) = 0.3×100 + 0.3×80 + 0.4×(-40) = 38 < v(C) = 64 → Choose C

### Risk Attitudes

Even with equal expected payoffs, people may prefer different options:

**Example - Insurance Decision:**

| Action | Outcomes | Calculation | Expected Payoff |
|--------|----------|-------------|-----------------|
| Buy (B) | Various accident scenarios | Complex lottery | 0 |
| No Buy (N) | Nothing changes | Certain | 0 |

Both have expected payoff = 0, but:
- **Risk Averse**: Prefers the certain outcome (Buy insurance)
- **Risk Neutral**: Indifferent between options
- **Risk Loving**: Prefers the gamble (Don't buy insurance)

### Expected Utility Theory - Summary

**Core Principle:**
When faced with uncertain outcomes, a rational decision-maker chooses the action that maximizes expected payoff.

**Formal Definition:**
A player with payoff function u(·) over outcomes is rational if he chooses action a* ∈ A such that:

v(a*) = E[u(x)|a*] ≥ E[u(x)|a] = v(a) for all a ∈ A

**Key Components:**
1. Likelihood of each outcome (probabilities)
2. Desirability of each outcome (payoffs)
3. Weighted average combining both

### Continuous Outcome Spaces

When outcomes form a continuous range (e.g., X = [0, 10]):
- Infinitely many possible outcomes
- Cannot use simple summation
- Requires integration with probability density functions (covered later)

---

## Key Formulas Summary

| Concept | Formula |
|---------|---------|
| Number of outcome pairs | ⁿC₂ = n(n-1)/2 |
| Expected Payoff | E[u(x)\|p] = Σ pₖ · u(xₖ) |
| FOC for maximization | dv/da = 0 |
| SOC for maximum | d²v/da² < 0 |

---

## Key Definitions

| Term | Definition |
|------|------------|
| **Game** | Mathematical model of strategic interaction |
| **Rational Preference** | Complete and transitive preference relation |
| **Payoff Function** | Numerical representation of preferences |
| **Lottery** | Probability distribution over outcomes |
| **Expected Payoff** | Weighted average of payoffs by probabilities |
| **Dominant Strategy** | Best choice regardless of what others choose |
| **Nature** | Pseudo-player representing randomness/chance |

---

*Last Updated: February 2026*
