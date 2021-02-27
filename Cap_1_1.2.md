# Demostraciones
## 1.1 Introduccion
La lógica es la estructura sobre la cual las demostraciones rigurosas son construidas. Sin algunos conceptos básicos de lógica,los cuales estudiaremos en este capıtulo, no es posible construir demostraciones correctas.Será suficiente para nuestros propósitos un acercamiento a estos conceptos de lógica de una manera informal (y breve). Si bien la lógica es el fundamento del raciocinio matemático, es importante no sobre enfatizar el uso de la la lógica en las matematicas. Fuera de el campo de la lógica matemática, las demostraciones en matemáicas casi nunca involucran lógica formal, tampoco ellas generalmente involucran símbolos de lógica (aunque necesitaremos de ellos en este capítulo).

La lógica es un tema antiguo, que se remonta en Occidente a pensadores como Aristóteles, así como a antiguos pensadores no occidentales. Al haberse originado como un análisis de la argumentación válida, la lógica está fuertemente vinculada a la filosofía. Los matemáticos han desarrollado un enfoque matemático de la lógica, aunque no existe una frontera rígida entre el estudio de la lógica por parte de los matemáticos y de los filósofos; de hecho, algunos lógicos han destacado en ambos campos. Algunos aspectos de la lógica han adquirido una nueva importancia en los últimos años con la llegada de los ordenadores, ya que las ideas lógicas están en la base de algunos aspectos de la informática. Para más información sobre la lógica tradicional, véase [Cop68], que es muy legible, y [KMM80], que es más formal. Para la lógica matemática, véase [End72], [Mal79] o [EFT94]. Véase la introducción al capítulo 1 del último de estos libros para una discusión de la relación de la lógica matemática con la lógica tradicional. Para una interesante discusión de la lógica, véase [EC89, capítulos 19 y 20]. Para un tratamiento de la lógica en el contexto de la informática, véase [DSW94, Parte 3]. Aunque la lógica informal que discutimos en este capítulo proporciona la base para las pruebas rigurosas, la lógica informal no es en sí misma rigurosa. De ahí que el presente capítulo se diferencie sustancialmente del resto del libro en que es totalmente informal.

Dado que sólo empezaremos a hablar de las pruebas matemáticas en el próximo capítulo, por ahora nuestra discusión no está escrita en el estilo apropiado para las pruebas rigurosas. Lo mismo ocurre con los ejercicios de este capítulo. En este capítulo, y a lo largo de todo el texto, utilizaremos las propiedades básicas de los números enteros, racionales y reales en algunos de nuestros ejemplos. Supondremos que el lector está familiarizado de manera informal con estos números. Las propiedades básicas de los números naturales se discutirán brevemente en la sección 6.2. En el Apéndice encontrará una breve lista de algunas de las propiedades estándar de los números reales; en [Blo11, capítulos 1 y 2] encontrará un tratamiento detallado de los sistemas numéricos estándar. El aspecto de las matemáticas que estamos aprendiendo en este texto consiste en enunciar resultados, como teoremas, y luego demostrarlos. Por supuesto, hay una gran cantidad de intuición, exploración informal, cálculo y trabajo pesado para averiguar qué es lo que se intenta demostrar, pero eso es otra cuestión. La lógica, en su forma más básica, se ocupa de la construcción de enunciados bien formados y de argumentos válidos; estas dos nociones formarán el marco lógico para el correcto planteamiento y demostración de teoremas. La matemática real de las demostraciones tendrá que esperar hasta el capítulo 2 

## 1.2 Statements
Cuando demostramos teoremas en matemáticas, estamos demostrando la verdad de ciertos enunciados. Por lo tanto, tenemos que empezar nuestra discusión sobre la lógica con una mirada a los enunciados, y a cómo reconocemos ciertas afirmaciones como verdaderas o falsas. Un enunciado es cualquier cosa que podamos decir, escribir o expresar de otro modo que sea verdadera o falsa. Por ejemplo, la expresión "Fred Smith tiene veinte años" es un enunciado, porque puede ser verdadero o falso. Puede que no sepamos si esta afirmación es realmente verdadera o no, porque para saberlo tendríamos que conocer alguna información sobre Fred Smith, por ejemplo su fecha de nacimiento, y puede que no dispongamos de esa información. Para que algo sea una afirmación, tiene que ser verdadera o falsa en principio; no importa si podemos verificar personalmente su verdad o falsedad. Por el contrario, la expresión "Cómete una piña" no es una afirmación, porque no puede decirse que sea verdadera o falsa.

