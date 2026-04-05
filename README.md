# Colecciones-de-datos-listas-conjuntos-y-diccionarios[semana 15 py](https://github.com/user-attachments/files/26491153/semana.15.py)
# Diccionario para almacenar estudiantes y sus notas
estudiantes = {}

# Función para agregar estudiante
def agregar_estudiante():
    nombre = input("Ingrese el nombre del estudiante: ")
    nota = float(input("Ingrese la nota del estudiante: "))
    estudiantes[nombre] = nota
    print("Estudiante agregado correctamente.\n")

# Función para mostrar estudiantes
def mostrar_estudiantes():
    if len(estudiantes) == 0:
        print("No hay estudiantes registrados.\n")
    else:
        print("Lista de estudiantes:")
        for nombre, nota in estudiantes.items():
            print(f"{nombre}: {nota}")
        print()

# Función para buscar estudiante
def buscar_estudiante():
    nombre = input("Ingrese el nombre a buscar: ")
    if nombre in estudiantes:
        print(f"La nota de {nombre} es {estudiantes[nombre]}\n")
    else:
        print("Estudiante no encontrado.\n")

# Función para eliminar estudiante
def eliminar_estudiante():
    nombre = input("Ingrese el nombre a eliminar: ")
    if nombre in estudiantes:
        del estudiantes[nombre]
        print("Estudiante eliminado.\n")
    else:
        print("Estudiante no encontrado.\n")

# Menú principal
while True:
    print("=== MENÚ ===")
    print("1. Agregar estudiante")
    print("2. Mostrar estudiantes")
    print("3. Buscar estudiante")
    print("4. Eliminar estudiante")
    print("5. Salir")
    
    opcion = input("Seleccione una opción: ")
    
    if opcion == "1":
        agregar_estudiante()
    elif opcion == "2":
        mostrar_estudiantes()
    elif opcion == "3":
        buscar_estudiante()
    elif opcion == "4":
        eliminar_estudiante()
    elif opcion == "5":
        print("Programa finalizado.")
        break
    else:
        print("Opción inválida.\n")
