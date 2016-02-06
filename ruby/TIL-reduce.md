## Método .reduce

El método `reduce` se usa para efectuar una operación sobre todos los elementos de un array. Toma dos parámetros: el valor inicial, y el símbolo de la operación a efectuar.

```ruby
mi_array = [1,2,3,4,5]

# Suma
mi_array.reduce(0, :+)
#=> 15

# Resta
mi_array.reduce(0, :-)
#=> -15

# Multiplicación
mi_array.reduce(1, :*)
#=> 120
# Si usáramos 0 como valor inicial, sería igual a 0 x 1 x 2 x 3... #=> 0

```
