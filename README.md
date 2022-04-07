# Flow-Shop-Scheduling
Es un problema combinacional en el que se necesita organizar el procesamiento de un conjunto de trabajos divididos en operaciones y cada operación se lleva a cabo en un recurso compartido.
En el FSS (Flow Shop Scheduling) se dan tiempos _Pkj_ para cada trabajo _j_ en cada máquina _k_ y una secuencia de trabajo _S=(s1,s2,...,sn)_ donde _n_ trabajos _(j = 1,2,...,n)_ serán procesados por _m_ máquinas _(k = 1,2,...,m)_ por lo que el objetivo de FSSP es encontrar un
orden de secuencia para el procesamiento de operaciones con el valor mínimo para el *_MakeSpan._*

El _*MakeSpan*_ para una organización de trabajo en particular se compone del total tiempo transcurrido desde el comienzo del primer trabajo hasta el término del último trabajo. El *_MakeSpan_* es por lo tanto un característica de todo el problema.

El FSSP se resume a determinar la permutación optima para minimizar el _MakeSpan_, es decir, minimizar la suma del tiempo en el que se completa cada trabajo. Con 2 máquinas, el problema se puede resolver en un tiempo _ø(nlogn)_ usando el algoritmo de _Johnson_, sin embargo, para más de 2 máquinas, el problema se convierte en _NP Hard_. 

# Datos del problema
_n:_  Número total de trabajos a programar

_m:_  Número de máquinas en el sistema

_Wj:_ Peso del trabajo _j_, _j = 1, 2,..., n_

_Pi,j:_  Tiempo de procesamiento del trabajo _j, j = 1, 2,..., n_, en la máquina _i, i = 1, 2,..., m_

_Ci,j:_  Tiempo de finalización del trabajo _j, j = 1, 2,..., n_, en la máquina _i, i = 1, 2,..., m_

_Cj:_  Tiempo de finalización del trabajo _j, j = 1, 2,..., n_, en la última máquina _( = C m,j)_

# Modelo
El problema de Flow Shop es generalmente entendido como un problema de permutaciones. El retraso entre el inicio de una tarea y otro es:

# Función Objetivo
max f(S,x) EL objetivo al solucionar el problema es disminuir el tiempo total de procesamiento desde el inicio de la tarea 1 del trabajo 1 hasta la tarea n del trabajo n.

