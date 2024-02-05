<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calificaciones</title>
</head>
<body>

<script>
  /*
   declarar varias notas de un alumno en un array
   a) Visualizar su media.
   b) Si la media es aprobada o no.
   c) Visualizar aquellas notas superiores a la media.

  */
  // ================== FUNCIONES ===========================
  // Función para calcular la media de las notas
  function Media(tab_notas) {
    var suma = 0;
    for (var i = 0; i < tab_notas.length; i++) {
      suma += tab_notas[i];
    }
    return suma / tab_notas.length;
  }


  // Función para obtener las notas aprobadas
  function Visualizar1(med) {
    document.write("La media es: "+med+"<br>")
    if (med >= 5) {
        document.write("La media si es aprobada <br>")
      } else
      {
        document.write("La media NO es aprobada <br>")
      }
  }

  

  // Función para visualizar notas superiores a la media
  function Visualizar2(tab_notas, med) {
    document.write("Valores superiores a la media: <br>")
    for (const i in tab_notas){
      if (tab_notas[i] > med){
        document.write(tab_notas[i]+"<br>");
      }
    }
  }

// ======================= PROGRAMA PRINCIPAL =================
  // Declarar un array con notas
  var tab_notas = [8, 9, 7, 5, 2];

  // Llamar a la función para mostrar resultados
  media_resul = Media (tab_notas)
  Visualizar1(media_resul)
  Visualizar2(tab_notas, media_resul)

</script>

</body>
</html>
