---
description: In questo argomento viene descritto come utilizzare l'origine sequenza per riprodurre una sequenza di file.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Come creare una playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527690"
---
# <a name="how-to-create-a-playlist"></a>Come creare una playlist

In questo argomento viene descritto come utilizzare l'origine sequenza per riprodurre una sequenza di file.

## <a name="overview"></a>Panoramica

Per riprodurre file multimediali in una sequenza, l'applicazione deve aggiungere topologie in una sequenza per creare una playlist e accodare tali topologie nella sessione multimediale per la riproduzione.

L'origine di Sequencer garantisce una riproduzione uniforme inizializzando e caricando la topologia successiva prima che la sessione multimediale inizi a riprodurre la topologia corrente. Ciò consente all'applicazione di avviare rapidamente la topologia successiva ogni volta che è necessario.

La sessione multimediale è responsabile dell'inserimento dei dati nei sink e della riproduzione delle topologie nell'origine della sequenza. Inoltre, la sessione multimediale gestisce l'ora di presentazione per i segmenti.

Per ulteriori informazioni sul modo in cui l'origine di Sequencer gestisce le topologie, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).

Questa procedura dettagliata include i passaggi seguenti:

1.  [Prerequisiti](#prerequisites)
2.  [Inizializzazione di Media Foundation](#initializing-media-foundation)
3.  [Creazione di oggetti Media Foundation](#creating-media-foundation-objects)
4.  [Creazione dell'origine supporto](#creating-the-media-source)
5.  [Creazione di topologie parziali](#creating-partial-topologies)
6.  [Aggiunta di topologie all'origine del sequencer](#adding-topologies-to-the-sequencer-source)
7.  [Impostazione della prima topologia nella sessione multimediale](#setting-the-first-topology-on-the-media-session)
8.  [Accodamento della topologia successiva nella sessione multimediale](#queuing-the-next-topology-on-the-media-session)
9.  [Rilascio dell'origine del sequencer](#releasing-the-sequencer-source)

Gli esempi di codice illustrati in questo argomento sono estratti dall'argomento [codice di esempio dell'origine sequencer](sequencer-source-example-code.md), che contiene il codice di esempio completo.

## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare questa procedura dettagliata, acquisire familiarità con i concetti Media Foundation seguenti:

-   [Sessione multimediale](media-session.md)
-   [Topologie](topologies.md)
-   [Generatori di eventi multimediali](media-event-generators.md)
-   [Descrittori di presentazione](presentation-descriptors.md)

Vedere anche [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md), perché il codice di esempio shwon qui si espande sul codice in questo argomento.

## <a name="initializing-media-foundation"></a>Inizializzazione di Media Foundation

Prima di poter usare qualsiasi interfaccia o metodo di Media Foundation, inizializzare Media Foundation chiamando la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Creazione di oggetti Media Foundation

Successivamente, creare gli oggetti Media Foundation seguenti:

-   Sessione multimediale. Questo oggetto espone l'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , che fornisce i metodi per riprodurre, sospendere e arrestare la topologia corrente.
-   Origine Sequencer. Questo oggetto espone l'interfaccia [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , che fornisce metodi per l'aggiunta, l'aggiornamento e l'eliminazione di topologie in una sequenza.

1.  Chiamare la funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.
2.  Chiamare [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) per richiedere il primo evento dalla sessione multimediale.
3.  Chiamare la funzione [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) per creare l'origine del sequencer.

Il codice seguente crea la sessione multimediale e richiede il primo evento:


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>Creazione dell'origine supporto

Successivamente, creare un'origine multimediale per il primo segmento della playlist. Usare il [resolver di origine](source-resolver.md) per creare un'origine multimediale da un URL. A tale scopo, chiamare la funzione [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) per creare un resolver di origine e quindi chiamare il metodo [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) per creare l'origine multimediale.

Per informazioni sulle origini multimediali, vedere [origini multimediali](media-sources.md).

## <a name="creating-partial-topologies"></a>Creazione di topologie parziali

Ogni segmento nell'origine del sequencer ha una propria topologia parziale. Successivamente, creare topologie parziali per le origini multimediali. Per una topologia parziale, i nodi di origine della topologia sono connessi direttamente ai nodi di output, senza specificare alcuna trasformazione intermedia. La sessione multimediale usa l'oggetto caricatore della topologia per risolvere la topologia. Dopo la risoluzione di una topologia, vengono aggiunti i decodificatori e altri nodi di trasformazione richiesti. L'origine del sequencer può inoltre contenere topologie complete.

Per creare l'oggetto topologia, usare la funzione [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) e quindi usare l'interfaccia [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) per creare nodi di flusso.

Per istruzioni dettagliate sull'utilizzo di questi elementi di programmazione per la creazione di topologie, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).

Un'applicazione può riprodurre una parte selezionata dell'origine nativa configurando il nodo di origine. A tale scopo, impostare l'attributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) e l'attributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) nei nodi della topologia del **\_ \_ \_ nodo della topologia MF SOURCESTREAM** . Specificare l'ora di inizio del supporto e l'ora di fine del supporto relativa all'inizio dell'origine nativa come tipi **UInt64** .

## <a name="adding-topologies-to-the-sequencer-source"></a>Aggiunta di topologie all'origine del sequencer

Successivamente, aggiungere all'origine sequencer le topologie parziali create. A ogni elemento Sequence, denominato *segmento*, viene assegnato un identificatore **MFSequencerElementId** . Per ulteriori informazioni sul modo in cui l'origine di Sequencer gestisce le topologie, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).

Dopo che tutte le topologie sono state aggiunte all'origine sequencer, l'applicazione deve contrassegnare l'ultimo segmento nella sequenza per terminare la riproduzione nella pipeline. Senza questo flag, l'origine del sequencer prevede l'aggiunta di più topologie.

1.  Chiamare il metodo [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) per aggiungere una topologia specifica all'origine del sequencer.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) aggiunge la topologia specificata alla sequenza. Questo metodo restituisce l'identificatore del segmento nel parametro *pdwId* .

    Se la topologia è l'ultima nell'origine del sequencer, passare SequencerTopologyFlags \_ Last nel parametro *dwFlags* . Questo valore è definito nell'enumerazione [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .

2.  Chiamare [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) per aggiornare i flag per la topologia associata all'identificatore di segmento nell'elenco di input. In questo caso, la chiamata indica che il segmento specificato è l'ultimo segmento del sequencer. Questa chiamata è facoltativa se l'ultima topologia è specificata nella chiamata [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

L'applicazione può sostituire la topologia di un segmento con un'altra topologia chiamando [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) e passando la nuova topologia in *pTopology*. Se sono presenti nuove origini native nella nuova topologia, le origini vengono aggiunte alla cache di origine. Viene aggiornato anche l'elenco di preroll.

## <a name="setting-the-first-topology-on-the-media-session"></a>Impostazione della prima topologia nella sessione multimediale

Accodare quindi la prima topologia nell'origine della sequenza nella sessione multimediale. Per ottenere la prima topologia dall'origine del sequencer, l'applicazione deve chiamare il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Questo metodo restituisce la topologia parziale, che viene risolta dalla sessione multimediale.

Per informazioni sulle topologie parziali, vedere [informazioni sulle topologie](about-topologies.md).

1.  Recuperare l'origine multimediale nativa per la prima topologia dell'origine della sequenza.
2.  Creare un descrittore di presentazione per l'origine multimediale chiamando il metodo [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .
3.  Recuperare la topologia associata per la presentazione chiamando il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
4.  Impostare la prima topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Chiamare la [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il parametro *DwSetTopologyFlags* impostato su **null**. Indica alla sessione multimediale di avviare la topologia specificata quando la topologia corrente è stata completata. Poiché in questo caso, la topologia specificata è la prima topologia e non è presente alcuna presentazione corrente, la sessione multimediale avvia immediatamente la nuova presentazione.

    Il valore **null** indica anche che la sessione multimediale deve risolvere la topologia perché la topologia restituita dal provider di topologia è sempre una topologia parziale.


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a>Accodamento della topologia successiva nella sessione multimediale

Successivamente, l'applicazione deve gestire l'evento [MENewPresentation](menewpresentation.md) .

L'origine di sequencer genera [MENewPresentation](menewpresentation.md) quando la sessione multimediale inizia a riprodurre un segmento con un altro segmento che lo segue. Questo evento informa l'applicazione della successiva topologia nell'origine della sequenza fornendo il descrittore di presentazione per il segmento successivo nell'elenco di preroll. L'applicazione deve recuperare la topologia associata, usando il provider di topologia e accodarla nella sessione multimediale. L'origine di Sequencer esegue quindi la preregistrazione di questa topologia, che garantisce una transizione senza problemi tra le presentazioni.

Quando l'applicazione esegue la ricerca in più segmenti, l'applicazione riceve diversi eventi [MENewPresentation](menewpresentation.md) poiché l'origine del sequencer aggiorna l'elenco di preroll e imposta la topologia corretta. L'applicazione deve gestire ogni evento e accodare la topologia restituita nei dati dell'evento, nella sessione multimediale. Per informazioni sull'omissione dei segmenti, vedere [uso dell'origine di Sequencer](using-the-sequencer-source.md).

Per informazioni su come ottenere le notifiche di origine di Sequencer, vedere [eventi di origine di Sequencer](sequencer-source-events.md).

1.  Nel gestore dell'evento [MENewPresentation](menewpresentation.md) recuperare il descrittore di presentazione per il segmento successivo dai dati dell'evento.
2.  Ottenere la topologia associata per la presentazione chiamando il metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
3.  Impostare la topologia nella sessione multimediale chiamando il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue.

    La sessione multimediale avvia la nuova presentazione quando la presentazione corrente è stata completata.


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>Rilascio dell'origine del sequencer

Arrestare infine l'origine del sequencer. A tale scopo, chiamare il metodo [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine del sequencer. Questa chiamata arresta tutte le origini multimediali native sottostanti nell'origine del sequencer.

Dopo il rilascio dell'origine del sequencer, l'applicazione deve chiudere e arrestare la sessione multimediale chiamando [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) e [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in questo ordine.

Per evitare perdite di memoria, l'applicazione deve rilasciare i puntatori alle interfacce Media Foundation quando non sono più necessari.

## <a name="next-steps"></a>Passaggi successivi

Questa procedura dettagliata illustra come creare una playlist di base usando l'origine del sequencer. Dopo aver creato la playlist, potrebbe essere necessario aggiungere funzionalità avanzate, ad esempio l'omissione del segmento, la modifica dello stato di riproduzione e la ricerca all'interno di un segmento. L'elenco seguente contiene i collegamenti agli argomenti correlati:

-   [Come controllare gli Stati di presentazione](how-to-control-presentation-states.md): l'origine di Sequencer si basa sulla sessione multimediale per fornire il controllo del trasporto, ad esempio riproduzione, pausa e arresto.
-   [Come eseguire lo scrubbing,](how-to-perform-scrubbing.md) descrive i passaggi necessari per cercare una posizione specifica in un flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



