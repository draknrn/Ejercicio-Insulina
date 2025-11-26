#  Peso molecular de Insulina en Python

Este repositorio contiene dos scripts en Python que trabajan con la secuencia de la insulina humana:

- `string-insulin.py`: calcula el peso molecular aproximado de la insulina a partir de su secuencia de aminoácidos.
- `net-charge.py`: calcula la carga neta de la insulina a distintos valores de pH (de 0 a 14).

## Requisitos

- Python 3.6 o superior (idealmente Python 3.10).

## Archivos

### 1. `string-insulin.py`

Este script:

1. Define la secuencia de **preproinsulina** y la divide en:
   - Péptido señal (`lsInsulin`)
   - Cadena B (`bInsulin`)
   - Cadena A (`aInsulin`)
   - Péptido conector C (`cInsulin`)
2. Construye la secuencia de **insulina madura** concatenando `bInsulin + aInsulin`.
3. Imprime en pantalla:
   - La secuencia completa de la preproinsulina.
   - La secuencia de la cadena A de la insulina.
4. Define un diccionario `aaWeights` con el peso molecular aproximado de cada aminoácido.
5. Cuenta cuántas veces aparece cada aminoácido en la secuencia de insulina.
6. Calcula el **peso molecular aproximado** de la insulina como la suma de:
   > (número de AA) × (peso de cada AA)
7. Compara el valor calculado con un valor de referencia (`molecularWeightInsulinActual = 5807.63`)
   y muestra el **porcentaje de error**.

**Cómo ejecutarlo:**

```bash
python3 string-insulin.py
