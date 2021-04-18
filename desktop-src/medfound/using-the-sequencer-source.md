---
description: In questo argomento viene descritto come utilizzare l'origine di Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Utilizzo dell'origine sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308984"
---
# <a name="using-the-sequencer-source"></a>Utilizzo dell'origine sequencer

In questo argomento viene descritto come utilizzare l' [origine di Sequencer](sequencer-source.md). Contiene le sezioni seguenti:

-   [Overview](#overview)
-   [Aggiunta di topologie](#adding-topologies)
-   [Eliminazione di topologie](#deleting-topologies)
-   [Ignorare un segmento](#skipping-to-a-segment)
-   [Argomenti correlati](#related-topics)

Per una panoramica generale dell'origine di Sequencer, vedere [informazioni sull'origine di Sequencer](about-the-sequencer-source.md).

## <a name="overview"></a>Panoramica

L'origine di Sequencer espone le interfacce seguenti.



| Interfaccia                                                                        | Descrizione                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Espone la funzionalità generica di origine dei supporti.                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Consente all'applicazione di aggiungere o rimuovere topologie.                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Recupera la topologia successiva da accodare nella sessione multimediale.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Usato dalla sessione multimediale per terminare i segmenti. Le applicazioni non utilizzano questa interfaccia. |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Esegue una query sull'origine del sequencer per le [interfacce del servizio](service-interfaces.md).     |



 

Per riprodurre una sequenza di origini multimediali, seguire questa procedura:

1.  Per creare l'origine del sequencer, chiamare la funzione [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .
2.  Per ogni segmento, creare una topologia di riproduzione, come descritto in [creazione di topologie di riproduzione](creating-playback-topologies.md). Per aggiungere la topologia alla presentazione, chiamare [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Prima di avviare la riproduzione, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del sequencer. Questo metodo restituisce un puntatore a un descrittore di presentazione per il primo segmento. Per ottenere la topologia associata a questo segmento, chiamare **QueryInterface** sull'origine del sequencer per l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) . Passare il descrittore della presentazione al metodo [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Questo metodo restituisce un puntatore alla topologia.
4.  Passare la topologia per il primo segmento alla sessione multimediale chiamando il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue della sessione multimediale.
5.  Avviare la riproduzione chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).
6.  Quando l'origine del sequencer è pronta per la prerolling del segmento successivo, invia un evento [MENewPresentation](menewpresentation.md) i cui dati dell'evento sono un puntatore di interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) . Anche in questo caso, ottenere la topologia per il segmento chiamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) nell'origine del sequencer e impostare la topologia nella sessione multimediale chiamando [**la topologia.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) Non è necessario riavviare l'origine multimediale; verrà automaticamente riprodotto fino al segmento successivo.
7.  Prima di chiudere l'applicazione, arrestare l'origine del sequencer chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).

Nel codice seguente viene illustrato come ottenere la topologia e impostarla nella sessione multimediale:


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



Per un esempio di codice completo, vedere [codice di esempio dell'origine sequencer](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Aggiunta di topologie

L'origine di Sequencer gestisce due elenchi di topologie: l' *elenco di input* e l'elenco di *preroll*.

L'elenco di input è una raccolta di topologie corrispondenti ai segmenti della playlist, nell'ordine in cui sono stati aggiunti dall'applicazione chiamando [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology). Questo metodo assegna a ogni topologia un *identificatore di segmento* univoco del tipo **MFSequencerElementId**. L'identificatore di segmento viene impostato come attributo per tutti i nodi della topologia di origine. Un'applicazione può ottenere l'identificatore di segmento da un nodo di origine usando l'attributo [ \_ ElementID della \_ sequenza \_ MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) . L'elenco di input può includere topologie duplicate se l'applicazione ha chiamato **AppendTopology** nella stessa topologia più di una volta. Tuttavia, vengono identificati da identificatori di segmenti univoci.

L'elenco preroll è una raccolta di topologie di elenco di input inizializzate in preparazione per la riproduzione. In questo modo, la sessione multimediale passa alla topologia successiva facilmente al termine della topologia attiva. L'applicazione non è in grado di aggiungere o rimuovere direttamente le topologie dall'elenco preroll; viene generato dall'origine del sequencer quando viene selezionata una topologia dall'elenco di input per la riproduzione. In questo modo, l'origine del sequencer aggiungerà la topologia successiva dall'elenco di input all'elenco preroll. Dopo questa operazione, l'origine sequencer genera in modo asincrono l'evento [MENewPresentation](menewpresentation.md) e passa il descrittore di presentazione per la topologia di preroll come dati dell'evento. L'applicazione deve restare in ascolto di questo evento usando l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale e accodare la topologia di preroll nella sessione multimediale chiamando [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Questa operazione deve essere eseguita prima che la sessione multimediale completi la riproduzione della topologia attiva. La **topologia** informa la sessione multimediale sulla successiva topologia che deve essere riprodotta al termine della riproduzione della topologia attiva. Per garantire un treansition trasparente, l'applicazione deve chiamare la **topologia** prima che la sessione multimediale venga completata con la topologia precedente. In caso contrario, si verifica un divario tra i segmenti.

L'evento [MENewPresentation](menewpresentation.md) viene generato purché esista una topologia successiva alla topologia attiva. Di conseguenza, se l'elenco di input contiene una sola topologia o se la topologia attiva è l'ultima nell'elenco di input, questo evento non viene generato.

L'elenco preroll viene sincronizzato con l'elenco di input e viene aggiornato ogni volta che viene aggiunta o eliminata una topologia dall'elenco di input.

## <a name="deleting-topologies"></a>Eliminazione di topologie

Per rimuovere una topologia dall'origine del sequencer, un'applicazione deve chiamare il metodo [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e specificare l'identificatore del segmento.

Prima di chiamare [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), l'applicazione deve assicurarsi che la sessione multimediale non usi la topologia che l'applicazione vuole eliminare. A tale scopo, prima che l'applicazione chiami **DeleteTopology**, è necessario che si verifichino entrambe le condizioni seguenti:

-   [](mesessiontopologystatus.md) \_ \_ Per la topologia per garantire che la sessione multimediale abbia completato la riproduzione, viene ricevuto l'evento MESessionTopologyStatus con MF TOPOSTATUS terminato.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) con MF \_ TOPOSTATUS \_ Started \_ source viene ricevuto per la topologia successiva per assicurarsi che la sessione multimediale abbia iniziato a riprodurre la topologia successiva, viene ricevuto l'evento [MESessionEnded](mesessionended.md) per assicurarsi che la sessione multimediale venga eseguita con l'ultima topologia nell'origine del sequencer.

Se il segmento da eliminare è la topologia attiva, la riproduzione viene arrestata e l'origine del sequencer genera l'evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) . Se la topologia attiva è anche l'ultima topologia, viene generato l'evento [MEEndOfPresentation](meendofpresentation.md) .

## <a name="skipping-to-a-segment"></a>Ignorare un segmento

Un'applicazione può passare a un segmento specifico nella sequenza avviando la [sessione multimediale](media-session.md) con un offset del segmento, come indicato di seguito:

1.  Chiamare la funzione [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) per creare l'offset del segmento. Specificare l'identificatore del segmento nel parametro *dwID* . (L'identificatore è stato restituito dal metodo [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando la topologia è stata aggiunta per la prima volta all'origine del sequencer). Il parametro *hnsOffset* specifica un offset temporale, relativo all'inizio del segmento. La riproduzione verrà avviata in questo momento. Per il parametro *pvarSegmentOffset* , passare l'indirizzo di un **PROPVARIANT** vuoto. Quando la funzione restituisce, questo **PROPVARIANT** contiene l'offset del segmento.

2.  Chiamare il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) nella sessione multimediale. Per il parametro *pguidTimeFormat* , usare l'offset del segmento di formato dell'ora MF valore GUID \_ \_ \_ \_ . Questo valore indica la ricerca in base all'offset del segmento. Per il parametro *pvarStartPosition* , passare l'indirizzo del **PROPVARIANT** creato nel passaggio precedente.

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



Quando l'applicazione esegue la ricerca tra segmenti, l'applicazione riceve diversi eventi quando l'origine del sequencer termina il segmento corrente e prepara la riproduzione del nuovo segmento. Poiché questi eventi vengono ricevuti in modo asincrono, è difficile prevedere la sequenza esatta di eventi. Questi eventi sono i seguenti:

-   L'origine di Sequencer Invia un evento [MENewPresentation](menewpresentation.md) per il nuovo segmento a cui è stata ignorata la sessione multimediale.

-   Quando l'origine del sequencer termina il segmento attivo, invia l'evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .
-   L'origine del sequencer Annulla quindi la topologia di preroll. Ciò comporta gli eventi seguenti per la topologia annullata:

    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ Ready.
    -   Evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il flag di origine con MF \_ TOPOSTATUS \_ avviato \_ .
    -   Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) con l'attributo della [ \_ \_ topologia di origine eventi \_ \_ MF](mf-event-source-topology-canceled-attribute.md) per indicare che la topologia è stata annullata dall'origine del sequencer.

-   L'origine di Sequencer invia quindi gli eventi per il nuovo segmento, inclusi i vari eventi [MESessionTopologyStatus](mesessiontopologystatus.md) .
-   Se il nuovo segmento non è l'ultimo nell'elenco, l'origine del sequencer aggiorna l'elenco di preroll e genera un altro [MENewPresentation](menewpresentation.md) per la nuova topologia di preroll. Per informazioni sulle topologie nell'elenco preroll, vedere [informazioni sull'origine del sequencer](about-the-sequencer-source.md).

Per ulteriori informazioni sugli eventi inviati dall'origine sequencer, vedere l'argomento relativo [agli eventi di origine di Sequencer](sequencer-source-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



