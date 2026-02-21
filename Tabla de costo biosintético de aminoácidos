src/main.py
# METABOLIC-COST-AMR: Herramienta de Cálculo Estequiométrico
# Autora: Liseth Yeraldin Nieto Taborda

# Tabla de costo biosintético de aminoácidos (ATP equivalentes en E. coli)
# Referencia: Akashi & Gojobori (2002) PNAS
AA_COST_ATP = {
    'A': 11.7, 'R': 27.3, 'N': 14.7, 'D': 12.7, 'C': 24.7,
    'E': 15.3, 'Q': 16.3, 'G': 11.7, 'H': 38.3, 'I': 32.3,
    'L': 27.3, 'K': 30.3, 'M': 34.3, 'F': 52.0, 'P': 20.3,
    'S': 11.7, 'T': 18.7, 'W': 74.3, 'Y': 50.0, 'V': 23.3
}

def calcular_carga_metabolica(secuencia_proteina):
    """
    Calcula el costo total de ATP para la síntesis de una secuencia proteica.
    """
    total_atp = 0
    # Limpia la secuencia de espacios o saltos de línea
    secuencia = secuencia_proteina.strip().upper()
    
    for aa in secuencia:
        if aa in AA_COST_ATP:
            total_atp += AA_COST_ATP[aa]
        else:
            # Si hay un carácter extraño (como un '*' de stop codon), lo ignora
            continue
            
    return round(total_atp, 2)

if __name__ == "__main__":
    # Ejemplo con una secuencia corta de prueba (Beta-lactamasa parcial)
    test_sequence = "MSIQHFRVALIPFFAAFCLPVFA"
    resultado = calcular_carga_metabolica(test_sequence)
    
    print("--- Análisis de Carga Metabólica (In Silico) ---")
    print(f"Secuencia analizada: {test_sequence}")
    print(f"Costo total estimado: {resultado} moléculas de ATP")
