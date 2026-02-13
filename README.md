# Diseño de un modelo de optimización

## Un problema hipotético

Un país pequeño se encuentra en guerra y actualmente cuenta únicamente con dos fábricas activas para abastecer al ejército. Las prioridades estratégicas establecidas por el alto mando militar son la producción de armas, alimentos y municiones.

Los recursos disponibles permiten producir como máximo 150 armas, 600 unidades de alimento y 1200 municiones. La fábrica 1 produce por cada hora de operación 3 armas, 2 unidades de alimento y 1 munición, mientras que la fábrica 2 produce 1 arma, 3 unidades de alimento y 2 municiones por hora.

El costo de operación por hora es de 10 000 USD para la fábrica 1 y 7 000 USD para la fábrica 2. Para poder sostener el esfuerzo bélico, se requiere producir al menos 20 armas, 200 unidades de alimento y 150 municiones.

Además, por razones logísticas y estratégicas, se ha determinado que la fábrica 2 debe operar al menos el doble de horas que la fábrica 1.

El objetivo es determinar cuántas horas debe operar cada fábrica de forma que se minimice el costo total de producción, cumpliendo todas las restricciones establecidas.

$\begin{align}
\mathbf{min}\quad z &= 10000x_1 + 7000x_2 \\[6pt]
\text{s.a.}\quad
\begin{cases}
3x_1 + x_2 \geq 20 & \text{(armas mínimas)}\\
3x_1 + x_2 \leq 150 & \text{(armas máximas)}\\[4pt]

2x_1 + 3x_2 \geq 200 & \text{(alimento mínimo)}\\
2x_1 + 3x_2 \leq 600 & \text{(alimento máximo)}\\[4pt]

x_1 + 2x_2 \geq 150 & \text{(municiones mínimas)}\\
x_1 + 2x_2 \leq 1200 & \text{(municiones máximas)}\\[4pt]

x_2 \geq 2x_1 & \text{(prioridad estratégica)}\\

x_1, x_2 \geq 0
\end{cases}
\end{align}$