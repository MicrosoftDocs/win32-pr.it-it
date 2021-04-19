---
description: In questo argomento viene descritto come creare una topologia per la riproduzione audio o video.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Creazione di topologie di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305464"
---
# <a name="creating-playback-topologies"></a>Creazione di topologie di riproduzione

In questo argomento viene descritto come creare una topologia per la riproduzione audio o video. Per la riproduzione di base, è possibile creare una topologia parziale, in cui i nodi di origine sono connessi direttamente ai nodi di output. Non è necessario inserire nodi per le trasformazioni intermedie, ad esempio decodificatori o convertitori di colori. La sessione multimediale utilizzerà il caricatore della topologia per risolvere la topologia e il caricatore della topologia inserirà le trasformazioni necessarie.

-   [Creazione della topologia](#creating-the-topology)
-   [Connessione di flussi a sink multimediali](#connecting-streams-to-media-sinks)
-   [Creazione del sink multimediale](#creating-the-media-sink)
-   [Passaggi successivi](#next-steps)
-   [Argomenti correlati](#related-topics)

## <a name="creating-the-topology"></a>Creazione della topologia

Ecco i passaggi generali per la creazione di una topologia di riproduzione parziale da un'origine multimediale:

1.  Creare l'origine multimediale. Nella maggior parte dei casi, si userà il resolver di origine per creare l'origine multimediale. Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md).
2.  Ottenere il descrittore di presentazione dell'origine multimediale.
3.  Creare una topologia vuota.
4.  Usare il descrittore della presentazione per enumerare i descrittori del flusso. Per ogni descrittore di flusso:
    1.  Ottenere il tipo di supporto principale del flusso, ad esempio audio o video.
    2.  Controllare se il flusso è attualmente selezionato. Facoltativamente, è possibile selezionare o deselezionare un flusso, in base al tipo di supporto.
    3.  Se il flusso è selezionato, creare un oggetto attivazione per il sink multimediale, in base al tipo di supporto del flusso.
    4.  Aggiungere un nodo di origine per il flusso e un nodo di output per il sink multimediale.
    5.  Connettere il nodo di origine al nodo di output.

Per semplificare il processo, il codice di esempio in questo argomento è organizzato in diverse funzioni. La funzione di primo livello è denominata `CreatePlaybackTopology` . Sono necessari tre parametri:

-   Puntatore a un'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.
-   Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione. Ottenere questo puntatore chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Per le origini con più presentazioni, i descrittori di presentazione per le presentazioni successive vengono recapitati nell'evento [MENewPresentation](menewpresentation.md) .
-   Handle per una finestra dell'applicazione. Se l'origine ha un flusso video, il video verrà visualizzato in questa finestra.

La funzione restituisce un puntatore a una topologia di riproduzione parziale nel parametro *ppTopology* .


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



Questa funzione esegue questa procedura:

1.  Chiamare [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) per creare la topologia. Inizialmente, la topologia non contiene alcun nodo.
2.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) per ottenere il numero di flussi nella presentazione.
3.  Per ogni flusso, chiamare la funzione definita dall'applicazione `AddBranchToPartialTopology` a un ramo nella topologia. Questa funzione è illustrata nella sezione successiva.

## <a name="connecting-streams-to-media-sinks"></a>Connessione di flussi a sink multimediali

Per ogni flusso selezionato, aggiungere un nodo di origine e un nodo di output, quindi connettere i due nodi. Il nodo di origine rappresenta il flusso. Il nodo di output rappresenta il [renderer video migliorato](enhanced-video-renderer.md) (EVR) o il [renderer di streaming audio](streaming-audio-renderer.md) (SAR).

La `AddBranchToPartialTopology` funzione, mostrata nell'esempio successivo, accetta i parametri seguenti:

-   Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.
-   Puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.
-   Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione.
-   Indice in base zero del flusso.
-   Handle per la finestra del video. Questo handle viene usato solo per il flusso video.


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



La funzione esegue le operazioni seguenti:

1.  Chiama [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passa l'indice del flusso. Questo metodo restituisce un puntatore al descrittore del flusso per il flusso, insieme a un valore booleano che indica se il flusso è selezionato.
2.  Se il flusso non è selezionato, la funzione viene chiusa e restituisce S \_ OK, perché non è necessario che l'applicazione crei un ramo della topologia per un flusso a meno che non sia selezionato.
3.  Se il flusso è selezionato, la funzione completa il ramo della topologia come indicato di seguito:
    1.  Crea un oggetto attivazione per il sink, chiamando la funzione CreateMediaSinkActivate definita dall'applicazione. Questa funzione è illustrata nella sezione successiva.
    2.  Aggiunge un nodo di origine alla topologia. Il codice per questo passaggio è illustrato nell'argomento [creazione di nodi di origine](creating-source-nodes.md).
    3.  Aggiunge un nodo di output alla topologia. Il codice per questo passaggio è illustrato nell'argomento [creazione di nodi di output](creating-output-nodes.md).
    4.  Connette i due nodi chiamando [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) nel nodo di origine. Connettendo i nodi, l'applicazione indica che il nodo upstream deve recapitare i dati al nodo downstream. Un nodo di origine ha un output e un nodo di output ha un input, quindi entrambi gli indici del flusso sono pari A zero.

Le applicazioni più avanzate possono selezionare o deselezionare i flussi, anziché usare la configurazione predefinita dell'origine. Un'origine potrebbe avere più flussi ed è possibile che sia selezionata per impostazione predefinita. Il descrittore di presentazione dell'origine multimediale dispone di un set predefinito di selezioni di flusso. In un semplice file video con un solo flusso audio e un flusso video, l'origine multimediale in genere seleziona entrambi i flussi per impostazione predefinita. Tuttavia, un file potrebbe avere più flussi audio per lingue diverse o più flussi video codificati a velocità in bit diverse. In tal caso, alcuni flussi verranno deselezionati per impostazione predefinita. L'applicazione può modificare la selezione chiamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) sul descrittore della presentazione.

## <a name="creating-the-media-sink"></a>Creazione del sink multimediale

La funzione Next crea un oggetto Activation per il sink del supporto EVR o SAR.


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



Questa funzione esegue questa procedura:

1.  Chiama [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso. Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

2.  Chiama [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Questo metodo restituisce il GUID del tipo principale per il flusso.

3.  Se il tipo di flusso è audio, la funzione chiama [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) per creare l'oggetto attivazione renderer audio. Se il tipo di flusso è video, la funzione chiama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione del renderer video. Entrambe queste funzioni restituiscono un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Questo puntatore viene usato per inizializzare il nodo di output per il sink, come illustrato in precedenza.

Per qualsiasi altro tipo di flusso, in questo esempio viene restituito un codice di errore. In alternativa, è possibile deselezionare semplicemente il flusso.

## <a name="next-steps"></a>Passaggi successivi

Per riprodurre un file multimediale alla volta, accodare la topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). La sessione multimediale utilizzerà il caricatore della topologia per risolvere la topologia. Per un esempio completo, vedere [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come riprodurre file multimediali non protetti](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