Es importante distinguir entre las expresiones inglesas que podemos decir y las afirmaciones que hacen. Por ejemplo, cuando escribimos "Fred Smith is twenty years old", también podríamos haber escrito "Fred Smith's age is twenty". Estas dos expresiones inglesas no son idénticas porque no tienen exactamente las mismas palabras, pero ciertamente hacen la misma afirmación. Por comodidad, nos referiremos a expresiones como "Fred Smith tiene veinte años" como afirmaciones, aunque debemos darnos cuenta de que en realidad nos estamos refiriendo a la afirmación que hace la expresión. En la práctica, no debería haber ninguna confusión sobre este punto.

Cuando tratemos con afirmaciones, partiremos de dos premisas: todo enunciado es verdadero o falso, y ningún enunciado es a la vez verdadero y falso. La primera de estas suposiciones, a menudo conocida como la Ley del Medio Excluido (y conocida habitualmente como bivalencia), puede parecer bastante inocua, pero de hecho algunos matemáticos han optado por trabajar sin este poderoso axioma. La mayoría de los matemáticos sí utilizan la Ley del Medio Excluido (el autor de este libro entre ellos), y no dudaremos en utilizarla implícitamente a lo largo de este libro. Una de las consecuencias de esta ley es que si una afirmación no es falsa, entonces debe ser verdadera. Por tanto, para demostrar que algo es verdadero, bastaría con demostrar que no es falso; esta estrategia es muy útil en algunas pruebas. Los matemáticos que no aceptan la Ley del Medio Excluido no considerarán válida ninguna prueba que utilice la ley (aunque la incorrección de una prueba no implica la falsedad del enunciado que se demuestra, sino que hay que buscar otra prueba). Véase [Wil65, capítulo 10] o [Cop68, sección 8.7] para una mayor discusión de estas cuestiones.

Si lo único que pudiéramos hacer con los enunciados es decidir si algo es un enunciado o no, todo el concepto carecería de interés. Lo que hace que los enunciados sean más valiosos para nuestros propósitos es que hay una serie de formas útiles de formar nuevos enunciados a partir de otros anteriores. Un análogo a esto serían las formas que tenemos de combinar números para obtener otros nuevos, como la suma y la multiplicación; si no tuviéramos estas operaciones, los números no serían muy interesantes. En esta sección se discutirán cinco formas de formar nuevos enunciados a partir de otros antiguos, que corresponden a las expresiones inglesas: and; or; not; if, then; if and only if. Los enunciados a partir de los cuales formamos uno nuevo se denominarán a veces enunciados componentes del nuevo enunciado.

Para definir estas cinco construcciones, P y Q son enunciados. Nuestra primera construcción, la conjunción de P y Q, que se denota P ∧ Q, es el enunciado que, intuitivamente, es verdadero si tanto P como Q son verdaderos, y es falso en caso contrario. Leemos P ∧ Q como "P y Q". La definición precisa de P ∧ Q viene dada por la "tabla de verdad"

<p align="center">
<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Btabular%7D%7Bcc%7Cc%7D%0AP%20%26%20Q%20%26%20P%24%5Cland%24Q%20%5C%5C%0A%5Chline%0AT%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20F%20%5C%5C%0A%5Cend%7Btabular%7D%0A" alt="
\begin{tabular}{cc|c}
P &amp; Q &amp; P$\land$Q \\
\hline
T &amp; T &amp; T \\
T &amp; F &amp; F \\
F &amp; T &amp; F \\
F &amp; F &amp; F \\
\end{tabular}
" />
</p>

Esta tabla de verdad, y todas las demás similares, muestra si el nuevo enunciado (en este caso P∧Q) es verdadero o falso para cada combinación posible de la verdad o falsedad de cada uno de P y Q.

 Como ejemplo de conjunción, dejemos que P = "hoy llueve" y que Q = "hoy hace frío". El enunciado P∧Q sería formalmente "hoy llueve y hoy hace frío". Por supuesto, podríamos expresar la misma idea de forma más sucinta en inglés diciendo "it is raining and cold today". En general, intentaremos utilizar enunciados que se lean bien en inglés, además de ser lógicamente correctos. El uso coloquial de la palabra "and" difiere del uso matemático indicado anteriormente. El uso matemático significa la tabla de verdad anterior, y nada más, mientras que coloquialmente hay otros significados además de éste. Una fuente de confusión con la palabra "y" que conviene evitar es el uso coloquial de esta palabra en el sentido de "por tanto". Por ejemplo, no es raro encontrar una frase como "De la ecuación anterior vemos que 3x < 6, y x < 2". Lo que realmente se quiere decir con esta frase es "De la ecuación anterior vemos que 3x < 6, lo que implica que x < 2". Este uso de "y" para significar "por lo tanto" prácticamente nunca es necesario, y como puede llevar a posibles confusiones, es mejor evitarlo. Estaría bien decir "De la ecuación anterior vemos que 3x < 6, y x < 2", porque en ese caso la "y" está funcionando sólo como la conjunción entre las dos partes de la oración, y no es un sustituto de la palabra "por lo tanto". 

