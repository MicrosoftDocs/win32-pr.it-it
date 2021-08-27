---
description: Le sezioni seguenti descrivono come Direct3D gestisce le conversioni tra tipi di dati.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Regole di conversione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b5ba37305fb7cadc229a614b883519cf6c5f45
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626297"
---
# <a name="data-conversion-rules"></a>Regole di conversione dei dati

Le sezioni seguenti descrivono come Direct3D gestisce le conversioni tra tipi di dati.

-   [Terminologia dei tipi di dati](#data-type-terminology)
-   [Conversione a virgola mobile](#floating-point-conversion)
    -   [Converso da una rappresentazione di intervallo superiore a una rappresentazione di intervallo inferiore](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Conversione da una rappresentazione di intervallo inferiore a una rappresentazione di intervallo superiore](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversione integer](#integer-conversion)
-   [Conversione di interi a virgola fissa](#fixed-point-integer-conversion)
-   [Argomenti correlati](#related-topics)

## <a name="data-type-terminology"></a>Terminologia dei tipi di dati

Il set di termini seguente viene successivamente usato per caratterizzare varie conversioni di formato.



| Termine  | Definizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNORM | Intero normalizzato con segno, ovvero per un numero di complemento a n bit 2, il valore massimo significa 1,0f (ad esempio, il valore a 5 bit 01111 esegue il mapping a 1,0f) e il valore minimo significa -1,0f (ad esempio, il valore a 5 bit 10000 esegue il mapping a -1,0f). Inoltre, il secondo numero minimo esegue il mapping a -1,0f (ad esempio, il valore a 5 bit 10001 esegue il mapping a -1,0f). Sono quindi disponibili due rappresentazioni integer per -1,0f. È disponibile una singola rappresentazione per 0.0f e una singola rappresentazione per 1.0f. Viene così restituito un set di rappresentazioni integer per i valori a virgola mobile spaziati in modo uniforme nell'intervallo (-1,0f... 0,0f) e anche un set complementare di rappresentazioni per i numeri nell'intervallo (0,0f... 1.0f) |
| UNORM | Intero normalizzato senza segno, vale a dire che per un numero a n bit, tutti gli 0 significano 0,0f e tutti 1 significa 1,0f. Viene rappresentata una sequenza di valori a virgola mobile con spazi uniforme da 0,0f a 1,0f. Ad esempio, uno UNORM a 2 bit rappresenta 0,0f, 1/3, 2/3 e 1,0f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SINT  | Intero con segno. Numero intero complementare di 2. Ad esempio, un SINT a 3 bit rappresenta i valori integrali -4, -3, -2, -1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Intero senza segno. Ad esempio, un UINT a 3 bit rappresenta i valori integrali 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Valore a virgola mobile in una delle rappresentazioni definite da Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Simile a UNORM, in quanto per un numero a n bit, tutti gli 0 significa 0,0f e tutti 1 significa 1,0f. Tuttavia, a differenza di UNORM, con SRGB la sequenza di codifiche di interi senza segno tra tutti gli 0 e tutti gli 1 rappresenta una progressione non lineare nell'interpretazione a virgola mobile dei numeri, da 0,0f a 1,0f. Approssimativamente, se questa progressione non lineare, SRGB, viene visualizzata come sequenza di colori, apparirebbe come una rampa lineare di livelli di luminosità per un osservatore "medio", in condizioni di visualizzazione "medie", su uno schermo "medio". Per informazioni dettagliate, vedere lo standard dei colori SRGB, IEC 61996-2-1, in IEC (International Electrotechnical Commission).                |



 

## <a name="floating-point-conversion"></a>Conversione a virgola mobile

Ogni volta che si verifica una conversione a virgola mobile tra rappresentazioni diverse, incluse le rappresentazioni a virgola mobile, si applicano le regole seguenti.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Converso da una rappresentazione di intervallo superiore a una rappresentazione di intervallo inferiore

-   L'arrotondamento a zero viene usato durante la conversione in un altro formato float. Se la destinazione è un formato intero o a virgola fissa, viene usato round-to-nearest-even, a meno che la conversione non sia documentata in modo esplicito come l'uso di un altro comportamento di arrotondamento, ad esempio round-to-nearest per FLOAT in SNORM, FLOAT in UNORM o FLOAT in SRGB. Altre eccezioni sono le istruzioni ftoi e ftou shader, che usano round-to-zero. Infine, le conversioni da float a fisso usate dal campionatore di trama e dal rasterizzatore hanno una tolleranza specificata misurata in Unità ultima posizione da un ideale estremamente preciso.
-   Per i valori di origine maggiori dell'intervallo dinamico di un formato di destinazione dell'intervallo inferiore ,ad esempio Un valore float a 32 bit di grandi dimensioni viene scritto in un elemento RenderTarget float a 16 bit, il valore massimo rappresentabile (con segno appropriato), SENZA includere l'infinito con segno (a causa dell'arrotondamento a zero descritto in precedenza).
-   NaN in un formato di intervallo superiore verrà convertito nella rappresentazione NaN nel formato di intervallo inferiore se la rappresentazione NaN esiste nel formato di intervallo inferiore. Se il formato inferiore non ha una rappresentazione NaN, il risultato sarà 0.
-   InF in un formato di intervallo superiore verrà convertito in INF nel formato di intervallo inferiore, se disponibile. Se il formato inferiore non ha una rappresentazione INF, verrà convertito nel valore massimo rappresentabile. Il segno verrà mantenuto se disponibile nel formato di destinazione.
-   La denorm in un formato di intervallo superiore verrà convertita nella rappresentazione Denorm nel formato di intervallo inferiore, se disponibile nel formato di intervallo inferiore e la conversione è possibile. In caso contrario, il risultato è 0. Il bit di segno verrà mantenuto se disponibile nel formato di destinazione.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Conversione da una rappresentazione di intervallo inferiore a una rappresentazione di intervallo superiore

-   NaN in un formato di intervallo inferiore verrà convertito nella rappresentazione NaN nel formato di intervallo superiore, se disponibile nel formato di intervallo superiore. Se il formato di intervallo superiore non ha una rappresentazione NaN, verrà convertito in 0.
-   INF in un formato di intervallo inferiore verrà convertito nella rappresentazione INF nel formato di intervallo superiore, se disponibile nel formato di intervallo superiore. Se il formato superiore non ha una rappresentazione INF, verrà convertito nel valore massimo rappresentabile (MAX \_ FLOAT in tale formato). Il segno verrà mantenuto se disponibile nel formato di destinazione.
-   La denorm in un formato di intervallo inferiore verrà convertita in una rappresentazione normalizzata nel formato di intervallo superiore, se possibile, oppure in una rappresentazione denorm nel formato di intervallo superiore se la rappresentazione denorm esiste. In caso di esito negativo, se il formato di intervallo superiore non ha una rappresentazione denorm, verrà convertito in 0. Il segno verrà mantenuto se disponibile nel formato di destinazione. Si noti che i numeri float a 32 bit vengono conteggiati come formato senza una rappresentazione Denorm (perché Denorms nelle operazioni su float a 32 bit scarica per firmare il valore 0 mantenuto).

## <a name="integer-conversion"></a>Conversione integer

Nella tabella seguente vengono descritte le conversioni da diverse rappresentazioni descritte in precedenza ad altre rappresentazioni. Vengono visualizzate solo le conversioni effettivamente eseguite in Direct3D.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>SNORM</td>
<td>FLOAT</td>
<td>Dato un valore intero a n bit che rappresenta l'intervallo con segno da [-1,0f a 1,0f], la conversione in virgola mobile è la seguente.<br/>
<ul>
<li>Il valore più negativo viene mappato a -1,0f. Ad esempio, il valore a 5 bit 10000 esegue il mapping a -1,0f.</li>
<li>Ogni altro valore viene convertito in un valore float (chiamato c) e quindi result = c * (1,0f / (2⁽ⁿ⁻⁾-1)). Ad esempio, il valore a 5 bit 10001 viene convertito in -15,0f e quindi diviso per 15,0f, generando -1,0f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SNORM</td>
<td>Dato un numero a virgola mobile, la conversione in un valore integer a n bit che rappresenta l'intervallo con segno da [-1.0f a 1.0f] è la seguente.<br/>
<ul>
<li>Lasciare che c rappresenti il valore iniziale.</li>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0f, incluso INF, viene impostata su 1.0f.</li>
<li>Se c < -1.0f, incluso -INF, viene impostata su -1.0f.</li>
<li>Conversione dalla scala float alla scala integer: c = c * (2ⁿ⁻-1).</li>
<li>Eseguire la conversione in un intero come indicato di seguito.
<ul>
<li>Se c >= 0, c = c + 0,5f, in caso contrario c = c - 0,5f.</li>
<li>Eliminare la frazione decimale e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un intero.</li>
</ul></li>
</ul>
A questa conversione è consentita una tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Last-Place (sul lato integer). Ciò significa che dopo la conversione da float a integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore di formato di destinazione rappresentabile può eseguire il mapping a tale valore. Il requisito di invertibilità dei dati aggiuntivo garantisce che la conversione non si ricrea nell'intervallo e che tutti i valori di output siano raggiungibili. Nelle costanti illustrate di seguito <em>xx</em> deve essere sostituito con la versione Direct3D, ad esempio 10, 11 o 12.<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>Il valore n bit iniziale viene convertito in float (0,0f, 1,0f, 2,0f e così via) e quindi diviso per (2ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Lasciare che c rappresenti il valore iniziale.<br/>
<ul>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0f, incluso INF, viene impostata su 1.0f.</li>
<li>Se c < 0.0f, incluso -INF, viene impostata su 0,0f.</li>
<li>Eseguire la conversione da scala float a scala intera: c = c * (2ⁿ-1).</li>
<li>Eseguire la conversione in integer.
<ul>
<li>c = c + 0,5f.</li>
<li>La frazione decimale viene eliminata e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un intero.</li>
</ul></li>
</ul>
Questa conversione è consentita una tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (sul lato integer). Ciò significa che dopo la conversione da float a scala integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore di formato di destinazione rappresentabile è autorizzato a eseguire il mapping a tale valore. Il requisito di invertibilità dei dati aggiuntivo garantisce che la conversione non si ricrea nell'intervallo e che tutti i valori di output siano raggiungibili.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>FLOAT</td>
<td>Di seguito è riportata la conversione ideale da SRGB a FLOAT.<br/>
<ul>
<li>Prendere il valore iniziale a n bit, convertirlo in float (0,0f, 1.0f, 2.0f e così via). chiamare questo oggetto c.</li>
<li>c = c * (1,0f / (2ⁿ-1))</li>
<li>Se (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) quindi: result = c / D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, else: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2)D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Questa conversione consente una tolleranza di D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP Unit-Last-Place (sul lato SRGB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRGB</td>
<td>Di seguito è riportata la conversione ideale float -> SRGB.<br/> Supponendo che il componente di colore SRGB di destinazione abbia n bit:<br/>
<ul>
<li>Si supponga che il valore iniziale sia c.</li>
<li>Se c è NaN, il risultato è 0.</li>
<li>Se c > 1.0f, incluso INF, è impostata su 1.0f.</li>
<li>Se c < 0.0f, incluso -INF, viene impostata su 0,0f.</li>
<li>Se (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) quindi: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 * c, else: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 * c(D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) - D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Eseguire la conversione da scala float a scala intera: c = c * (2ⁿ-1).</li>
<li>Converti in integer:
<ul>
<li>c = c + 0,5f.</li>
<li>La frazione decimale viene eliminata e il valore a virgola mobile rimanente (integrale) viene convertito direttamente in un intero.</li>
</ul></li>
</ul>
Questa conversione è consentita una tolleranza di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (sul lato integer). Ciò significa che dopo la conversione da float a scala integer, qualsiasi valore all'interno di D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place di un valore di formato di destinazione rappresentabile è autorizzato a eseguire il mapping a tale valore. Il requisito di invertibilità dei dati aggiuntivo garantisce che la conversione non si ricrea nell'intervallo e che tutti i valori di output siano raggiungibili.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>SINT con più bit</td>
<td>Per eseguire la conversione da SINT a SINT con più bit, il bit più significativo (MSB) del numero iniziale è esteso al segno ai bit aggiuntivi disponibili nel formato &quot; &quot; di destinazione.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT con più bit</td>
<td>Per eseguire la conversione da UINT a SINT con più bit, il numero viene copiato nei bit meno significativi (LSB) del formato di destinazione e i DATABASE aggiuntivi vengono riempiti con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>UINT con più bit</td>
<td>Per eseguire la conversione da SINT a UINT con più bit: se negativo, il valore viene impostato su 0. In caso contrario, il numero viene copiato nelle LSB del formato di destinazione e gli oggetti MSB aggiuntivi vengono riempiti con 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT con più bit</td>
<td>Per eseguire la conversione da UINT a UINT con più bit, il numero viene copiato negli LSB del formato di destinazione e gli oggetti MSB aggiuntivi vengono riempiti con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT o UINT</td>
<td>SINT o UINT con un numero minore o uguale di bit</td>
<td>Per eseguire la conversione da SINT o UINT a SINT o UINT con un numero minore o uguale di bit (e/o modifica della firma), il valore iniziale viene semplicemente impostato sull'intervallo del formato di destinazione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversione di numeri interi a virgola fissa

Gli interi a virgola fissa sono semplicemente numeri interi di alcune dimensioni in bit che hanno un separatore decimale implicito in una posizione fissa.

Il tipo di dati "integer" onnipresente è un caso speciale di un intero a virgola fissa con il decimale alla fine del numero.

Le rappresentazioni di numeri a virgola fissa sono caratterizzate da: i.f, dove i è il numero di bit interi e f è il numero di bit frazionari. Ad esempio, 16,8 indica un numero intero a 16 bit seguito da 8 bit di frazione. La parte integer viene archiviata nel complemento di 2, almeno come definito qui (anche se può essere definita in modo uguale anche per gli interi senza segno). La parte frazionaria viene archiviata in formato non firmato. La parte frazionaria rappresenta sempre la frazione positiva tra i due valori integrali più vicini, a partire dal valore più negativo.

Le operazioni di addizione e sottrazione su numeri a virgola fissa vengono eseguite semplicemente usando l'aritmetica di interi standard, senza tenere conto della posizione in cui si trova il decimale implicito. L'aggiunta di 1 a un numero a virgola fissa 16,8 significa semplicemente aggiungere 256, poiché il separatore decimale è a 8 posizioni dalla fine meno significativa del numero. Altre operazioni, ad esempio la moltiplicazione, possono essere eseguite anche semplicemente usando l'aritmetica dei numeri interi, a condizione che l'effetto sul decimale fisso sia contabile. Ad esempio, la moltiplicazione di due numeri interi 16,8 usando una moltiplicazione integer produce un risultato di 32,16.

Le rappresentazioni integer a virgola fissa vengono usate in due modi in Direct3D.

-   Le posizioni dei vertici post-ritagliate nel rasterizzatore vengono bloccate al punto fisso, per distribuire in modo uniforme la precisione nell'area RenderTarget. Molte operazioni di rasterizzazione, tra cui l'eliminazione del viso come esempio, si verificano su posizioni ancorate a virgola fissa, mentre altre operazioni, ad esempio la configurazione dell'interpolatore di attributi, usano le posizioni che sono state convertite in virgola mobile dalle posizioni ancorate a virgola fissa.
-   Le coordinate di trama per le operazioni di campionamento vengono bloccate a un punto fisso (dopo essere state ridimensionate in base alle dimensioni della trama), per distribuire in modo uniforme la precisione nello spazio trame, scegliendo le posizioni/pesi del tocco del filtro. I valori di peso vengono convertiti nuovamente in virgola mobile prima che venga eseguita l'aritmetica di filtro effettiva.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Numero intero a virgola fissa</td>
<td>Di seguito è riportata la procedura generale per la conversione di un numero a virgola mobile n in un intero a virgola fissa i.f, dove i è il numero di bit interi (con segno) e f è il numero di bit frazionari.<br/>
<ul>
<li>Compute FixedMin = -2⁽ⁱ⁻¹⁾</li>
<li>Compute FixedMax = 2⁽ⁱ⁻¹⁾ - 2<sup>(-f)</sup></li>
<li>Se n è un NaN, result = 0; se n è +Inf, result = FixedMax*2<sup>f</sup>; se n è -Inf, result = FixedMin*2<sup>f</sup></li>
<li>Se n >= FixedMax, result = Fixedmax*2<sup>f</sup>; if n <= FixedMin, result = FixedMin*2 <sup> f</sup></li>
<li>Else calcola n*2<sup>f e</sup> converte in integer.</li>
</ul>
Alle implementazioni è consentita la tolleranza D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unit-last-place nel risultato integer, anziché il valore infinitamente preciso n*2<sup>f</sup> dopo l'ultimo passaggio precedente.<br/></td>
</tr>
<tr class="even">
<td>Numero intero a virgola fissa</td>
<td>FLOAT</td>
<td>Si supponga che la rappresentazione a virgola fissa specifica da convertire in float non contenga più di 24 bit di informazioni, di cui non più di 23 bit nel componente frazionario. Si supponga che un determinato numero a virgola fissa, fxp, sia in formato i.f (i bit integer, f bits fraction). La conversione in float è simile al seguente pseudocodice.<br/> float result = (float)(fxp >> f) + // extract integer<br/> <dl> ((float)(fxp & (2<sup>f</sup> - 1)) / (2<sup>f</sup>)); // estrarre la frazione<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




