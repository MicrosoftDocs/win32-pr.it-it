---
title: Regole a virgola mobile (Direct3D 11)
description: Direct3D 11 supporta diverse rappresentazioni a virgola mobile. Tutti i calcoli a virgola mobile operano in un subset definito delle regole a virgola mobile a precisione singola IEEE 754 32 bit.
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83c87db0daa69c0393d0399ece5bdb6cf01d519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399138"
---
# <a name="floating-point-rules-direct3d-11"></a>Regole a virgola mobile (Direct3D 11)

Direct3D 11 supporta diverse rappresentazioni a virgola mobile. Tutti i calcoli a virgola mobile operano in un subset definito delle regole a virgola mobile a precisione singola IEEE 754 32 bit.

-   [regole a virgola mobile a 32 bit](#32-bit-floating-point-rules)
    -   [Regole IEEE-754 rispettate](#honored-ieee-754-rules)
    -   [Deviazioni o requisiti aggiuntivi da regole IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [regole a virgola mobile a 64 bit (precisione doppia)](#64-bit-double-precision-floating-point-rules)
-   [regole a virgola mobile a 16 bit](#16-bit-floating-point-rules)
-   [regole a virgola mobile a 11 e 10 bit](#11-bit-and-10-bit-floating-point-rules)
-   [Argomenti correlati](#related-topics)

## <a name="32-bit-floating-point-rules"></a>regole a virgola mobile a 32 bit

Sono disponibili due set di regole: quelle conformi a IEEE-754 e quelle che si scostano dallo standard.

### <a name="honored-ieee-754-rules"></a>Regole IEEE-754 rispettate

Alcune di queste regole sono una singola opzione in cui IEEE-754 offre opzioni.

-   Divide per 0 produce +/-INF, eccetto 0/0, che restituisce NaN.
-   log di (+/-) 0 produce-INF. il log di un valore negativo (diverso da-0) produce NaN.
-   La radice quadrata reciproca (RSQ) o radice quadrata (sqrt) di un numero negativo produce NaN. L'eccezione è-0; sqrt (-0) produce-0 e RSQ (-0) produce-INF.
-   INF-INF = NaN
-   (+/-) INF/(+/-) INF = NaN
-   (+/-) INF \* 0 = Nan
-   NaN (any OP) any-value = NaN
-   I confronti EQ, GT, GE, LT e LE, quando uno o entrambi gli operandi è NaN restituisce **false**.
-   I confronti ignorano il segno di 0 (quindi + 0 è uguale a-0).
-   Il confronto NE, quando uno o entrambi gli operandi è NaN restituisce **true**.
-   I confronti di qualsiasi valore non NaN rispetto a +/-INF restituiscono il risultato corretto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Deviazioni o requisiti aggiuntivi da regole IEEE-754

-   IEEE-754 richiede che le operazioni a virgola mobile producano un risultato che rappresenta il valore rappresentabile più vicino a un risultato preciso all'infinito, noto come arrotondato al più vicino. Direct3D 11 definisce lo stesso requisito: le operazioni a virgola mobile a 32 bit producono un risultato compreso tra 0,5 unit-Last-Place (ULP rispetto) del risultato di precisione infinita. Ciò significa che, ad esempio, l'hardware può troncare i risultati a 32 bit, anziché eseguire l'operazione più vicina, perché questo genera un errore di al massimo 0,5 ULP rispetto. Questa regola si applica solo a addizioni, sottrazioni e moltiplicazioni.
-   Non è previsto alcun supporto per eccezioni a virgola mobile, bit di stato o trap.
-   Le denormazioni vengono scaricate allo zero senza segno per l'input e l'output di qualsiasi operazione matematica a virgola mobile. Vengono eseguite eccezioni per qualsiasi operazione di I/O o spostamento dei dati che non modifica i dati.
-   Gli Stati che contengono valori a virgola mobile, ad esempio viewport MinDepth/MaxDepth, i valori BorderColor, possono essere forniti come valori di deregolazione e possono o meno essere scaricati prima che l'hardware li usi.
-   Le operazioni minime o massime scaricano le denormazioni per il confronto, ma il risultato può essere scaricato o meno.
-   L'input NaN in un'operazione produce sempre NaN nell'output. Tuttavia, non è necessario che lo schema di bit esatto di NaN sia uguale, a meno che l'operazione non sia un'istruzione di spostamento non elaborata, che non modifica i dati.
-   Le operazioni min o Max per le quali un solo operando è NaN restituiscono l'altro operando come risultato (contrariamente alle regole di confronto esaminate in precedenza). Si tratta di una regola IEEE 754R.

    La specifica IEEE-754R per le operazioni min e Max a virgola mobile indica che se uno degli input a min o Max è un valore di QNaN non interattiva, il risultato dell'operazione è l'altro parametro. Ad esempio:

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    Una revisione della specifica IEEE-754R ha adottato un comportamento diverso per min e Max quando un input è un valore SNaN di "segnalazione" rispetto a un valore di QNaN:

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    In genere, Direct3D segue gli standard per aritmetici: IEEE-754 e IEEE-754R. Ma in questo caso, abbiamo una deviazione.

    Le regole aritmetiche in Direct3D 10 e versioni successive non fanno alcuna distinzione tra i valori NaN quiet e Signaling (QNaN e SNaN). Tutti i valori NaN vengono gestiti allo stesso modo. Nel caso di min e Max, il comportamento di Direct3D per qualsiasi valore NaN è simile al modo in cui QNaN viene gestito nella definizione IEEE-754R. (Per completezza-se entrambi gli input sono NaN, viene restituito qualsiasi valore NaN).

-   Un'altra regola IEEE 754R è che min (-0, + 0) = = min (+ 0,-0) = =-0 e Max (-0, + 0) = = Max (+ 0,-0) = = + 0, che rispetta il segno, a differenza delle regole di confronto per zero con segno (come illustrato in precedenza). Direct3D consiglia il comportamento IEEE 754R qui, ma non lo impone. è possibile che il risultato del confronto degli zeri sia dipendente dall'ordine dei parametri, usando un confronto che ignora i segni.
-   x \* 1.0 f restituisce sempre x (eccetto la denormazione scaricata).
-   x/1.0 f restituisce sempre x (eccetto la denormazione scaricata).
-   x +/-0,0 f restituisce sempre x (eccetto la denormazione scaricata). Ma-0 + 0 = + 0.
-   Le operazioni fuse, ad esempio Mad, DP3, producono risultati che non sono meno accurati rispetto al peggiore ordine seriale possibile di valutazione dell'espansione non fusa dell'operazione. La definizione del peggiore ordinamento possibile, allo scopo di tollerare, non è una definizione fissa per un'operazione di cui è stata eseguita la fusione. dipende dai valori specifici degli input. I singoli passaggi nell'espansione non fusa sono consentiti per ciascuna tolleranza ULP rispetto (o per tutte le istruzioni che Direct3D chiama con una tolleranza di lassismo maggiore di 1 ULP rispetto, maggiore è la tolleranza di lassismo).
-   Le operazioni fuse rispettano le stesse regole NaN delle operazioni non fuse.
-   sqrt e RCP hanno una tolleranza ULP rispetto. Le istruzioni per la radice quadrata reciproca e reciproca dello shader, [**RCP**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) e [**RSQ**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-), hanno un requisito di precisione separata distinto.
-   Multiply e divide each operano a livello di precisione a virgola mobile a 32 bit (accuratezza a 0,5 ULP rispetto per Multiply, 1,0 ULP rispetto per reciproca). Se x/y viene implementato direttamente, i risultati devono essere di precisione maggiore o uguale a quello di un metodo in due passaggi.

## <a name="64-bit-double-precision-floating-point-rules"></a>regole a virgola mobile a 64 bit (precisione doppia)

I driver hardware e display supportano facoltativamente la virgola mobile a precisione doppia. Per indicare il supporto, quando si chiama [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la [**\_ funzionalità d3d11 \_ Doubles**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature), il driver imposta **DoublePrecisionFloatShaderOps** dei dati della [**funzionalità di d3d11 \_ \_ \_ Double**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) su true. Il driver e l'hardware devono supportare tutte le istruzioni a virgola mobile a precisione doppia.

Le istruzioni a precisione doppia seguono i requisiti del comportamento IEEE 754R.

Il supporto per la generazione di valori denormalizzati è necessario per i dati a precisione doppia (nessun comportamento di scaricamento zero). Analogamente, le istruzioni non leggono i dati denormalizzati come zero con segno, rispettano il valore della denorma.

## <a name="16-bit-floating-point-rules"></a>regole a virgola mobile a 16 bit

Direct3D 11 supporta inoltre le rappresentazioni a 16 bit dei numeri a virgola mobile.

Formato:

-   1 bit/i di segno nella posizione del bit MSB
-   5 bit di esponente polarizzato (e)
-   10 bit di frazione (f), con un bit nascosto aggiuntivo

Un valore float16 (v) segue le regole seguenti:

-   Se e = = 31 e f! = 0, v è NaN indipendentemente da s
-   Se e = = 31 e f = = 0, v = (-1) s \* Infinity (Signed Infinity)
-   Se e è compreso tra 0 e 31, v = (-1) s \* 2 (e-15) \* (1. f)
-   Se e = = 0 e f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (numeri denormalizzati)
-   Se e = = 0 e f = = 0, v = (-1) s \* 0 (con segno zero)

le regole a virgola mobile a 32 bit sono disponibili anche per i numeri a virgola mobile a 16 bit, adattati per il layout di bit descritto in precedenza. Alcune eccezioni:

-   Precisione: le operazioni non fuse sui numeri a virgola mobile a 16 bit producono un risultato che rappresenta il valore rappresentabile più vicino a un risultato preciso all'infinito (arrotondato al più vicino anche per IEEE-754, applicato ai valori a 16 bit). le regole a virgola mobile a 32 bit rispettano una tolleranza ULP rispetto, le regole a virgola mobile a 16 bit sono conformi a 0,5 ULP rispetto per le operazioni non fuse e 0,6 ULP rispetto per le operazioni fuse.
-   i numeri a virgola mobile a 16 bit conservano le norme.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>regole a virgola mobile a 11 e 10 bit

Direct3D 11 supporta inoltre formati a virgola mobile a 11 e 10 bit.

Formato:

-   Nessun bit di segno
-   5 bit di esponente polarizzato (e)
-   6 bit della frazione (f) per un formato a 11 bit, a 5 bit di frazione (f) per un formato a 10 bit, con un bit nascosto aggiuntivo in entrambi i casi.

Un valore float11/float10 (v) segue le regole seguenti:

-   Se e = = 31 e f! = 0, v è NaN
-   Se e = = 31 e f = = 0, v = + Infinity
-   Se e è compreso tra 0 e 31, v = 2 (e-15) \* (1. f)
-   Se e = = 0 e f! = 0, v = \* 2 (e-14) \* (0. f) (numeri denormalizzati)
-   Se e = = 0 e f = = 0, v = 0 (zero)

le regole a virgola mobile a 32 bit sono disponibili anche per i numeri a virgola mobile a 11 bit e a 10 bit, adattati per il layout di bit descritto in precedenza. Le eccezioni sono le seguenti:

-   Precisione: le regole a virgola mobile a 32 bit aderiscono a 0,5 ULP rispetto.
-   i numeri a virgola mobile 10/11 bit conservano le norme.
-   Qualsiasi operazione che comporterebbe un numero minore di zero viene fissata a zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 