Otro uso coloquial de "y" que difiere del uso matemático, aunque es menos probable que nos cause problemas aquí, se ve en la afirmación "Fred y Susan están casados". Interpretado en el sentido matemático estricto, sólo podríamos deducir de este enunciado que cada uno de Fred y Susan está casado, posiblemente con personas diferentes. En cambio, en el uso coloquial, este enunciado se interpretaría casi siempre como que Fred y Susan están casados entre sí. En la escritura literaria, suele ser valiosa cierta medida de ambigüedad, o algún significado implícito que no se declara explícitamente. En cambio, en matemáticas, la precisión es fundamental y la ambigüedad debe evitarse a toda costa. Cuando se utilice un término matemático, hay que atenerse siempre a la definición matemática precisa, independientemente de cualquier otro uso coloquial. Por ejemplo, en la escritura matemática, si quisiéramos indicar que Fred y Susana están casados entre sí, deberíamos decir explícitamente "Fred y Susana están casados entre sí", y si quisiéramos decir sólo que cada uno de Fred y Susana está casado, deberíamos decir "Fred está casado y Susana está casada". 

Nuestra segunda construcción, la disyunción de P y Q, que se denota P∨Q, es el enunciado que, intuitivamente, es verdadero si P es verdadero o Q es verdadero o ambos son verdaderos, y es falso en caso contrario. Leemos P∨Q como "P o Q". La definición precisa de P∨Q es dada por la tabla de verdad 


<p align ="center">
<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Btabular%7D%7Bcc%7Cc%7D%0AP%20%26%20Q%20%26%20P%24%5Clor%24Q%20%5C%5C%0A%5Chline%0AT%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20T%20%5C%5C%0AF%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20F%20%5C%5C%0A%5Cend%7Btabular%7D%0A" alt="
\begin{tabular}{cc|c}
P &amp; Q &amp; P$\lor$Q \\
\hline
T &amp; T &amp; T \\
T &amp; F &amp; T \\
F &amp; T &amp; T \\
F &amp; F &amp; F \\
\end{tabular}
" />
</p>

La verdad del enunciado P∨Q significa que al menos una de P o Q es verdadera. Aunque escribimos P∨Q en inglés como "P or Q", es muy importante distinguir el uso matemático de la palabra "or" del uso coloquial de la palabra. El uso matemático de la palabra "o" siempre significa un "o" inclusivo, de modo que si "P o Q" es verdadero, entonces o P es verdadero, o Q es verdadero, o ambos P y Q son verdaderos. En cambio, el uso coloquial de la palabra "o" suele significar una "o" exclusiva, que no permite que tanto P como Q sean verdaderas. En este texto, al igual que en todos los trabajos matemáticos, siempre nos referiremos a una "o" inclusiva, como se indica en la tabla de verdad anterior. 

Un ejemplo sencillo de disyunción es el enunciado "mi coche es rojo o lloverá hoy". Este enunciado tiene la forma P ∨ Q, donde P = "mi coche es rojo", y Q = "lloverá hoy". La verdad de este enunciado implica que al menos uno de los enunciados "mi coche es rojo" o "lloverá hoy" es verdadero. Lo único que no se permite es que tanto "mi coche es rojo" como "lloverá hoy" sean falsos.

Considere ahora el enunciado "esta noche veré una obra de teatro o veré una película". En el uso coloquial sería común interpretar este enunciado como un o exclusivo, lo que significa que o bien veré una obra de teatro, o bien veré una película, pero no ambas cosas. En el uso coloquial, si quisiera incluir la posibilidad de que pudiera ver tanto una obra de teatro como una película, probablemente diría "esta noche veré una obra de teatro, o veré una película, o ambas cosas". En cambio, en el uso matemático, la afirmación "esta noche veré una obra de teatro o veré una película" se interpretaría siempre como que o bien veré una obra de teatro, o bien veré una película, o ambas cosas. En el uso matemático, si quisiera excluir la posibilidad de que pudiera ver tanto una obra de teatro como una película, diría "esta noche veré una obra de teatro o veré una película, pero no ambas".

Otra fuente de confusión que implica la palabra "o" y que conviene evitar es el uso coloquial de esta palabra en el sentido de "es decir". Consideremos la frase coloquial "cuando estuve en Francia disfruté comiendo el fromage, o, queso local". Lo que realmente se quiere decir es "cuando estuve en Francia, disfruté comiendo el fromage local, es decir, el queso". Este uso de "o" es mejor evitarlo en la escritura matemática, porque prácticamente nunca es necesario y puede llevar a confusión. 

