# Inteligencia-Artificial
Algoritmo A*

Pseudocódigo

A*(Grafo, Inicio, Meta, Heurística)

  Crear ColaDePrioridad PQ (almacena [f(n), nodo])
  
  Crear Diccionario G_COSTOS (inicializado en infinito)
  
  Insertar [Heurística(Inicio), Inicio] en PQ
  
  G_COSTOS[Inicio] = 0
  
  MIENTRAS PQ no esté vacía:
    NodoActual = Extraer el de menor f(n) en PQ
    SI NodoActual es Meta: TERMINAR (Éxito)
    PARA cada Vecino de NodoActual con costo C:
      NuevoG = G_COSTOS[NodoActual] + C
      SI NuevoG < G_COSTOS[Vecino]:
        G_COSTOS[Vecino] = NuevoG
        F_Costo = NuevoG + Heurística(Vecino)
        Insertar [F_Costo, Vecino] en PQ
