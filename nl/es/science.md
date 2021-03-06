---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-07"

subcollection: personality-insights

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:deprecated: .deprecated}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# La ciencia detrás del servicio
{: #science}

Una teoría bien aceptada de psicología, marketing y otros campos es lo que refleja el lenguaje humano la personalidad, el estilo de pensamiento, las conexiones sociales y los estados emocionales. La frecuencia con la que las personas utilizan determinadas categorías de palabras puede proporcionar pistas a estas características. Varios investigadores descubrieron que las variaciones en el uso de las palabras en escritos como blogs, ensayos y tweets pueden predecir aspectos de la personalidad ([Fast y Funder, 2008](/docs/services/personality-insights?topic=personality-insights-references#fast2008); [Gill et al., 2009](/docs/services/personality-insights?topic=personality-insights-references#gill2009); [Golbeck et al., 2011](/docs/services/personality-insights?topic=personality-insights-references#golbeck2011); [Hirsh y Peterson, 2009](/docs/services/personality-insights?topic=personality-insights-references#hirsh2009); y [Yarkoni, 2010](/docs/services/personality-insights?topic=personality-insights-references#yarkoni2010)).
{: shortdesc}

{{site.data.keyword.IBM_notm}} realizó un conjunto de estudios para comprender si las características de personalidad que se deducen de los datos de redes sociales pueden predecir el comportamiento y las preferencias de las personas. {{site.data.keyword.IBM_notm}} ha descubierto que las personas con características de personalidad específicas responden y retwittean en mayor número en las tareas de recopilación y difusión de información. Por ejemplo, las personas con una alta puntuación en búsqueda de emociones son más propensas a responder, mientras que quienes tengan una alta puntuación en precaución son menos propensos a hacerlo ([Mahmud et al., 2013](/docs/services/personality-insights?topic=personality-insights-references#mahmud2013)). Asimismo, las personas con puntuación elevada en modestia, apertura y amigabilidad son más propensas a difundir información ([Lee et al., 2014](/docs/services/personality-insights?topic=personality-insights-references#lee2014)).

{{site.data.keyword.IBM_notm}} también ha descubierto que las personas con una alta apertura y con un bajo rango emocional (neurosis) como se deduce del lenguaje de las redes sociales respondieron más favorablemente (por ejemplo, pulsando un enlace de anuncio o siguiendo una cuenta). Estos resultados están corroborados por una comprobación de la verdad sobre el terreno, basada en encuestas. Por ejemplo, dirigirse al 10 por ciento de usuarios en términos de más alta apertura y menor rango emocional dio lugar a aumentos en la tasa de pulsación de 6,8 al 11,3 por ciento y en la tasa de seguimiento de 4,7 al 8,8 por ciento.

Varios estudios recientes revelaron resultados similares para las características que se calculan a partir de los datos de las redes sociales. Un estudio reciente con datos del almacén minorista ha descubierto que las personas con puntuación alta en orden, autodisciplina y precaución y baja en falta de moderación tienen un 40 por ciento más de probabilidad de responder a los cupones que la población aleatoria. Un segundo estudio ha descubierto que las personas con valores específicos mostraron intereses de lectura específicos ([Hsieh et al. 2014](/docs/services/personality-insights?topic=personality-insights-references#hsieh2014)). Por ejemplo, las personas con un mayor valor de autotrascendencia demostraron un interés en la lectura de artículos sobre el entorno, y las personas con un valor más alto de superación personal mostraron un interés en la lectura de artículos sobre trabajo. Un tercer estudio de más de 600 usuarios de Twitter descubrió que las características de personalidad de una persona pueden predecir su preferencia de marca con una precisión del 65 por ciento.

Las siguientes secciones amplían estas conclusiones de alto nivel para describir la investigación y el desarrollo que hay detrás del servicio {{site.data.keyword.personalityinsightsshort}}. Para obtener más información sobre los estudios que aplican el servicio a casos concretos, consulte [El servicio en acción](/docs/services/personality-insights?topic=personality-insights-applied).

## Cómo comprender los modelos de personalidad
{: #researchModels}

Para el servicio {{site.data.keyword.personalityinsightsshort}}, {{site.data.keyword.IBM_notm}} ha desarrollado modelos para deducir puntuaciones para las dimensiones y facetas de los Cinco grandes, las Necesidades y los Valores a partir de información textual. Los modelos de los que informa el servicio se basan en la investigación en los campos de la psicología, la psicolingüística y el marketing:

-   El [modelo de los cinco grandes](/docs/services/personality-insights?topic=personality-insights-models) es uno de los modelos de personalidad más estudiados desarrollado por psicólogos ([Costa y McCrae, 1992](/docs/services/personality-insights?topic=personality-insights-references#costa1992) y [Norman, 1963](/docs/services/personality-insights?topic=personality-insights-references#norman1963)). Es el modelo de personalidad más ampliamente utilizado para describir cómo una persona se relaciona en general con el mundo. El servicio calcula las cinco dimensiones y treinta facetas del modelo. Se hace referencia normalmente a las dimensiones mediante el mnemónico *OCEAN*, donde *O* representa la apertura (Openness), *C* la responsabilidad (Conscientiousness), *E* la extraversión (Extraversion), *A* la simpatía (Agreeableness), y *N* la neurosis (Neuroticism). (Dado que el término neurosis puede tener un significado clínico específico, el servicio presenta tal información con un título más general: Rango emocional).
-   [Necesidades](/docs/services/personality-insights?topic=personality-insights-needs) son un aspecto importante del comportamiento humano. La bibliografía de investigación sugiere que varios tipos de necesidades humanas son universales e influyen directamente en el comportamiento de los consumidores ([Kotler y Armstrong, 2013](/docs/services/personality-insights?topic=personality-insights-references#kotler2013) y [Ford, 2005](/docs/services/personality-insights?topic=personality-insights-references#ford2005)). Las doce categorías de necesidades de las que informa el servicio están descritas en la bibliografía de marketing como deseos que una persona espera cumplir al considerar un producto o servicio.
-   [Valores](/docs/services/personality-insights?topic=personality-insights-values) transmite lo que es más importante para una persona. Son "objetivos deseables y transituacionales, distintos en importancia, que sirven como principios rectores en la vida de las personas" ([Schwartz, 2006](/docs/services/personality-insights?topic=personality-insights-references#schwartz2006)). Schwartz resume cinco características que son comunes a todos los valores:

    1.  Los valores son creencias.
    1.  Los valores son un constructo motivacional.
    1.  Los valores trascienden acciones y situaciones específicas.
    1.  Los valores guían la selección o evaluación de acciones, políticas, personas y eventos.
    1.  Los valores varían en función de la importancia relativa y se pueden categorizar por importancia.

    El servicio calcula los cinco valores humanos básicos propuestos por Schwartz y validados en más de veinte países ([Schwartz, 1992](/docs/services/personality-insights?topic=personality-insights-references#schwartz1992)).

## Cómo se deducen las características de personalidad
{: #researchInfer}

El servicio {{site.data.keyword.personalityinsightsshort}} deduce las características de personalidad de la información textual basada en un enfoque de vocabulario abierto. Este método refleja la tendencia más reciente en la investigación sobre la deducción de personalidad ([Arnoux et al., 2017](/docs/services/personality-insights?topic=personality-insights-references#arnoux2017), [Schwartz et al., 2013](/docs/services/personality-insights?topic=personality-insights-references#schwartz2013) y [Plank y Hovy, 2015](/docs/services/personality-insights?topic=personality-insights-references#plank2015)).

El servicio señaliza en primer lugar el texto de entrada para desarrollar una representación en un espacio de dimensión *n*. El servicio utiliza una técnica de inclusión de palabras de código abierto, [GloVe ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://nlp.stanford.edu/projects/glove/){: new_window}, para obtener una representación de vectores para las palabras que se encuentran en el texto de entrada ([Pennington et al., 2014](/docs/services/personality-insights?topic=personality-insights-references#pennington2014)). Más tarde, suministra esta representación a un algoritmo de aprendizaje de máquina que deduce un perfil de personalidad con las características de los Cinco grandes, de las Necesidades y de los Valores. Para entrenar el algoritmo, el servicio utiliza puntuaciones procedentes de encuestas realizadas entre miles de usuarios junto con los datos de sus canales de Twitter.

{{site.data.keyword.IBM_notm}} ha desarrollado los modelos para todos los idiomas soportados de forma idéntica. Los modelos fueron desarrollados independientemente de la demografía de los usuarios como edad, sexo o cultura. En el futuro, {{site.data.keyword.IBM_notm}} puede desarrollar modelos específicos para distintas categorías demográficas.

Las versiones anteriores del servicio utilizaban el diccionario de psicolingüística LIWC (Linguistic Inquiry and Word Count) con su modelo de aprendizaje de máquina. Sin embargo, el enfoque de vocabulario abierto consigue mejores resultados que el modelo basado en LIWC. Para obtener más información sobre la precisión del servicio para cada idioma en términos de Error absoluto medio promedio (MAE, Average Mean Absolute Error) y correlación, consulte [Cómo de preciso es el servicio](#researchPrecise). Para obtener instrucciones sobre el suministro de texto de entrada para lograr los resultados más precisos, consulte [Proporcionar suficiente entrada](/docs/services/personality-insights?topic=personality-insights-input#sufficient).

## Cómo de preciso es el servicio
{: #researchPrecise}

{{site.data.keyword.IBM_notm}} realizó un estudio de validación para comprender la precisión del enfoque del servicio para deducir un perfil de personalidad. {{site.data.keyword.IBM_notm}} ha recopilado respuestas de encuestas y publicaciones de Twitter desde entre 1500 y 2000 participantes para todas las características e idiomas. Para establecer *datos de campo*, los participantes tomaron cuatro conjuntos de pruebas psicométricas estándares:

-   Un modelo de los cinco grandes con 50 elementos derivados de IPIP (International Personality Item Pool)
-   Una faceta de 120 elementos derivada de IPIP-NEO (IPIP Neuroticism, Extraversion &amp; Openness)
-   Unas Necesidades fundamentales de 52 elementos desarrolladas por {{site.data.keyword.IBM_notm}}
-   Unos Valores básicos de 26 elementos desarrollados por Schwartz

{{site.data.keyword.IBM_notm}} a continuación comparó las puntuaciones derivadas de sus modelos con las puntuaciones basadas en encuestas para los usuarios de Twitter. Basándose en estos resultados, {{site.data.keyword.IBM_notm}} determinó el [Error absoluto medio promedio](#preciseMAE) y [correlación promedio](#preciseCorrelation) entre las puntuaciones deducidas y reales para las distintas categorías de características de personalidad. El [MAE promedio por idioma y correlación](#precisePerLanguage) proporciona los valores estadísticos para cada idioma soportado.

### Error absoluto medio promedio
{: #preciseMAE}

*MAE (Error absoluto medio, Mean Absolute Error)* es una métrica utilizada para medir la diferencia entre los valores reales y predichos. Para el servicio {{site.data.keyword.personalityinsightsshort}}, el valor real, o datos de campo, es la puntuación de personalidad que se ha obtenido administrando una encuesta de personalidad. El valor predicho es la puntuación que produce los modelos del servicio.

{{site.data.keyword.IBM_notm}} ha calculado el MAE tomando el promedio del valor absoluto de la diferencia entre las puntuaciones reales y predichas. {{site.data.keyword.IBM_notm}} ha utilizado el valor absoluto porque predecir más o menos del valor real es irrelevante. Mientras haya una diferencia, el modelo es penalizado por la magnitud del error. Cuanto menor sea el MAE, mejor será el rendimiento del modelo. {{site.data.keyword.IBM_notm}} utiliza una escala de 0 a 1 para MAE, donde 0 significa que no hay error (el valor predicho es exactamente el mismo que el valor real), y 1 significa error máximo.

### Correlación promedio
{: #preciseCorrelation}

*Correlación promedio* es un término estadístico que mide la interdependencia de dos variables. Con esta medida, {{site.data.keyword.IBM_notm}} ha medido la correlación entre las puntuaciones deducidas y reales para las distintas categorías de características de personalidad. Si la puntuación predicha realiza el seguimiento de cerca de los resultados reales, la puntuación de correlación es alta; de lo contrario, la puntuación será baja.

{{site.data.keyword.IBM_notm}} mide la correlación en una escala de -1 a 1:

-   1 indica una relación lineal directa (creciente) perfecta.
-   -1 indica una relación lineal inversa (decreciente) perfecta.

En todos los demás casos, el valor está entre estos extremos. Si las variables son independientes (no tienen relación en absoluto), la correlación será 0.

{{site.data.keyword.IBM_notm}} busca números que estén más cerca del 1 para obtener las mejores predicciones. Pero las personalidades son difíciles de predecir basadas únicamente en texto, y es raro ver correlaciones que superen el 0,4 para estos tipos de modelos psicológicos. En la bibliografía de investigación para este dominio, las correlaciones superiores a 0,2 se consideran aceptables.

### MAE promedio por idioma y correlación
{: #precisePerLanguage}

La tabla siguiente muestra los resultados de MAE promedio por idioma y correlación para el servicio {{site.data.keyword.personalityinsightsshort}}. Los resultados colocan el servicio al frente de la deducción de personalidad de datos textuales como indican [Schwartz et al. (2013)](/docs/services/personality-insights?topic=personality-insights-references#schwartz2013) y [Plank y Hovy (2015)](/docs/services/personality-insights?topic=personality-insights-references#plank2015).

<table summary="Para cada fila que identifica un idioma en la primera columna, las dos filas siguientes proporcionan el MAE promedio y la correlación promedio de las dimensiones de los Cinco Grandes, las facetas de los Cinco Grandes, las Necesidades y los Valores.">
  <caption>Tabla 1. MAE y correlación promedio por idioma</caption>
  <tr>
    <th id="language" style="text-align:left; vertical-align:bottom">
      Idioma
    </th>
    <th id="dimensions" style="text-align:center; vertical-align:bottom">
      Dimensiones de los Cinco grandes
    </th>
    <th id="facets" style="text-align:center; vertical-align:bottom">
      Facetas de los Cinco grandes
    </th>
    <th id="needs" style="text-align:center; vertical-align:bottom">
      Necesidades
    </th>
    <th id="values" style="text-align:center; vertical-align:bottom">
      Valores
    </th>
  </tr>
  <tr>
    <th id="arabic" headers="language" colspan="5" style="text-align:left">
      **Árabe**
    </th>
  </tr>
  <tr>
    <td headers="language arabic" style="text-align:left">
      MAE promedio
    </td>
    <td headers="dimensions arabic" style="text-align:center">
      0,09
    </td>
    <td headers="facets arabic" style="text-align:center">
      0,12
    </td>
    <td headers="needs arabic" style="text-align:center">
      0,11
    </td>
    <td headers="values arabic" style="text-align:center">
      0,10
    </td>
  </tr>
  <tr>
    <td headers="language arabic" style="text-align:left">
      Correlación promedio
    </td>
    <td headers="dimensions arabic" style="text-align:center">
      0,17
    </td>
    <td headers="facets arabic" style="text-align:center">
      0,14
    </td>
    <td headers="needs arabic" style="text-align:center">
      0,13
    </td>
    <td headers="values arabic" style="text-align:center">
      0,14
    </td>
  </tr>
  <tr>
    <th id="english" headers="language" colspan="5" style="text-align:left">
      **Inglés**
    </th>
  </tr>
  <tr>
    <td headers="language english" style="text-align:left">
      MAE promedio
    </td>
    <td headers="dimensions english" style="text-align:center">
      0,12
    </td>
    <td headers="facets english" style="text-align:center">
      0,12
    </td>
    <td headers="needs english" style="text-align:center">
      0,11
    </td>
    <td headers="values english" style="text-align:center">
      0,11
    </td>
  </tr>
  <tr>
    <td headers="language english" style="text-align:left">
      Correlación promedio
    </td>
    <td headers="dimensions english" style="text-align:center">
      0,33
    </td>
    <td headers="facets english" style="text-align:center">
      0,28
    </td>
    <td headers="needs english" style="text-align:center">
      0,22
    </td>
    <td headers="values english" style="text-align:center">
      0,24
    </td>
  </tr>
  <tr>
    <th id="japanese" headers="language" colspan="5" style="text-align:left">
      **Japonés**
    </th>
  </tr>
  <tr>
    <td headers="language japanese" style="text-align:left">
      MAE promedio
    </td>
    <td headers="dimensions japanese" style="text-align:center">
      0,11
    </td>
    <td headers="facets japanese" style="text-align:center">
      0,12
    </td>
    <td headers="needs japanese" style="text-align:center">
      0,11
    </td>
    <td headers="values japanese" style="text-align:center">
      0,11
    </td>
  </tr>
  <tr>
    <td headers="language japanese" style="text-align:left">
      Correlación promedio
    </td>
    <td headers="dimensions japanese" style="text-align:center">
      0,27
    </td>
    <td headers="facets japanese" style="text-align:center">
      0,22
    </td>
    <td headers="needs japanese" style="text-align:center">
      0,25
    </td>
    <td headers="values japanese" style="text-align:center">
      0,19
    </td>
  </tr>
  <tr>
    <th id="korean" headers="language" colspan="5" style="text-align:left">
      **Coreano**
    </th>
  </tr>
  <tr>
    <td headers="language korean" style="text-align:left">
      MAE promedio
    </td>
    <td headers="dimensions korean" style="text-align:center">
      0,11
    </td>
    <td headers="facets korean" style="text-align:center">
      0,12
    </td>
    <td headers="needs korean" style="text-align:center">
      0,11
    </td>
    <td headers="values korean" style="text-align:center">
      0,11
    </td>
  </tr>
  <tr>
    <td headers="language korean" style="text-align:left">
      Correlación promedio
    </td>
    <td headers="dimensions korean" style="text-align:center">
      0,21
    </td>
    <td headers="facets korean" style="text-align:center">
      0,21
    </td>
    <td headers="needs korean" style="text-align:center">
      0,13
    </td>
    <td headers="values korean" style="text-align:center">
      0,12
    </td>
  </tr>
  <tr>
    <th id="spanish" headers="language" colspan="5" style="text-align:left">
      **Español**
    </th>
  </tr>
  <tr>
    <td headers="language spanish" style="text-align:left">
      MAE promedio
    </td>
    <td headers="dimensions spanish" style="text-align:center">
      0,10
    </td>
    <td headers="facets spanish" style="text-align:center">
      0,12
    </td>
    <td headers="needs spanish" style="text-align:center">
      0,12
    </td>
    <td headers="values spanish" style="text-align:center">
      0,11
    </td>
  </tr>
  <tr>
    <td headers="language spanish" style="text-align:left">
      Correlación promedio
    </td>
    <td headers="dimensions spanish" style="text-align:center">
      0,35
    </td>
    <td headers="facets spanish" style="text-align:center">
      0,21
    </td>
    <td headers="needs spanish" style="text-align:center">
      0,24
    </td>
    <td headers="values spanish" style="text-align:center">
      0,19
    </td>
  </tr>
</table>

Para calcular las puntuaciones del percentil, {{site.data.keyword.IBM_notm}} ha recopilado un conjunto de datos muy grande de usuarios de Twitter y ha calculado sus retratos de personalidad:

-   Un millón de usuarios de inglés
-   Doscientos mil usuarios de coreano
-   Cien mil usuarios de árabe y de japonés
-   Ochenta mil usuarios para español

{{site.data.keyword.IBM_notm}} a continuación ha comparado las puntuaciones en bruto de cada perfil calculado con la distribución de perfiles de los conjuntos de datos para determinar los percentiles.

Para la entrada en árabe y coreano, el servicio no puede producir percentiles significativos ni puntuaciones en bruto para algunas características de personalidad. Para obtener más información, consulte [Limitaciones para entrada en árabe y coreano](/docs/services/personality-insights?topic=personality-insights-numeric#limitations).
{: note}

## Comprensión de las preferencias de consumo
{: #researchPrefs}

Se ha estudiado la relación entre personalidad y comportamiento de compra en diversos productos y servicios:

-   [Chen (2007)](/docs/services/personality-insights?topic=personality-insights-references#chen2007), al probar preferencias sobre alimentos orgánicos, ha indicado que las características de personalidad del individuo juegan un papel importante en el establecimiento de criterios personales de elección de alimentos.
-   [Schlegelmilch et al. (1996)](/docs/services/personality-insights?topic=personality-insights-references#schlegelmilch1996) han explorado la relación entre variables de personalidad y comportamiento de compra proambiental. Los autores mostraron que la conciencia ambiental global de los consumidores tiene un impacto positivo en las decisiones de compra ecológica.
-   [Hymbaugh y Garrett (2007)](/docs/services/personality-insights?topic=personality-insights-references#hymbaugh1974) han investigado la relación entre personalidad y paracaidismo y han descubierto que las personas con una puntuación alta en osadía y búsqueda de emociones se suelen dar el capricho del paracaidismo. (Para obtener más información, consulte [Supervisión de riesgos](/docs/services/personality-insights?topic=personality-insights-applied#otherRisk)).

Aplicar estas relaciones conocidas entre comportamientos de consumo y personalidad es difícil. La mayoría de estos trabajos han utilizado datos de personalidad derivados de encuestas, y sus modelos no están públicamente disponibles. Por lo tanto, {{site.data.keyword.IBM_notm}} ha decidido obtener estos modelos de preferencias de consumo directamente. Al entrenar los modelos, {{site.data.keyword.IBM_notm}} ha utilizado las puntuaciones de personalidad que se han devuelto desde el servicio {{site.data.keyword.personalityinsightsshort}} como características. Como resultado, al aplicar estos modelos para calcular las características de personalidad de un usuario con el servicio, las predicciones podrían ser más precisas.

## Cómo se deducen las preferencias de consumo
{: #researchInferPrefs}

El servicio {{site.data.keyword.personalityinsightsshort}} deduce preferencias de consumo basadas en los resultados de su perfil de personalidad para el autor del texto de entrada. En la bibliografía existente, {{site.data.keyword.IBM_notm}} ha identificado las 104 preferencias de consumo que han demostrado estar correlacionadas con la personalidad. Entre estas, se incluyen preferencias relacionadas con las compras, las películas, la música, y otras categorías. {{site.data.keyword.IBM_notm}} a continuación ha creado una encuesta psicométrica para evaluar la inclinación de un individuo para cada comportamiento de consumo.

{{site.data.keyword.IBM_notm}} ha obtenido respuestas a su encuesta de cerca de 600 personas para las que también tenía datos de Twitter (más de 200 tweets creados por los propios usuarios). {{site.data.keyword.IBM_notm}} ha enviado los tweets al servicio para recopilar un perfil de personalidad para cada persona. A continuación, ha creado un clasificador para cada preferencia de consumo, donde el conjunto de características de entrada era la información de personalidad.

Para la integración con el servicio, {{site.data.keyword.IBM_notm}} ha seleccionado solo aquellas preferencias de consumo para las que la clasificación basada en la personalidad ha funcionado al menos un 9 por ciento mejor que la clasificación aleatoria. De las 104 preferencias originales, 42 satisfacen este criterio y se exponen como preferencias de consumo por el servicio.

<!--
COMMENTED FOR REMOVAL OF LIWC AND SAMPLING ERROR 08/10/2016

## How media influence inferred characteristics

{{site.data.keyword.IBM_notm}} conducted a validation study to understand the effect of media on inferred characteristics. To determine the accuracy of the service's approach to estimating characteristics, {{site.data.keyword.IBM_notm}} compared scores that were derived by its models with survey-based scores for Twitter users (for instance, approximately 500 users for English and more than 600 for Spanish).

To establish ground truth, participants took three sets of standard psychometric tests: 50-item Big Five (derived from the International Personality Item Pool, or IPIP), 52-item fundamental Needs (developed by {{site.data.keyword.IBM_notm}}), and 26-item basic Values (developed by Schwartz). {{site.data.keyword.IBM_notm}} conducted the study in two phases:

-   For the first study, conducted in 2013, {{site.data.keyword.IBM_notm}} recruited 256 Twitter users ([Gou and others, 2014](/docs/services/personality-insights?topic=personality-insights-references#gou2014)). Although the models were learned from different sources, {{site.data.keyword.IBM_notm}} found that for more than 80 percent of the Twitter users, scores for characteristics that were inferred for all three models correlated significantly with survey-based scores (p-value &lt; 0.05 and correlation coefficient between 0.05 and 0.80). Specifically, scores that were derived by the service correlated with survey-based scores as follows:
    -   For 80.8 percent of participants' Big Five scores (p-value &lt; 0.05 and correlation coefficients between 0.05 and 0.75)
    -   For 86.6 percent of participants' Needs scores (p-value &lt; 0.05 and correlation coefficient between 0.05 and 0.80)
    -   For 98.21 percent of participants' Values scores (p-value &lt; 0.05 and correlation coefficients between 0.05 and 0.55)
-   For the second study, conducted in 2015, {{site.data.keyword.IBM_notm}} recruited another set of 237 Twitter users. The study found that for Big Five and Values, scores for inferred characteristics correlated significantly with survey-based scores (p-value &lt; 0.05 and correlation coefficient between 0.07 and 0.21) for every Twitter user. For needs, such significant correlation was observed for 90 percent of the users (p value &lt; 0.05 and correlation coefficient between 0.01 and 0.20).

In both studies, participants also rated on a five-point scale how well each derived characteristic matched their perceptions of themselves. Their ratings suggest that the inferred characteristics largely matched their self-perceptions. Specifically, means of all ratings were above 3 ("somewhat") out of 5 ("perfect").

-   For the 256 Twitter users of the first study, means were 3.4 (with a standard deviation of 1.14) for Big Five, 3.39 (with a standard deviation of 1.34) for Needs, and 3.13 (with a standard deviation of 1.17) for Values.
-   For the 237 Twitter users of the second study, means were 3.31 (with a standard deviation of 1.18) for Big Five, 3.37 (with a standard deviation of 1.22) for Needs, and 3.36 (with a standard deviation of 1.18) for Values.

COMMENTED FOR REMOVAL OF LIWC AND SAMPLING ERROR 08/10/2016
-->

## Notas sobre encuestas de personalidad
{: #researchSurveys}

Al desarrollar el servicio {{site.data.keyword.personalityinsightsshort}}, {{site.data.keyword.IBM_notm}} se ha basado en encuestas de personalidad para establecer los datos de campo para deducir la personalidad. Los datos de campo hacen referencia a los datos reales obtenidos mediante la observación directa en lugar de mediante inferencia. Una medida típica de precisión para cualquier modelo de aprendizaje de máquina es comparar las puntuaciones deducidas por el modelo con los datos de campo. Las secciones anteriores describen cómo ha utilizado {{site.data.keyword.IBM_notm}} las encuestas para validar la precisión del servicio.

Las notas siguientes aclaran el uso de las encuestas de personalidad y de la estimación de personalidad basada en encuesta:

-   Las encuestas de personalidad son largas y se tarda mucho tiempo en completarlas. Los resultados de las encuestan están restringidos por el número de usuarios de Twitter que quisieron y estuvieron disponibles para participar en el estudio de {{site.data.keyword.IBM_notm}}. {{site.data.keyword.IBM_notm}} planea realizar estudios de validación con más usuarios, así como con usuarios de otros medios en línea como el correo electrónico, los blogs y los foros.
-   La estimación de personalidad basada en encuestas se basa en el autoinforme, lo que no siempre puede ser un verdadero reflejo de la personalidad de alguien: Algunos usuarios pueden dar respuestas ruidosas a tales encuestas. Para reducir el ruido, {{site.data.keyword.IBM_notm}} ha filtrado las respuestas de la encuesta incluyendo preguntas de comprobación de la atención y descartando las encuestas realizadas demasiado rápido.
-   Aunque la correlación entre las puntuaciones deducidas y basadas en encuesta es positiva y significativa, los resultados implican que las puntuaciones deducidas no pueden siempre correlacionarse con los resultados basados en encuestas. Algunos investigadores de fuera de {{site.data.keyword.IBM_notm}} también han realizado experimentos para comparar cómo coinciden las puntuaciones bien deducidas con las obtenidas de encuestas, y nadie ha informado de una coincidencia totalmente coherente:
    -   [Golbeck et al. (2011)](/docs/services/personality-insights?topic=personality-insights-references#golbeck2011) han informado de un índice de errores del 10 al 18 por ciento al hacer coincidir las puntuaciones deducidas con puntuaciones basadas en encuestas.
    -   [Sumner et al. (2012)](/docs/services/personality-insights?topic=personality-insights-references#sumner2012) han informado de aproximadamente un 65 por ciento de precisión para la predicción de personalidad.
    -   [Mairesse y Walker (2006)](/docs/services/personality-insights?topic=personality-insights-references#mairesse2006) han informado de entre un 60 y un 70 por ciento de precisión para la predicción de personalidad de los Cinco grandes.

En general, está ampliamente aceptado en la bibliografía de investigación que las puntuaciones autoinformadas de encuestas de personalidad no siempre coinciden totalmente con las puntuaciones deducidas del texto. Lo que es más importante, sin embargo, es que {{site.data.keyword.IBM_notm}} ha encontrado que las características deducidas de texto a menudo pueden predecir fiablemente el comportamiento del mundo real.