Nuestra tercera construcción, la negación de P, que se denota ¬P, es el enunciado que, intuitivamente, es verdadero si P es falso, y es falso si P es verdadero. Leemos ¬P como "no P".

La precisa definición de no p está definida en la tabla de verdad

<p align="center">

<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Btabular%7D%7Bc%7Cc%7D%0AP%20%26%20%C2%ACP%20%5C%5C%0A%5Chline%0AT%20%26%20F%5C%5C%0AF%20%26%20T%5C%5C%0A%5Cend%7Btabular%7D%0A" alt="
\begin{tabular}{c|c}
P &amp; ¬P \\
\hline
T &amp; F\\
F &amp; T\\
\end{tabular}
" />

</p>
Sea P = "A Susana le gustan los plátanos blandos". No funcionaría en inglés escribir ¬P como "Not Susan likes mushy bananas", tanto porque no es un inglés correcto, como porque parece que el sujeto de la frase es alguien llamado "Not Susan". La forma más directa de negar P es escribir ¬P = "no es el caso que a Susana le gusten los plátanos blandos". Aunque formalmente es correcta, esta última afirmación es bastante incómoda de leer, y es preferible sustituirla por una expresión más fácil de leer, por ejemplo "A Susana no le gustan los plátanos blandos". 

/Nuestras dos últimas formas de combinar enunciados, ambas relacionadas con la idea de implicación lógica, son algo más sutiles que las que hemos visto hasta ahora. Consideremos el enunciado "Si Fred se va de vacaciones, leerá un libro". ¿Qué significaría decir que esta afirmación es verdadera? No significaría que Fred se vaya de vacaciones, ni que vaya a leer un libro. La verdad de esta afirmación sólo significa que si ocurre una cosa (a saber, que Fred se va de vacaciones), entonces ocurrirá otra cosa (a saber, que Fred leerá un libro). En otras palabras, la única forma en que esta afirmación sería falsa sería si Fred se va de vacaciones, pero no lee un libro. La verdad de esta afirmación no diría nada sobre si Fred se irá o no de vacaciones, ni tampoco sobre lo que ocurrirá si Fred no se va de vacaciones. En particular, si Fred no se va de vacaciones, entonces no se contradice esta afirmación si Fred lee un libro. 

Consideremos ahora la afirmación "Si la hierba es verde, entonces París está en Francia". ¿Es cierto este enunciado? En el uso coloquial, esta afirmación parecería extraña, porque no parece haber ninguna conexión inherente, por no hablar de causalidad, entre la primera parte de la frase y la segunda. En el uso matemático, sin embargo, queremos poder decidir si un enunciado de cualquier forma es verdadero simplemente conociendo la verdad o falsedad de cada uno de sus enunciados componentes, sin tener que evaluar algo más vago como la causalidad. Por ejemplo, la afirmación "Las vacas producen leche y los coches hacen ruido" es ciertamente verdadera, aunque las dos partes de la frase no estén intrínsecamente conectadas. Del mismo modo, la afirmación "Si la hierba es verde, entonces París está en Francia" también debería poder decidirse como verdadera o falsa dependiendo únicamente de si "la hierba es verde" y "París está en Francia" son verdaderos o falsos. Al igual que en el párrafo anterior, adoptamos el enfoque de que un enunciado de la forma "si P entonces Q" debe ser verdadero si no se da el caso de que P sea verdadero y Q sea falso. Por lo tanto, dado que la hierba es efectivamente verde y París está efectivamente en Francia, la afirmación "Si la hierba es verde, entonces París está en Francia" es verdadera. Este enfoque de la noción de "si... entonces..." es algo diferente del uso coloquial del término, al igual que nuestros usos de "y" y "o" no eran los mismos que sus usos coloquiales. Formalizamos este enfoque de la siguiente manera. 

