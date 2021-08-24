---
description: Questo argomento descrive come usare l'origine sequenza per riprodurre una sequenza di file.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Come creare una playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d2a36735d29510e0622882a399fff199fd2289261453a51f281414b5076826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828171"
---
# <a name="how-to-create-a-playlist"></a>Come creare una playlist

Questo argomento descrive come usare l'origine sequenza per riprodurre una sequenza di file.

## <a name="overview"></a>Panoramica

Per riprodurre file multimediali in una sequenza, l'applicazione deve aggiungere topologie in una sequenza per creare una playlist e accodare tali topologie nella sessione multimediale per la riproduzione.

L'origine sequencer garantisce una riproduzione facile inizializzando e caricando la topologia successiva prima che la sessione multimediale inizi a riprodurre la topologia corrente. In questo modo l'applicazione può avviare rapidamente la topologia successiva ogni volta che è necessaria.

La sessione multimediale è responsabile dell'alimentazione dei dati ai sink e della riproduzione delle topologie nell'origine della sequenza. Inoltre, la sessione multimediale gestisce l'ora di presentazione per i segmenti.

Per altre informazioni sul modo in cui l'origine sequencer gestisce le topologie, vedere [Informazioni sull'origine sequencer.](about-the-sequencer-source.md)

Questa procedura dettagliata contiene i passaggi seguenti:

