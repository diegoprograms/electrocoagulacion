# Guía — Diseño y dimensionamiento del electrocoagulador de flujo continuo

## Propósito

Transformar la investigación bibliográfica de la etapa 2 y los cálculos iniciados en clase en una propuesta de diseño del electrocoagulador: voltaje de operación, separación entre ánodo y cátodo, dimensiones y área de las placas, velocidad del agua, caudal y presupuesto de materiales.

**Trabajaremos con flujo continuo. Cada grupo debe llevar a la próxima clase los cálculos ya realizados, el esquema de su propuesta y el valor cotizado de los materiales necesarios.** En clase compararemos las propuestas para avanzar hacia un solo diseño colectivo.

## 1. De los artículos a las decisiones de diseño

Retomen los artículos investigados por su grupo en la etapa 2. Extraigan los datos que permiten sustentar su propuesta e indiquen la página, tabla o figura de donde proviene cada uno.

| Parámetro | Valor y unidad reportados en el artículo | Valor propuesto por el grupo | Fuente y justificación de la elección |
|---|---|---|---|
| Tipo de agua y contaminante o parámetro a tratar | | | |
| Material del ánodo y del cátodo | | | |
| Voltaje y tipo de alimentación eléctrica | | | |
| Corriente o densidad de corriente, si se reporta | | | |
| Separación entre electrodos | | | |
| Largo, altura sumergida, espesor y número de placas | | | |
| Área activa de los electrodos y caras consideradas | | | |
| Configuración y conexión de los electrodos | | | |
| Caudal y volumen útil del reactor | | | |
| Tiempo de tratamiento o de residencia, según corresponda | | | |

Distingan los datos publicados de los valores calculados y de los supuestos del grupo. Si falta un dato, escriban «no reportado»; no lo atribuyan al artículo. Los resultados de aguas y configuraciones diferentes deben compararse teniendo en cuenta esas diferencias. Un ensayo por lotes puede orientar la selección de parámetros, pero su tiempo de tratamiento no se convierte automáticamente en tiempo de residencia de un reactor continuo.