Nuestra cuarta construcción, el condicional de P a Q, que se denota P → Q, es el enunciado que, intuitivamente, es verdadero si nunca se da el caso de que P sea verdadero y Q sea falso. Leemos P → Q como "si P entonces Q". La definición precisa de P → Q se da en la tabla de verdad
<p align="center">
<img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Btabular%7D%7Bcc%7Cc%7D%0AP%20%26%20Q%20%26%20P%24%5Cto%24Q%20%5C%5C%0A%5Chline%0AT%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20T%20%5C%5C%0A%5Cend%7Btabular%7D%0A" alt="
\begin{tabular}{cc|c}
P &amp; Q &amp; P$\to$Q \\
\hline
T &amp; T &amp; T \\
T &amp; F &amp; F \\
F &amp; T &amp; T \\
F &amp; F &amp; T \\
\end{tabular}
" /></p>
Las dos primeras filas de la tabla de verdad son bastante razonables intuitivamente. Si P es verdadero y Q es verdadero, entonces ciertamente P → Q debe ser verdadero; si P es verdadero y Q es falso, entonces P → Q debe ser falso. Las filas tercera y cuarta de la tabla de verdad, que dicen que la afirmación P → Q es verdadera siempre que P es falsa, independientemente del valor de Q, son menos obvias intuitivamente. Sin embargo, no hay otra forma plausible de rellenar estas filas, dado que queremos que las entradas de la tabla de verdad dependan sólo de la verdad o falsedad de P y Q, y que la única situación que nos preocupa principalmente es que no queremos que P sea verdadera y Q sea falsa. Además, si hiciéramos falso el valor de P → Q en la tercera y cuarta filas, obtendríamos una tabla de verdad idéntica a la tabla de verdad para P ∧ Q, lo que haría que P → Q fuera redundante. La tabla de verdad anterior para P ∧ Q, que es universalmente aceptada por matemáticos y lógicos, puede parecer extraña a primera vista, y quizá incluso contraria a la intuición, pero es importante acostumbrarse a ella, porque siempre utilizaremos P → Q tal como la hemos definido.

 Un ejemplo sencillo de enunciado condicional es "si hoy llueve, entonces veré una película esta tarde". Este enunciado tiene la forma P → Q, donde P = "llueve hoy", y Q = "veré una película esta tarde". La verdad de este enunciado no dice que llueva hoy, ni que vaya a ver una película esta tarde. Sólo dice lo que ocurrirá si llueve hoy, que es que veré una película esta tarde. Si no llueve, todavía podría ver una película esta tarde, o podría no hacerlo; ambas posibilidades serían consistentes con la verdad del enunciado original "si llueve hoy, entonces veré una película esta tarde." 

Aunque lo normal es escribir P → Q, lo que cuenta no es el orden de escritura, sino la relación lógica. Sería idéntico escribir Q ← P en lugar de P → Q. De cualquier manera, cada uno de P y Q tiene un papel especificado -y distinto-. Por el contrario, si escribimos Q → P, entonces hemos intercambiado los papeles de Q y P, lo que resulta en una afirmación que no es equivalente a P → Q (como se discutirá en la sección 1.3). Existen diversas variantes en cuanto a la forma de escribir el enunciado P → Q en inglés. Además de escribir "si P entonces Q", también podríamos escribir cualquiera de las siguientes:

Si P, Q;
 Q si P;
 P sólo si Q;
 Q siempre que P;
 Suponiendo que P, entonces Q;
 Q dado que P;
 P es suficiente para Q;
 Q es necesario para P.

Cada una de estas variantes es útil en determinadas situaciones. Por ejemplo, el enunciado "si llueve hoy, entonces veré una película esta tarde" podría escribirse igualmente "veré una película esta tarde si llueve hoy". También sería formalmente correcto decir "si llueve hoy es suficiente para que vea una película esta tarde", aunque tal frase sería, por supuesto, bastante incómoda.

Nuestra quinta construcción, el bicondicional de P a Q, que se denota P ↔ Q, es el enunciado que, intuitivamente, es verdadero si P y Q son ambos verdaderos o ambos falsos, y es falso en caso contrario. Leemos P ↔ Q como "P si y sólo si Q". La frase "si y sólo si" se suele abreviar como "si". La definición precisa de P ↔ Q se da en la tabla de verdad 
<p align="center">
<img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Btabular%7D%7Bcc%7Cc%7D%0AP%20%26%20Q%20%26%20P%24%5Cleftrightarrow%24Q%20%5C%5C%0A%5Chline%0AT%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20T%20%5C%5C%0A%5Cend%7Btabular%7D%0A" alt="
\begin{tabular}{cc|c}
P &amp; Q &amp; P$\leftrightarrow$Q \\
\hline
T &amp; T &amp; T \\
T &amp; F &amp; F \\
F &amp; T &amp; F \\
F &amp; F &amp; T \\
\end{tabular}
" /></p>

