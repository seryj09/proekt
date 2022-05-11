# proekt
Solve equation using Neural Networks

![image](https://user-images.githubusercontent.com/68564759/167892664-734ef863-549f-4032-9a41-530991af902e.png)


## Основные идеи: 

# 1) 
Имеем нейронную сеть,которая на вход принимает пространственную и временную параметры - x и t, далее нейронная сеть, зависящая от параметров NN(x,t,ϴ) выдаёт нам функцию u(x,t), от которой дальше расчитываются частные производные, и подставляются в наше уравнение. 
Далее по правилам, которые будут изложены ниже, вычисляет Loss и минимизируем его, получая оптимальные параметры ϴ 

# 2) 
Правила вычисления Loss:
Считаем Loss как квадрат потери ошибки:
u(x,t) - решение;
<img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="f(x,t,λ) = u_t + N(u(x,t),λ) " />
<img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="MSE = MSE_u+MSE_f" />
<img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="MSE_u = \frac{1}{N_u} \sum\limits_{1}^{N_u}|u(x^i_u , t^i_u)-u^i|^2" />
<img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="MSE_f = \frac{1}{N_f} \sum\limits_{1}^{N_f}|f(x^i_f , t^i_f)|^2" />

<!-- <img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="" /> -->