Como referencia para discutir el flujo continuo, Salinas-Echeverría y colaboradores (2023) estudiaron un reactor de 20 canales en serie, volumen efectivo de 8,7 L y una condición de 300 mL/min y 30 V. Estos datos pertenecen a ese montaje y **no son valores asignados a nuestro proyecto**. Consulten el [registro institucional del artículo](https://rise.ecotec.edu.ec/en/publications/evaluation-of-a-continuous-flow-electrocoagulation-reactor-for-tu/) y su texto completo antes de trasladar dimensiones o condiciones.

## 2. Cálculos que deben llevar terminados a la próxima clase

Presenten el procedimiento, las ecuaciones, la sustitución de valores, las unidades y la interpretación de cada resultado. Continúen el modelo iniciado en clase y declaren sus supuestos.

### A. Campo eléctrico entre las placas

1. Dibujen el ánodo y el cátodo, su polaridad, la separación y la dirección del campo.
2. Completen el desarrollo con la ley de Gauss para dos placas paralelas ideales, despreciando efectos de borde:

   $$\oint \vec E\cdot d\vec A=\frac{Q_{\mathrm{enc}}}{\varepsilon},\qquad E=\frac{\sigma}{\varepsilon}.$$

   Aquí, $\sigma$ es la magnitud de la densidad superficial de carga de cada placa y $\varepsilon$ la permitividad del medio idealizado. Una lámina aislada aporta $\sigma/(2\varepsilon)$; entre dos láminas con cargas opuestas de igual magnitud se suman ambos aportes.

3. Relacionen el campo uniforme con la diferencia de potencial entre placas:

   $$E\approx\frac{|\Delta V|}{d}.$$

4. Calculen el campo con el voltaje y la separación propuestos. Expresen $d$ en metros y $E$ en V/m o N/C. Indiquen si la separación es pequeña frente a las dimensiones de las placas, condición del modelo usado.

Esta es una aproximación didáctica. En el reactor real, parte del voltaje aplicado corresponde a procesos en las interfaces de los electrodos; no toda la tensión de la fuente equivale necesariamente a una caída uniforme en el agua.

### B. Desviación de una partícula: leyes de Newton y movimiento acelerado

Definan el eje $x$ en la dirección del flujo y el eje $y$ hacia la placa de destino. Identifiquen la masa $m$, la carga $q$, la posición de entrada y la distancia transversal $s$ que debe recorrer la partícula. Justifiquen el origen de $m$ y $q$: dato de clase, fuente o supuesto explícito. **No asignen la carga del electrón a una partícula contaminante sin justificación.**

Para el modelo ideal de campo constante, sin arrastre y con velocidad transversal inicial nula:

$$F_y=qE_y,\qquad a_y=\frac{qE_y}{m},\qquad s=\frac12|a_y|t_{\mathrm{desv}}^2.$$

$$t_{\mathrm{desv}}=\sqrt{\frac{2ms}{|q|E}}.$$

- Indiquen hacia qué placa se desvía la partícula según el signo de su carga.
- Usen $s=d/2$ únicamente si suponen que entra por el plano medio entre las placas; para otra posición, calculen la distancia correspondiente.
- Si su modelo utiliza una velocidad transversal inicial distinta de cero, inclúyanla en la ecuación de movimiento.
- Si no disponen de $m$ o $q$, lleven el desarrollo simbólico y señalen el dato faltante. Cualquier ejemplo numérico con valores supuestos debe identificarse como tal.

**Alcance del cálculo:** el agua ejerce arrastre sobre las partículas y la electrocoagulación involucra formación de coagulantes y flóculos. La trayectoria ideal calculada en clase no demuestra que el contaminante llegue realmente a una placa ni garantiza su remoción. La propuesta debe contrastarse con las condiciones experimentales de los artículos.

### C. Tamaño de las placas y velocidad del flujo

Sea $L$ la longitud sumergida de la placa paralela al flujo y $H$ su altura sumergida. Para una velocidad longitudinal constante $u$ en el modelo ideal:

$$t_{\mathrm{paso}}=\frac{L}{u}.$$

Para que la partícula alcance la placa antes de salir de la región de campo, el modelo exige $t_{\mathrm{paso}}\geq t_{\mathrm{desv}}$. Por tanto:

$$L_{\min}=u\,t_{\mathrm{desv}},\qquad u_{\max}=\frac{L}{t_{\mathrm{desv}}}.$$

Propongan una longitud y calculen la velocidad compatible, o propongan una velocidad y calculen la longitud mínima. Expliquen qué variable fijaron primero y por qué. Comparen el resultado con las dimensiones y condiciones de los artículos.

Calculen también el área sumergida de una cara:

$$A_{\mathrm{cara}}=L H.$$

Especifiquen cuántas placas y caras participan. Distingan el área activa usada en los cálculos de la superficie total de lámina que se necesita comprar, incluyendo la parte destinada a sujeción y conexión.

### D. Del flujo al caudal

Para un canal rectangular lleno de agua, entre dos placas separadas una distancia $d$ y con altura de agua $H$:

$$A_{\mathrm{paso}}=dH,\qquad Q=uA_{\mathrm{paso}},\qquad t_{\mathrm{res}}=\frac{V_{\mathrm{útil}}}{Q}.$$

Aquí $Q$ representa caudal y $V_{\mathrm{útil}}$ el volumen de agua del reactor. No confundan el área de paso del agua con el área de los electrodos. Para varios canales en paralelo, sumen sus caudales; para canales en serie, el caudal es el mismo a través de ellos. Adapten el cálculo a su geometría.

Presenten el caudal en m³/s y L/min y comparen el tiempo de residencia con la bibliografía. La relación entre longitud y velocidad del modelo de partícula, por sí sola, no fija un tiempo de tratamiento eficaz.

## 3. Esquema y resumen de la propuesta

Lleven un dibujo con medidas que muestre la entrada y salida del agua, dirección del flujo, dimensiones del recipiente, ubicación de las placas, separación, altura sumergida y conexiones eléctricas.

Incluyan una tabla final con los valores propuestos de voltaje, separación, campo eléctrico, dimensiones y número de placas, área activa, velocidad, caudal y volumen útil. Cada valor debe remitir a un cálculo, un artículo o un supuesto declarado. Señalen qué datos siguen pendientes de obtener.

## 4. Materiales y presupuesto

**Con base en sus cálculos y en los artículos, cada grupo debe consultar y llevar el valor de los materiales necesarios para construir su propuesta.** Los precios deben expresarse en pesos colombianos (COP), con proveedor o enlace y fecha de consulta. No basta una lista de materiales sin cantidades, especificaciones ni precios.

Completen la siguiente tabla según su diseño. Las filas son una base para cotizar; las cantidades y capacidades se determinan con su propuesta.

| Material o componente | Especificación sustentada en el diseño | Cantidad y unidad de compra | Valor unitario (COP) | Subtotal (COP) | Proveedor / enlace y fecha |
|---|---|---|---|---|---|
| Placas para ánodo y cátodo | Metal, dimensiones, espesor, número y costo de corte | | | | |
| Recipiente o cuerpo del reactor | Material, dimensiones y volumen útil | | | | |
| Separadores y soportes de placas | Material aislante y separación requerida | | | | |
| Fuente de corriente continua | Rango de voltaje y capacidad de corriente justificados | | | | |
| Sistema de alimentación de agua | Bomba o alimentación por gravedad, según caudal requerido | | | | |
| Mangueras, conexiones y regulación de flujo | Diámetros, longitudes y compatibilidad con el montaje | | | | |
| Recipientes de alimentación y recolección | Capacidad según caudal y duración prevista | | | | |
| Cables, terminales y elementos de conexión | Cantidad y características según corriente y montaje | | | | |
| Sellos, fijaciones y otros elementos del diseño | Especificar | | | | |
| Transporte y servicios de fabricación | Indicar qué incluyen y evitar duplicar costos | | | | |
| **Total de compra** | | | | **Por calcular** | |

$$C_i=n_i p_i,\qquad C_{\mathrm{total}}=\sum_i C_i.$$

Para elegir la fuente no basta el voltaje: registren la corriente reportada o estimada. Si el artículo ofrece densidad de corriente $j$, pueden usar $I=jA_{\mathrm{activa}}$, respetando la definición de área y la configuración eléctrica de ese artículo. Si falta información para dimensionar un componente, indiquen qué falta y presenten su cotización como provisional.

Distingan los materiales que deben comprarse de los que ya están disponibles o se prestarían. Registren por separado el valor de referencia de estos últimos y el desembolso requerido. Indiquen si los precios incluyen impuestos, envío y corte. Si un elemento no tiene cotización, márquenlo como pendiente y presenten el total como parcial; no lo contabilicen como gratuito.

**No se asigna un presupuesto único desde esta guía:** el valor depende de las dimensiones y componentes que justifique cada grupo. El entregable es un presupuesto cotizado, vinculado a esa propuesta.

## 5. Entrega para la próxima clase

Cada grupo debe llevar:

1. La tabla de parámetros extraídos de sus artículos y la justificación de los valores elegidos.
2. Los cálculos completos de campo eléctrico, fuerza, aceleración, desviación, dimensiones de placas, velocidad, caudal y tiempo de residencia, con sus unidades y supuestos.
3. El esquema dimensionado y la tabla resumen de su propuesta.
4. La lista de materiales con cantidades, especificaciones, precios, fuentes de cotización y total en COP.

Registren los documentos en [aportes de estudiantes](aportes_estudiantes/README.md) e identifiquen grupo, integrantes, fecha y fuentes. Si un dato indispensable no está disponible, lleven el procedimiento desarrollado hasta donde ese dato permita y expliquen cómo lo obtendrían.

**Fecha de entrega: próxima clase, según lo indicado por el docente.**

## Puesta en común

Compararemos la coherencia entre bibliografía, cálculos, dimensiones, flujo y costo. Los resultados de cada grupo serán propuestas para discutir; los acuerdos se registrarán en [decisiones y preguntas](DECISIONES_Y_PREGUNTAS.md), y la comparación en la [síntesis colectiva](SINTESIS_COLECTIVA.md).

[Volver a la etapa](README.md).