Un ejemplo de enunciado bicondicional es "Iré a dar un paseo si y sólo si Fred me acompaña". Este enunciado tiene la forma P ↔ Q, donde P = "Iré a dar un paseo", y Q = "Fred se unirá a mí". La verdad de este enunciado no dice que vaya a dar un paseo o que Fred se una a mí. Dice que, o bien Fred se unirá a mí y yo iré a dar un paseo, o bien que no ocurrirá ninguna de las dos cosas. En otras palabras, no puede darse el caso de que Fred se una a mí y yo no vaya a dar un paseo, y tampoco puede darse el caso de que yo vaya a dar un paseo y Fred no se una a mí.
Hay algunas variaciones en cuanto a la forma de escribir el enunciado P ↔ Q en inglés. Además de escribir "P si y sólo si Q", es común escribir "P es necesario y suficiente para Q". 
En la sección 1.3 aclararemos más el significado de los enunciados bicondicionales. Entre otras cosas, veremos que el orden de escritura de un enunciado bicondicional no supone ninguna diferencia, es decir, no importa si escribimos P ↔ Q o Q ↔ P.

 Ahora que hemos definido las cinco formas básicas de combinar enunciados, podemos formar enunciados compuestos más complicados utilizando combinaciones de las operaciones básicas. Por ejemplo, podemos formar P ∨(Q → ¬R) a partir de los enunciados P, Q y R. Tenemos que usar paréntesis en este enunciado compuesto, para asegurarnos de que no es ambiguo. Utilizamos la convención estándar de que ¬ tiene prioridad sobre las otras cuatro operaciones, pero ninguna de estas cuatro tiene prioridad sobre las demás. Por lo tanto, escribir "P∨Q → ¬R" sería ambiguo, y nunca escribiríamos una expresión así. 

