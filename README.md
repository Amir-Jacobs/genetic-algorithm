# Genetic Algorithm - Phrase Guesser

A fun little project that uses a genetic algorithm to evolve a population of random strings until one matches a target phrase.

## Why Genetic Algorithms Matter

While this project guesses a simple phrase, the same underlying technique powers solutions to problems that are too complex for brute-force or traditional approaches. Genetic algorithms shine whenever the search space is enormous and a "good enough" answer is valuable.

### Real-World Applications

- **Optimization & Scheduling** — Genetic algorithms are used to optimize crew schedules, flight routes, and factory job sequencing, minimizing downtime and cost.
- **Machine Learning & Neural Networks** — Neuroevolution evolves the architecture or weights of neural networks, training agents to play video games, control robots, and solve complex tasks.
- **Drug Discovery & Bioinformatics** — Candidate molecules can be evolved to maximize binding affinity to a target protein, dramatically speeding up early-stage drug design.

The core idea — generate diverse candidates, evaluate them, keep the best, and introduce small random changes — is broadly applicable to any domain where you can define a fitness function.

## How It Works

The algorithm simulates natural selection to "guess" a target sentence:

1. **Initialization** — A population of 1,500 random strings (DNA) is created, each the same length as the target phrase.
2. **Fitness** — Each member is scored by how many characters match the target.
3. **Selection** — A mating pool is built where fitter members appear more often, giving them a higher chance of reproducing.
4. **Crossover** — Two parents are picked at random from the pool and combined at a random midpoint to produce a child.
5. **Mutation** — Each child has a small chance (1%) of a random character being swapped, keeping diversity in the gene pool.
6. **Repeat** — Steps 2–5 loop until a perfect match is found.

## Project Structure

```
src/com/company/
├── Main.java        # Entry point — runs the evolution loop
├── DNA.java         # Represents a single member's genes (char array)
└── Population.java  # Manages the population, selection, and generation cycle
```

## Running

Compile and run with any Java toolchain:

```bash
javac src/com/company/*.java
java -cp src com.company.Main
```

The default target phrase is `"never gonna give you up"`. Change it in `Main.java` to try a different sentence (lowercase a–z and spaces).

## Example Output

```
nvael goina giveeyou up
neveu gonna give you up
never gonna give you up

Generations: 87
Average fitness: 0.413520
Result: never gonna give you up
```

## Built With

- Java

## License

This project was made just for fun — use it however you like.