1.  [Prerequisiti](#prerequisites)
2.  [Inizializzazione Media Foundation](#initializing-media-foundation)
3.  [Creazione Media Foundation oggetti](#creating-media-foundation-objects)
4.  [Creazione dell'origine multimediale](#creating-the-media-source)
5.  [Creazione di topologie parziali](#creating-partial-topologies)
6.  [Aggiunta di topologie all'origine sequencer](#adding-topologies-to-the-sequencer-source)
7.  [Impostazione della prima topologia nella sessione multimediale](#setting-the-first-topology-on-the-media-session)
8.  [Accodamento della topologia successiva nella sessione multimediale](#queuing-the-next-topology-on-the-media-session)
9.  [Rilascio dell'origine sequencer](#releasing-the-sequencer-source)

Gli esempi di codice illustrati in questo argomento sono estratti dall'argomento Codice di esempio del codice sorgente di [Sequencer](sequencer-source-example-code.md), che contiene il codice di esempio completo.

## <a name="prerequisites"></a>Prerequisiti

Prima di iniziare questa procedura dettagliata, acquisire familiarità con i Media Foundation seguenti:

-   [Sessione multimediale](media-session.md)
-   [Topologie](topologies.md)
-   [Generatori di eventi multimediali](media-event-generators.md)
-   [Descrittori di presentazione](presentation-descriptors.md)

Vedere anche [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), perché il codice di esempio shwon qui si espande sul codice in tale argomento.

## <a name="initializing-media-foundation"></a>Inizializzazione Media Foundation

Prima di poter usare qualsiasi Media Foundation o metodi, inizializzare Media Foundation chiamando la [**funzione MFStartup.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Per altre informazioni, vedere [Inizializzazione Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Creazione Media Foundation oggetti

Creare quindi gli oggetti Media Foundation seguenti:

-   Sessione multimediale. Questo oggetto espone [**l'interfaccia IMFMediaSession,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) che fornisce metodi per riprodurre, sospendere e arrestare la topologia corrente.
-   Origine sequencer. Questo oggetto espone [**l'interfaccia IMFSequencerSource,**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) che fornisce metodi per aggiungere, aggiornare ed eliminare topologie in una sequenza.

1.  Chiamare la [**funzione MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.
2.  Chiamare [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) per richiedere il primo evento dalla sessione multimediale.
3.  Chiamare la [**funzione MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) per creare l'origine sequencer.

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



## <a name="creating-the-media-source"></a>Creazione dell'origine multimediale

Creare quindi un'origine multimediale per il primo segmento di playlist. Usare il [sistema di risoluzione dell'origine](source-resolver.md) per creare un'origine multimediale da un URL. A tale scopo, chiamare la funzione [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) per creare un sistema di risoluzione di origine e quindi chiamare il metodo [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) per creare l'origine multimediale.

Per informazioni sulle origini multimediali, vedere [Origini multimediali](media-sources.md).

## <a name="creating-partial-topologies"></a>Creazione di topologie parziali

Ogni segmento nell'origine sequencer ha una propria topologia parziale. Creare quindi topologie parziali per le origini multimediali. Per una topologia parziale, i nodi di origine della topologia sono connessi direttamente ai nodi di output, senza specificare trasformazioni intermedie. La sessione multimediale usa l'oggetto caricatore della topologia per risolvere la topologia. Dopo aver risolto una topologia, vengono aggiunti i decodificatori necessari e altri nodi di trasformazione. L'origine sequencer può contenere anche topologie complete.

Per creare l'oggetto topologia, usare la [**funzione MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) e quindi usare l'interfaccia [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) per creare nodi di flusso.

Per istruzioni complete sull'uso di questi elementi di programmazione per creare topologie, vedere [Creazione di topologie di riproduzione](creating-playback-topologies.md).

Un'applicazione può riprodurre una parte selezionata dell'origine nativa configurando il nodo di origine. A tale scopo, impostare l'attributo [**\_ MF TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) e l'attributo [**\_ MF TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) nei nodi della topologia **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE.** Specificare l'ora di inizio e l'ora di arresto del supporto rispetto all'inizio dell'origine nativa come **tipi UINT64.**

## <a name="adding-topologies-to-the-sequencer-source"></a>Aggiunta di topologie all'origine sequencer

Aggiungere quindi all'origine sequencer le topologie parziali create. A ogni elemento di sequenza, denominato *segmento*, viene assegnato un **identificatore MFSequencerElementId.** Per altre informazioni sul modo in cui l'origine sequencer gestisce le topologie, vedere [Informazioni sull'origine sequencer.](about-the-sequencer-source.md)

Dopo aver aggiunto tutte le topologie all'origine sequencer, l'applicazione deve contrassegnare l'ultimo segmento della sequenza per terminare la riproduzione nella pipeline. Senza questo flag, l'origine sequencer prevede l'aggiunta di più topologie.

1.  Chiamare il [**metodo IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) per aggiungere una topologia specifica all'origine sequencer.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) aggiunge la topologia specificata alla sequenza. Questo metodo restituisce l'identificatore di segmento nel *parametro pdwId.*

    Se la topologia è l'ultima nell'origine sequencer, passare SequencerTopologyFlags \_ Last nel *parametro dwFlags.* Questo valore è definito [**nell'enumerazione MFSequencerTopologyFlags.**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags)

2.  Chiamare [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) per aggiornare i flag per la topologia associata all'identificatore di segmento nell'elenco di input. In questo caso, la chiamata indica che il segmento specificato è l'ultimo segmento nel sequencer. Questa chiamata è facoltativa se nella chiamata [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) viene specificata l'ultima topologia.

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

    

L'applicazione può sostituire la topologia di un segmento con un'altra topologia chiamando [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) e passando la nuova topologia in *pTopology*. Se nella nuova topologia sono presenti nuove origini native, le origini vengono aggiunte alla cache di origine. Viene aggiornato anche l'elenco di pre-registrazione.

## <a name="setting-the-first-topology-on-the-media-session"></a>Impostazione della prima topologia nella sessione multimediale

Accodare quindi la prima topologia nell'origine della sequenza nella sessione multimediale. Per ottenere la prima topologia dall'origine sequencer, l'applicazione deve chiamare il metodo [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Questo metodo restituisce la topologia parziale, risolta dalla sessione multimediale.

Per informazioni sulle topologie parziali, vedere [Informazioni sulle topologie](about-topologies.md).

1.  Recuperare l'origine multimediale nativa per la prima topologia dell'origine della sequenza.
2.  Creare un descrittore di presentazione per l'origine multimediale chiamando il [**metodo IMFMediaSource::CreatePresentationDescriptor.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)
3.  Recuperare la topologia associata per la presentazione chiamando il [**metodo IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology)
4.  Impostare la prima topologia nella sessione multimediale chiamando [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Chiamare [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il *parametro dwSetTopologyFlags* impostato su **NULL.** Indica alla sessione multimediale di avviare la topologia specificata al termine della topologia corrente. Poiché in questo caso la topologia specificata è la prima topologia e non è presente alcuna presentazione corrente, la sessione multimediale avvia immediatamente la nuova presentazione.

    Il **valore NULL** indica anche che Media Session deve risolvere la topologia perché la topologia restituita dal provider di topologia è sempre una topologia parziale.


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

Successivamente, l'applicazione deve gestire [l'evento MENewPresentation.](menewpresentation.md)

L'origine sequencer genera [MENewPresentation](menewpresentation.md) quando la sessione multimediale avvia la riproduzione di un segmento con un altro segmento che lo segue. Questo evento informa l'applicazione sulla topologia successiva nell'origine della sequenza fornendo il descrittore di presentazione per il segmento successivo nell'elenco di preroll. L'applicazione deve recuperare la topologia associata, usando il provider di topologia, e accodarla nella sessione multimediale. L'origine sequencer esegue quindi la pre-registrazione di questa topologia, assicurando una transizione facile tra le presentazioni.

Quando l'applicazione cerca tra segmenti, l'applicazione riceve diversi eventi [MENewPresentation](menewpresentation.md) quando l'origine sequencer aggiorna l'elenco di preroll e configura la topologia corretta. L'applicazione deve gestire ogni evento e accodare la topologia restituita nei dati dell'evento nella sessione multimediale. Per informazioni sull'ignorare i segmenti, vedere [Uso dell'origine sequencer](using-the-sequencer-source.md).

Per informazioni sul recupero di notifiche di origine sequencer, vedere [Eventi di origine sequencer](sequencer-source-events.md).

1.  Nel gestore [dell'evento MENewPresentation](menewpresentation.md) recuperare il descrittore di presentazione per il segmento successivo dai dati dell'evento.
2.  Ottenere la topologia associata per la presentazione chiamando il [**metodo IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology)
3.  Impostare la topologia nella sessione multimediale chiamando il [**metodo IMFMediaSession::SetTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)

    La sessione multimediale avvia la nuova presentazione al termine della presentazione corrente.


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



## <a name="releasing-the-sequencer-source"></a>Rilascio dell'origine sequencer

Infine, arrestare l'origine sequencer. A tale scopo, chiamare il [**metodo IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine sequencer. Questa chiamata arresta tutte le origini multimediali native sottostanti nell'origine sequencer.

Dopo il rilascio dell'origine sequencer, l'applicazione deve chiudere e arrestare la sessione multimediale chiamando [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) e [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)in tale ordine.

Per evitare perdite di memoria, l'applicazione deve rilasciare puntatori Media Foundation interfacce quando non sono più necessarie.

## <a name="next-steps"></a>Passaggi successivi

Questa procedura dettagliata illustra come creare una playlist di base usando l'origine sequencer. Dopo aver creato la playlist, è possibile aggiungere funzionalità avanzate, ad esempio l'ignoramento del segmento, la modifica dello stato di riproduzione e la ricerca all'interno di un segmento. L'elenco seguente include collegamenti agli argomenti correlati:

-   [Come controllare gli stati di presentazione:](how-to-control-presentation-states.md)l'origine sequencer si basa sulla sessione multimediale per fornire il controllo del trasporto, ad esempio Play, Pause e Stop.
-   [Come eseguire lo scrubbing](how-to-perform-scrubbing.md) descrive i passaggi necessari per cercare una posizione specifica in un flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



