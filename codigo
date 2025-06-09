def buscar_patente(patentes_ordenadas, patente_buscada):
    """Implementa búsqueda binaria para encontrar una patente"""
    izquierda, derecha = 0, len(patentes_ordenadas) - 1
    
    while izquierda <= derecha:
        medio = (izquierda + derecha) // 2
        patente_actual, dni = patentes_ordenadas[medio]
        
        if patente_actual == patente_buscada:
            return dni
        elif patente_actual < patente_buscada:
            izquierda = medio + 1
        else:
            derecha = medio - 1
    
    return None


def busqueda_binaria():
    # Base de datos ordenada por patente
    base_datos = [
        ("ABC123", "12123456"),
        ("ABC234", "18128458"),
        ("ABC345", "16424486"),
        ("ABC456", "23423456"),
        ("ABC567", "30123445"),
        ("DFG123", "11234868"),
        ("DFG234", "36623666"),
        ("DFG345", "81284861"),
        ("DFG456", "12123456"),
        ("DFG567", "44483456"),
        ("HIJ567", "23123456"),
        ("KLM123", "21923456"),
        ("KLM234", "86123456"),
        ("KLM345", "62123456"),
        ("KLM456", "92219456")
    ]
    
    # Ordenamos por patente (requisito para búsqueda binaria)
    base_datos.sort()
    
    print("Sistema de Control de Acceso - Garaje Privado")
    print("--------------------------------------------")
    
    while True:
        print("\nOpciones:")
        print("1. Verificar patente")
        print("2. Salir del sistema")
        
        opcion = input("Seleccione una opción (1/2): ")
        
        if opcion == "1":
            patente = input("Ingrese la matrícula del vehículo (ej: ABC123): ").strip().upper()
            
            dni = buscar_patente(base_datos, patente)
            
            if dni:
                print("\nResultado de búsqueda:")
                print(f"Patente: {patente}")
                print(f"DNI del conductor: {dni}")
                print("\nAcceso: PERMITIDO ✅")
            else:
                print("\nPatente no registrada en la base de datos")
                print("Acceso: DENEGADO ❌")
        
        elif opcion == "2":
            print("Saliendo del sistema...")
            break
        
        else:
            print("Opción no válida. Por favor ingrese 1 o 2.")


if __name__ == "__main__":
    busqueda_binaria()