![objFunction](https://user-images.githubusercontent.com/56168289/160326128-09805bfd-a54d-4067-9d44-83431d6d2835.png)

# Solución inicial

_Aleatoria_

 |  |  |  |  |
 | :---: | :---: | :---: | :---: |
 | 3 | 1 | 4 | 2 |
 
 # Solución Vecina
 
 _Intercambio de orden de trabajos_
 
 Inicial:
 
 |  |  |  |  |
 | :---: | :---: | :---: | :---: |
 | 3 | 1 | 4 | 2 |
 
 Vecina:
 
 |  |  |  |  |
 | :---: | :---: | :---: | :---: |
 | 2 | 1 | 4 | 3 |

# Aplicaciones

Su aplicación es amplia:

  → para programar el despacho de vuelos en aeropuertos
  
  → programar líneas de producción en un fábrica
  
  → programación de cirugías
  
  → reparación de equipos o maquinarias de un taller

# Ejemplo

| Trabajos |  M1  |  M2  |  M3  |  M4  |
| :---: | :---: | :---: | :---: | :---: |
| Trabajo 1 |  5  |  4  |  4  |  3  |
| Trabajo 2 |  5  |  4  |  4  |  6  |
| Trabajo 3 |  3  |  2  |  3  |  3  |
| Trabajo 4 |  6  |  4  |  4  |  2  |
| Trabajo 5 |  3  |  4  |  1  |  5  |

 ![EjemploFSS](https://user-images.githubusercontent.com/56168289/160938652-5fa3ea8b-89a2-4a4b-abee-2bdf0da8e2dd.png)

# Instancias
2

5

100
| Trabajos |  M1  |  M2  |  M3  |  M4  |
| :---: | :---: | :---: | :---: | :---: |
| Trabajo  1  |   3   |   14   |   11   |   1   |
| Trabajo  2  |   12   |   14   |   11   |   15   |
| Trabajo  3  |   8   |   9   |   14   |   8   |
| Trabajo  4  |   13   |   6   |   12   |   7   |
| Trabajo  5  |   12   |   12   |   2   |   6   |
| Trabajo  6  |   2   |   7   |   2   |   6   |
| Trabajo  7  |   12   |   8   |   7   |   5   |
| Trabajo  8  |   8   |   7   |   1   |   8   |
| Trabajo  9  |   11   |   15   |   6   |   14   |
| Trabajo  10  |   12   |   12   |   13   |   9   |
| Trabajo  11  |   7   |   9   |   13   |   1   |
| Trabajo  12  |   7   |   11   |   3   |   5   |
| Trabajo  13  |   6   |   14   |   9   |   9   |
| Trabajo  14  |   4   |   6   |   3   |   6   |
| Trabajo  15  |   12   |   2   |   14   |   14   |
| Trabajo  16  |   3   |   13   |   2   |   3   |
| Trabajo  17  |   13   |   5   |   8   |   3   |
| Trabajo  18  |   14   |   12   |   13   |   1   |
| Trabajo  19  |   8   |   9   |   15   |   1   |
| Trabajo  20  |   4   |   2   |   5   |   10   |
| Trabajo  21  |   8   |   14   |   3   |   13   |
| Trabajo  22  |   9   |   13   |   4   |   2   |
| Trabajo  23  |   1   |   12   |   3   |   12   |
| Trabajo  24  |   2   |   13   |   3   |   1   |
| Trabajo  25  |   5   |   12   |   15   |   14   |
| Trabajo  26  |   14   |   4   |   11   |   3   |
| Trabajo  27  |   1   |   11   |   1   |   13   |
| Trabajo  28  |   11   |   5   |   13   |   4   |
| Trabajo  29  |   4   |   3   |   1   |   3   |
| Trabajo  30  |   11   |   3   |   8   |   4   |
| Trabajo  31  |   7   |   2   |   2   |   7   |
| Trabajo  32  |   11   |   2   |   15   |   11   |
| Trabajo  33  |   1   |   5   |   10   |   2   |
| Trabajo  34  |   11   |   9   |   5   |   13   |
| Trabajo  35  |   1   |   6   |   9   |   11   |
| Trabajo  36  |   11   |   3   |   9   |   10   |
| Trabajo  37  |   11   |   3   |   12   |   8   |
| Trabajo  38  |   13   |   10   |   7   |   4   |
| Trabajo  39  |   13   |   4   |   10   |   10   |
| Trabajo  40  |   13   |   15   |   5   |   6   |
| Trabajo  41  |   12   |   3   |   4   |   1   |
| Trabajo  42  |   6   |   4   |   13   |   10   |
| Trabajo  43  |   15   |   3   |   6   |   5   |
| Trabajo  44  |   2   |   6   |   14   |   6   |
| Trabajo  45  |   2   |   15   |   1   |   3   |
| Trabajo  46  |   1   |   12   |   9   |   2   |
| Trabajo  47  |   4   |   12   |   7   |   4   |
| Trabajo  48  |   9   |   9   |   14   |   12   |
| Trabajo  49  |   8   |   3   |   5   |   4   |
| Trabajo  50  |   8   |   8   |   5   |   14   |
| Trabajo  51  |   6   |   3   |   7   |   1   |
| Trabajo  52  |   13   |   14   |   5   |   9   |
| Trabajo  53  |   13   |   7   |   4   |   10   |
| Trabajo  54  |   9   |   15   |   12   |   6   |
| Trabajo  55  |   13   |   3   |   10   |   3   |
| Trabajo  56  |   6   |   6   |   8   |   10   |
| Trabajo  57  |   12   |   3   |   9   |   7   |
| Trabajo  58  |   1   |   2   |   3   |   4   |
| Trabajo  59  |   9   |   8   |   1   |   8   |
| Trabajo  60  |   5   |   15   |   1   |   7   |
| Trabajo  61  |   11   |   3   |   2   |   8   |
| Trabajo  62  |   7   |   7   |   2   |   2   |
| Trabajo  63  |   8   |   7   |   4   |   8   |
| Trabajo  64  |   7   |   2   |   11   |   12   |
| Trabajo  65  |   7   |   14   |   1   |   1   |
| Trabajo  66  |   1   |   2   |   9   |   6   |
| Trabajo  67  |   11   |   3   |   6   |   5   |
| Trabajo  68  |   3   |   5   |   11   |   15   |
| Trabajo  69  |   10   |   2   |   13   |   12   |
| Trabajo  70  |   12   |   8   |   1   |   13   |
| Trabajo  71  |   1   |   12   |   13   |   7   |
| Trabajo  72  |   7   |   13   |   12   |   14   |
| Trabajo  73  |   2   |   4   |   5   |   5   |
| Trabajo  74  |   1   |   2   |   4   |   4   |
| Trabajo  75  |   15   |   3   |   8   |   4   |
| Trabajo  76  |   9   |   13   |   9   |   10   |
| Trabajo  77  |   10   |   15   |   4   |   14   |
| Trabajo  78  |   3   |   9   |   11   |   6   |
| Trabajo  79  |   6   |   14   |   7   |   11   |
| Trabajo  80  |   6   |   13   |   9   |   9   |
| Trabajo  81  |   7   |   9   |   7   |   10   |
| Trabajo  82  |   7   |   6   |   10   |   15   |
| Trabajo  83  |   5   |   13   |   12   |   5   |
| Trabajo  84  |   4   |   7   |   14   |   5   |
| Trabajo  85  |   10   |   8   |   9   |   6   |
| Trabajo  86  |   3   |   15   |   10   |   13   |
| Trabajo  87  |   12   |   14   |   10   |   12   |
| Trabajo  88  |   5   |   3   |   2   |   10   |
| Trabajo  89  |   3   |   1   |   10   |   5   |
| Trabajo  90  |   13   |   12   |   6   |   11   |
| Trabajo  91  |   1   |   9   |   1   |   6   |
| Trabajo  92  |   5   |   3   |   2   |   14   |
| Trabajo  93  |   10   |   10   |   15   |   9   |
| Trabajo  94  |   6   |   15   |   2   |   11   |
| Trabajo  95  |   3   |   2   |   11   |   4   |
| Trabajo  96  |   6   |   13   |   3   |   14   |
| Trabajo  97  |   6   |   9   |   5   |   13   |
| Trabajo  98  |   10   |   1   |   12   |   8   |
| Trabajo  99  |   3   |   3   |   14   |   6   |
