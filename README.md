# PROGRAMA-PYTHON-PROBLEMA-1
DESARROLLLO PROBLEMA 1 
# DUVAN SANTIAGO BISBICUS ILES
# GRUPO 706
# INGENIERIA DE SISTEMAS 

# Lista con los datos de las sesiones
# [ID Cliente, Duración, Número de clics]

datos = [
    [1001, 210, 10],
    [1002, 50, 1],
    [1003, 130, 6],
    [1004, 40, 4],
    [1005, 260, 15]
]


# Función para revisar el nivel de compromiso
def revisar_compromiso(tiempo, clics):

    # compromiso alto
    if tiempo > 180 and clics > 8:
        nivel = "Alto"

    # compromiso bajo
    elif tiempo < 60 or clics < 3:
        nivel = "Bajo"

    # los demás casos
    else:
        nivel = "Medio"

    return nivel


print("REPORTE FINAL")
print("-------------------")

# recorrer la matriz
for fila in datos:

    cliente = fila[0]
    tiempo = fila[1]
    clics = fila[2]

    resultado = revisar_compromiso(tiempo, clics)

    print("Cliente:", cliente)
    print("Clasificación:", resultado)
    print("-------------------")
