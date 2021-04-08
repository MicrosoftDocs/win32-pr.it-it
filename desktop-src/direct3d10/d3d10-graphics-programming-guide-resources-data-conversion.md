---
description: Nelle sezioni seguenti viene descritto il modo in cui Direct3D gestisce le conversioni tra tipi di dati.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Regole di conversione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61abdc58811af9155c67d7b32bcd47e9d4b71ea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748266"
---
# <a name="data-conversion-rules"></a>Regole di conversione dei dati

Nelle sezioni seguenti viene descritto il modo in cui Direct3D gestisce le conversioni tra tipi di dati.

-   [Terminologia del tipo di dati](#data-type-terminology)
-   [Conversione da virgola mobile](#floating-point-conversion)
    -   [Conververting da una rappresentazione di intervallo superiore a una rappresentazione di un intervallo inferiore](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Conversione da una rappresentazione di intervallo inferiore a una rappresentazione di un intervallo superiore](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversione integer](#integer-conversion)
-   [Conversione integer a virgola fissa](#fixed-point-integer-conversion)
-   [Argomenti correlati](#related-topics)

## <a name="data-type-terminology"></a>Terminologia del tipo di dati

Il set di termini seguente viene successivamente usato per caratterizzare le varie conversioni di formato.



| Termine  | Definizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RUSSAre | Intero con segno normalizzato, ovvero per un numero di complemento a n bit 2, il valore massimo significa 1,0 f (ad esempio, il valore a 5 bit 01111 viene mappato a 1,0 f) e il valore minimo indica-1.0 f (ad esempio, il valore a 5 bit 10000 viene mappato a-1.0 f). Inoltre, il secondo numero minimo viene mappato a-1.0 f (ad esempio, il valore a 5 bit 10001 esegue il mapping a-1.0 f). Sono pertanto presenti due rappresentazioni integer per-1.0 f. Esiste una singola rappresentazione per 0,0 f e una singola rappresentazione per 1.0 f. Il risultato è un set di rappresentazioni integer per i valori a virgola mobile equidistanti nell'intervallo (-1.0 f... 0.0 f) e anche un set di rappresentazioni complementari per i numeri nell'intervallo (0,0 f... 1.0 f) |
| UNORM | Intero senza segno normalizzato, vale a dire che per un numero a n bit, tutti 0 significa 0,0 f e tutti i 1 significa 1,0 f. Viene rappresentata una sequenza di valori a virgola mobile con spazi uniformi da 0,0 f a 1,0 f. ad esempio, un UNORM a 2 bit rappresenta 0,0 f, 1/3, 2/3 e 1.0 f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SINT  | Intero con segno. intero complemento a 2. ad esempio, un SINT a 3 bit rappresenta i valori integrali-4,-3,-2,-1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Intero senza segno. ad esempio, una UINT a 3 bit rappresenta i valori integrali 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Valore a virgola mobile in una delle rappresentazioni definite da Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Analogamente a UNORM, in quanto per un numero a n bit, tutti 0 significa 0,0 f e tutti i 1 significa 1.0 f. Tuttavia, a differenza di UNORM, con SRGB la sequenza di Unsigned Integer codifiche tra tutti gli 0 e tutti i valori di 1 rappresenta una progressione non lineare nell'interpretazione dei numeri a virgola mobile, da 0,0 f a 1,0 f. Approssimativamente, se questa progressione non lineare, SRGB, viene visualizzata come sequenza di colori, viene visualizzata come una rampa lineare di livelli di luminosità a un osservatore "medio", in condizioni di visualizzazione "media", su una visualizzazione "media". Per informazioni dettagliate, vedere la pagina relativa allo standard dei colori SRGB, IEC 61996-2-1, alle IEC (International Electrotechnical Commission).                |



 

## <a name="floating-point-conversion"></a>Conversione da virgola mobile

Ogni volta che si verifica una conversione a virgola mobile tra rappresentazioni diverse, incluse le rappresentazioni a o dalle rappresentazioni a virgola mobile, vengono applicate le regole seguenti.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Conververting da una rappresentazione di intervallo superiore a una rappresentazione di un intervallo inferiore

-   L'arrotondamento a zero viene usato durante la conversione in un altro formato float. Se la destinazione è un numero intero o un formato a virgola fissa, viene utilizzato anche l'arrotondamento al più vicino, a meno che la conversione non venga documentata in modo esplicito come utilizzo di un altro comportamento di arrotondamento, ad esempio round-to-più vicino per FLOAT a RUSSAr, FLOAT a UNORM o FLOAT a SRGB. Altre eccezioni sono le istruzioni shader Ftoi e ftou, che usano l'arrotondamento a zero. Infine, le conversioni da float a fisso usate dal campionatore di trame e dal rasterizzatore hanno una tolleranza specificata misurata in unità-Last-Place da un ideale perfettamente preciso.
-   Per i valori di origine maggiori dell'intervallo dinamico di un formato di destinazione di un intervallo inferiore (ad esempio un valore float a 32 bit di grandi dimensioni viene scritto in un RenderTarget float a 16 bit, il valore massimo rappresentabile (con segno appropriato) risulta, ESCLUSo l'infinito con segno (a causa dell'arrotondamento a zero descritto in precedenza).
-   NaN in un formato di intervallo superiore verrà convertito nella rappresentazione NaN nel formato di intervallo inferiore se la rappresentazione NaN esiste nel formato di intervallo inferiore. Se il formato inferiore non ha una rappresentazione NaN, il risultato sarà 0.
-   INF in un formato di intervallo superiore verrà convertito in INF nel formato di intervallo inferiore, se disponibile. Se il formato inferiore non dispone di una rappresentazione INF, verrà convertito nel valore massimo rappresentabile. Il segno verrà mantenuto se disponibile nel formato di destinazione.
-   La deregolazione in un formato di intervallo superiore verrà convertita nella rappresentazione denormalizzata nel formato di intervallo inferiore, se disponibile nel formato di intervallo inferiore e la conversione è possibile; in caso contrario, il risultato è 0. Il bit di segno verrà mantenuto se disponibile nel formato di destinazione.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Conversione da una rappresentazione di intervallo inferiore a una rappresentazione di un intervallo superiore

-   NaN in un formato di intervallo inferiore verrà convertito nella rappresentazione NaN nel formato di intervallo superiore se disponibile nel formato di intervallo superiore. Se il formato di intervallo superiore non ha una rappresentazione NaN, verrà convertito in 0.
-   INF in un formato di intervallo inferiore verrà convertito nella rappresentazione INF nel formato di intervallo superiore se disponibile nel formato di intervallo superiore. Se il formato superiore non dispone di una rappresentazione INF, viene convertito nel valore massimo rappresentabile (valore \_ float massimo in tale formato). Il segno verrà mantenuto se disponibile nel formato di destinazione.
-   La deregolazione in un formato di intervallo inferiore sarà convertita in una rappresentazione normalizzata nel formato di intervallo superiore, se possibile, o in caso contrario a una rappresentazione denormalizzata nel formato di intervallo superiore se la rappresentazione della deregolazione esiste. In caso contrario, se il formato di intervallo superiore non ha una rappresentazione denormalizzata, verrà convertito in 0. Il segno verrà mantenuto se disponibile nel formato di destinazione. Si noti che i numeri a virgola mobile a 32 bit vengono conteggiati come formato senza una rappresentazione della denorma (poiché le denormazioni nelle operazioni su valori float a 32 bit vengono mantenute per segno mantenuto 0).

## <a name="integer-conversion"></a>Conversione integer

Nella tabella seguente vengono descritte le conversioni da varie rappresentazioni descritte in precedenza ad altre rappresentazioni. Vengono visualizzate solo le conversioni effettivamente presenti in Direct3D.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di dati di origine</th>
<th>Tipo di dati di destinazione</th>
<th>Regola di conversione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RUSSAre</td>
<td>FLOAT</td>
<td>Dato un valore integer a n bit che rappresenta l'intervallo con segno [-1.0 f a 1,0 f], la conversione a virgola mobile è la seguente.<br/>
<ul>
<li>Il valore più negativo viene mappato a-1.0 f. ad esempio, il valore a 5 bit 10000 viene mappato a-1.0 f.</li>
<li>Ogni altro valore viene convertito in un valore float (chiamato c) e quindi result = c * (1.0 f/(2 ⁽ Grigioni ⁻ ¹ ⁾-1)). Ad esempio, il valore a 5 bit 10001 viene convertito in-15.0 f, quindi diviso per 15.0 f, cedendo-1.0 f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>RUSSAre</td>
<td>Dato un numero a virgola mobile, la conversione in un valore integer a n bit che rappresenta l'intervallo con segno [-1.0 f a 1,0 f] è la seguente.<br/>
<ul>
<li>Consentire a c di rappresentare il valore iniziale.</li>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0 f, incluso INF, viene fissato a 1,0 f.</li>
<li>Se c <-1.0 f, incluso-INF, viene fissato a-1.0 f.</li>
<li>Conversione dalla scala float alla scala integer: c = c * (2 Grigioni ⁻ ¹-1).</li>
<li>Eseguire la conversione in un numero intero come indicato di seguito.
<ul>
<li>Se c >= 0, c = c + 0,5 f, in caso contrario c = c-0.5 f.</li>
<li>Eliminare la frazione decimale e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un numero intero.</li>
</ul></li>
</ul>
Questa conversione è consentita per la tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Place (sul lato Integer). Ciò significa che dopo la conversione da float a scala integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore del formato di destinazione rappresentabile è autorizzato a eseguire il mapping a tale valore. Il requisito aggiuntivo di inversione dei dati garantisce che la conversione sia nondecreasing nell'intervallo e che tutti i valori di output siano raggiungibili. Nelle costanti illustrate qui, <em>XX</em> deve essere sostituito con la versione Direct3D, ad esempio 10, 11 o 12.<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>Il valore a n bit iniziale viene convertito in float (0,0 f, 1.0 f, 2.0 f e così via) e quindi diviso per (2 Grigioni-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Consentire a c di rappresentare il valore iniziale.<br/>
<ul>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0 f, incluso INF, viene fissato a 1,0 f.</li>
<li>Se c < 0,0 f, incluso-INF, viene fissato a 0,0 f.</li>
<li>Conversione dalla scala float alla scala integer: c = c * (2 Grigioni-1).</li>
<li>Converte in Integer.
<ul>
<li>c = c + 0,5 f.</li>
<li>La frazione decimale viene eliminata e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un numero intero.</li>
</ul></li>
</ul>
Questa conversione è consentita per la tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unità-Last-Place (sul lato Integer). Ciò significa che dopo la conversione da float a scala integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore del formato di destinazione rappresentabile è autorizzato a eseguire il mapping a tale valore. Il requisito aggiuntivo di inversione dei dati garantisce che la conversione sia nondecreasing nell'intervallo e che tutti i valori di output siano raggiungibili.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>FLOAT</td>
<td>Di seguito è riportata la conversione ideale di SRGB per FLOAT.<br/>
<ul>
<li>Prendere il valore a n bit iniziale, convertirlo in float (0,0 f, 1.0 f, 2.0 f e così via); chiamare questo c.</li>
<li>c = c * (1.0 f/(2 Grigioni-1))</li>
<li>If (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) Then: result = c/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_1; else: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_2) D3D<em>XX</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Questa conversione è consentita per la tolleranza di D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP unità-Ultima posizione (sul lato sRGB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRGB</td>
<td>Di seguito è riportata la conversione ideale di FLOAT > SRGB.<br/> Supponendo che il componente colore SRGB di destinazione disponga di n bit:<br/>
<ul>
<li>Si supponga che il valore iniziale sia c.</li>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0 f, incluso INF, viene fissato a 1,0 f.</li>
<li>Se c < 0,0 f, incluso-INF, viene fissato a 0,0 f.</li>
<li>If (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD): c = d3d<em>XX</em>_FLOAT_TO_SRGB_SCALE_1 * c; else: c = D3D<em>XX</em>_FLOAT_TO_SRGB_SCALE_2 * c (D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR)-D3D<em>XX</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Conversione dalla scala float alla scala integer: c = c * (2 Grigioni-1).</li>
<li>Converti in Integer:
<ul>
<li>c = c + 0,5 f.</li>
<li>La frazione decimale viene eliminata e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un numero intero.</li>
</ul></li>
</ul>
Questa conversione è consentita per la tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unità-Last-Place (sul lato Integer). Ciò significa che dopo la conversione da float a scala integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore del formato di destinazione rappresentabile è autorizzato a eseguire il mapping a tale valore. Il requisito aggiuntivo di inversione dei dati garantisce che la conversione sia nondecreasing nell'intervallo e che tutti i valori di output siano raggiungibili.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>SINT con più bit</td>
<td>Per eseguire la conversione da SINT a un SINT con più bit, il bit più significativo (MSB) del numero iniziale viene &quot; esteso &quot; con segno ai bit aggiuntivi disponibili nel formato di destinazione.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT con più bit</td>
<td>Per eseguire la conversione da UINT a un SINT con più bit, il numero viene copiato nei bit meno significativi del formato di destinazione (LSB) e altri MSBs vengono riempiti con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>UINT con più bit</td>
<td>Per eseguire la conversione da SINT a UINT con più bit: se negativo, il valore viene impostato su 0. In caso contrario, il numero viene copiato nel LSB del formato di destinazione e i MSB aggiuntivi vengono riempiti con 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT con più bit</td>
<td>Per eseguire la conversione da UINT a UINT con più bit, il numero viene copiato nel LSB del formato di destinazione e i MSB aggiuntivi vengono riempiti con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT o UINT</td>
<td>SINT o UINT con minore o uguale bit</td>
<td>Per eseguire la conversione da SINT o UINT a SINT o UINT con un numero minore o uguale di bit (e/o una modifica di firma), il valore iniziale viene semplicemente limitato all'intervallo del formato di destinazione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversione integer a virgola fissa

Gli Integer a virgola fissa sono semplicemente numeri interi di una dimensione di bit che hanno un separatore decimale implicito in una posizione fissa.

Il tipo di dati "Integer" universale è un caso speciale di un numero intero a virgola fissa con il separatore decimale alla fine del numero.

Le rappresentazioni di numeri a virgola fissa sono caratterizzate da: i. f, dove i è il numero di bit integer e f è il numero di bit frazionari. ad esempio, 16,8 indica un Integer a 16 bit seguito da 8 bit della frazione. La parte integer viene archiviata nel complemento di 2, almeno come definito qui (anche se può essere definita ugualmente per gli interi senza segno). La parte frazionaria è archiviata in forma non firmata. La parte frazionaria rappresenta sempre la frazione positiva tra i due valori integrali più vicini, a partire dal più negativo.

Le operazioni di addizione e sottrazione su numeri a virgola fissa vengono eseguite semplicemente utilizzando i calcoli Integer standard, senza alcuna considerazione sulla posizione del decimale implicito. L'aggiunta di 1 a un numero a virgola fissa 16,8 significa semplicemente l'aggiunta di 256, perché il separatore decimale è 8 posizioni nell'oggetto dall'estremità meno significativa del numero. È possibile eseguire altre operazioni, ad esempio la moltiplicazione, usando semplicemente i calcoli Integer, a condizione che l'effetto sul numero decimale fisso venga considerato. Se ad esempio si moltiplicano due interi 16,8 usando una moltiplicazione Integer, viene prodotto un risultato 32,16.

Le rappresentazioni Integer a virgola fissa vengono utilizzate in due modi in Direct3D.

-   Le posizioni dei vertici post-ritagliate nel rasterizzatore sono bloccate in un punto fisso, per distribuire in modo uniforme la precisione nell'area RenderTarget. Molte operazioni di rasterizzazione, tra cui l'abbattimento della faccia come un esempio, si verificano in posizioni bloccate a virgola fissa, mentre altre operazioni, ad esempio l'installazione di un interpolatore di attributi, usano posizioni che sono state convertite in virgola mobile dalle posizioni bloccate a virgola fissa.
-   Le coordinate di trama per le operazioni di campionamento vengono bloccate a un punto fisso (dopo la scalabilità in base alle dimensioni della trama), per distribuire in modo uniforme la precisione nello spazio di trama, scegliendo filtra i percorsi/pesi. I valori di peso vengono riconvertiti in virgola mobile prima dell'effettiva esecuzione aritmetica del filtro.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di dati di origine</th>
<th>Tipo di dati di destinazione</th>
<th>Regola di conversione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLOAT</td>
<td>Intero a virgola fissa</td>
<td>Di seguito è riportata la procedura generale per la conversione di un numero a virgola mobile n in un intero a virgola fissa i. f, dove i è il numero di bit Integer (con segno) e f è il numero di bit frazionari.<br/>
<ul>
<li>Compute FixedMin =-2 ⁽ ⁱ ⁻ ¹ ⁾</li>
<li>Compute FixedMax = 2 ⁽ ⁱ ⁻ ¹ ⁾-2<sup>(-f)</sup></li>
<li>Se n è un valore NaN, result = 0; Se n è + inf, result = FixedMax * 2<sup>f</sup>; Se n è-inf, result = FixedMin * 2<sup>f</sup></li>
<li>Se n >= FixedMax, result = Fixedmax * 2<sup>f</sup>; Se n <= FixedMin, result = FixedMin * 2 <sup> f</sup></li>
<li>Else Compute n * 2<sup>f</sup> e Convert in Integer.</li>
</ul>
Le implementazioni sono consentite con D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP la tolleranza dell'ultima posizione nel risultato Integer, anziché il valore infinitamente preciso n * 2<sup>f</sup> dopo l'ultimo passaggio precedente.<br/></td>
</tr>
<tr class="even">
<td>Intero a virgola fissa</td>
<td>FLOAT</td>
<td>Si supponga che la rappresentazione a virgola fissa specifica che viene convertita in float non contenga più di 24 bit di informazioni, non più di 23 bit nel componente frazionario. Si supponga che un determinato numero a virgola fissa, FXP, si trovi nel form i. f (i bit Integer, f bits frazioni). La conversione in float è simile al seguente pseudocodice.<br/> float result = (float) (FXP >> f) +//Extract Integer<br/> <dl> ((float) (FXP & (2<sup>f</sup> - 1))/(2<sup>f</sup>));//Estrai frazione<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




