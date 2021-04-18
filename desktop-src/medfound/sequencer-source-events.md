---
description: Eventi di origine di Sequencer
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Eventi di origine di Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309006"
---
# <a name="sequencer-source-events"></a>Eventi di origine di Sequencer

Quando l' [origine del sequencer](sequencer-source.md) riproduce una sequenza di file, la sessione multimediale Invia generalmente tutti gli stessi eventi inviati durante la riproduzione normale e che vengono elencati in eventi della [sessione multimediale](media-session-events.md). L'applicazione ottiene questi eventi usando l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale.

Sono inoltre disponibili alcuni eventi specifici per i segmenti della playlist.



| Event                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Segnala all'applicazione di preregistrare la topologia successiva.<br/> Per garantire una transizione uniforme tra due presentazioni consecutive, l'origine del sequencer carica in anticipo la topologia successiva. Mentre la topologia attiva è ancora in riproduzione, l'origine del sequencer Invia questo evento per la topologia successiva, purché sia disponibile una topologia successiva nell'origine.<br/> I dati dell'evento per questo evento sono rappresentati dal descrittore della presentazione per la topologia successiva. L'applicazione è responsabile dell'impostazione della topologia corrispondente nella sessione multimediale, come descritto in [uso dell'origine di Sequencer](using-the-sequencer-source.md).<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | L'origine di sequencer genera questo evento quando la sessione multimediale ha completato la riproduzione del segmento corrente, se tale segmento è seguito da un altro segmento. Se il segmento corrente è l'ultimo, l'origine del sequencer genera invece l'evento [MEEndOfPresentation](meendofpresentation.md) .<br/> La sessione multimediale trasmette questo evento all'applicazione. In genere, l'applicazione riceve [MEEndOfPresentationSegment](meendofpresentationsegment.md) dopo che la sessione multimediale ha avviato l'elaborazione del segmento successivo, ma mentre i sink del supporto continuano a consegnare gli esempi per il segmento precedente.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), con stato **MF \_ TOPOSTATUS \_ sink \_ cambiato**. | La sessione multimediale genera questo evento quando esegue una transizione alla topologia successiva nell'origine del sequencer e i sink di supporto hanno completato la riproduzione della topologia precedente. Questo evento contiene un puntatore alla topologia successiva.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Esempio 1: riproduzione senza omissione

Quando l'origine del sequencer è complessa, il numero di eventi che si ottengono dalla sessione multimediale può generare confusione, soprattutto perché gli eventi associati a un segmento sono spesso con interfoliazione con gli eventi per il segmento successivo.

Nel primo esempio, l'applicazione Accoda tre segmenti, S1, S2 e S3. Il terzo segmento presenta l' **\_ ultimo flag SequencerTopologyFlags** , per segnalare che si tratta dell'ultimo segmento della sequenza. Il segmento a cui corrisponde ogni evento viene specificato tra parentesi. Sono elencate anche le chiamate di [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) dell'applicazione per rendere più chiaro l'ordine delle operazioni.

-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (inizio di S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fine S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminato** (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ sink \_ spostato** (transizione a S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (inizio di S2)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fine S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminato** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ sink \_ spostato** (transizione a S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (inizio S3)
-   [MEEndOfPresentation](meendofpresentation.md) (fine S3; ultimo segmento)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminato**
-   [MESessionEnded](mesessionended.md)

Questo elenco non include tutti gli eventi che potrebbero essere ricevuti. (Ad esempio, omette l'evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) , che viene inviato ogni volta che le funzionalità della sessione cambiano. Un'applicazione riceve in genere più eventi MESessionCapabilitiesChanged in una presentazione. Gli eventi elencati di seguito sono quelli che mostrano la transizione da un segmento a quello successivo. Gli eventi più importanti sono [MENewPresentation](menewpresentation.md), che segnala all'applicazione di eseguire la preregistrazione della topologia successiva e [MEEndOfPresentationSegment](meendofpresentationsegment.md), che segnala la fine di un segmento (ad eccezione dell'ultimo segmento).

Poiché gli eventi in Media Foundation sono asincroni e non vengono serializzati con le chiamate al metodo, l'ordine esatto potrebbe variare. Ad esempio, è possibile ricevere **l' \_ origine MF TOPOSTATUS \_ avviata \_** per S1 prima che l'applicazione chiami la [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per S2.

Inoltre, potrebbe non essere possibile ottenere tutti gli eventi elencati qui. Gli eventi [MEEndOfPresentation](meendofpresentation.md) e [MESessionEnded](mesessionended.md) , ad esempio, non vengono inviati a meno che l'ultimo segmento non includa l' **\_ ultimo flag SequencerTopologyFlags** .

Infine, questo elenco non indica il passaggio del tempo. L'ora da "Start di S1" a "End of S1" è l'intera durata di S1, che può essere di pochi secondi o di molte ore, a seconda dell'origine.

## <a name="example-2-playback-with-segment-skipping"></a>Esempio 2: riproduzione con segmento ignorato

In questo esempio, l'applicazione Accoda gli stessi segmenti, ma passa al segmento 3 mentre il segmento 1 sta eseguendo la riproduzione. In questo caso, vengono inviati gli eventi seguenti:

-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (preroll S2)
-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (inizio di S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   L'applicazione chiama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (passa a S3)
-   [MENewPresentation](menewpresentation.md) (preroll S3)
-   L'applicazione chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 annullata)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminato** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ sink \_ spostato** (transizione a S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 annullata)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminato** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ sink \_ spostato** (transizione a S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **TOPOSTATUS \_ pronto** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (S3)

Quando l'applicazione chiama [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per passare al segmento 3, l'origine del sequencer Annulla il segmento 1, che rimane in riproduzione. L'evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) per questo segmento contiene l'attributo della [**\_ \_ topologia di origine eventi \_ \_ MF**](mf-event-source-topology-canceled-attribute.md) , che indica che il segmento è stato interrotto perché è stato annullato. Quindi, poiché il segmento 2 è già sottoposta a rollback, il segmento viene avviato ma viene immediatamente annullato. L'evento MEEndOfPresentationSegment per il segmento 2 contiene anche l'attributo per la **\_ \_ topologia dell'origine eventi MF \_ \_ annullata** . La sessione può quindi passare al segmento 3 e riprodurla normalmente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'origine del sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 




