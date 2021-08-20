---
description: Eventi di origine sequencer
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Eventi di origine sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6237d5b79be9555f6d3f00da870ac461b86395e84d837bd0cc5818040e20cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058118"
---
# <a name="sequencer-source-events"></a>Eventi di origine sequencer

Quando [l'origine Sequencer](sequencer-source.md) riproduce una sequenza di file, la sessione multimediale invia in genere tutti gli stessi eventi inviati durante la riproduzione normale e elencati in Eventi della [sessione multimediale.](media-session-events.md) L'applicazione ottiene questi eventi usando [**l'interfaccia IMFMediaEventGenerator della sessione**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) multimediale.

Esistono anche alcuni eventi specifici dei segmenti di playlist.



| Event                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Segnala all'applicazione di eseguire la pre-registrazione della topologia successiva.<br/> Per garantire una transizione senza problemi tra due presentazioni consecutive, l'origine Sequencer carica in anticipo la topologia successiva. Durante la riproduzione della topologia attiva, l'origine sequencer invia questo evento per la topologia successiva, purché sia disponibile una topologia successiva nell'origine.<br/> Questi dati di evento per questo evento sono il descrittore di presentazione per la topologia successiva. L'applicazione è responsabile dell'impostazione della topologia corrispondente nella sessione multimediale, come descritto in [Uso dell'origine Sequencer.](using-the-sequencer-source.md)<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | L'origine sequencer genera questo evento quando la sessione multimediale ha completato la riproduzione del segmento corrente, se tale segmento è seguito da un altro segmento. Se il segmento corrente è l'ultimo, l'origine sequencer genera invece [l'evento MEEndOfPresentation.](meendofpresentation.md)<br/> La sessione multimediale inoltra questo evento all'applicazione. In genere, l'applicazione riceve [MEEndOfPresentationSegment](meendofpresentationsegment.md) dopo che la sessione multimediale ha avviato l'elaborazione del segmento successivo, ma mentre i sink multimediali forniscono ancora gli esempi per il segmento precedente.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), con stato **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED**. | La sessione multimediale genera questo evento quando esegue una transizione alla topologia successiva nell'origine sequencer e i sink multimediali hanno completato la riproduzione della topologia precedente. Questo evento contiene un puntatore alla topologia successiva.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Esempio 1: Riproduzione senza ignorare

Quando l'origine sequencer è coinvolta, il numero di eventi che si ottengono dalla sessione multimediale può generare confusione, soprattutto perché gli eventi associati a un segmento sono spesso interleaved con gli eventi per il segmento successivo.

Nel primo esempio l'applicazione accoda tre segmenti, S1, S2 e S3. Il terzo segmento ha il flag **SequencerTopologyFlags \_ Last,** per segnalare che si tratta dell'ultimo segmento nella sequenza. Il segmento a cui corrisponde ogni evento è specificato tra parentesi. Sono elencate anche [**le chiamate SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) dell'applicazione, per rendere più chiaro l'ordine delle operazioni.

-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (start of S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fine di S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transizione a S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (start of S2)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fine di S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transizione a S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (start of S3)
-   [MEEndOfPresentation](meendofpresentation.md) (fine di S3; ultimo segmento)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED**
-   [MESessionEnded](mesessionended.md)

Questo elenco non include tutti gli eventi che è possibile ricevere. Ad esempio, omette l'evento [MESessionCapabilitiesChanged,](mesessioncapabilitieschanged.md) che viene inviato ogni volta che le funzionalità della sessione cambiano. Un'applicazione riceve in genere più eventi MESessionCapabilitiesChanged in una presentazione. Gli eventi elencati di seguito mostrano la transizione da un segmento a quello successivo. Gli eventi più importanti sono [MENewPresentation,](menewpresentation.md)che segnala all'applicazione di eseguire la pre-registrazione della topologia successiva, e [MEEndOfPresentationSegment,](meendofpresentationsegment.md)che segnala la fine di un segmento (ad eccezione dell'ultimo segmento).

Poiché gli eventi in Media Foundation sono asincroni e non vengono serializzati con chiamate al metodo, l'ordine esatto può variare. Ad esempio, è possibile ricevere **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** per S1 prima che l'applicazione chiami [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per S2.

Inoltre, è possibile che non tutti gli eventi elencati qui. Gli [eventi MEEndOfPresentation](meendofpresentation.md) e [MESessionEnded,](mesessionended.md) ad esempio, non vengono inviati a meno che l'ultimo segmento non abbia il flag **SequencerTopologyFlags \_ Last.**

Infine, questo elenco non indica il passaggio del tempo. L'ora da "inizio di S1" a "fine di S1" è l'intera durata di S1, che può essere di pochi secondi o molte ore, a seconda dell'origine.

## <a name="example-2-playback-with-segment-skipping"></a>Esempio 2: Riproduzione con segmento ignorato

In questo esempio l'applicazione accoda gli stessi segmenti, ma passa al segmento 3 durante la riproduzione del segmento 1. In questo caso, vengono inviati gli eventi seguenti:

-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (start of S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [**L'applicazione chiama IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (passa a S3)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   [**L'applicazione chiama IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 annullato)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transizione a S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ READY** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 annullato)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ ENDED** (S2)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ SINK \_ SWITCHED** (transizione a S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **TOPOSTATUS \_ READY** (S3)
-   [MESessionTopologyStatus:](mesessiontopologystatus.md) **MF \_ TOPOSTATUS \_ STARTED \_ SOURCE** (S3)

Quando l'applicazione chiama [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per passare al segmento 3, l'origine sequencer annulla il segmento 1, che è ancora in riproduzione. [L'evento MEEndOfPresentationSegment](meendofpresentationsegment.md) per questo segmento contiene l'attributo [**MF \_ EVENT SOURCE \_ \_ TOPOLOGY \_ CANCELED,**](mf-event-source-topology-canceled-attribute.md) che indica che il segmento è terminato perché è stato annullato. Quindi, poiché il segmento 2 è già pre-rolled, tale segmento viene avviato ma immediatamente annullato. L'evento MEEndOfPresentationSegment per il segmento 2 contiene anche l'attributo **MF \_ EVENT SOURCE \_ \_ TOPOLOGY \_ CANCELED.** La sessione può quindi passare al segmento 3 e riprodurla normalmente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'origine Sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 




