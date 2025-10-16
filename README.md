# Fish Population Modelling

This is a brief summary of a paper I wrote in a Mathematical Biology Undergraduate course. The paper is available to read in the repository above.
In this project I recreated the results from a paper Titled: "Demand-induced regime shift in fishery: A mathematical perspective" found https://www.sciencedirect.com/science/article/pii/S0025556423000494.
I conducted further stability analysis and examined the effect of different parameters on the Fish population.

## Explaining This Repository:

- `Solving_System_and_Testing_Stability` → Using solve_ivp to solve the system and the jacobian to understand the stability of different fixed points
- `Animations_Varied_Parameters`→ Animating parameters changing and how the system evolves

 
## 1. The Variables
 
| Variable | Description                  |
| -------- | ---------------------------- |
| **X(t)** | Biomass of healthy fish      |
| **Y(t)** | Biomass of infected fish     |
| **H(t)** | Harvesting effort            |
| **P(t)** | Market price of healthy fish |

## 2. The Parameters Varied

| Symbol | Description                                                              |
| :----: | :----------------------------------------------------------------------- |
|  **τ** | Taxation rate imposed on harvested fish                                  |
|  **λ** | Transmission rate of infection between healthy and infected fish         |
|  **K** | Environmental carrying capacity (maximum sustainable biomass)            |
|  **A** | Maximum market demand (controls the saturation level of consumer demand) |

- For details on the parameters which were not varied read the paper in the repository above.

## 3. The System of Equations

```math
\frac{dX}{dt} = rX \left(1 - \frac{X + Y}{K}\right) - \lambda XY - \frac{q_1 X H}{X + D_1}
```

```math
\frac{dY}{dt} = \lambda XY - \mu Y - \frac{q_2 Y H}{Y + D_2}
```

```math
\frac{dH}{dt} = \phi_1 H \left[\left(\frac{q_1 (P - \tau) X}{X + D_1} + \frac{q_2 (p - \tau) Y}{Y + D_2}\right) - c \right]
```

```math
\frac{dP}{dt} = \phi_2 P \left(\frac{A}{1 + BP} - \frac{q_1 X H}{X + D_1}\right)
```


## 4. The fixed points that existed

#### Equilibrium 1 - The Healthy Fish Equilibrium


<img width="447" height="313" alt="image" src="https://github.com/user-attachments/assets/bd79794e-02f6-4dc8-a4dc-101b380d7a22" />


#### Equilibrium 2 - The Healthy and Infected Fish Equilibrium

<img width="447" height="313" alt="image" src="https://github.com/user-attachments/assets/c53e3b66-7534-499f-aa85-6e5c916d1afa" />


#### Equilibrium 3 - The disease free Equilibrium

<img width="447" height="313  " alt="image" src="https://github.com/user-attachments/assets/b18338cb-8987-4c40-a4e7-366f26a0d03a" />


#### Equilibrium 4 - The Endemic Equilibrium

<img width="447" height="313" alt="image" src="https://github.com/user-attachments/assets/50a03f7f-6025-446d-bdb6-36c2d8d30d7d" />


## 5. How the parameters effected these points
- For detailed explanation on this read the paper in the repository. Below is a few nice animations to grasp how the system changes with the different parameters

#### Varying the system with **λ** (The Transmission rate of infection between healthy and infected fish)
![animation for lambda t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/fb8d5c42-e6d6-4215-810d-78b973eca000)


#### Varying the system with **K** (Environmental carrying capacity (maximum sustainable biomass))
![animation for K t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/7abf47ec-86aa-447d-8a73-2d215d6d802f)


#### Varying the system with **A** (Maximum market demand (controls the saturation level of consumer demand))
![animation for A t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/7a0652aa-5078-405c-9b89-4c3a68008032)


#### Varying the system with  **τ** (Taxation rate imposed on harvested fish)  
![animation for tau t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/25a52869-4db6-4020-b9eb-cdc9e96c2605)


## 6. Conclusion
The table below highlights how a regime shift in the fish population can occur due to the four parameters examined. 

<img width="900" height="180" alt="image" src="https://github.com/user-attachments/assets/5e9a7edb-e7c0-44d1-be0f-8e15fc88cf12" />

 
This model shows that **overfishing and population collapse can arise from economic pressures** ,such as high demand or low taxation, not just biological limits.  By linking economic factors to ecological dynamics, the model provides a more realistic framework for understanding how policy and economics directly influence fish population stability.






