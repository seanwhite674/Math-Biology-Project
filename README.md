# Math-Biology-Project

- To add to This:
  - Explain what each parameter varied is. Quickly show bifurcation diagrams and explain what animation does
  - Explain what each dependent variable is and how they correspond to graphs.
 
## 1. The Variables
 
| Variable | Description                  |
| -------- | ---------------------------- |
| **X(t)** | Biomass of healthy fish      |
| **Y(t)** | Biomass of infected fish     |
| **H(t)** | Harvesting effort            |
| **P(t)** | Market price of healthy fish |

## 2. The parameters Varied

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


# 3. The fixed points that existed

## Equilibrium 1 - The Healthy Fish Equilibrium


<img width="447" height="313" alt="image" src="https://github.com/user-attachments/assets/bd79794e-02f6-4dc8-a4dc-101b380d7a22" />



## Equilibrium 2 - The Healthy and Infected Fish Equilibrium


## Equilibrium 3 - The disease free Equilibrium


## Equilibrium 4 - The Endemic Equilibrium





## Varying the system with lambda
![animation for lambda t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/fb8d5c42-e6d6-4215-810d-78b973eca000)
## Showing that in the region where the endemic fixed point is stable the system does eventually collapse to the endemic fixed points

![large lambda goes to endemic state](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/058ef232-228d-45b3-a02a-ecb8ad5887e1)

## Varying the system with K
![animation for K t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/7abf47ec-86aa-447d-8a73-2d215d6d802f)
## Showing that in the region where the endemic fixed point is stable the system does eventually collapse to the endemic fixed points

![large K goes to endemic state](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/f469c072-5138-4c9b-a59e-2787384597c2)
## Varying the system with A
![animation for A t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/7a0652aa-5078-405c-9b89-4c3a68008032)

## Varying the system with tau
![animation for tau t=1000](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/25a52869-4db6-4020-b9eb-cdc9e96c2605)

## Showing that in the region where the endemic fixed point is stable the system does eventually collapse to the endemic fixed points
![large tau goes to endemic state](https://github.com/seanwhite674/Math-Biology-Project/assets/110498155/0acca3ab-fb60-4369-a504-0871b62a950c)
