---
description: Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Come scrivere un presentatore EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e80c2c6397282b93aef1db0e5c491234e045472
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474747"
---
# <a name="how-to-write-an-evr-presenter"></a>Come scrivere un presentatore EVR

Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR). Un presentatore personalizzato può essere usato con DirectShow e Media Foundation; le interfacce e il modello a oggetti sono gli stessi per entrambe le tecnologie, anche se la sequenza esatta delle operazioni può variare.

Il codice di esempio in questo argomento è stato adattato dall'esempio [EVRPresenter](evrpresenter-sample.md), disponibile in Windows SDK.

In questo argomento sono incluse le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Modello a oggetti del presentatore](#presenter-object-model)
    -   [Dati Flow all'interno dell'EVR](#data-flow-inside-the-evr)
    -   [Stati del presentatore](#presenter-states)
    -   [Interfacce del presentatore](#presenter-interfaces)
    -   [Implementazione di IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [Implementazione di IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implementazione di IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [Implementazione di IMFClockStateSink](#implementing-imfclockstatesink)
    -   [Implementazione di IMFRateSupport](#implementing-imfratesupport)
    -   [Invio di eventi all'EVR](#sending-events-to-the-evr)
-   [Formati di negoziazione](#negotiating-formats)
-   [Gestione del dispositivo Direct3D](#managing-the-direct3d-device)
    -   [Allocazione di superfici Direct3D](#allocating-direct3d-surfaces)
    -   [Esempi di rilevamento](#tracking-samples)
-   [Elaborazione dell'output](#processing-output)
    -   [Ridipingere i frame](#repainting-frames)
    -   [Esempi di pianificazione](#scheduling-samples)
    -   [Presentazione di esempi](#presenting-samples)
    -   [Rettangoli di origine e destinazione](#source-and-destination-rectangles)
    -   [Fine del flusso](#end-of-stream)
-   [Esecuzione di istruzioni per i frame](#frame-stepping)
    -   [Implementazione dell'esecuzione di istruzioni per i frame](#implementing-frame-stepping)
-   [Impostazione del presentatore nel EVR](#setting-the-presenter-on-the-evr)
    -   [Impostazione del presenter in DirectShow](#setting-the-presenter-in-directshow)
    -   [Impostazione del presenter in Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Prima di scrivere un presentatore personalizzato, è necessario avere familiarità con le tecnologie seguenti:

-   Renderer video avanzato. Vedere [Renderer video avanzato](enhanced-video-renderer.md).
-   Grafica Direct3D. Non è necessario comprendere la grafica 3D per scrivere un presentatore, ma è necessario sapere come creare un dispositivo Direct3D e gestire le superfici Direct3D. Se non si ha familiarità con Direct3D, leggere le sezioni "Dispositivi Direct3D" e "Risorse Direct3D" nella documentazione di DirectX Graphics SDK.
-   DirectShow grafici di filtro o Media Foundation pipeline, a seconda della tecnologia che verrà utilizzata dall'applicazione per il rendering del video.
-   [Media Foundation trasforma](media-foundation-transforms.md). Il mixer EVR è una Media Foundation e il presentatore chiama i metodi direttamente sul mixer.
-   Implementazione di oggetti COM. Il presentatore è un oggetto COM in-process a thread libero.

## <a name="presenter-object-model"></a>Modello a oggetti del presentatore

Questa sezione contiene una panoramica del modello a oggetti e delle interfacce del presentatore.

### <a name="data-flow-inside-the-evr"></a>Dati Flow all'interno dell'EVR

L'EVR usa due componenti plug-in per eseguire il rendering del video: il *mixer* e *il presentatore*. Il mixer unisce i flussi video e, se necessario, deinterlaces il video. Il presentatore disegna (o *presenta)* il video sullo schermo e pianifica quando viene disegnato ogni fotogramma. Le applicazioni possono sostituire uno di questi oggetti con un'implementazione personalizzata.

L'EVR ha uno o più flussi di input e il mixer ha un numero corrispondente di flussi di input. Il flusso 0 è sempre il *flusso di riferimento*. Gli altri flussi sono *sottostream*, che il mixer combina alfa nel flusso di riferimento. Il flusso di riferimento determina la frequenza fotogrammi master per il video composito. Per ogni fotogramma di riferimento, il mixer accetta il frame più recente da ogni flusso secondario, li combina alfa nel frame di riferimento e restituisce un singolo frame composito. Il mixer esegue anche la deinterlacing e la conversione dei colori da YUV a RGB, se necessario. L'EVR inserisce sempre il mixer nella pipeline video, indipendentemente dal numero di flussi di input o dal formato video. L'immagine seguente illustra questo processo.

![diagramma che mostra il flusso di riferimento e il flusso secondario che punta al mixer, che punta al presentatore, che punta alla visualizzazione](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Il presentatore esegue le attività seguenti:

-   Imposta il formato di output nel mixer. Prima dell'inizio dello streaming, il presentatore imposta un tipo di supporto nel flusso di output del mixer. Questo tipo di supporto definisce il formato dell'immagine composita.
-   Crea il dispositivo Direct3D.
-   Alloca le superfici Direct3D. Il mixer esegue il blits dei fotogrammi compositi su queste superfici.
-   Ottiene l'output dal mixer.
-   Pianifica la presentazione dei frame. L'EVR fornisce l'orologio della presentazione e il presentatore pianifica i fotogrammi in base a questo orologio.
-   Presenta ogni frame usando Direct3D.
-   Esegue il frame stepping e lo scrubbing.

### <a name="presenter-states"></a>Stati del presentatore

In qualsiasi momento, il presentatore si trova in uno degli stati seguenti:

-   *Avviato*. L'orologio di presentazione dell'EVR è in esecuzione. Il presentatore pianifica i fotogrammi video per la presentazione non appena arrivano.
-   *In pausa.* L'orologio della presentazione viene sospeso. Il presentatore non presenta nuovi esempi, ma mantiene la coda di esempi pianificati. Se vengono ricevuti nuovi esempi, il presentatore li aggiunge alla coda.
-   *Arrestato*. L'orologio della presentazione viene arrestato. Il presentatore rimuove tutti gli esempi pianificati.
-   *Arrestare*. Il presentatore rilascia tutte le risorse correlate allo streaming, ad esempio le superfici Direct3D. Si tratta dello stato iniziale del presentatore e dello stato finale prima dell'eliminazione del presentatore.

Nel codice di esempio in questo argomento lo stato del presentatore è rappresentato da un'enumerazione :


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Alcune operazioni non sono valide mentre il presentatore è in stato di arresto. Il codice di esempio verifica questo stato chiamando un metodo helper:


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Interfacce del presentatore

Un presentatore è necessario per implementare le interfacce seguenti:



| Interfaccia                                                                | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Notifica al presentatore quando l'orologio dell'EVR cambia stato. Vedere [Implementazione di IMFClockStateSink](#implementing-imfclockstatesink).                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Consente all'applicazione e ad altri componenti nella pipeline di ottenere le interfacce dal presentatore.                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Consente al presentatore di ottenere le interfacce dall'EVR o dal mixer. Vedere [Implementazione di IMFTopologyServiceLookupClient.](#implementing-imftopologyservicelookupclient) |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Assicura che il presentatore e il mixer usino tecnologie compatibili. Vedere [Implementazione di IMFVideoDeviceID.](#implementing-imfvideodeviceid)                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Elabora i messaggi provenienti da EVR. Vedere [Implementazione di IMFVideoPresenter.](#implementing-imfvideopresenter)                                                             |



 

Le interfacce seguenti sono facoltative:



| Interfaccia                                                | Descrizione                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Consente al presentatore di usare supporti protetti. Implementare questa interfaccia se il presentatore è un componente attendibile progettato per funzionare nel percorso del supporto protetto (PMP). |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Segnala l'intervallo di velocità di riproduzione supportate dal presentatore. Vedere [Implementazione di IMFRateSupport.](#implementing-imfratesupport)                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mappe coordinate del fotogramma video di output alle coordinate sul fotogramma video di input.                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Segnala informazioni sulle prestazioni. L'EVR usa queste informazioni per la gestione del controllo di qualità. Questa interfaccia è documentata in DirectShow SDK.                        |



 

È anche possibile fornire interfacce per consentire all'applicazione di comunicare con il presentatore. A questo scopo, il presentatore standard implementa l'interfaccia [**IMFVideoDisplayControl.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) È possibile implementare questa interfaccia o definirne una personalizzata. L'applicazione ottiene le interfacce dal presentatore chiamando [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) su EVR. Quando il GUID del **servizio MR_VIDEO_RENDER_SERVICE**, EVR passa la **richiesta GetService** al presentatore.

### <a name="implementing-imfvideodeviceid"></a>Implementazione di IMFVideoDeviceID

[**L'interfaccia IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un metodo, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)che restituisce un GUID del dispositivo. Il GUID del dispositivo garantisce che il presentatore e il mixer usino tecnologie compatibili. Se i GUID del dispositivo non corrispondono, l'inizializzazione dell'EVR non riesce.

Il mixer e il presentatore standard usano entrambi Direct3D 9, con il GUID del dispositivo uguale **IID_IDirect3DDevice9**. Se si intende usare il presentatore personalizzato con il mixer standard, il GUID del dispositivo del presentatore deve essere **IID_IDirect3DDevice9**. Se si sostituiscono entrambi i componenti, è possibile definire un nuovo GUID del dispositivo. Nella parte restante di questo articolo si presuppone che il presentatore usi Direct3D 9. Ecco l'implementazione standard di [**GetDeviceID:**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



Il metodo deve avere esito positivo anche quando il presentatore viene arrestato.

### <a name="implementing-imftopologyservicelookupclient"></a>Implementazione di IMFTopologyServiceLookupClient

[**L'interfaccia IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) consente al presentatore di ottenere i puntatori di interfaccia da EVR e dal mixer come indicato di seguito:

1.  Quando EVR inizializza il presentatore, chiama il metodo [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentatore. L'argomento è un puntatore [**all'interfaccia IMFTopologyServiceLookup di EVR.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup)
2.  Il presentatore chiama [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) per ottenere i puntatori a interfaccia dall'EVR o dal mixer.

Il [**metodo LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) è simile al [**metodo IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Entrambi i metodi accettano un GUID del servizio e un identificatore di interfaccia (IID) come input, ma **LookupService** restituisce una matrice di puntatori a interfaccia, mentre **GetService** restituisce un singolo puntatore. In pratica, tuttavia, è sempre possibile impostare le dimensioni della matrice su 1. L'oggetto sottoposto a query dipende dal GUID del servizio:

-   Se il GUID del servizio **MR_VIDEO_RENDER_SERVICE**, viene eseguita una query sull'EVR.
-   Se il GUID del servizio **MR_VIDEO_MIXER_SERVICE**, viene eseguita una query sul mixer.

Nell'implementazione [**di InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)ottenere le interfacce seguenti da EVR:



| Interfaccia EVR                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Consente al presentatore di inviare messaggi all'EVR. Questa interfaccia è definita in DirectShow SDK, quindi i messaggi seguono il modello per gli eventi DirectShow, non per Media Foundation eventi.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Rappresenta l'orologio dell'EVR. Il presentatore usa questa interfaccia per pianificare gli esempi per la presentazione. L'EVR può essere eseguito senza clock, pertanto questa interfaccia potrebbe non essere disponibile. In caso contrario, ignorare il codice di errore [**da LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> L'orologio implementa anche [**l'interfaccia IMFTimer.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) Nella pipeline Media Foundation l'orologio implementa [**l'interfaccia IMFPresentationClock.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) Non implementa questa interfaccia in DirectShow.<br/> |



 

Ottenere le interfacce seguenti dal mixer:



| Mixer Interfaccia                              | Descrizione                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Consente al presentatore di comunicare con il mixer.       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Consente al presentatore di convalidare il GUID del dispositivo del mixer. |



 

Il codice seguente implementa il [**metodo InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Quando i puntatori a interfaccia ottenuti da [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) non sono più validi, EVR chiama [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). All'interno di questo metodo rilasciare tutti i puntatori a interfaccia e impostare lo stato del presentatore per l'arresto:


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



L'EVR chiama [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) per vari motivi, tra cui:

-   Disconnessione o riconnessione dei pin (DirectShow) o aggiunta o rimozione di sink di flusso (Media Foundation).
-   Modifica del formato.
-   Impostazione di un nuovo orologio.
-   Arresto finale di EVR.

Durante la durata del presentatore, EVR potrebbe chiamare [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) più volte.

### <a name="implementing-imfvideopresenter"></a>Implementazione di IMFVideoPresenter

[**L'interfaccia IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) eredita [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e aggiunge due metodi:



| Metodo                                                               | Descrizione                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Restituisce il tipo di contenuto multimediale dei fotogrammi video compositi. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Segnala al presentatore di eseguire varie azioni.      |



 

Il [**metodo GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) restituisce il tipo di supporto del presentatore. Per informazioni dettagliate sull'impostazione del tipo di supporto, vedere [Formati di negoziazione.](#negotiating-formats) Il tipo di supporto viene restituito come [**puntatore a interfaccia IMFVideoMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) Nell'esempio seguente si presuppone che il presentatore archivi il tipo di supporto come [**puntatore IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Per ottenere **l'interfaccia IMFVideoMediaType** dal tipo di supporto, chiamare **QueryInterface:**


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Il [**metodo ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) è il meccanismo principale per la comunicazione tra EVR e il presentatore. Vengono definiti i messaggi seguenti. I dettagli dell'implementazione di ogni messaggio sono disponibili nella parte restante di questo argomento.



| Message                                | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Il tipo di supporto di output del mixer non è valido. Il presentatore deve negoziare un nuovo tipo di supporto con il mixer. Vedere [Formati di negoziazione.](#negotiating-formats)                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Lo streaming è stato avviato. Questo messaggio non richiede alcuna azione specifica, ma è possibile usarla per allocare risorse.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | Lo streaming è terminato. Rilasciare tutte le risorse allocate in risposta al **MFVP_MESSAGE_BEGINSTREAMING** messaggio.                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Il mixer ha ricevuto un nuovo esempio di input e potrebbe essere in grado di generare un nuovo frame di output. Il presentatore deve [**chiamare IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) nel mixer. Vedere [Elaborazione dell'output.](#processing-output) |
| **MFVP_MESSAGE_ENDOFSTREAM**         | La presentazione è terminata. Vedere [Fine del flusso.](#end-of-stream)                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | L'EVR sta scaricando i dati nella pipeline di rendering. Il presentatore deve rimuovere tutti i fotogrammi video pianificati per la presentazione.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Richiede al presentatore di inoltrare N fotogrammi. Il presentatore deve rimuovere i fotogrammi N-1 successivi e visualizzare il fotogramma N. Vedere [Esecuzione di istruzioni nei frame.](#frame-stepping)                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Annulla l'esecuzione passo a passo dei fotogrammi.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementazione di IMFClockStateSink

Il presentatore deve implementare [**l'interfaccia IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) come parte dell'implementazione di [**IMFVideoPresenter,**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)che eredita **IMFClockStateSink.** L'EVR usa questa interfaccia per notificare al presentatore ogni volta che lo stato dell'orologio dell'EVR cambia. Per altre informazioni sugli stati dell'orologio, vedere [Presentation Clock](presentation-clock.md).

Di seguito sono riportate alcune linee guida per l'implementazione dei metodi in questa interfaccia. Tutti i metodi devono avere esito negativo se il presentatore viene arrestato.




| | | <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"> <strong>OnClockStart</strong></a> | <ol><li>Impostare lo stato del presentatore su started.</li><li>Se <em>llClockStartOffset</em> non è <strong>PRESENTATION_CURRENT_POSITION</strong>, scaricare la coda di esempi del presentatore. Equivale a ricevere un messaggio <strong>MFVP_MESSAGE_FLUSH</strong> messaggio.</li><li>Se una richiesta di passaggio del frame precedente è ancora in sospeso, elaborare la richiesta (vedere <a href="#frame-stepping">Esecuzione istruzione/istruzione del frame).</a> In caso contrario, provare a elaborare l'output del mixer (vedere <a href="#processing-output">Elaborazione dell'output).</a></li></ol> | | <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"> <strong>OnClockStop</strong></a> | <ol><li>Impostare lo stato del presentatore su Arrestato.</li><li>Scaricare la coda di esempi del presentatore.</li><li>Annulla tutte le operazioni in sospeso del passaggio del frame.</li></ol> | | <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause |</strong></a> Impostare lo stato del presentatore su Sospeso. | | <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a> | Trattare come <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart,</strong></a> ma non scaricare la coda di campioni. | | <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"> <strong>OnClockSetRate</strong></a> | <ol><li>Se la frequenza cambia da zero a diversa da zero, annullare l'esecuzione delle istruzioni dei fotogrammi.</li><li>Archiviare la nuova frequenza di clock. La frequenza di clock influisce sulla presentazione dei campioni. Per altre informazioni, vedere <a href="#scheduling-samples">Esempi di pianificazione.</a></li></ol> | 




 

### <a name="implementing-imfratesupport"></a>Implementazione di IMFRateSupport

Per supportare velocità di riproduzione diverse da 1×, il presentatore deve implementare [**l'interfaccia IMFRateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) Di seguito sono riportate alcune linee guida per l'implementazione dei metodi in questa interfaccia. Tutti i metodi devono avere esito negativo dopo l'arresto del presentatore. Per altre informazioni su questa interfaccia, vedere [Controllo della frequenza.](rate-control.md)



| valore                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Restituisce zero per indicare che non è presente alcuna velocità di riproduzione minima.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Per la riproduzione senza thinning, la velocità di riproduzione non deve superare la frequenza di aggiornamento del *monitor:* frequenza massima di aggiornamento  =   (Hz) / frequenza *dei fotogrammi video* (fps). La frequenza dei fotogrammi video è specificata nel tipo di contenuto multimediale del presentatore. <br/> Per la riproduzione con thinning, la velocità di riproduzione è illimitata; restituisce il valore **FLT_MAX**. In pratica, l'origine e il decodificatore saranno i fattori limitanti durante la riproduzione con thinning. <br/> Per la riproduzione inversa, restituisce il valore negativo della frequenza massima.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Restituisce **MF_E_UNSUPPORTED_RATE** se il valore assoluto di *flRate* supera la velocità di riproduzione massima del presentatore. Calcolare la velocità di riproduzione massima come descritto per [**GetFastestRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)                                                                                                                                                                                                                                                                                    |



 

L'esempio seguente illustra come implementare [**il metodo GetFastestRate:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



L'esempio precedente chiama un metodo helper, GetMaxRate, per calcolare la velocità massima di riproduzione in avanti:

L'esempio seguente illustra come implementare il [**metodo IsRateSupported:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Invio di eventi all'EVR

Il presentatore deve notificare all'EVR diversi eventi. A tale scopo, usa l'interfaccia [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) di EVR, ottenuta quando EVR chiama il metodo [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentatore. **L'interfaccia IMediaEventSink** è in origine DirectShow, ma viene usata sia nel DirectShow EVR che nel Media Foundation. Il codice seguente illustra come inviare un evento all'EVR:


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



Nella tabella seguente sono elencati gli eventi inviati dal presentatore, insieme ai parametri dell'evento.




| Event | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a> | Il presentatore ha completato il rendering di tutti i fotogrammi dopo MFVP_MESSAGE_ENDOFSTREAM messaggio.<br /><ul><li><em>Param1:</em>HRESULT che indica lo stato dell'operazione.</li><li><em>Param2:</em>non usato.</li></ul>Per altre informazioni, vedere <a href="#end-of-stream">Fine del flusso.</a><br /> | 
| <a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a> | Il dispositivo Direct3D è stato modificato.<br /><ul><li><em>Param1:</em>non usato.</li><li><em>Param2:</em>non usato.</li></ul>Per altre informazioni, vedere <a href="#managing-the-direct3d-device">Gestione del dispositivo Direct3D.</a><br /> | 
| <a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a> | Si è verificato un errore che richiede l'arresto del flusso.<br /><ul><li><em>Param1:</em> <strong>HRESULT</strong> che indica l'errore che si è verificato.</li><li><em>Param2:</em>non usato.</li></ul> | 
| <a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a> | Specifica il tempo necessario al presentatore per eseguire il rendering di ogni frame. Facoltativo.<br /><ul><li><em>Param1:</em>puntatore a un valore <strong>LONGLONG</strong> costante che contiene la quantità di tempo per l'elaborazione del frame, in unità di 100 nanosecondi.</li><li><em>Param2:</em>non usato.</li></ul>Per altre informazioni, vedere <a href="#processing-output">Elaborazione dell'output.</a><br /> | 
| <a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a> | Specifica il tempo di ritardo corrente negli esempi di rendering. Se il valore è positivo, i campioni sono in ritardo rispetto alla pianificazione. Se il valore è negativo, i campioni sono in anticipo rispetto alla pianificazione. Facoltativo.<br /><ul><li><em>Param1:</em>puntatore a un <strong>valore LONGLONG</strong> costante che contiene il tempo di ritardo, in unità di 100 nanosecondi.</li><li><em>Param2:</em>non usato.</li></ul> | 
| <a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a> | Inviato immediatamente dopo <strong>EC_STEP_COMPLETE</strong> se la velocità di riproduzione è zero. Questo evento contiene il timestamp del frame visualizzato.<br /><ul><li><em>Param1:</em>32 bit inferiori del timestamp.</li><li><em>Param2:</em>32 bit superiori del timestamp.</li></ul>Per altre informazioni, vedere Esecuzione di <a href="#frame-stepping">istruzioni nei frame.</a><br /> | 
| <a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a> | Il presentatore ha completato o annullato un passaggio del frame.<br /><ul><li><em>Param1:</em>non usato.</li><li><em>Param2:</em>non usato.</li></ul>Per altre informazioni, vedere Esecuzione di <a href="#frame-stepping">istruzioni nei frame.</a><br /><blockquote>[!Note]<br />Una versione precedente della documentazione descriveva <em>Param1 in modo non</em> corretto. Questo parametro non viene usato per questo evento.</blockquote><br /> | 




 

## <a name="negotiating-formats"></a>Formati di negoziazione

Ogni volta che il presentatore riceve **un messaggio MFVP_MESSAGE_INVALIDATEMEDIATYPE** da EVR, deve impostare il formato di output nel mixer, come indicato di seguito:

1.  Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) sul mixer per ottenere un possibile tipo di output. Questo tipo descrive un formato che il mixer può produrre in base ai flussi di input e alle funzionalità di elaborazione video del dispositivo grafico.
2.  Controllare se il presentatore può usare questo tipo di supporto come formato di rendering. Ecco alcuni aspetti da controllare, anche se l'implementazione potrebbe avere requisiti specifici:

    -   Il video deve essere non compresso.
    -   Il video deve avere solo fotogrammi progressivi. Verificare che [**l'attributo MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) sia **uguale MFVideoInterlace_Progressive**.
    -   Il formato deve essere compatibile con il dispositivo Direct3D.

    Se il tipo non è accettabile, tornare al passaggio 1 e ottenere il tipo proposto successivo del mixer.

3.  Creare un nuovo tipo di supporto che sia un clone del tipo originale e quindi modificare gli attributi seguenti:

    -   Impostare [**l MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attributo uguale alla larghezza e all'altezza desiderate per le superfici Direct3D da allocare.
    -   Impostare [**l'MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) su **FALSE.**
    -   Impostare [](mf-mt-pixel-aspect-ratio-attribute.md) l MF_MT_PIXEL_ASPECT_RATIO attribuita del valore pari al valore PAR dello schermo (in genere 1:1).
    -   Impostare l'apertura geometrica [**(MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attributo ) su un rettangolo all'interno della superficie Direct3D. Quando il mixer genera un frame di output, esegue il blittang dell'immagine di origine in questo rettangolo. L'apertura geometrica può essere grande quanto la superficie o può essere un subrectangle all'interno della superficie. Per altre informazioni, vedere [Rettangoli di origine e destinazione.](#source-and-destination-rectangles)

4.  Per verificare se il mixer accetterà il tipo di output modificato, chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con il flag **MFT_SET_TYPE_TEST_ONLY.** Se il mixer rifiuta il tipo, tornare al passaggio 1 e ottenere il tipo successivo.
5.  Allocare un pool di superfici Direct3D, come descritto in [Allocazione di superfici Direct3D.](#allocating-direct3d-surfaces) Il mixer userà queste superfici quando disegna i fotogrammi video compositi.
6.  Impostare il tipo di output nel mixer chiamando [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) senza flag. Se la prima chiamata a **SetOutputType** ha avuto esito positivo nel passaggio 4, il metodo dovrebbe riuscire di nuovo.

Se il mixer esaure i tipi, il [**metodo GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) restituisce **MF_E_NO_MORE_TYPES**. Se il presentatore non riesce a trovare un tipo di output appropriato per il mixer, non è possibile eseguire il rendering del flusso. In tal caso, DirectShow o Media Foundation possibile provare un altro formato di flusso. Di conseguenza, il presentatore potrebbe ricevere **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messaggi in una riga fino a quando non viene trovato un tipo valido.

Il mixer crea automaticamente una letterbox del video, prendendo in considerazione le proporzioni pixel (PAR) dell'origine e della destinazione. Per ottenere risultati ottimali, la larghezza e l'altezza della superficie e l'apertura geometrica devono essere uguali alle dimensioni effettive in cui si vuole che il video venga visualizzato sullo schermo. L'immagine seguente illustra questo processo.

![diagramma che mostra un fram composito che porta a una superficie direct3d, che porta a una finestra](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

Il codice seguente illustra la struttura del processo. Alcuni dei passaggi vengono inseriti nelle funzioni helper, i cui dettagli esatti dipendono dai requisiti del presentatore.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Per altre informazioni sui tipi di file multimediali video, vedere [Tipi di file multimediali video.](video-media-types.md)

## <a name="managing-the-direct3d-device"></a>Gestione del dispositivo Direct3D

Il presentatore crea il dispositivo Direct3D e gestisce eventuali perdite di dispositivi durante lo streaming. Il presentatore ospita anche Gestione dispositivi Direct3D, che consente ad altri componenti di usare lo stesso dispositivo. Ad esempio, il mixer usa il dispositivo Direct3D per combinare i sottostream, i delnterlace ed eseguire regolazioni del colore. I decodificatori possono usare il dispositivo Direct3D per la decodifica con accelerazione video. Per altre informazioni sull'accelerazione video, vedere [Accelerazione video DirectX 2.0.](directx-video-acceleration-2-0.md)

Per configurare il dispositivo Direct3D, seguire questa procedura:

1.  Creare l'oggetto Direct3D chiamando **Direct3DCreate9** **o Direct3DCreate9Ex.**
2.  Creare il dispositivo chiamando **IDirect3D9::CreateDevice** o **IDirect3D9Ex::CreateDevice**.
3.  Creare gestione dispositivi chiamando [**DXVA2CreateDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)
4.  Impostare il dispositivo in Gestione dispositivi chiamando [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Se un altro componente della pipeline necessita di Gestione dispositivi, chiama [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nell'EVR, specificando MR_VIDEO_ACCELERATION_SERVICE **per** il GUID del servizio. EVR passa la richiesta al presentatore. Dopo che l'oggetto ottiene il puntatore [**IDirect3DDeviceManager9,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) può ottenere un handle per il dispositivo chiamando [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Quando l'oggetto deve usare il dispositivo, passa l'handle del dispositivo al metodo [**IDirect3DDeviceManager9::LockDevice,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) che restituisce un **puntatore IDirect3DDevice9.**

Dopo aver creato il dispositivo, se il presentatore elimina il dispositivo e ne crea uno nuovo, il presentatore deve chiamare [**nuovamente ResetDevice.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) Il **metodo ResetDevice** invalida tutti gli handle di dispositivo esistenti, causando la restituzione di [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE**. Questo codice di errore segnala ad altri oggetti che usano il dispositivo di aprire un nuovo handle di dispositivo. Per altre informazioni sull'uso di Gestione dispositivi, vedere [Gestione dispositivi Direct3D.](direct3d-device-manager.md)

Il presentatore può creare il dispositivo in modalità finestra o in modalità esclusiva a schermo intero. Per la modalità finestra, è necessario fornire all'applicazione un modo per specificare la finestra video. Il presentatore standard implementa il [**metodo IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) a questo scopo. È necessario creare il dispositivo quando il presentatore viene creato per la prima volta. In genere, al momento non si conoscono tutti i parametri del dispositivo, ad esempio la finestra o il formato del buffer nascosto. È possibile creare un dispositivo temporaneo e sostituirlo in&; ricordarsi di chiamare \# [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) in Gestione dispositivi.

Se si crea un nuovo dispositivo o si chiama **IDirect3DDevice9::Reset** o **IDirect3DDevice9Ex::ResetEx** in un dispositivo esistente, inviare un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) all'EVR. Questo evento notifica all'EVR di rinegoziare il tipo di supporto. L'EVR ignora i parametri dell'evento per questo evento.

### <a name="allocating-direct3d-surfaces"></a>Allocazione di superfici Direct3D

Dopo che il presentatore ha impostato il tipo di supporto, può allocare le superfici Direct3D, che verranno usate dal mixer per scrivere i fotogrammi video. La superficie deve corrispondere al tipo di supporto del presentatore:

-   Il formato della superficie deve corrispondere al sottotipo multimediale. Ad esempio, se il sottotipo **è MFVideoFormat_RGB24**, il formato della superficie deve **essere D3DFMT_X8R8G8B8**. Per altre informazioni sui sottotipi e sui formati Direct3D, vedere [GUID del sottotipo video.](video-subtype-guids.md)
-   La larghezza e l'altezza della superficie devono corrispondere alle dimensioni specificate [**nell'attributo MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) del tipo di supporto.

Il modo consigliato per allocare le superfici dipende dal fatto che il presentatore venga eseguito in modalità finestra o a schermo intero.

Se il dispositivo Direct3D è in finestra, è possibile creare diverse catene di scambio, ognuna con un singolo buffer nascosto. Con questo approccio, è possibile presentare ogni superficie in modo indipendente, perché la presentazione di una catena di scambio non interferisce con le altre catene di scambio. Il mixer può scrivere dati su una superficie mentre un'altra superficie è pianificata per la presentazione.

Prima di tutto, decidere il numero di catene di scambio da creare. È consigliabile almeno tre. Per ogni catena di scambio, eseguire le operazioni seguenti:

1.  Chiamare **IDirect3DDevice9::CreateAdditionalSwapChain** per creare la catena di scambio.
2.  Chiamare **IDirect3DSwapChain9::GetBackBuffer** per ottenere un puntatore alla superficie del buffer nascosto della catena di scambio.
3.  Chiamare [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) e passare un puntatore alla superficie. Questa funzione restituisce un puntatore a un oggetto video di esempio. L'oggetto video di esempio implementa l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e il presentatore usa questa interfaccia per distribuire la superficie al mixer quando il presentatore chiama il metodo [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer. Per altre informazioni sull'oggetto video di esempio, vedere [Esempi video.](video-samples.md)
4.  Archiviare [**il puntatore IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una coda. Il presentatore estrarrà gli esempi da questa coda durante l'elaborazione, come descritto in [Elaborazione dell'output.](#processing-output)
5.  Mantenere un riferimento al **puntatore IDirect3DSwapChain9** in modo che la catena di scambio non sia rilasciata.

In modalità esclusiva a schermo intero, il dispositivo non può avere più di una catena di scambio. Questa catena di scambio viene creata in modo implicito quando si crea il dispositivo a schermo intero. La catena di scambio può avere più di un buffer nascosto. Sfortunatamente, tuttavia, se si presenta un buffer nascosto mentre si scrive in un altro buffer nascosto nella stessa catena di scambio, non esiste un modo semplice per coordinare le due operazioni. Ciò è dovuto al modo in cui Direct3D implementa il capovolgimento della superficie. Quando si chiama Present, il driver di grafica aggiorna i puntatori di superficie nella memoria grafica. Se si mantendono puntatori **IDirect3DSurface9** quando si chiama **Present,** questi puntino a buffer diversi dopo la fine **della** chiamata a Present.

L'opzione più semplice è creare un campione video per la catena di scambio. Se si sceglie questa opzione, seguire la stessa procedura descritta per la modalità finestra. L'unica differenza è che la coda di esempio contiene un singolo esempio video. Un'altra opzione è creare superfici fuori schermo e quindi eseguire il blittamento nel buffer nascosto. Le superfici create devono supportare il metodo [**IDirectXVideoProcessor::VideoProcessBlt,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) che il mixer usa per combinare i fotogrammi di output.

### <a name="tracking-samples"></a>Esempi di rilevamento

Quando il presentatore alloca per la prima volta gli esempi di video, li inserisce in una coda. Il presentatore estrae da questa coda ogni volta che deve ottenere un nuovo fotogramma dal mixer. Dopo che il mixer ha restituito il frame, il presentatore sposta l'esempio in una seconda coda. La seconda coda è per gli esempi in attesa dei relativi orari di presentazione pianificati.

Per semplificare il monitoraggio dello stato di ogni esempio, l'oggetto video di esempio implementa [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) È possibile usare questa interfaccia come segue:

1.  Implementare [**l'interfaccia IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) nel presentatore.
2.  Prima di inserire un esempio nella coda pianificata, eseguire una query sull'oggetto video di esempio per [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

3.  Chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntatore all'interfaccia di callback.
4.  Quando l'esempio è pronto per la presentazione, rimuoverlo dalla coda pianificata, presentarlo e rilasciare tutti i riferimenti all'esempio.
5.  L'esempio richiama il callback. L'oggetto di esempio non viene eliminato in questo caso perché contiene un conteggio dei riferimenti su se stesso fino a quando non viene richiamato il callback.
6.  All'interno del callback, restituire l'esempio alla coda disponibile.

Non è necessario che un presentatore usi [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) per tenere traccia degli esempi. È possibile implementare qualsiasi tecnica più adatta alla progettazione. Uno dei vantaggi di **IMFTrackedSample** è che è possibile spostare le funzioni di pianificazione e rendering del presentatore in oggetti helper e questi oggetti non necessitano di alcun meccanismo speciale per richiamare il presentatore quando rilasciano esempi video perché l'oggetto di esempio fornisce tale meccanismo.

Il codice seguente illustra come impostare il callback:


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



Nel callback chiamare [**IMFAsyncResult::GetObject sull'oggetto**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) risultato asincrono per recuperare un puntatore all'esempio:


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Elaborazione dell'output

Ogni volta che il mixer riceve un nuovo esempio di input, l'EVR invia **un messaggio MFVP_MESSAGE_PROCESSINPUTNOTIFY** al presentatore. Questo messaggio indica che il mixer potrebbe avere un nuovo fotogramma video da distribuire. In risposta, il presentatore chiama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer. Se il metodo ha esito positivo, il presentatore pianifica l'esempio per la presentazione.

Per ottenere l'output dal mixer, seguire questa procedura:

1.  Controllare lo stato dell'orologio. Se l'orologio è in pausa, ignorare il **MFVP_MESSAGE_PROCESSINPUTNOTIFY** a meno che non si tratta del primo fotogramma video. Se l'orologio è in esecuzione o se si tratta del primo fotogramma video, continuare.
2.  Ottenere un esempio dalla coda di esempi disponibili. Se la coda è vuota, significa che tutti i campioni allocati sono attualmente pianificati per la presentazione. In questo caso, ignorare **il MFVP_MESSAGE_PROCESSINPUTNOTIFY** al momento. Quando l'esempio successivo diventa disponibile, ripetere i passaggi elencati qui.
3.  (Facoltativo). Se l'orologio è disponibile, ottenere l'ora corrente (*T1*) chiamando [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer. Se **ProcessOutput ha** esito positivo, l'esempio contiene un fotogramma video. Se il metodo ha esito negativo, controllare il codice restituito. I codici di errore seguenti **di ProcessOutput** non sono errori critici:

    

    | Codice di errore                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Il mixer necessita di più input prima di poter produrre un nuovo frame di output.<br/> Se si ottiene questo codice di errore, verificare se eVR ha raggiunto la fine del flusso e rispondere di conseguenza, come descritto in [Fine del flusso.](#end-of-stream) In caso contrario, ignorare **questo MF_E_TRANSFORM_NEED_MORE_INPUT** messaggio. L'EVR ne invierà un altro quando il mixer riceverà più input.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Il tipo di output del mixer non è più valido, probabilmente a causa di una modifica del formato upstream.<br/> Se si ottiene questo codice di errore, impostare il tipo di supporto del presentatore su **NULL.** L'EVR richiederà un nuovo formato.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Il mixer richiede un nuovo tipo di supporto.<br/> Se si ottiene questo codice di errore, rinegoziare il tipo di output del mixer come descritto in [Formati di negoziazione.](#negotiating-formats)<br/>                                                                                                                                                                                                        |

    

     

    Se [**ProcessOutput ha**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) esito positivo, continuare.

5.  (Facoltativo). Se l'orologio è disponibile, ottenere l'ora corrente (*T2*). La quantità di latenza introdotta dal mixer è (*T2*  -  *T1*). Inviare **un EC_PROCESSING_LATENCY** con questo valore all'EVR. L'EVR usa questo valore per il controllo di qualità. Se non è disponibile alcun orologio, non esiste alcun motivo per inviare **l'EC_PROCESSING_LATENCY** evento.
6.  (Facoltativo). Eseguire una query [**sull'esempio per IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) e chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) come descritto in [Esempi di rilevamento.](#tracking-samples)
7.  Pianificare l'esempio per la presentazione.

Questa sequenza di passaggi può terminare prima che il presentatore osceni l'output dal mixer. Per assicurarsi che nessuna richiesta sia eliminata, è necessario ripetere gli stessi passaggi quando si verificano le condizioni seguenti:

-   Viene chiamato il metodo [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink::OnClockStart** del presentatore. Viene gestito il caso in cui il mixer ignora l'input perché l'orologio è in pausa (passaggio 1).
-   Viene richiamato il callback [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) Questo gestisce il caso in cui il mixer riceve l'input, ma tutti gli esempi video del presentatore sono in uso (passaggio 2).

I diversi esempi di codice seguenti illustrano questi passaggi in modo più dettagliato. Il presentatore chiama `ProcessInputNotify` il metodo (illustrato nell'esempio seguente) quando ottiene il **MFVP_MESSAGE_PROCESSINPUTNOTIFY** messaggio.


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Questo `ProcessInputNotify` metodo imposta un flag booleano per registrare il fatto che il mixer ha un nuovo input. Chiama quindi il `ProcessOutputLoop` metodo , illustrato nell'esempio seguente. Questo metodo tenta di eseguire il pull del maggior numero possibile di campioni dal mixer:


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



Il `ProcessOutput` metodo , illustrato nell'esempio seguente, tenta di ottenere un singolo fotogramma video dal mixer. Se non è disponibile alcun fotogramma video, restituisce S_FALSE o un codice di errore, che interrompe `ProcessSample` il ciclo in `ProcessOutputLoop` . La maggior parte delle operazioni viene eseguita all'interno del `ProcessOutput` metodo :


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Alcune osservazioni su questo esempio:

-   La *m_SamplePool* si presuppone che sia un oggetto raccolta che contiene la coda di esempi video disponibili. Il metodo `GetSample` dell'oggetto restituisce **MF_E_SAMPLEALLOCATOR_EMPTY** se la coda è vuota.
-   Se il metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer restituisce MF_E_TRANSFORM_NEED_MORE_INPUT, significa che il mixer non può produrre altri output, quindi il presentatore *cancella il* flag m_fSampleNotify.
-   Il `TrackSample` metodo , che imposta il callback [**IMFTrackedSample,**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) è illustrato nella sezione Esempi [di rilevamento](#tracking-samples).

### <a name="repainting-frames"></a>Ridisegno di frame

In alcuni casi il presentatore potrebbe dover ridisegnare il fotogramma video più recente. Ad esempio, il presentatore standard ridisegna il frame nelle situazioni seguenti:

-   In modalità finestra, in risposta **WM_PAINT** messaggi ricevuti dalla finestra dell'applicazione. Vedere [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Se il rettangolo di destinazione cambia quando l'applicazione chiama [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Usare la procedura seguente per richiedere al mixer di creare nuovamente il frame più recente:

1.  Ottenere un video di esempio dalla coda.
2.  Eseguire una query sull'esempio per [**l'interfaccia IMFDesiredSample.**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)
3.  Chiamare [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Specificare il timestamp del fotogramma video più recente. È necessario memorizzare nella cache questo valore e aggiornarlo per ogni frame.
4.  Chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer.

Quando si ridisegna un frame, è possibile ignorare l'orologio della presentazione e presentarlo immediatamente.

### <a name="scheduling-samples"></a>Esempi di pianificazione

I fotogrammi video possono raggiungere l'EVR in qualsiasi momento. Il presentatore è responsabile della presentazione di ogni fotogramma all'ora corretta, in base al timestamp del fotogramma. Quando il presentatore ottiene un nuovo esempio dal mixer, inserisce l'esempio nella coda pianificata. In un thread separato, il presentatore ottiene continuamente il primo esempio dall'head della coda e determina se:

-   Presentare l'esempio.
-   Mantenere l'esempio nella coda perché è in anticipo.
-   Eliminare l'esempio perché è in ritardo. Anche se è consigliabile evitare di eliminare i frame, se possibile, potrebbe essere necessario se il presentatore continua a essere indietro.

Per ottenere il timestamp per un fotogramma video, chiamare [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) nell'esempio video. Il timestamp è relativo all'orologio di presentazione dell'EVR. Per ottenere l'ora dell'orologio corrente, chiamare [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Se l'EVR non dispone di un orologio di presentazione o se un campione non ha un timestamp, è possibile presentare l'esempio immediatamente dopo averlo visualizzato.

Per ottenere la durata di ogni esempio, chiamare [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Se l'esempio non ha una durata, è possibile usare la [**funzione MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) per calcolare la durata dalla frequenza dei fotogrammi.

Quando si pianificano gli esempi, tenere presente quanto segue:

-   Se la velocità di riproduzione è più veloce o più lenta della velocità normale, l'orologio viene eseguito a una velocità più veloce o più lenta. Ciò significa che il timestamp di un campione fornisce sempre l'ora di destinazione corretta rispetto all'orologio della presentazione. Tuttavia, se si traducono gli orari di presentazione in un'altra ora dell'orologio (ad esempio, il contatore delle prestazioni ad alta risoluzione), è necessario ridimensionare gli orari in base alla velocità dell'orologio. Se la velocità del clock cambia, l'EVR chiama il metodo [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del presentatore.
-   La velocità di riproduzione può essere negativa per la riproduzione inversa. Quando la velocità di riproduzione è negativa, l'orologio della presentazione viene eseguito all'indietro. In altre parole, il tempo *N* + 1 si verifica prima dell'ora *N*.

L'esempio seguente calcola quanto è in anticipo o in ritardo un campione rispetto all'orologio della presentazione:


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



L'orologio di presentazione è in genere guidato dall'orologio di sistema o dal renderer audio. Il renderer audio deriva il tempo dalla velocità con cui la scheda audio utilizza l'audio. In generale, l'orologio della presentazione non è sincronizzato con la frequenza di aggiornamento del monitoraggio.

Se i parametri di  presentazione Direct3D specificano D3DPRESENT_INTERVAL_DEFAULT o **D3DPRESENT_INTERVAL_ONE** per l'intervallo di presentazione, l'operazione Present attende il retrace verticale del monitoraggio.  Si tratta di un modo semplice per evitare la rimozione, ma riduce l'accuratezza dell'algoritmo di pianificazione. Al contrario, se l'intervallo di presentazione è D3DPRESENT_INTERVAL_IMMEDIATE , il metodo **Present** viene eseguito immediatamente, causando  la rimozione, a meno che l'algoritmo di pianificazione non sia sufficientemente accurato da chiamare **Present solo** durante il periodo di retrace verticale.

Le funzioni seguenti consentono di ottenere informazioni di temporizzazione accurate:

-   **IDirect3DDevice9::GetRasterStatus** restituisce informazioni sul raster, inclusa la riga di analisi corrente e se il raster si trova nel punto vuoto verticale.
-   **DwmGetCompositionTimingInfo restituisce** informazioni sull'intervallo per gestione finestre desktop. Queste informazioni sono utili se la composizione del desktop è abilitata.

### <a name="presenting-samples"></a>Presentazione di esempi

In questa sezione si presuppone che sia stata creata una catena di scambio separata per ogni superficie, come descritto in [Allocazione di superfici Direct3D](#allocating-direct3d-surfaces). Per presentare un esempio, ottenere la catena di scambio dall'esempio video come segue:

1.  Chiamare [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) nell'esempio video per ottenere il buffer.
2.  Eseguire una query sul buffer per [**l'interfaccia IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
3.  Chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere **l'interfaccia IDirect3DSurface9** della superficie Direct3D. È possibile combinare questo passaggio e il passaggio precedente in uno chiamando [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)
4.  Chiamare **IDirect3DSurface9::GetContainer** sulla superficie per ottenere un puntatore alla catena di scambio.
5.  Chiamare **IDirect3DSwapChain9::P resent** nella catena di scambio.

Il codice seguente illustra questi passaggi:


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Rettangoli di origine e destinazione

Il *rettangolo di* origine è la parte del fotogramma video da visualizzare. È definito rispetto a un sistema di coordinate normalizzato, in cui l'intero fotogramma video occupa un rettangolo con coordinate {0, 0, 1, 1}. Il *rettangolo di destinazione* è l'area all'interno della superficie di destinazione in cui viene disegnato il fotogramma video. Il presentatore standard consente a un'applicazione di impostare questi rettangoli chiamando [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Sono disponibili diverse opzioni per l'applicazione di rettangoli di origine e di destinazione. La prima opzione è consentire al mixer di applicarle:

-   Impostare il rettangolo di origine usando [**l'attributo VIDEO_ZOOM_RECT.**](video-zoom-rect-attribute.md) Il mixer applicherà il rettangolo di origine quando esegue il blits del video sulla superficie di destinazione. Il rettangolo di origine predefinito del mixer è l'intero frame.
-   Impostare il rettangolo di destinazione come apertura geometrica nel tipo di output del mixer. Per altre informazioni, vedere [Formati di negoziazione](#negotiating-formats).

La seconda opzione è applicare i rettangoli quando si **IDirect3DSwapChain9::P resent** specificando i parametri *pSourceRect* e *pDestRect* nel **metodo Present.** È possibile combinare queste opzioni. Ad esempio, è possibile impostare il rettangolo di origine nel mixer, ma applicare il rettangolo di destinazione nel **metodo** Present.

Se l'applicazione modifica il rettangolo di destinazione o ridimensiona la finestra, potrebbe essere necessario allocare nuove superfici. In tal caso, è necessario prestare attenzione a sincronizzare questa operazione con il thread di pianificazione. Scaricare la coda di pianificazione ed eliminare gli esempi precedenti prima di allocare nuove superfici.

### <a name="end-of-stream"></a>Fine del flusso

Al termine di ogni flusso di input nell'EVR, l'EVR invia **un** messaggio MFVP_MESSAGE_ENDOFSTREAM al presentatore. Al momento della ricezione del messaggio, tuttavia, potrebbero essere rimasti alcuni fotogrammi video da elaborare. Prima di rispondere al messaggio di fine flusso, è necessario svuotare tutto l'output dal mixer e presentare tutti i fotogrammi rimanenti. Dopo aver presentato l'ultimo frame, inviare **un EC_COMPLETE** evento all'EVR.

Nell'esempio seguente viene illustrato un metodo che invia **l'EC_COMPLETE** evento se vengono soddisfatte diverse condizioni. In caso contrario, restituisce S_OK senza inviare l'evento:


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Questo metodo controlla gli stati seguenti:

-   Se la *m_fSampleNotify* variabile **è TRUE,** significa che il mixer ha uno o più fotogrammi che non sono ancora stati elaborati. Per informazioni dettagliate, vedere [Elaborazione dell'output.](#processing-output)
-   La *m_fEndStreaming* è un flag booleano il cui valore iniziale **è FALSE.** Il presentatore imposta il flag su **TRUE** quando l'EVR invia il **MFVP_MESSAGE_ENDOFSTREAM** messaggio.
-   Si `AreSamplesPending` presuppone che il metodo restituirà **TRUE** purché uno o più frame siano in attesa nella coda pianificata.

Nel metodo [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) impostare *m_fEndStreaming* su **TRUE** e chiamare quando l'EVR invia il MFVP_MESSAGE_ENDOFSTREAM `CheckEndOfStream` messaggio: 


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Chiamare inoltre se il metodo `CheckEndOfStream` [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer restituisce **MF_E_TRANSFORM_NEED_MORE_INPUT**. Questo codice di errore indica che il mixer non ha altri esempi di input (vedere [Output di elaborazione](#processing-output)).

## <a name="frame-stepping"></a>Esecuzione di istruzioni per i frame

L'EVR è progettato per supportare il frame stepping DirectShow e lo scrubbing in Media Foundation. L'esecuzione di istruzioni e lo scrubbing dei fotogrammi sono concettualmente simili. In entrambi i casi, l'applicazione richiede un fotogramma video alla volta. Internamente, il presentatore usa lo stesso meccanismo per implementare entrambe le funzionalità.

L'esecuzione di istruzioni DirectShow fotogrammi funziona come segue:

-   L'applicazione chiama [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). Il numero di passaggi è specificato nel *parametro dwSteps.* L'EVR invia **MFVP_MESSAGE_STEP** messaggio al presentatore, dove il parametro del messaggio (*ulParam*) è il numero di passaggi.
-   Se l'applicazione chiama [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o modifica lo stato del grafo (in esecuzione, sospeso **o** arrestato), l'EVR invia un MFVP_MESSAGE_CANCELSTEP messaggio.

Lo scrubbing in Media Foundation funziona come segue:

-   L'applicazione imposta la velocità di riproduzione su zero chiamando [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).
-   Per eseguire il rendering di un nuovo frame, l'applicazione chiama [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione desiderata. L'EVR invia **MFVP_MESSAGE_STEP** messaggio con *ulParam* uguale a 1.
-   Per arrestare lo scrubbing, l'applicazione imposta la velocità di riproduzione su un valore diverso da zero. L'EVR invia il **MFVP_MESSAGE_CANCELSTEP** messaggio.

Dopo aver ricevuto **il MFVP_MESSAGE_STEP,** il presentatore attende l'arrivo del frame di destinazione. Se il numero di passaggi è *N,* il presentatore rimuove gli esempi successivi *(N* - 1) e presenta *l'esempio N.* Quando il presentatore completa il passaggio [](../directshow/ec-step-complete.md) del frame, invia un evento EC_STEP_COMPLETE all'EVR con *lParam1* impostato su **FALSE.** Inoltre, se la frequenza di riproduzione è zero, il presentatore invia un [**evento EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) registrazione. Se EVR annulla l'esecuzione istruzione/routine del frame mentre un'operazione del passaggio del frame è ancora in sospeso, il presentatore invia un evento **EC_STEP_COMPLETE** con *lParam1* impostato su **TRUE.**

L'applicazione può incorniciare il passaggio o  lo scrubbing più volte, in modo che il presentatore possa ricevere più messaggi MFVP_MESSAGE_STEP prima di ricevere un **MFVP_MESSAGE_CANCELSTEP** messaggio. Inoltre, il presentatore può ricevere il **messaggio MFVP_MESSAGE_STEP** prima dell'avvio dell'orologio o mentre l'orologio è in esecuzione.

### <a name="implementing-frame-stepping"></a>Implementazione dell'esecuzione di istruzioni dei frame

In questa sezione viene descritto un algoritmo per implementare l'esecuzione di istruzioni dei frame. L'algoritmo di esecuzione delle istruzioni dei frame usa le variabili seguenti:

-   *step_count*. Intero senza segno che specifica il numero di passaggi nell'operazione di esecuzione delle istruzioni del frame corrente.
-   *step_queue*. Coda di [**puntatori IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
-   *step_state*. In qualsiasi momento, il presentatore può essere in uno degli stati seguenti per quanto riguarda l'esecuzione di istruzioni nei frame: 

    | State         | Descrizione                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Non l'esecuzione di istruzioni nei frame.                                                                                                                                                                                             |
    | WAITING       | Il presentatore ha ricevuto il **messaggio MFVP_MESSAGE_STEP,** ma l'orologio non è stato avviato.                                                                                                                  |
    | PENDING       | Il presentatore ha ricevuto il **messaggio MFVP_MESSAGE_STEP** e l'orologio è stato avviato, ma il presentatore è in attesa di ricevere il frame di destinazione.                                                             |
    | PROGRAMMATO     | Il presentatore ha ricevuto il frame di destinazione e lo ha pianificato per la presentazione, ma il frame non è stato presentato.                                                                                        |
    | COMPLETO      | Il presentatore ha presentato il frame di destinazione e inviato l'evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) ed è in attesa del **messaggio** MFVP_MESSAGE_STEP o **MFVP_MESSAGE_CANCELSTEP** successivo. |

    

     

    Questi stati sono indipendenti dagli stati del presentatore elencati nella sezione [Stati del presentatore](#presenter-states).

Per l'algoritmo frame-stepping vengono definite le procedure seguenti:

Procedura PrepareFrameStep

1.  Incrementare *step_count*.
2.  Impostare *step_state* su WAITING.
3.  Se l'orologio è in esecuzione, chiamare StartFrameStep.

Procedura StartFrameStep

1.  Se *step_state* è uguale a WAITING, *impostare* step_state su PENDING. Per ogni esempio in *step_queue*, chiamare DeliverFrameStepSample.
2.  Se *step_state* è uguale NOT_STEPPING, rimuovere tutti gli esempi *step_queue* e pianificarli per la presentazione.

Procedura CompleteFrameStep

1.  Impostare *step_state* su COMPLETE.
2.  Inviare l EC_STEP_COMPLETE eventi con *lParam1*  =  **FALSE.**
3.  Se la frequenza di clock è zero, inviare **l'evento EC_SCRUB_TIME** con l'ora di esempio.

Procedura DeliverFrameStepSample

1.  Se la frequenza di clock è pari a zero e *la durata* del campione del campione  +  *di* esempio  <  *è ,* eliminare il campione. Exit.
2.  Se *step_state* è uguale a SCHEDULED o COMPLETE, aggiungere l'esempio *step_queue*. Exit.
3.  Decremento *step_count*.
4.  Se *step_count* > 0, eliminare l'esempio. Exit.
5.  Se *step_state* è uguale a WAITING, aggiungere l'esempio *a step_queue*. Exit.
6.  Pianificare l'esempio per la presentazione.
7.  Impostare *step_state* su SCHEDULED.

Procedura CancelFrameStep

1.  Impostare *step_state* su NOT_STEPPING
2.  Reimpostare *step_count* su zero.
3.  Se il valore precedente di *step_state* è WAITING, PENDING o SCHEDULED, inviare EC_STEP_COMPLETE *con lParam1*  =  **TRUE**.

Chiamare queste procedure nel modo seguente:



| Metodo o messaggio del presentatore                                                   | Procedura           |
|-------------------------------------------------------------------------------|---------------------|
| **MFVP_MESSAGE_STEP** messaggio                                               | `PrepareFrameStep`  |
| **MFVP_MESSAGE_STEP** messaggio                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| Callback [**di IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

Il diagramma di flusso seguente illustra le procedure per la creazione di passaggi di frame.

![Diagramma di flusso che mostra i percorsi che iniziano con mfvp \- message \- step e mfvp \- message \- processinputnotify e terminano con "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Impostazione del presentatore nell'EVR

Dopo aver implementato il presentatore, il passaggio successivo consiste nel configurare EVR per usarlo.

### <a name="setting-the-presenter-in-directshow"></a>Impostazione del presenter in DirectShow

In un DirectShow appaltatore impostare il presentatore nell'EVR come indicato di seguito:

1.  Creare il filtro EVR chiamando **CoCreateInstance.** Il CLSID è **CLSID_EnhancedVideoRenderer**.
2.  Aggiungere l'EVR al grafico dei filtri.
3.  Creare un'istanza del presentatore. Il presentatore può supportare la creazione di oggetti COM standard **tramite IClassFactory,** ma questo non è obbligatorio.
4.  Eseguire una query sul filtro EVR per [**l'interfaccia IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
5.  Chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

### <a name="setting-the-presenter-in-media-foundation"></a>Impostazione del presenter in Media Foundation

In Media Foundation sono disponibili diverse opzioni, a seconda che si crei il sink del supporto EVR o l'oggetto di attivazione EVR. Per altre informazioni sugli oggetti attivazione, vedere [Oggetti attivazione.](activation-objects.md)

Per il sink del supporto EVR, eseguire le operazioni seguenti:

1.  Chiamare [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) per creare il sink multimediale.
2.  Creare un'istanza del presentatore.
3.  Eseguire una query sul sink dei supporti EVR per [**l'interfaccia IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
4.  Chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

Per l'oggetto attivazione EVR, eseguire le operazioni seguenti:

1.  Chiamare [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione.
2.  Impostare uno degli attributi seguenti nell'oggetto attivazione: 

    | Attributo                                                                                                         | Descrizione                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Puntatore a un oggetto attivazione per il presentatore.<br/> Con questo flag, è necessario fornire un oggetto attivazione per il presentatore. L'oggetto attivazione deve implementare [**l'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID del presentatore.<br/> Con questo flag, il presentatore deve supportare la creazione di oggetti COM standard **tramite IClassFactory.**<br/>                                                                                         |

    

     

3.  Facoltativamente, impostare [**l'MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS'attributo**](mf-activate-custom-video-presenter-flags-attribute.md) nell'oggetto attivazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> <dt>

[Esempio di EVRPresenter](evrpresenter-sample.md)
</dt> </dl>

 

 
