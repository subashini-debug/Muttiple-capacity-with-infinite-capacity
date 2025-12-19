# Multiple server with infinite capacity - (M/M/c):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 10 seconds, serivice time of two lathe machine follow exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

## Procedure :


<img src="https://github.com/user-attachments/assets/de1d6c19-005b-491b-8a0d-531779e449d5" width="1000" height="10000000"/>




## Experiment:

![image](https://user-images.githubusercontent.com/103921593/203238035-1c8109bc-cbf2-4c77-baea-c5b682a752ef.png)


## Program
import math


lam = 1 / 10        # arrival rate
mu  = 1 / 8         # service rate
c   = 2             # servers

rho = lam / (c * mu)


p0 = 1 / (
    sum((lam / mu) ** n / math.factorial(n) for n in range(c)) +
    ((lam / mu) ** c) / (math.factorial(c) * (1 - rho))
)

Lq = (p0 * (lam / mu) ** c * rho) / (math.factorial(c) * (1 - rho) ** 2)
Ls = Lq + lam / mu
Wq = Lq / lam
Ws = Ls / lam

print("Average materials in system (Ls):", round(Ls, 3))
print("Average materials in conveyor (Lq):", round(Lq, 3))
print("Waiting time in system (Ws):", round(Ws, 3), "sec")
print("Waiting time in conveyor (Wq):", round(Wq, 3), "sec")


# Inputs

<img src="https://github.com/user-attachments/assets/de1d6c19-005b-491b-8a0d-531779e449d5" width="1000" height="10000000"/>
## Output :

<img src="https://github.com/user-attachments/assets/de1d6c19-005b-491b-8a0d-531779e449d5" width="1000" height="10000000"/>

<img src="https://github.com/user-attachments/assets/de1d6c19-005b-491b-8a0d-531779e449d5" width="1000" height="10000000"/>
## Result : 


<img src="https://github.com/user-attachments/assets/de1d6c19-005b-491b-8a0d-531779e449d5" width="1000" height="10000000"/>