Podemos formar la tabla de verdad del enunciado P∨(Q → ¬R), haciendo una operación a la vez, como sigue:
<p align="center"><img src="https://i.upmath.me/svg/%0A%5Cbegin%7Barray%7D%7Bc%7Cc%7Cc%7Cc%7Cc%7Cc%7D%0AP%20%26%20Q%20%26%20R%20%26%20%5Cneg%20R%20%26%20Q%20%5Crightarrow%20%5Cneg%20R%20%26%20P%20%5Cvee(Q%20%5Crightarrow%20%5Cneg%20R)%20%5C%5C%0A%5Chline%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%5C%5C%0AT%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%0A%5Cend%7Barray%7D%0A" alt="
\begin{array}{c|c|c|c|c|c}
P &amp; Q &amp; R &amp; \neg R &amp; Q \rightarrow \neg R &amp; P \vee(Q \rightarrow \neg R) \\
\hline T &amp; T &amp; T &amp; F &amp; F &amp; T \\
T &amp; T &amp; F &amp; T &amp; T &amp; T \\
T &amp; F &amp; T &amp; F &amp; T &amp; T \\
T &amp; F &amp; F &amp; T &amp; T &amp; T \\
F &amp; T &amp; T &amp; F &amp; F &amp; F \\
F &amp; T &amp; F &amp; T &amp; T &amp; T \\
F &amp; F &amp; T &amp; F &amp; T &amp; T \\
F &amp; F &amp; F &amp; T &amp; T &amp; T
\end{array}
" />
</p>
Para ahorrar tiempo y esfuerzo, es posible escribir una tabla de verdad más pequeña con la misma información que la tabla de verdad anterior, escribiendo una columna a la vez, y etiquetando las columnas en el orden en que las escribimos. En la tabla de verdad que se muestra a continuación, primero escribimos las columnas 1 y 2, que son sólo copias de las columnas P y Q; luego escribimos la columna 3, que es la negación de la columna R; la columna 4 se forma a partir de las columnas 2 y 3, y la columna 5 se forma a partir de las columnas 1 y 4. Ponemos la etiqueta "5" en un recuadro, para destacar que su columna es el resultado final de la tabla de verdad, y se refiere al enunciado compuesto en el que estamos interesados. Es, por supuesto, el mismo resultado que en la tabla de verdad anterior
<p align="center"><img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Barray%7D%7Bllllllll%7D%0AP%20%26%20Q%20%26%20R%20%26%20P%20%26%20%5Cvee%20%26%20(Q%20%26%20%5Crightarrow%20%26%20%5Cneg%20R)%20%5C%5C%0A%5Chline%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AT%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%5C%5C%0AT%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20F%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0A%26%20%26%201%20%26%205%20%26%202%20%26%204%20%26%203%0A%5Cend%7Barray%7D%0A" alt="
\begin{array}{llllllll}
P &amp; Q &amp; R &amp; P &amp; \vee &amp; (Q &amp; \rightarrow &amp; \neg R) \\
\hline T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; F &amp; F \\
T &amp; T &amp; F &amp; T &amp; T &amp; T &amp; T &amp; T \\
T &amp; F &amp; T &amp; T &amp; T &amp; F &amp; T &amp; F \\
T &amp; F &amp; F &amp; T &amp; T &amp; F &amp; T &amp; T \\
F &amp; T &amp; T &amp; F &amp; F &amp; T &amp; F &amp; F \\
F &amp; T &amp; F &amp; F &amp; T &amp; T &amp; T &amp; T \\
F &amp; F &amp; T &amp; F &amp; T &amp; F &amp; T &amp; F \\
F &amp; F &amp; F &amp; F &amp; T &amp; F &amp; T &amp; T \\
&amp; &amp; 1 &amp; 5 &amp; 2 &amp; 4 &amp; 3
\end{array}
" /></p>
Al igual que podemos formar enunciados compuestos escritos con símbolos, también podemos formar dichos enunciados escritos en inglés. El papel que desempeñan los paréntesis para evitar la ambigüedad en los enunciados escritos con símbolos lo desempeñan a menudo los signos de puntuación en inglés. Por ejemplo, la frase "Me gusta comer manzanas o peras, y me gusta comer melocotones" no es ambigua. Si dejamos que A = "me gusta comer manzanas", que B = "me gusta comer peras" y que C = "me gusta comer melocotones", la frase puede escribirse en símbolos como (A∨B)∧C. Por otro lado, supongamos que nos dan el enunciado (A∨B)∧C, y nos dicen que lo traduzcamos al inglés, sabiendo que A = "I like to eat apples", etc., pero sin saber que el enunciado ha sido formulado originalmente en inglés. Una traducción cuidadosa al inglés podría dar como resultado el enunciado original, o alguna variante igualmente válida, como "I like to eat apples o I like to eat pears, and I like to eat peaches". Por desgracia, a menudo se hacen traducciones imprecisas como "Me gusta comer manzanas o peras y melocotones", o "Me gusta comer manzanas, o me gusta comer peras, y me gusta comer melocotones". Estos dos enunciados son ambiguos; la ambigüedad en el primer enunciado se debe a la falta de puntuación necesaria, y la ambigüedad en el segundo enunciado se debe a una puntuación incorrecta. En ambos enunciados, el problema de la puntuación no es una cuestión de gramática, sino de captar con precisión y sin ambigüedades el significado del enunciado (A∨B)∧C. Terminamos esta sección con una breve mención de dos conceptos importantes. Una tautología es un enunciado que siempre es verdadero por necesidad lógica, independientemente de que los enunciados que lo componen sean verdaderos o falsos, y de lo que observemos en el mundo real. Una contradicción es una afirmación que siempre es falsa por necesidad lógica. La mayoría de los enunciados que encontramos no son de ninguno de estos tipos. Por ejemplo, la afirmación "Irene es pelirroja" no es ni una tautología ni una contradicción, porque no es necesariamente ni verdadera ni falsa: es lógicamente plausible que Irene sea pelirroja y es igualmente plausible que no lo sea. Incluso la afirmación "1 ̸= 2" no es una tautología. Ciertamente es verdadera en nuestro sistema matemático estándar, por lo que sabemos, pero la verdad de esta afirmación es una observación sobre la forma en que los seres humanos han construido su sistema numérico, no una necesidad lógica. Un ejemplo de tautología es la afirmación "Irene es pelirroja o no es pelirroja". Parece intuitivamente claro que esta afirmación es una tautología, y podemos verificar este hecho formalmente utilizando tablas de verdad. Sea P = "Irene es pelirroja". Entonces la tautología pretendida es el enunciado P∨¬P. La tabla de verdad de este enunciado es
<p align="center"><img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Barray%7D%7Bl%7Clll%7D%0AP%20%26%20P%20%26%20%5Cwedge%20%26%20%5Cneg%20P%20%5C%5C%0A%5Chline%20T%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20F%20%26%20T%20%5C%5C%0A%26%201%20%26%203%20%26%202%0A%5Cend%7Barray%7D%0A" alt="
\begin{array}{l|lll}
P &amp; P &amp; \wedge &amp; \neg P \\
\hline T &amp; T &amp; F &amp; F \\
F &amp; F &amp; F &amp; T \\
&amp; 1 &amp; 3 &amp; 2
\end{array}
" /></p>
Vemos en la columna 3 que el enunciado P∨¬P es siempre verdadero, independientemente de que P sea verdadero o falso. Este hecho nos dice que P∨¬P es una tautología. En general, un enunciado es una tautología si, como se verifica mediante una tabla de verdad, siempre es verdadero, independientemente de que los enunciados que lo componen sean verdaderos o falsos. El enunciado "Irene es pelirroja y no es pelirroja" es una contradicción. En símbolos este enunciado es P∧¬P, y su tabla de verdad es
<p align="center"><img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Barray%7D%7Bl%7Clll%7D%0AP%20%26%20P%20%26%20%5Cwedge%20%26%20%5Cneg%20P%20%5C%5C%0A%5Chline%20T%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20F%20%26%20T%20%5C%5C%0A%26%201%20%26%203%20%26%202%0A%5Cend%7Barray%7D%0A" alt="
\begin{array}{l|lll}
P &amp; P &amp; \wedge &amp; \neg P \\
\hline T &amp; T &amp; F &amp; F \\
F &amp; F &amp; F &amp; T \\
&amp; 1 &amp; 3 &amp; 2
\end{array}
" /></p>

