# Informes para el proyecto final Machine Learning UPC

![Logo UPC](https://th.bing.com/th/id/OIP.uI-98YWzIvsuhXVyKRkv9gHaHk?pid=ImgDet&rs=1)

## Integrantes
#### - Humbser Meza, Diego Fernando		u202012711
#### - Charapaqui Reluz, Alcides Rommel		u202021294
#### - Llaguento de la Cruz, Marlon Omar		u20201B055

# Milestone 4: Tarea Académica 3: Desarrollo Integral de GAN para la Transformación de Modelos 3D

# Introducción

La transición de diseños digitales a objetos físicos mediante la impresión 3D es un proceso que combina precisión técnica con creatividad. Comienza con la elección de modelos tridimensionales, como camas en el formato .OFF, un estándar para geometrías 3D detalladas. Estos modelos son transformados en BinVoxels, una representación voxelizada que optimiza la manipulación de los datos en tres dimensiones.

Mediante la implementación de Redes Generativas Antagónicas (GAN), tecnologías de aprendizaje profundo avanzadas, se procesan y generan nuevos modelos en Bin Voxels. Este proceso permite la creación de variantes estructuradas y refinadas de los modelos originales, demostrando las capacidades predictivas y creativas de la GAN.

El último paso es convertir estos modelos generados en formato .STL, esencial para la impresión 3D. Este formato permite una transferencia precisa de los modelos digitales a la impresora 3D, culminando así el proceso de diseño y fabricación digital. La metodología establece una fusión entre el modelado avanzado y la manufactura aditiva, una verdadera representación de cómo los conceptos se materializan en el mundo real.


## Configuración del Entorno de Entrenamiento

### Repositorio:
- **Creación del Repositorio**
  - Implementar un repositorio en GitHub o similar, con una estructura clara.
  - Incluir directorios separados para scripts, datasets, documentación y resultados de entrenamiento.
- **Gestión con Issues**
  - Asignar tareas detalladas utilizando issues.
  ![Issues](https://cdn.discordapp.com/attachments/1177509564141273118/1177821559319183370/image.png?ex=6573e6ce&is=656171ce&hm=d2dd6195d2149a639feb19f7615792777a6f389298accdcbb8fcd94751febb4a&)
  - Categorizar issues con etiquetas por urgencia, tipo (bug, mejora, tarea), y asignar responsables.
- **Definición de Milestones**
  - Establecer milestones para reflejar el progreso cronológico.
  ![Milestones](https://cdn.discordapp.com/attachments/1159637113541759146/1177821715867369642/image.png?ex=6573e6f3&is=656171f3&hm=479b482765d0855f6c8cef0955c07826f40865e6feccae4171629b51bf8acf12&)
  - Definir fechas específicas y objetivos a corto y largo plazo.

### Gestión de Tareas

#### Objetivos:

- **Definición de Milestones**
  - Establecer hitos que indiquen progresos importantes como la adquisición de datos, conversión de datos, y fases iniciales de entrenamiento y prueba de la GAN.

- **Búsqueda y Adquisición de Dataset**
  - Descargar [ModelNet10](https://vision.princeton.edu/projects/2014/3DShapeNets/ModelNet10.zip), enfocándose en modelos 3D de camas en formato .off.
    ![dataset STL](https://cdn.discordapp.com/attachments/1159637113541759146/1177792932061904976/image.png?ex=6573cc25&is=65615725&hm=8507e984b540ca98f89340a42f9660167289f7b31df4a53cbd226b545953cb2e&)
    ![dataset images](https://cdn.discordapp.com/attachments/1159637113541759146/1177793088907907082/image.png?ex=6573cc4a&is=6561574a&hm=3f1b75477442acc30100d37715a98c12b39ca8826eec5f9b0e40a649247964d9&)

- **Conversión de Datos**
  - Transformar modelos 3D de camas de .off a Binvoxels, y luego a STL.

- **Preparación para la GAN**
  - Crear una primera versión de la GAN que utilice datos STL para generar nuevos modelos 3D de camas.
  - Desarrollar la arquitectura inicial de la GAN, seleccionando hiperparámetros adecuados.
  - Implementar una pipeline de datos que gestione la entrada/salida de modelos 3D y se encargue del preprocesamiento y normalización de los mismos.

## Metodología

La transformación y procesamiento de modelos 3D comienza con modelos en formato .OFF, específicamente de camas, que representan el punto de partida de nuestro flujo de trabajo. Estos modelos 3D son transformados a un formato intermedio o representación de voxelización conocida como "BinVoxels".

![diagrama del modelo](https://cdn.discordapp.com/attachments/1159637113541759146/1177698207573217341/ditfFBumg.png?ex=657373ed&is=6560feed&hm=34de3fbebdc0412c6828b66c2e16a1daab1f50b30790425c72acc220a1bdba57&)

A continuación, los BinVoxels se utilizan como entrada para una Red Generativa Antagónica (GAN), que procesa los datos y genera un nuevo modelo 3D en formato Bin Voxels. Este nuevo modelo generado se convierte finalmente al formato .STL, que es un estándar comúnmente utilizado para la impresión 3D y otras aplicaciones de modelado 3D.

![Vizualización del stl](https://cdn.discordapp.com/attachments/1159637113541759146/1177720245608267806/bed_0001_0.5_-0.5_0_3.png?ex=65738873&is=65611373&hm=382008d12db50d9675c04b8dfa49d0c91a2cf0725c42332a6123e6dc6d98de93&)

# Impresión 3D

El software utilizado para la impresión y visualización del resultado en formato .stl es PrusaSlicer 2.7.0. A continuación, se presentan imágenes que muestran el proceso y el resultado final:

![Bed.stl](https://cdn.discordapp.com/attachments/1159637113541759146/1177725721519591556/image.png?ex=65738d8d&is=6561188d&hm=4d80a46dca56054fae3a1771c064bedbbcbcdc6bd393eaed010d7eab87413998&)

En la siguiente imagen se puede apreciar un soporte para la impresión generado por el mismo software:

![3d model with supports](https://cdn.discordapp.com/attachments/1159637113541759146/1177726994859962388/image.png?ex=65738ebc&is=656119bc&hm=3da52e78c7ee0d25172e8163f393943c146f32d8e4588da65df030fa9a0d6a39&)

Una vez preparado el modelo, se procede a exportarlo en formato .gcode, que es el utilizado para la impresión 3D en las máquinas de la UPC.

![foto UPC](https://cdn.discordapp.com/attachments/1159637113541759146/1177729941383680120/IMG_0097_3.jpg?ex=6573917b&is=65611c7b&hm=b25d688b3e1b3b39c170f3a75494aae95b0619bcba5d8e3501fe4f9a75331da5&)

# Milestone 5: Tarea Académica 4: Desarrollo Integral de GAN para la Transformación de Modelos 3D

## Metodología:

![Diagrama_Metodologia](https://cdn.discordapp.com/attachments/1159637113541759146/1177738528831053955/daWZeAxnJ.png?ex=6573997a&is=6561247a&hm=5eeebe0d0c40aa9fd908a47e481377af72cc2564d45ef449e46dc396b3326433&)

## Composición de la GAN
La GAN se compone de dos bloques principales que son redes neuronales: el generador y el discriminador.

## Función del Generador
El generador tiene la tarea de "generar" objetos en formato STL que intentan replicar la forma de una cama.

## Evaluación por el Discriminador
Una vez que el generador crea un objeto, entra en juego el discriminador. Su función es determinar si el objeto generado es una cama o no.

## Retroalimentación y Ajuste del Generador
Si el discriminador decide que el objeto no es una cama, el generador actualiza sus pesos (ajusta su modelo interno) y vuelve a crear un objeto. Este proceso de retroalimentación se repite, con el generador intentando mejorar su capacidad de crear objetos que parezcan camas.

## Entrenamiento del Discriminador
Paralelamente, el discriminador se entrena con datos de un dataset. Este entrenamiento le permite mejorar su habilidad para calificar correctamente el trabajo del generador.

## Conclusión del Entrenamiento
El proceso de entrenamiento se considera completo cuando el generador crea objetos que el discriminador consistentemente califica como camas. En este punto, el generador está adecuadamente entrenado para crear objetos que se asemejan mucho o son idénticos a una cama.

## Pseudocódigo:

```python
class Generador:
    def __init__(self):
        # Inicializar parámetros del generador

    def generar_objeto(self):
        # Generar un objeto en formato STL simulando una cama
        return objeto

    def actualizar_pesos(self, feedback):
        # Actualizar los pesos del modelo basado en el feedback del discriminador

class Discriminador:
    def __init__(self, dataset):
        # Inicializar parámetros del discriminador
        self.dataset = dataset

    def entrenar(self):
        # Entrenar el discriminador con el dataset

    def evaluar(self, objeto):
        # Evaluar si el objeto generado por el generador es una cama
        return es_cama

# Inicialización
generador = Generador()
discriminador = Discriminador(dataset)

# Proceso de entrenamiento
entrenamiento_completo = False
while not entrenamiento_completo:
    objeto = generador.generar_objeto()
    es_cama = discriminador.evaluar(objeto)

    if not es_cama:
        generador.actualizar_pesos(feedback="mejorar")
    
    discriminador.entrenar()

    # Criterio para determinar si el entrenamiento está completo
    if criterio_de_finalizacion_cumplido:
        entrenamiento_completo = True

# El generador ahora está entrenado para crear objetos que parecen camas
```
# Milestone final: Trabajo Final

## Resultados
![entrenamiento](https://cdn.discordapp.com/attachments/1177509564141273118/1177791229904306227/verificacion_4.jpg?ex=6573ca8f&is=6561558f&hm=4d2028725f308378b52fa2c01e2c479c257d9aa69ce168a9d1eaa961b9a4d778&)

Tras un entrenamiento de 4 horas, el modelo GAN ha logrado generar un objeto con características similares a una cama. El modelo produce un archivo STL, que representa una cama parecida a los ejemplos proporcionados en su dataset entrenado.

![Resultado final](https://cdn.discordapp.com/attachments/1159637113541759146/1177787298201477241/image.png?ex=6573c6e6&is=656151e6&hm=b35598297851a1dfefa56f9fca2b53fee535c84fcda375ed05c55e833f0f906d&)

# Conclusiones

## Resultados del Entrenamiento de la GAN
Tras el entrenamiento, la Red Generativa Antagónica (GAN) ha demostrado su capacidad para generar un objeto con características notablemente similares a una cama. Este logro se materializa en un archivo STL, que no solo permite una visualización detallada del objeto, sino que también facilita su impresión mediante tecnología 3D. Este avance representa un paso significativo en la aplicación práctica de las GANs, demostrando su potencial en la creación de modelos tridimensionales complejos y detallados.

## Mejora Continua y Limitaciones
Con cada época de entrenamiento, el modelo GAN perfecciona su habilidad para replicar con mayor precisión la forma de una cama, evidenciando una mejora continua en la parte generadora de la red. Sin embargo, es importante reconocer que los resultados obtenidos, aunque impresionantes, no están exentos de errores, especialmente a nivel geométrico. Estas imperfecciones son un recordatorio de las limitaciones inherentes a la tecnología actual y de los desafíos que aún enfrentamos en el campo de la inteligencia artificial y el aprendizaje automático.

## Consideraciones sobre Recursos y Expectativas
Un factor crítico en la eficacia de nuestro modelo GAN es la disponibilidad de recursos tecnológicos y de tiempo. Las GANs son conocidas por su alta demanda en términos de capacidad de procesamiento, memoria RAM, almacenamiento y otros componentes de hardware. Además, el tiempo es un recurso esencial, ya que un entrenamiento más prolongado con más capas, neuronas y épocas puede resultar en mejoras significativas en la calidad de los outputs. Dadas estas consideraciones, los resultados obtenidos están en línea con las expectativas y reflejan las realidades actuales en el desarrollo y la aplicación de modelos de aprendizaje profundo.





