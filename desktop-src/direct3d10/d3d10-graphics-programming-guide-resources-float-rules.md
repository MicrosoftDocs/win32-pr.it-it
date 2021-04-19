---
description: Direct3D 10 supporta più rappresentazioni a virgola mobile diverse. Tutti i calcoli a virgola mobile operano in un subset definito del comportamento a virgola mobile a precisione singola IEEE 754 32 bit.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Regole del punto di FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304803"
---
# <a name="floating-point-rules-direct3d-10"></a>Regole a virgola mobile (Direct3D 10)

Direct3D 10 supporta più rappresentazioni a virgola mobile diverse. Tutti i calcoli a virgola mobile operano in un subset definito del comportamento a virgola mobile a precisione singola IEEE 754 32 bit.

-   [Regole Floating-Point a 32 bit](#32-bit-floating-point-rules)
    -   [Regole IEEE-754 rispettate](#honored-ieee-754-rules)
    -   [Deviazioni o requisiti aggiuntivi da regole IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Regole Floating-Point a 16 bit](#16-bit-floating-point-rules)
-   [Regole di Floating-Point a 11 e 10 bit](#11-bit-and-10-bit-floating-point-rules)
-   [Argomenti correlati](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Regole Floating-Point a 32 bit

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

-   IEEE-754 richiede che le operazioni a virgola mobile producano un risultato che rappresenta il valore rappresentabile più vicino a un risultato preciso all'infinito, noto come arrotondato al più vicino. Direct3D 10, tuttavia, definisce un requisito più flessibile: le operazioni a virgola mobile a 32 bit producono un risultato che si trova all'interno di un'unità-Last-Place (1 ULP rispetto) del risultato preciso all'infinito. Ciò significa che, ad esempio, l'hardware può troncare i risultati a 32 bit, anziché eseguire il round-to-the-even più vicino, perché questo genera un errore al massimo di un ULP rispetto.
-   Non è previsto alcun supporto per eccezioni a virgola mobile, bit di stato o trap.
-   Le denormazioni vengono scaricate allo zero senza segno per l'input e l'output di qualsiasi operazione matematica a virgola mobile. Vengono eseguite eccezioni per qualsiasi operazione di I/O o spostamento dei dati che non modifica i dati.
-   Gli Stati che contengono valori a virgola mobile, ad esempio viewport MinDepth/MaxDepth, i valori BorderColor e così via, possono essere forniti come valori denorm e possono essere scaricati o meno prima dell'utilizzo da parte dell'hardware.
-   Le operazioni minime o massime scaricano le denormazioni per il confronto, ma il risultato può essere scaricato o meno.
-   L'input NaN in un'operazione produce sempre NaN nell'output. Tuttavia, non è necessario che lo schema di bit esatto di NaN sia uguale, a meno che l'operazione non sia un'istruzione di spostamento non elaborata, che non modifica i dati.
-   Le operazioni min o Max per le quali un solo operando è NaN restituiscono l'altro operando come risultato (contrariamente alle regole di confronto precedenti). Si tratta di una nuova regola IEEE (IEEE 754R), necessaria in Direct3D 10.
-   Un'altra nuova regola IEEE 754R è che min (-0, + 0) = = min (+ 0,-0) = =-0 e Max (-0, + 0) = = Max (+ 0,-0) = = + 0, che rispettano il segno, a differenza delle regole di confronto per zero con segno (sopra indicato). Direct3D 10 consiglia il comportamento IEEE 754R qui, ma non verrà applicato; è possibile che il risultato del confronto degli zeri sia dipendente dall'ordine dei parametri, usando un confronto che ignora i segni.
-   x \* 1.0 f restituisce sempre x (eccetto la denormazione scaricata).
-   x/1.0 f restituisce sempre x (eccetto la denormazione scaricata).
-   x +/-0,0 f restituisce sempre x (eccetto la denormazione scaricata). Ma-0 + 0 = + 0.
-   Le operazioni fuse, ad esempio Mad, DP3, producono risultati che non sono meno accurati rispetto al peggiore ordine seriale possibile di valutazione dell'espansione non fusa dell'operazione. Si noti che la definizione del peggiore ordinamento possibile, per finalità di tolleranza, non è una definizione fissa per un'operazione di cui è stata eseguita la fusione. dipende dai valori specifici degli input. I singoli passaggi nell'espansione non fusa sono consentiti per ciascuna tolleranza ULP rispetto (o per tutte le istruzioni che Direct3D 10 chiama con una tolleranza di lassismo maggiore di 1 ULP rispetto, maggiore è la tolleranza di lassismo).
-   Le operazioni fuse rispettano le stesse regole NaN delle operazioni non fuse.
-   Multiply e divide each operano a livello di precisione a virgola mobile a 32 bit (accuratezza su 1 ULP rispetto).

## <a name="16-bit-floating-point-rules"></a>Regole Floating-Point a 16 bit

Direct3D 10 supporta inoltre le rappresentazioni a 16 bit dei numeri a virgola mobile.

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

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Regole di Floating-Point a 11 e 10 bit

Direct3D 10 supporta inoltre formati a virgola mobile a 11 e 10 bit.

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

le regole a virgola mobile a 32 bit sono inoltre disponibili per i numeri a virgola mobile a 11 e 10 bit, adattati per il layout di bit descritto in precedenza. Le eccezioni sono le seguenti:

-   Precisione: le regole a virgola mobile a 32 bit aderiscono a 0,5 ULP rispetto.
-   i numeri a virgola mobile 10/11 bit conservano le norme.
-   Qualsiasi operazione che comporterebbe un numero minore di zero, viene fissata su zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



