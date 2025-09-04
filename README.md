# Simulating the Pandemic Flu Spread in a Classroom

#### Overview
This project simulates how a flu outbreak might spread within a classroom of 61 students. We model the epidemic starting with one infected student, who can infect others with a 1% daily transmission probability (p = 0.01). Each infected student remains contagious for three days.

The simulation explores:
- Epidemic spread under daily infections versus weekday-only infections (to mimic school schedules).
- Average number of infections per day and how quickly the epidemic grows.
- Epidemic duration distributions (how long outbreaks typically last).
- The impact of partial immunity scenarios (e.g., 50% of students vaccinated at random).

Across 1000 simulations, results show that:
- On average, ~30 out of 61 students (≈50%) become infected before the epidemic resolves.
- Epidemics often last 30–50 days in the weekday-only model, with a right-skewed duration distribution.
- Random immunization significantly reduces infections and outbreak length, though not eliminating flu risk completely.

#### Background & Motivation
Understanding flu spread in small, enclosed environments like classrooms is critical for anticipating outbreaks and designing effective interventions. Simulation models help explore possible outcomes where direct prediction is difficult. This project applies an agent-based simulation approach, building on epidemiological principles (e.g., SEIR-type models) to capture randomness and student-level interactions.

#### Methods
- Population: 61 students, 1 initially infected.
- Infection probability: 1% chance per day for each susceptible-infectious interaction.
- Contagious period: 3 days per infected student.
- Simulation runs: 1000 trials to estimate averages and distributions.

#### Outputs:
- Line plot of expected total infections by day.
- Histogram of epidemic durations across simulations.

#### Code
The Python script (flu_simulation.py) runs 1000 Monte Carlo simulations and produces:
- Expected infection curve across days.
- Epidemic duration histogram.

#### Technologies used:
- Python
- NumPy (stochastic simulation)
- Matplotlib (visualization)

#### Results
- Expected Infections: On average, about half the class becomes infected.
- Duration: Outbreaks range widely; weekday-only simulations prolong spread.
- Immunity: 50% immunization significantly “flattens the curve,” reducing both total infections and outbreak duration.
