---
description: Questo argomento descrive come usare l'origine Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Uso dell'origine Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b0607d65d02e507f576a5177ea432f3f7e0fab57c3b575fbb34240a46e91be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972730"
---
# <a name="using-the-sequencer-source"></a>Uso dell'origine Sequencer

In questo argomento viene descritto come utilizzare [l'origine Sequencer](sequencer-source.md). Contiene le sezioni seguenti:

-   [Overview](#overview)
-   [Aggiunta di topologie](#adding-topologies)
-   [Eliminazione di topologie](#deleting-topologies)
-   [Ignorare un segmento](#skipping-to-a-segment)
-   [Argomenti correlati](#related-topics)

Per una panoramica generale dell'origine sequencer, vedere [Informazioni sull'origine Sequencer.](about-the-sequencer-source.md)

## <a name="overview"></a>Panoramica

L'origine sequencer espone le interfacce seguenti.



| Interfaccia                                                                        | Descrizione                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Espone la funzionalità generica dell'origine multimediale.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Consente all'applicazione di aggiungere o rimuovere topologie.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera la topologia successiva da accodare nella sessione multimediale.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Usato dalla sessione multimediale per terminare i segmenti. Le applicazioni non usano questa interfaccia. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Esegue una query sull'origine sequencer per [le interfacce del servizio](service-interfaces.md).     |



 

Per riprodurre una sequenza di origini multimediali, seguire questa procedura:

1.  Per creare l'origine sequencer, chiamare [**la funzione MFCreateSequencerSource.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource)
2.  Per ogni segmento, creare una topologia di riproduzione, come descritto in [Creazione di topologie di riproduzione.](creating-playback-topologies.md) Per aggiungere la topologia alla presentazione, chiamare [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Prima di avviare la riproduzione, chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine sequencer. Questo metodo restituisce un puntatore a un descrittore di presentazione per il primo segmento. Per ottenere la topologia associata a questo segmento, chiamare **QueryInterface** sull'origine sequencer per [**l'interfaccia IMFMediaSourceTopologyProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) Passare il descrittore di presentazione al [**metodo IMFMediaSourceTopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Questo metodo restituisce un puntatore alla topologia.
4.  Passare la topologia per il primo segmento alla sessione multimediale chiamando il metodo [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) della sessione multimediale.
5.  Avviare la riproduzione chiamando [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Quando l'origine sequencer è pronta per eseguire la pre-registrazione del segmento successivo, invia un evento [MENewPresentation](menewpresentation.md) i cui dati dell'evento sono un puntatore a interfaccia [**IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) Anche in questo caso, ottenere la topologia per il segmento chiamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) nell'origine sequencer e impostare la topologia nella sessione multimediale chiamando [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Non è necessario avviare nuovamente l'origine multimediale. verrà riprodotto automaticamente fino al segmento successivo.
7.  Prima della chiusura dell'applicazione, arrestare l'origine sequencer chiamando [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

Il codice seguente illustra come ottenere la topologia e impostarla nella sessione multimediale:


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



Per un esempio di codice completo, vedere [Codice di esempio del codice sorgente di Sequencer.](sequencer-source-example-code.md)

## <a name="adding-topologies"></a>Aggiunta di topologie

L'origine sequencer gestisce due elenchi di topologie: *l'elenco di input* e l'elenco di *preroll*.

L'elenco di input è una raccolta di topologie corrispondenti ai segmenti di playlist, nell'ordine in cui sono stati aggiunti dall'applicazione chiamando [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Questo metodo assegna a ogni topologia un identificatore *di segmento univoco* di **tipo MFSequencerElementId**. L'identificatore di segmento viene impostato come attributo per tutti i nodi della topologia di origine. Un'applicazione può ottenere l'identificatore di segmento da un nodo di origine usando [l'attributo MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID.](mf-toponode-sequence-elementid-attribute.md) L'elenco di input può avere topologie duplicate se l'applicazione denominata **AppendTopology** nella stessa topologia più volte; tuttavia, sono identificati dai relativi identificatori di segmento univoci.

L'elenco di preroll è una raccolta di topologie di elenco di input inizializzate in preparazione per la riproduzione. In questo modo la sessione multimediale può passare facilmente alla topologia successiva al termine della topologia attiva. L'applicazione non può aggiungere o rimuovere direttamente topologie dall'elenco di preroll. viene generato dall'origine sequencer quando viene selezionata una topologia dall'elenco di input per la riproduzione. In questo modo l'origine sequencer aggiunge la topologia successiva dall'elenco di input all'elenco di preroll. Dopo questa operazione, l'origine sequencer genera in modo asincrono l'evento [MENewPresentation](menewpresentation.md) e passa il descrittore di presentazione per la topologia di preroll come dati dell'evento. L'applicazione deve restare in ascolto di questo evento usando l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale e accodare la topologia di preroll nella sessione multimediale chiamando [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Questa operazione deve essere eseguita prima che la sessione multimediale completi la riproduzione della topologia attiva. **SetTopology** comunica alla sessione multimediale la topologia successiva che deve essere riprodotta al termine della riproduzione della topologia attiva. Per garantire una continuità, l'applicazione deve chiamare **SetTopology** prima che la sessione multimediale completi la riproduzione della topologia precedente. In caso contrario, si presenterà un divario tra i segmenti.

[L'evento MENewPresentation](menewpresentation.md) viene generato finché è presente una topologia che segue la topologia attiva. Di conseguenza, se l'elenco di input contiene una sola topologia o se la topologia attiva è l'ultima nell'elenco di input, questo evento non viene generato.

L'elenco di preroll viene sincronizzato con l'elenco di input e aggiornato ogni volta che una topologia viene aggiunta o eliminata dall'elenco di input.

## <a name="deleting-topologies"></a>Eliminazione di topologie

Per rimuovere una topologia dall'origine sequencer, un'applicazione deve chiamare il metodo [**IMFSequencerSource::D eleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e specificare l'identificatore del segmento.

Prima di [**chiamare DeleteTopology,**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)l'applicazione deve assicurarsi che La sessione multimediale non utilizzi la topologia che l'applicazione vuole eliminare. A tale scopo, è necessario eseguire entrambe le operazioni seguenti prima che l'applicazione **chiami DeleteTopology:**

-   [L'evento MESessionTopologyStatus](mesessiontopologystatus.md) con MF TOPOSTATUS ENDED viene ricevuto per la topologia per garantire che la sessione multimediale \_ abbia completato la \_ riproduzione.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) con MF TOPOSTATUS STARTED SOURCE viene ricevuto per la topologia successiva per garantire che la sessione multimediale abbia avviato la riproduzione della topologia successiva. Viene ricevuto l'evento \_ \_ \_ [MESessionEnded](mesessionended.md) per assicurarsi che la sessione multimediale sia stata eseguita con l'ultima topologia nell'origine Sequencer.

Se il segmento da eliminare è la topologia attiva, la riproduzione viene arrestata e l'origine sequencer genera [l'evento MEEndOfPresentationSegment.](meendofpresentationsegment.md) Se anche la topologia attiva è l'ultima topologia, viene generato [l'evento MEEndOfPresentation.](meendofpresentation.md)

## <a name="skipping-to-a-segment"></a>Ignorare un segmento

Un'applicazione può passare a un segmento specifico nella sequenza avviando [la sessione multimediale](media-session.md) con un offset di segmento, come indicato di seguito:

1.  Chiamare la [**funzione MFCreateSequencerSegmentOffset per**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) creare l'offset del segmento. Specificare l'identificatore del segmento nel *parametro dwId.* L'identificatore è stato restituito dal [**metodo IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando è stata aggiunta per la prima volta la topologia all'origine sequencer. Il *parametro hnsOffset* specifica una scostamento dell'ora rispetto all'inizio del segmento. La riproduzione verrà avviata in questa fase. Per il *parametro pvarSegmentOffset,* passare l'indirizzo di un **oggetto PROPVARIANT vuoto.** Quando la funzione viene restituita, **questa proprietà PROPVARIANT** contiene l'offset del segmento.

2.  Chiamare il [**metodo IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) nella sessione multimediale. Per il *parametro pguidTimeFormat* usare il valore GUID MF \_ TIME FORMAT SEGMENT \_ \_ \_ OFFSET. Questo valore indica la ricerca in base all'offset del segmento. Per il *parametro pvarStartPosition,* passare l'indirizzo dell'oggetto **PROPVARIANT** creato nel passaggio precedente.

Nell'esempio di codice seguente viene illustrato come passare all'inizio di un segmento specificato in una sequenza.


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Quando l'applicazione esegue la ricerca tra segmenti, riceve diversi eventi quando l'origine sequencer termina il segmento corrente e si prepara a riprodurre il nuovo segmento. Poiché questi eventi vengono ricevuti in modo asincrono, è difficile prevedere la sequenza esatta di eventi. Questi eventi sono i seguenti:

-   L'origine sequencer invia [un evento MENewPresentation](menewpresentation.md) per il nuovo segmento a cui la sessione multimediale viene ignorata.

-   Quando l'origine sequencer termina il segmento attivo, invia [l'evento MEEndOfPresentationSegment.](meendofpresentationsegment.md)
-   L'origine sequencer annulla quindi la topologia di preroll. Di seguito sono riportati gli eventi per la topologia annullata:

    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ READY.
    -   [Evento MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ STARTED \_ SOURCE.
    -   [Evento MEEndOfPresentationSegment](meendofpresentationsegment.md) con l'attributo [MF \_ EVENT SOURCE \_ \_ TOPOLOGY \_ CANCELED](mf-event-source-topology-canceled-attribute.md) per indicare che la topologia è stata annullata dall'origine sequencer.

-   Successivamente, l'origine sequencer invia gli eventi per il nuovo segmento, inclusi vari [eventi MESessionTopologyStatus.](mesessiontopologystatus.md)
-   Se il nuovo segmento non è l'ultimo nell'elenco, l'origine sequencer aggiorna l'elenco di preroll e genera un'altra [meNewPresentation](menewpresentation.md) per la nuova topologia di preroll. Per informazioni sulle topologie nell'elenco di preroll, vedere [About the Sequencer Source](about-the-sequencer-source.md).

Altre informazioni sugli eventi inviati dall'origine Sequencer sono disponibili nell'argomento [Eventi di origine sequencer](sequencer-source-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



