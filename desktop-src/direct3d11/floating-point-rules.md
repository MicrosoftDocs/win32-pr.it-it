---
title: Regole a virgola mobile (Direct3D 11)
description: Direct3D 11 supporta diverse rappresentazioni a virgola mobile. Tutti i calcoli a virgola mobile operano in base a un subset definito delle regole a virgola mobile a precisione singola IEEE 754 a 32 bit.
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d802c3ebc682ced58ceddbe3db0091755d0b30bb79ffbfc9ddb454d5d4d383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677111"
---
# <a name="floating-point-rules-direct3d-11"></a>Regole a virgola mobile (Direct3D 11)

Direct3D 11 supporta diverse rappresentazioni a virgola mobile. Tutti i calcoli a virgola mobile operano in base a un subset definito delle regole a virgola mobile a precisione singola IEEE 754 a 32 bit.

-   [Regole a virgola mobile a 32 bit](#32-bit-floating-point-rules)
    -   [Regole IEEE-754 rispettate](#honored-ieee-754-rules)
    -   [Deviazioni o requisiti aggiuntivi dalle regole IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Regole a virgola mobile a 64 bit (precisione doppia)](#64-bit-double-precision-floating-point-rules)
-   [Regole a virgola mobile a 16 bit](#16-bit-floating-point-rules)
-   [Regole a virgola mobile a 11 bit e a 10 bit](#11-bit-and-10-bit-floating-point-rules)
-   [Argomenti correlati](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Regole a virgola mobile a 32 bit

Esistono due set di regole: quelle conformi allo standard IEEE-754 e quelle che si discostono dallo standard.

### <a name="honored-ieee-754-rules"></a>Regole IEEE-754 rispettate

Alcune di queste regole sono un'unica opzione in cui IEEE-754 offre opzioni.

-   La divisione per 0 produce +/- INF, ad eccezione di 0/0 che restituisce NaN.
-   il log di (+/-) 0 produce -INF. log di un valore negativo (diverso da -0) produce NaN.
-   La radice quadrata reciproca (rsq) o radice quadrata (sqrt) di un numero negativo produce NaN. L'eccezione è -0. sqrt(-0) produce -0 e rsq(-0) produce -INF.
-   INF - INF = NaN
-   (+/-) INF / (+/-)INF = NaN
-   (+/-) INF \* 0 = NaN
-   NaN (qualsiasi OP) any-value = NaN
-   I confronti EQ, GT, GE, LT e LE quando uno o entrambi gli operandi sono NaN restituisce **FALSE.**
-   I confronti ignorano il segno 0 (quindi +0 è uguale a -0).
-   L'OPERATORE di confronto, quando uno o entrambi gli operandi è NaN restituisce **TRUE.**
-   I confronti di qualsiasi valore non NaN con +/- INF restituiscono il risultato corretto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Deviazioni o requisiti aggiuntivi dalle regole IEEE-754

-   IEEE-754 richiede operazioni a virgola mobile per produrre un risultato che sia il valore rappresentabile più vicino a un risultato con precisione infinita, noto come round-to-nearest-even. Direct3D 11 definisce lo stesso requisito: le operazioni a virgola mobile a 32 bit producono un risultato entro 0,5 unità(ULP) del risultato con precisione infinita. Ciò significa che, ad esempio, all'hardware è consentito troncare i risultati a 32 bit anziché eseguire il round-to-nearest-even, perché ciò comporta un errore di al massimo 0,5 ULP. Questa regola si applica solo all'addizione, alla sottrazione e alla moltiplicazione.
-   Non è disponibile alcun supporto per eccezioni a virgola mobile, bit di stato o trap.
-   I denorm vengono scaricati in modo da mantenere il segno zero all'input e all'output di qualsiasi operazione matematica a virgola mobile. Vengono effettuate eccezioni per qualsiasi operazione di I/O o spostamento dei dati che non modifica i dati.
-   Gli stati che contengono valori a virgola mobile, ad esempio Viewport MinDepth/MaxDepth, i valori BorderColor, possono essere forniti come valori di denorm e possono essere scaricati o meno prima che l'hardware li usi.
-   Le operazioni min o max scaricano i denorm per il confronto, ma il risultato può essere o meno denorm scaricato.
-   L'input NaN per un'operazione produce sempre NaN nell'output. Tuttavia, lo schema di bit esatto del valore NaN non deve rimanere lo stesso (a meno che l'operazione non sia un'istruzione di spostamento non elaborata, che non modifica i dati).
-   Le operazioni min o max per cui solo un operando è NaN restituiscono l'altro operando come risultato (contrariamente alle regole di confronto osservate in precedenza). Si tratta di una regola IEEE 754R.

    La specifica IEEE-754R per le operazioni min e max a virgola mobile indica che se uno degli input per min o max è un valore QNaN non interattiva, il risultato dell'operazione è l'altro parametro. Esempio:

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    Una revisione della specifica IEEE-754R ha adottato un comportamento diverso per min e max quando un input è un valore SNaN di "segnalazione" rispetto a un valore QNaN:

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    In genere, Direct3D segue gli standard per l'aritmetica: IEEE-754 e IEEE-754R. In questo caso, tuttavia, si ha una deviazione.

    Le regole aritmetiche in Direct3D 10 e versioni successive non fanno alcuna distinzione tra i valori NaN non interattiva e di segnalazione (QNaN e SNaN). Tutti i valori NaN vengono gestiti nello stesso modo. Nel caso di min e max, il comportamento di Direct3D per qualsiasi valore NaN è simile al modo in cui QNaN viene gestito nella definizione IEEE-754R. Per completezza, se entrambi gli input sono NaN, viene restituito qualsiasi valore NaN.

-   Un'altra regola IEEE 754R è che min(-0,+0) == min(+0,-0) == -0 e max(-0,+0) == max(+0,-0) == +0, che rispetta il segno, a differenza delle regole di confronto per lo zero con segno (come illustrato in precedenza). Direct3D consiglia il comportamento di IEEE 754R, ma non lo applica. è consentito che il risultato del confronto degli zeri di dislovi in base all'ordine dei parametri, usando un confronto che ignora i segni.
-   x \* 1.0f restituisce sempre x (ad eccezione di denorm flushed).
-   x/1.0f restituisce sempre x (ad eccezione di denorm flushed).
-   x +/- 0,0f restituisce sempre x (ad eccezione di denorm flushed). Ma -0 + 0 = +0.
-   Le operazioni fuse (ad esempio, mad, dp3) producono risultati non meno accurati rispetto all'ordinamento seriale peggiore possibile della valutazione dell'espansione inutilizzata dell'operazione. La definizione dell'ordinamento peggiore possibile, ai fini della tolleranza, non è una definizione fissa per una determinata operazione fusa; dipende dai valori specifici degli input. I singoli passaggi nell'espansione non utilizzata sono ognuno dei quali è consentita una tolleranza 1 ULP (o per qualsiasi istruzione Direct3D chiama con una tolleranza di lax maggiore di 1 ULP, maggiore è la tolleranza lax).
-   Le operazioni fuse rispettano le stesse regole NaN delle operazioni non fuse.
-   sqrt e rcp hanno 1 tolleranza ULP. Le istruzioni della radice quadrata reciproca e reciproca dello shader, [**rcp**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) e [**rsq,**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-)hanno un proprio requisito di precisione di tipo relaxed separato.
-   La moltiplicazione e la divisione di ogni operare al livello di precisione a virgola mobile a 32 bit (accuratezza a 0,5 ULP per la moltiplicazione, 1,0 ULP per reciproco). Se x/y viene implementato direttamente, i risultati devono essere di maggiore o uguale accuratezza rispetto a un metodo in due passaggi.

## <a name="64-bit-double-precision-floating-point-rules"></a>Regole a virgola mobile a 64 bit (precisione doppia)

I driver hardware e di visualizzazione supportano facoltativamente la virgola mobile a precisione doppia. Per indicare il supporto, quando si chiama [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ DOUBLES,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)il driver imposta **DoublePrecisionFloatShaderOps** di [**D3D11 \_ FEATURE DATA \_ \_ DOUBLES**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) su TRUE. Il driver e l'hardware devono quindi supportare tutte le istruzioni a virgola mobile e precisione doppia.

Le istruzioni a precisione doppia seguono i requisiti di comportamento di IEEE 754R.

Il supporto per la generazione di valori denormalizzati è necessario per i dati a precisione doppia (nessun comportamento di scaricamento a zero). Analogamente, le istruzioni non leggono i dati denormalizzati come zero con segno, ma rispettano il valore di denorm.

## <a name="16-bit-floating-point-rules"></a>Regole a virgola mobile a 16 bit

Direct3D 11 supporta anche rappresentazioni a 16 bit di numeri a virgola mobile.

Formato:

-   1 bit di segno (s) nella posizione del bit MSB
-   5 bit di esponente distorto (e)
-   10 bit di frazione (f), con un bit nascosto aggiuntivo

Un valore float16 (v) segue queste regole:

-   se e == 31 e f != 0, v è NaN indipendentemente da s
-   se e == 31 e f == 0, v = (-1)s \* infinity (infinito con segno)
-   se e è compreso tra 0 e 31, v = (-1)s \* 2(e-15) \* (1.f)
-   se e == 0 e f != 0, v = (-1)s \* 2(e-14) \* (0.f) (numeri denormalizzati)
-   se e == 0 e f == 0, v = (-1)s \* 0 (zero con segno)

Le regole a virgola mobile a 32 bit contengono anche numeri a virgola mobile a 16 bit, regolati per il layout di bit descritto in precedenza. Alcune eccezioni:

-   Precisione: le operazioni non utilizzate sui numeri a virgola mobile a 16 bit producono un risultato che è il valore rappresentabile più vicino a un risultato con precisione infinita (arrotondare al pari più vicino, per IEEE-754, applicato ai valori a 16 bit). Le regole a virgola mobile a 32 bit rispettano la tolleranza 1 ULP, le regole a virgola mobile a 16 bit sono conformi a 0,5 ULP per le operazioni non utilizzate e a 0,6 ULP per le operazioni fuse.
-   I numeri a virgola mobile a 16 bit mantengono i denorm.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Regole a virgola mobile a 11 bit e a 10 bit

Direct3D 11 supporta anche formati a virgola mobile a 11 bit e a 10 bit.

Formato:

-   Nessun bit di segno
-   5 bit di esponente distorto (e)
-   6 bit di frazione (f) per un formato a 11 bit, 5 bit di frazione (f) per un formato a 10 bit, con un bit nascosto aggiuntivo in entrambi i casi.

Un valore float11/float10 (v) segue le regole seguenti:

-   se e == 31 e f != 0, v è NaN
-   se e == 31 e f == 0, quindi v = +infinito
-   se e è compreso tra 0 e 31, v = 2(e-15) \* (1.f)
-   se e == 0 e f != 0, v = \* 2(e-14) \* (0.f) (numeri denormalizzati)
-   se e == 0 e f == 0, v = 0 (zero)

Le regole a virgola mobile a 32 bit contengono anche numeri a virgola mobile a 11 e 10 bit, regolati per il layout di bit descritto in precedenza. Le eccezioni sono le seguenti:

-   Precisione: le regole a virgola mobile a 32 bit sono conformi a 0,5 ULP.
-   I numeri a virgola mobile a 10/11 bit mantengono i nomi.
-   Qualsiasi operazione che restituisce un numero minore di zero viene impostata su zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 