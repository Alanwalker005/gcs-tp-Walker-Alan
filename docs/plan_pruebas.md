# Plan de Pruebas

## Versión 1.1

### Casos de prueba

| ID | Descripción | Entrada | Resultado esperado |
|----|-------------|---------|--------------------|
| CP-01 | Solo números | `2805316677` | Válido (se guarda) |
| CP-02 | Un solo dígito | `5` | Válido (se guarda) |
| CP-03 | Letras y números | `2805aew` | Inválido (error) |
| CP-04 | Solo letras | `aew` | Inválido (error) |
| CP-05 | Contiene espacios | `2805 316677` | Inválido (error) |
| CP-06 | Contiene guiones | `2805-316677` | Inválido (error) |
| CP-07 | Contiene el símbolo + | `+542805316677` | Inválido (error) |
| CP-08 | Campo vacío | (vacío) | Inválido (error) |

### Cómo se ejecutan

- **Manuales:** abrir `src/index.html`, ingresar cada entrada en el campo Teléfono, apretar Guardar y comprobar el mensaje.
- **Automáticas:** `tests/test_validacion.js` contiene los mismos casos y verifica la función `validarTelefono`.

### Criterio de aceptación

Todos los casos deben dar el resultado esperado.