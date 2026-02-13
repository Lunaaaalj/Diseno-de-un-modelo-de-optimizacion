# Diseño de un modelo de optimización

## Un problema hipotético

Un país pequeño está en guerra, en este momento, solo tiene activas dos fábricas el ejército declaro tres prioridades, la producción de armas, comida y municiones. Asesores del gobierno han declarado que los recursos disponibles dan para producir 100 armas, 600 unidades de comida, y 1200 municiones. La fábrica 1 produce 3 armas, 2 unidades de comida y 1 munición cada hora, la fabrica 2 produce una arma, tres unidades de comida, y dos municiones cada hora, el costo de producción por hora, de la fábrica 1 es de 10000 USD, y de la fábrica 2 es de 7000 USD, además, se necesitan producir al menos 20 armas, 200 unidades de comida y 500 municiones para sustentar la guerra, y deberá haber mínimo el doble de municiones que de armas. ¿Cuántas horas deberá producir cada fábrica para minimizar el costo de la guerra?

\begin{align}
\mathbf{min}\quad z=10000x_1 + 7000x_2\\
s.t\begin{cases}
3x_1 + x_2 \geq 20\\
3x_1 + x_2 \leq 100\\
2x_1 + 3x_2 \geq 200\\
2x_2 + 3x_2 \leq 600\\
x_1 + 2x_2 \geq 500\\
x_1 + 2x_2 \leq 1200\\
x_2 \geq 2x_1
\end{cases}
\end{align}