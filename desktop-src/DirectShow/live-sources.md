---
description: Origini in tempo reale
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Origini in tempo reale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8872cc5489ae61f3b7b9629e97303ad033630346094f8f1faa013f5da81d9142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153199"
---
# <a name="live-sources"></a>Origini in tempo reale

Un'origine live, detta anche *origine push,* riceve i dati in tempo reale. Ad esempio, l'acquisizione di video e le trasmissioni di rete. In generale, un'origine in tempo reale non può controllare la velocità di arrivo dei dati.

Un filtro viene considerato un'origine live se si verifica una delle condizioni seguenti:

-   Il filtro restituisce il flag AM FILTER MISC FLAGS IS SOURCE dal metodo \_ \_ \_ \_ \_ [**IAMFilterMiscFlags::GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) e almeno uno dei relativi pin di output espone [**l'interfaccia IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)
-   Il filtro espone [**l'interfaccia IKsPropertySet**](ikspropertyset.md) e dispone di un pin di acquisizione (PIN \_ CATEGORY \_ CAPTURE). Per [altre informazioni, vedere Aggiungere un set](pin-property-set.md) di proprietà.

Se un filtro di origine live fornisce un orologio, Filter Graph Manager preferirà tale orologio quando sceglie l'orologio di riferimento del grafo. Per [altre informazioni, vedere Clock di](reference-clocks.md) riferimento.

**Latency**

La latenza di un filtro è la quantità di tempo necessario al filtro per elaborare un campione. Per le origini in tempo reale, la latenza è determinata dalle dimensioni del buffer usato per contenere i campioni. Si supponga, ad esempio, che il grafo del filtro abbia un'origine video con una latenza di 33 millisecondi (ms) e un'origine audio con una latenza di 500 ms. Ogni fotogramma video arriva al renderer video circa 470 ms prima che il campione audio corrispondente raggiunga il renderer audio. A meno che il grafo non compensi la differenza, l'audio e il video non verranno sincronizzati.

Le origini in tempo reale possono essere sincronizzate tramite [**l'interfaccia IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) Filter Graph Manager non sincronizza le origini in tempo reale a meno che l'applicazione non abiliti la sincronizzazione chiamando il metodo [**IAMGraphStreams::SyncUsingStreamOffset.**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) Se la sincronizzazione è abilitata, il filtro Graph Manager esegue una query su ogni filtro di origine **per IAMPushSource.** Se il filtro supporta **IAMPushSource,** Filter Graph Manager chiama [**IAMLatency::GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) per recuperare la latenza prevista del filtro. **L'interfaccia IAMPushSource** eredita [**IAMLatency.**](/windows/desktop/api/Strmif/nn-strmif-iamlatency) Dai valori di latenza combinati, Il gestore Graph filtro determina la latenza massima prevista nel grafico. Chiama quindi [**IAMPushSource::SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) per assegnare a ogni filtro di origine un offset di flusso, che tale filtro aggiunge ai timestamp generati.

Questo metodo è destinato principalmente all'anteprima live. Si noti tuttavia che un segnaposto di anteprima in un dispositivo di acquisizione dinamica (ad esempio una fotocamera) non imposta timestamp sui campioni forniti. Pertanto, per usare questo metodo con un dispositivo di acquisizione live, è necessario visualizzare l'anteprima dal pin di acquisizione. Per altre informazioni, vedere DirectShow [filtri di acquisizione video.](directshow-video-capture-filters.md)

Attualmente [**l'interfaccia IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) è supportata dal filtro [VFW Capture](vfw-capture-filter.md) e dal filtro [Acquisizione audio.](audio-capture-filter.md)

**Corrispondenza della frequenza**

Se un filtro del renderer pianifica i campioni usando un clock di riferimento, ma il filtro di origine li produce usando un clock diverso, possono verificarsi errori nella riproduzione. Il renderer potrebbe essere eseguito più velocemente rispetto all'origine, causando lacune nei dati. In caso contrario, potrebbe essere eseguito più lentamente rispetto all'origine, causando il "grappolo" degli esempi fino a quando a un certo punto il grafo non elimina i campioni. In genere, un'origine live non può controllare la frequenza di produzione, pertanto il renderer deve corrispondere alle frequenze con l'origine.

Attualmente, solo il renderer audio esegue la corrispondenza della frequenza, perché gli glitch nella riproduzione audio sono più evidenti rispetto agli anomalie nel video. Per eseguire la corrispondenza della frequenza, il renderer audio deve selezionare un elemento rispetto al quale corrisponderà alle frequenze. Usa l'algoritmo seguente:

-   Se il grafico non usa un clock di riferimento, il renderer audio non tenta di trovare corrispondenze. Ogni volta che il grafo non ha un clock di riferimento, il rendering degli esempi viene sempre eseguito immediatamente all'arrivo.
-   In caso contrario, se è presente un clock di riferimento per il grafo, il renderer audio verifica se è presente un'origine live a monte, usando i criteri descritti in precedenza. In caso contrario, il renderer audio non corrisponde alle frequenze.
-   Se è presente un'origine live upstream e tale origine espone l'interfaccia [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) sul pin di output, il renderer audio chiama [**IAMPushSource::GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Cerca uno dei flag seguenti:
    -   AM \_ PUSHSOURCECAPS \_ INTERNAL \_ RM. Questo flag indica che il filtro di origine ha un proprio meccanismo di corrispondenza della frequenza, quindi il renderer audio non corrisponde alle frequenze.
    -   AM \_ PUSHSOURCECAPS \_ NON \_ LIVE. Questo flag indica che il filtro di origine non è effettivamente un'origine live, anche se espone [**l'interfaccia IAMPushSource.**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) Pertanto, il renderer audio non corrisponde alle frequenze.
    -   CLOCK \_ PRIVATO AM PUSHSOURCECAPS. \_ \_ Questo flag indica che il filtro di origine usa un orologio privato per generare timestamp. In questo caso, il renderer audio corrisponde alle tariffe rispetto ai timestamp. Se tuttavia gli esempi non hanno timestamp, il renderer ignora questo flag.
-   Se [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) non restituisce alcun flag (zero), il comportamento del renderer audio dipende dall'orologio del grafo e dal fatto che gli esempi presentino timestamp:
    -   Se il renderer audio non è l'orologio del grafo e gli esempi hanno timestamp, il renderer audio corrisponde alle frequenze rispetto ai timestamp.
    -   Se gli esempi non hanno timestamp, il renderer audio prova a corrispondere alla frequenza dei dati audio in ingresso.
    -   Se il renderer audio è l'orologio del grafo, tenta di trovare la corrispondenza con la velocità dei dati in ingresso.

Il motivo dell'ultimo caso è il seguente: se il renderer audio è l'orologio di riferimento e il filtro di origine usa lo stesso clock per generare timestamp, il renderer audio non può trovare corrispondenze con i timestamp. In caso contrario, in effetti, si cerca di trovare una corrispondenza tra le tariffe e se stessa, causando una deriva dell'orologio. Di conseguenza, in questo caso il renderer corrisponde alla frequenza dei dati audio in ingresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