El enunciado P ∧ ¬P es siempre falso, independientemente de que P sea verdadero o falso. En general, un enunciado es una contradicción si, como se verifica utilizando una tabla de verdad, siempre es falso, independientemente de si sus enunciados componentes son verdaderos o falsos.

Que P ∨ ¬P sea una tautología, y que P ∧ ¬P sea una contradicción, parece bastante in- tuitivo. Sin embargo, es posible tener tautologías y contradicciones más complicadas (y no tan intuitivas). Por ejemplo, la tabla de verdad del enunciado [(P∧Q) → R] → [P → (Q → R)] es
<p align="center"><img align="center" src="https://i.upmath.me/svg/%0A%5Cbegin%7Barray%7D%7Bl%7Cc%7Cc%7Cccccccccccc%7D%0AP%20%26%20Q%20%26%20R%20%26%20%7B%5B(P%7D%20%26%20%5Cwedge%20%26%20Q%20%26%20%5Crightarrow%20%26%20R%20%26%20%5Crightarrow%20%26%20%7B%5BP%7D%20%26%20%5Crightarrow%20%26%20(Q%20%26%20%5Crightarrow%20%26%20R)%5D%20%5C%5C%0A%5Chline%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AT%20%26%20F%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0AT%20%26%20F%20%26%20F%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%5C%5C%0AF%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20T%20%26%20F%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%26%20F%20%26%20F%20%5C%5C%0AF%20%26%20F%20%26%20T%20%26%20F%20%26%20F%20%26%20F%20%26%20T%20%26%20T%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20T%20%5C%5C%0AF%20%26%20F%20%26%20F%20%26%20F%20%26%20F%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%26%20T%20%26%20F%20%5C%5C%0A%26%20%26%20%5Cmid%20%26%201%20%26%203%20%26%202%20%26%205%20%26%204%20%26%2011%20%26%209%20%26%2010%20%26%206%20%26%208%20%26%207%0A%5Cend%7Barray%7D%0A" alt="
\begin{array}{l|c|c|ccccccccccc}
P &amp; Q &amp; R &amp; {[(P} &amp; \wedge &amp; Q &amp; \rightarrow &amp; R &amp; \rightarrow &amp; {[P} &amp; \rightarrow &amp; (Q &amp; \rightarrow &amp; R)] \\
\hline T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T &amp; T \\
T &amp; T &amp; F &amp; T &amp; T &amp; T &amp; F &amp; F &amp; T &amp; T &amp; F &amp; T &amp; F &amp; F \\
T &amp; F &amp; T &amp; T &amp; F &amp; F &amp; T &amp; T &amp; T &amp; T &amp; T &amp; F &amp; T &amp; T \\
T &amp; F &amp; F &amp; T &amp; F &amp; F &amp; T &amp; F &amp; T &amp; T &amp; T &amp; F &amp; T &amp; F \\
F &amp; T &amp; T &amp; F &amp; F &amp; T &amp; T &amp; T &amp; T &amp; F &amp; T &amp; T &amp; T &amp; T \\
F &amp; T &amp; F &amp; F &amp; F &amp; T &amp; T &amp; F &amp; T &amp; F &amp; T &amp; T &amp; F &amp; F \\
F &amp; F &amp; T &amp; F &amp; F &amp; F &amp; T &amp; T &amp; T &amp; F &amp; T &amp; F &amp; T &amp; T \\
F &amp; F &amp; F &amp; F &amp; F &amp; F &amp; T &amp; F &amp; T &amp; F &amp; T &amp; F &amp; T &amp; F \\
&amp; &amp; \mid &amp; 1 &amp; 3 &amp; 2 &amp; 5 &amp; 4 &amp; 11 &amp; 9 &amp; 10 &amp; 6 &amp; 8 &amp; 7
\end{array}
" /></p>
Vemos en la columna 11 que el enunciado [(P ∧ Q) → R] → [P → (Q → R)] es siempre verdadero, independientemente de que cada uno de P, Q y R sea verdadero o falso. Por tanto, el enunciado es una tautología. Supongamos que P = "Sam está triste", que Q = "Warren está triste" y que R = "Sam y Warren comen pasta". Entonces el enunciado se convierte en "Si es cierto que si Sam y Warren están tristes entonces comen pasta, entonces es cierto que si Sam está triste, entonces si Warren está triste comen pasta". 
Como ejemplo de contradicción, el lector puede comprobar con una tabla de verdad que el enunciado [Q → (P∧¬Q)]∧Q es siempre falso.
