# Simulación de Transferencia de Calor No Lineal con Elementos Finitos

Este repositorio implementa tres métodos numéricos para resolver la ecuación de calor transitoria con propiedades térmicas dependientes de la temperatura (conductividad κ y calor específico α) en un dominio triangular con hipotenusa curva. Los códigos utilizan el método de elementos finitos (FEM) con mallas generadas mediante `pygmsh`.

## Archivos

- **`Método Implícito - Newton Galerkin.ipynb`**  
  Esquema implícito con linealización de Newton–Galerkin. Resuelve la no-linealidad mediante iteraciones de Newton, permitiendo pasos de tiempo grandes y estabilidad incondicional.

- **`Método Explícito No-Lineal.ipynb`**  
  Método explícito que actualiza las matrices en cada paso evaluando α y κ con la temperatura promediada del elemento del paso anterior.

- **`Método Explícito Lineal.ipynb`**  
  Método explícito con propiedades constantes (linealización). Las matrices se ensamblan una sola vez.

- **`properties_dataNonDim.csv`**  
  Datos adimensionales de α(θ) y κ(θ) en función de la temperatura normalizada θ.


## Requisitos

```bash
pip install numpy matplotlib pandas scipy pygmsh
