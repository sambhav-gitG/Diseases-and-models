Stochastic SEIR Epidemic Model on Networks

This repository contains a stochastic simulation of a generic epidemic spreading on a heterogeneous contact network using an SEIR (Susceptible–Exposed–Infected–Recovered) model.

The goal of this project is not to model a specific real disease, but to demonstrate how epidemic curves emerge from microscopic interaction rules on complex networks.

Model Overview

The population is represented as a Barabási–Albert scale-free network, capturing the presence of highly connected individuals (hubs).

Each individual can be in one of four states:

S – Susceptible

E – Exposed (infected but not yet infectious)

I – Infected and infectious

R – Recovered with permanent immunity

State Transitions
Transition	Meaning
S → E	Susceptible becomes exposed after contact with an infected individual
E → I	End of incubation period
I → R	Recovery

All transitions are stochastic and evaluated at each timestep.

Key Modelling Choice

Infected individuals do not contact all neighbours every timestep.

Instead, each infected person interacts with only a fixed number of randomly chosen neighbours per day, representing realistic limits on daily social interactions. This avoids unrealistically fast outbreaks caused by highly connected network hubs.

Assumptions

Closed population (no births or deaths)

Permanent immunity after recovery

Fixed daily contact capacity

Homogeneous disease parameters across individuals

Limitations

This model does not include:

Asymptomatic carriers

Behavioural adaptation (lockdowns, distancing, awareness)

Waning immunity or reinfections

Demographic turnover

As a result, the system always produces a single-wave epidemic.

What This Project Demonstrates

How epidemic curves arise from local contact dynamics

The impact of finite contact capacity on disease spread

The role of network heterogeneity in shaping outbreak evolution
