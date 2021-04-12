---
description: Origini attive
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Origini attive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481749"
---
# <a name="live-sources"></a>Origini attive

Un'origine live, detta anche *origine push*, riceve i dati in tempo reale. Gli esempi includono acquisizione video e trasmissioni di rete. In generale, un'origine live non può controllare la velocità di arrivo dei dati.

Un filtro viene considerato un'origine live se si verifica una delle condizioni seguenti:

-   Il filtro restituisce il \_ filtro am \_ \_ flag varie \_ è il \_ flag di origine del metodo [**IAMFilterMiscFlags:: GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) e almeno uno dei relativi pin di output espone l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) .
-   Il filtro espone l'interfaccia [**IKsPropertySet**](ikspropertyset.md) e include un pin di acquisizione ( \_ acquisizione della categoria pin \_ ). Per ulteriori informazioni, vedere il [set di proprietà pin](pin-property-set.md) .

Se un filtro di origine Live fornisce un clock, il gestore del grafico del filtro preferisce tale clock quando sceglie l'orologio di riferimento del grafo. Per ulteriori informazioni, vedere [clock di riferimento](reference-clocks.md) .

**Latency**

La latenza di un filtro è la quantità di tempo impiegato dal filtro per elaborare un campione. Per le origini live, la latenza è determinata dalla dimensione del buffer usato per conservare gli esempi. Si supponga, ad esempio, che il grafico di filtro includa un'origine video con una latenza di 33 millisecondi (MS) e un'origine audio con una latenza di 500 ms. Ogni fotogramma video arriva al renderer video circa 470 ms prima che l'esempio audio corrispondente raggiunga il renderer audio. Se il grafico non compensa la differenza, l'audio e il video non verranno sincronizzati.

Le origini attive possono essere sincronizzate tramite l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Filter Graph Manager non sincronizza le origini attive a meno che l'applicazione non consenta la sincronizzazione chiamando il metodo [**IAMGraphStreams:: SyncUsingStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) . Se la sincronizzazione è abilitata, il gestore del grafico dei filtri esegue una query su ogni filtro di origine per **IAMPushSource**. Se il filtro supporta **IAMPushSource**, il gestore del grafo dei filtri chiama [**IAMLatency:: getlatence**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) per recuperare la latenza prevista del filtro. (L'interfaccia **IAMPushSource** eredita [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency)). Dai valori di latenza combinati, il gestore del grafico dei filtri determina la latenza massima prevista nel grafico. Chiama quindi [**IAMPushSource:: SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) per assegnare a ogni filtro di origine un offset del flusso, che tale filtro aggiunge agli indicatori temporali che genera.

Questo metodo è destinato principalmente all'anteprima in tempo reale. Si noti tuttavia che un pin di anteprima in un dispositivo di acquisizione in tempo reale, ad esempio una fotocamera, non imposta i timestamp sugli esempi che fornisce. Pertanto, per usare questo metodo con un dispositivo di acquisizione in tempo reale, è necessario visualizzare l'anteprima dal pin di acquisizione. Per altre informazioni, vedere [filtri di acquisizione video DirectShow](directshow-video-capture-filters.md).

Attualmente l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) è supportata dal filtro di [acquisizione di VFW](vfw-capture-filter.md) e dal filtro di [acquisizione audio](audio-capture-filter.md) .

**Corrispondenza frequenza**

Se un filtro renderer Pianifica esempi utilizzando un clock di riferimento, ma il filtro di origine li produce utilizzando un clock diverso, è possibile che si verifichino problemi durante la riproduzione. Il renderer potrebbe essere eseguito più velocemente rispetto all'origine, causando gap nei dati. In alternativa, è possibile che venga eseguito più lentamente rispetto all'origine, causando il "gruppo di campioni" fino a un certo punto in cui il grafico eliminerà i campioni. In genere, un'origine live non può controllare la velocità di produzione, quindi il renderer deve corrispondere alle frequenze con l'origine.

Attualmente, solo il renderer audio esegue la corrispondenza della frequenza, perché i glitch nella riproduzione audio sono più evidenti rispetto ai glitch nei video. Per eseguire la corrispondenza della frequenza, il renderer audio deve selezionare un elemento rispetto al quale corrisponderà alle tariffe. Usa l'algoritmo seguente:

-   Se il grafico non usa un orologio di riferimento, il renderer audio non tenta di trovare una corrispondenza con le tariffe. Ogni volta che il grafico non ha un clock di riferimento, viene sempre eseguito il rendering degli esempi immediatamente dopo l'arrivo.
-   In caso contrario, se è presente un clock di riferimento per il grafo, il renderer audio controlla se è presente un'origine live upstream, usando i criteri descritti in precedenza. In caso contrario, il renderer audio non corrisponde alle tariffe.
-   Se è presente un'origine live upstream e tale origine espone l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) sul pin di output, il renderer audio chiama [**IAMPushSource:: GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Cerca uno dei flag seguenti:
    -   AM \_ PUSHSOURCECAPS \_ Internal \_ RM. Questo flag indica che il filtro di origine ha un proprio meccanismo di corrispondenza della frequenza, quindi il renderer audio non corrisponde alle tariffe.
    -   il \_ PUSHSOURCECAPS \_ non è \_ attivo. Questo flag indica che il filtro di origine non è realmente un'origine live, anche se espone l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Pertanto, il renderer audio non corrisponde alle tariffe.
    -   AM \_ PUSHSOURCECAPS \_ private \_ Clock. Questo flag indica che il filtro di origine utilizza un clock privato per generare timestamp. In questo caso, il renderer audio corrisponde alle frequenze rispetto ai timestamp. Se gli esempi non hanno timestamp, tuttavia, il renderer ignora questo flag.
-   Se [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) non restituisce alcun flag (zero), il comportamento del renderer audio dipende dal clock del grafico e dal fatto che gli esempi abbiano timestamp:
    -   Se il renderer audio non è il clock del grafico e gli esempi hanno timestamp, il renderer audio corrisponde alle frequenze rispetto ai timestamp.
    -   Se gli esempi non hanno timestamp, il renderer audio tenta di trovare la corrispondenza con la frequenza dei dati audio in ingresso.
    -   Se il renderer audio è il clock del grafico, tenta di trovare una corrispondenza con la velocità dei dati in ingresso.

Il motivo dell'ultimo caso è il seguente: se il renderer audio è il clock di riferimento e il filtro di origine usa lo stesso clock per generare timestamp, il renderer audio non può corrispondere alle frequenze rispetto ai timestamp. In caso affermativo, si tenterà di trovare una corrispondenza con le tariffe, che potrebbero causare la desincronizzazione del clock. Pertanto, in questo caso il renderer corrisponde alla frequenza dei dati audio in ingresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



