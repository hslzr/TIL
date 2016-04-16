## Date & Time Ranges

Éste es un error algo tonto con el que me topé hace un par de días. Sucede que al momento de realizar un rango entre dos fechas en algún momento, hay una diferencia *crucial* al momento de hacerlo entre objetos de la clase `Date` y `Time`

```ruby
this_week = Date.today.at_beginning_of_week..Date.today.at_end_of_week
```

`this_week` equivale a un rango de siete días, comprendidos entre el lunes y el domingo de la semana actual. Si lo convirtiésemos en un array, éste sería de *siete elementos*.

```ruby
that_week = Time.now.at_beginning_of_week+1.week..Time.now.at_end_of_week+1.week
```

Ahora `that_week` es igual a un rango de *segundos* comprendidos entre el lunes y el domingo de la semana próxima. Si lo convirtiésemos en un array, éste sería de *604,800* elementos; lo cual no es precisamente muy amigable con la memoria.
