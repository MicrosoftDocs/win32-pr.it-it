---
description: Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Come scrivere un presentatore EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556496"
---
# <a name="how-to-write-an-evr-presenter"></a>Come scrivere un presentatore EVR

Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR). Un presentatore personalizzato può essere usato sia con DirectShow che con Media Foundation; le interfacce e il modello a oggetti sono gli stessi per entrambe le tecnologie, sebbene la sequenza esatta di operazioni possa variare.

Il codice di esempio in questo argomento è stato adattato dall' [esempio EVRPresenter](evrpresenter-sample.md), fornito nella Windows SDK.

In questo argomento sono incluse le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Modello a oggetti Presenter](#presenter-object-model)
    -   [Flusso di dati all'interno di EVR](#data-flow-inside-the-evr)
    -   [Stati Presenter](#presenter-states)
    -   [Interfacce del Presenter](#presenter-interfaces)
    -   [Implementazione di IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [Implementazione di IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implementazione di IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [Implementazione di IMFClockStateSink](#implementing-imfclockstatesink)
    -   [Implementazione di IMFRateSupport](#implementing-imfratesupport)
    -   [Invio di eventi a EVR](#sending-events-to-the-evr)
-   [Formati di negoziazione](#negotiating-formats)
-   [Gestione del dispositivo Direct3D](#managing-the-direct3d-device)
    -   [Allocazione di superfici Direct3D](#allocating-direct3d-surfaces)
    -   [Esempi di rilevamento](#tracking-samples)
-   [Elaborazione dell'output](#processing-output)
    -   [Ridisegno di frame](#repainting-frames)
    -   [Esempi di pianificazione](#scheduling-samples)
    -   [Presentazione di esempi](#presenting-samples)
    -   [Rettangoli di origine e di destinazione](#source-and-destination-rectangles)
    -   [Fine del flusso](#end-of-stream)
-   [Esecuzione del frame](#frame-stepping)
    -   [Implementazione dell'esecuzione del frame](#implementing-frame-stepping)
-   [Impostazione del Presenter in EVR](#setting-the-presenter-on-the-evr)
    -   [Impostazione del Presenter in DirectShow](#setting-the-presenter-in-directshow)
    -   [Impostazione del Presenter in Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Prima di scrivere un presentatore personalizzato, è necessario avere familiarità con le tecnologie seguenti:

-   Renderer video migliorato. Vedere [renderer video migliorato](enhanced-video-renderer.md).
-   Grafica Direct3D. Non è necessario comprendere grafica 3D per scrivere un presentatore, ma è necessario sapere come creare un dispositivo Direct3D e gestire le superfici Direct3D. Se non si ha familiarità con Direct3D, vedere le sezioni "dispositivi Direct3D" e "risorse Direct3D" nella documentazione di DirectX Graphics SDK.
-   I grafici filtro DirectShow o la pipeline Media Foundation, a seconda della tecnologia che l'applicazione userà per eseguire il rendering del video.
-   [Media Foundation le trasformazioni](media-foundation-transforms.md). Il mixer EVR è una trasformazione Media Foundation e il Presenter chiama i metodi direttamente nel mixer.
-   Implementazione di oggetti COM. Presenter è un oggetto COM in-process a thread libero.

## <a name="presenter-object-model"></a>Modello a oggetti Presenter

Questa sezione contiene una panoramica del modello a oggetti Presenter e delle interfacce.

### <a name="data-flow-inside-the-evr"></a>Flusso di dati all'interno di EVR

EVR usa due componenti plug-in per il rendering del video: il *mixer* e il *presentatore*. Il mixer combina i flussi video e li Deinterlaccia se necessario. Il presentatore disegna (o *presenta*) il video sulla visualizzazione e pianifica quando viene disegnato ogni frame. Le applicazioni possono sostituire uno di questi oggetti con un'implementazione personalizzata.

Il EVR ha uno o più flussi di input e il mixer ha un numero corrispondente di flussi di input. Il flusso 0 è sempre il *flusso di riferimento*. Gli altri flussi sono *sottoflussi*, che il mixer Alpha-Blend nel flusso di riferimento. Il flusso di riferimento determina la frequenza dei fotogrammi master per il video composito. Per ogni fotogramma di riferimento, il mixer acquisisce il frame più recente da ogni sottoflusso, alfa li combina nel frame di riferimento e restituisce un singolo frame composito. Se necessario, il mixer esegue anche il deinterlacciamento e la conversione dei colori da YUV a RGB. Il EVR inserisce sempre il mixer nella pipeline video, indipendentemente dal numero di flussi di input o dal formato video. Questo processo è illustrato nella figura seguente.

![diagramma che mostra il flusso di riferimento e il sottoflusso che punta al mixer, che punta al Presenter, che punta alla visualizzazione](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Il Presenter esegue le attività seguenti:

-   Imposta il formato di output sul mixer. Prima dell'inizio del flusso, il relatore imposta un tipo di supporto nel flusso di output del mixer. Questo tipo di supporto definisce il formato dell'immagine composita.
-   Crea il dispositivo Direct3D.
-   Alloca superfici Direct3D. Il mixer Blits i frame compositi su queste superfici.
-   Ottiene l'output dal mixer.
-   Pianifica quando vengono presentati i frame. EVR fornisce il clock di presentazione e il Presenter Pianifica i frame in base a questo orologio.
-   Presenta ogni fotogramma usando Direct3D.
-   Esegue l'avanzamento e lo scrubbing del frame.

### <a name="presenter-states"></a>Stati Presenter

In qualsiasi momento, il Presenter si trova in uno degli Stati seguenti:

-   *Avviato*. Il clock di presentazione di EVR è in esecuzione. Il presentatore Pianifica i fotogrammi video per la presentazione all'arrivo.
-   In *pausa*. Il clock di presentazione è sospeso. Il Presenter non presenta nuovi esempi, ma mantiene la coda degli esempi pianificati. Se vengono ricevuti nuovi esempi, il relatore li aggiunge alla coda.
-   *Arrestato*. Il clock di presentazione è stato arrestato. Il relatore elimina tutti gli esempi pianificati.
-   *Arrestare*. Il Presenter rilascia tutte le risorse correlate al flusso, ad esempio le superfici Direct3D. Si tratta dello stato iniziale del presentatore e dello stato finale prima che il Presenter venga eliminato definitivamente.

Nel codice di esempio riportato in questo argomento lo stato del relatore è rappresentato da un'enumerazione:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Alcune operazioni non sono valide quando il Presenter è nello stato di arresto. Il codice di esempio controlla questo stato chiamando un metodo helper:


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



### <a name="presenter-interfaces"></a>Interfacce del Presenter

È necessario un presentatore per implementare le interfacce seguenti:



| Interfaccia                                                                | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Notifica al presentatore quando cambia lo stato dell'orologio del EVR. Vedere [implementazione di IMFClockStateSink](#implementing-imfclockstatesink).                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Fornisce un modo per l'applicazione e altri componenti nella pipeline di ottenere le interfacce dal presentatore.                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Consente al presentatore di ottenere le interfacce da EVR o dal mixer. Vedere [implementazione di IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient). |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Garantisce che il Presenter e il mixer usino tecnologie compatibili. Vedere [implementazione di IMFVideoDeviceID](#implementing-imfvideodeviceid).                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Elabora i messaggi dal EVR. Vedere [implementazione di IMFVideoPresenter](#implementing-imfvideopresenter).                                                             |



 

Le interfacce seguenti sono facoltative:



| Interfaccia                                                | Descrizione                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Consente al Presenter di utilizzare supporti protetti. Implementare questa interfaccia se il relatore è un componente attendibile progettato per funzionare nel percorso del supporto protetto (PMP). |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Segnala l'intervallo di velocità di riproduzione supportato dal Presenter. Vedere [implementazione di IMFRateSupport](#implementing-imfratesupport).                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Esegue il mapping delle coordinate del fotogramma video di output alle coordinate del fotogramma video di input.                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Segnala le informazioni sulle prestazioni. Il EVR usa queste informazioni per la gestione del controllo di qualità. Questa interfaccia è documentata in DirectShow SDK.                        |



 

È inoltre possibile fornire interfacce che consentono all'applicazione di comunicare con il relatore. Il presentatore standard implementa l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) a questo scopo. È possibile implementare questa interfaccia o definirne una personalizzata. L'applicazione ottiene le interfacce dal Presenter chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in EVR. Quando il GUID del servizio è **MR_VIDEO_RENDER_SERVICE**, il EVR passa la richiesta **GetService** al Presenter.

### <a name="implementing-imfvideodeviceid"></a>Implementazione di IMFVideoDeviceID

L'interfaccia [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un metodo, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), che restituisce un GUID del dispositivo. Il GUID del dispositivo garantisce che il relatore e il mixer usino tecnologie compatibili. Se i GUID del dispositivo non corrispondono, l'inizializzazione di EVR non riesce.

Il mixer e il Presenter standard usano entrambi Direct3D 9, con il GUID del dispositivo uguale a **IID_IDirect3DDevice9**. Se si intende usare il Presenter personalizzato con il mixer standard, il GUID del dispositivo del relatore deve essere **IID_IDirect3DDevice9**. Se si sostituiscono entrambi i componenti, è possibile definire un nuovo GUID del dispositivo. Nella parte restante di questo articolo si presuppone che il relatore usi Direct3D 9. Di seguito è illustrata l'implementazione standard di [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):


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



Il metodo deve avere esito positivo anche quando il Presenter viene arrestato.

### <a name="implementing-imftopologyservicelookupclient"></a>Implementazione di IMFTopologyServiceLookupClient

L'interfaccia [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) consente al presentatore di ottenere i puntatori di interfaccia da EVR e dal mixer come indicato di seguito:

1.  Quando EVR Inizializza il presentatore, chiama il metodo [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del Presenter. L'argomento è un puntatore all'interfaccia [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) di EVR.
2.  Il Presenter chiama [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) per ottenere i puntatori di interfaccia da EVR o dal mixer.

Il metodo [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) è simile al metodo [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Entrambi i metodi accettano un GUID del servizio e un identificatore di interfaccia (IID) come input, ma **LookupService** restituisce una matrice di puntatori di interfaccia, mentre **GetService** restituisce un solo puntatore. In pratica, tuttavia, è sempre possibile impostare la dimensione della matrice su 1. L'oggetto sottoposto a query dipende dal GUID del servizio:

-   Se il GUID del servizio è **MR_VIDEO_RENDER_SERVICE**, viene eseguita una query su EVR.
-   Se il GUID del servizio è **MR_VIDEO_MIXER_SERVICE**, viene eseguita una query sul mixer.

Nell'implementazione di [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), ottenere le interfacce seguenti da EVR:



| Interfaccia EVR                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Fornisce un modo per il relatore per inviare messaggi a EVR. Questa interfaccia è definita in DirectShow SDK, quindi i messaggi seguono il modello per gli eventi DirectShow, non Media Foundation gli eventi.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Rappresenta l'orologio del EVR. Il Presenter usa questa interfaccia per pianificare esempi per la presentazione. EVR può essere eseguito senza un clock, quindi questa interfaccia potrebbe non essere disponibile. In caso contrario, ignorare il codice di errore di [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> Il clock implementa anche l'interfaccia [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) . Nella pipeline Media Foundation il clock implementa l'interfaccia [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) . Questa interfaccia non viene implementata in DirectShow.<br/> |



 

Ottenere le interfacce seguenti dal mixer:



| Interfaccia mixer                              | Descrizione                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Consente al presentatore di comunicare con il mixer.       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Consente al presentatore di convalidare il GUID del dispositivo del mixer. |



 

Il codice seguente implementa il metodo [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


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



Quando i puntatori di interfaccia ottenuti da [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) non sono più validi, EVR chiama [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). All'interno di questo metodo rilasciare tutti i puntatori a interfaccia e impostare lo stato del relatore su Arresta:


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



EVR chiama [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) per vari motivi, tra cui:

-   Disconnessione o riconnessione di pin (DirectShow) o aggiunta o rimozione di sink di flusso (Media Foundation).
-   Modifica del formato.
-   Impostazione di un nuovo Clock.
-   Arresto finale del EVR.

Nel corso della durata del Presenter, il EVR potrebbe chiamare [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) più volte.

### <a name="implementing-imfvideopresenter"></a>Implementazione di IMFVideoPresenter

L'interfaccia [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) eredita [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e aggiunge due metodi:



| Metodo                                                               | Descrizione                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Restituisce il tipo di supporto dei fotogrammi video compositi. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Segnala al presentatore di eseguire varie azioni.      |



 

Il metodo [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) restituisce il tipo di supporto del relatore. Per informazioni dettagliate sull'impostazione del tipo di supporto, vedere la pagina relativa ai [formati di negoziazione](#negotiating-formats). Il tipo di supporto viene restituito come puntatore di interfaccia [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) . Nell'esempio seguente si presuppone che il relatore memorizzi il tipo di supporto come puntatore [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Per ottenere l'interfaccia **IMFVideoMediaType** dal tipo di supporto, chiamare **QueryInterface**:


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



Il metodo [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) è il meccanismo principale per la comunicazione tra EVR e il presentatore. Vengono definiti i messaggi seguenti. Nella parte restante di questo argomento vengono forniti i dettagli dell'implementazione di ogni messaggio.



| Message                                | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Il tipo di supporto di output del mixer non è valido. Il relatore deve negoziare un nuovo tipo di supporto con il mixer. Vedere la pagina relativa ai [formati di negoziazione](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Il flusso è stato avviato. Non è richiesta alcuna azione specifica da questo messaggio, ma è possibile utilizzarla per allocare le risorse.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | Il flusso è terminato. Rilasciare tutte le risorse allocate in risposta al messaggio di **MFVP_MESSAGE_BEGINSTREAMING** .                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Il mixer ha ricevuto un nuovo esempio di input e potrebbe essere in grado di generare un nuovo frame di output. Il Presenter deve chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer. Vedere [elaborazione dell'output](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | La presentazione è terminata. Vedere [la fine del flusso](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | EVR sta scaricando i dati nella relativa pipeline di rendering. Il relatore deve rimuovere tutti i fotogrammi video pianificati per la presentazione.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Richiede al presentatore di procedere con l'esecuzione di N frame. Il relatore deve rimuovere i frame N-1 successivi e visualizzare il frame ennesimo. Vedere [esecuzione del frame](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Annulla l'esecuzione del frame.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementazione di IMFClockStateSink

Il Presenter deve implementare l'interfaccia [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) come parte dell'implementazione di [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), che eredita **IMFClockStateSink**. EVR usa questa interfaccia per notificare al Presenter ogni volta che l'orologio del EVR cambia stato. Per altre informazioni sugli stati di clock, vedere [clock di presentazione](presentation-clock.md).

Di seguito sono riportate alcune linee guida per l'implementazione dei metodi in questa interfaccia. Tutti i metodi devono avere esito negativo se il Presenter viene arrestato.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>Impostare lo stato del relatore su avviato.</li>
<li>Se il <em>llClockStartOffset</em> non è <strong>PRESENTATION_CURRENT_POSITION</strong>, svuotare la coda degli esempi del relatore. Equivale alla ricezione di un messaggio di <strong>MFVP_MESSAGE_FLUSH</strong> .</li>
<li>Se una richiesta precedente di un passaggio del frame è ancora in sospeso, elaborare la richiesta (vedere <a href="#frame-stepping">esecuzione del frame</a>). In caso contrario, provare a elaborare l'output dal mixer. vedere <a href="#processing-output">elaborazione dell'output</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>Impostare lo stato del relatore su arrestato.</li>
<li>Scarica la coda degli esempi del relatore.</li>
<li>Annulla tutte le operazioni in sospeso nel passaggio del frame.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>Impostare lo stato del relatore su sospeso.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>Considerare lo stesso <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> , ma non scaricare la coda degli esempi.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>Se la frequenza è cambiata da zero a diverso da zero, annullare l'esecuzione del frame.</li>
<li>Archiviare la nuova frequenza di clock. La frequenza di clock influiscono sui casi in cui vengono presentati gli esempi. Per ulteriori informazioni, vedere la pagina relativa agli <a href="#scheduling-samples">esempi di pianificazione</a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implementazione di IMFRateSupport

Per supportare frequenze di riproduzione diverse dalla velocità di 1 ×, il relatore deve implementare l'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) . Di seguito sono riportate alcune linee guida per l'implementazione dei metodi in questa interfaccia. Tutti i metodi dovrebbero avere esito negativo dopo l'arresto del Presenter. Per altre informazioni su questa interfaccia, vedere [controllo della frequenza](rate-control.md).



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Restituisce zero per indicare una frequenza di riproduzione minima.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Per la riproduzione non diluita, la velocità di riproduzione non deve superare la frequenza di aggiornamento del monitoraggio: frequenza di aggiornamento *velocità massima*  =   (Hz)/ *frequenza dei fotogrammi video* (fps). La frequenza dei fotogrammi video è specificata nel tipo di supporto del relatore. <br/> Per la riproduzione diluita, la velocità di riproduzione non è vincolata; Restituisce il valore **FLT_MAX**. In pratica, l'origine e il decodificatore saranno i fattori che limitano la riproduzione. <br/> Per la riproduzione inversa, restituisce il valore negativo della frequenza massima.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Restituisce **MF_E_UNSUPPORTED_RATE** se il valore assoluto di *flRate* supera la frequenza massima di riproduzione del relatore. Calcolare la velocità di riproduzione massima come descritto per [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).                                                                                                                                                                                                                                                                                    |



 

Nell'esempio seguente viene illustrato come implementare il metodo [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :


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



Nell'esempio precedente viene chiamato un metodo helper, GetMaxRate, per calcolare la velocità massima di riproduzione in un secondo periodo:

Nell'esempio seguente viene illustrato come implementare il metodo [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :


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



### <a name="sending-events-to-the-evr"></a>Invio di eventi a EVR

Il relatore deve notificare il EVR di vari eventi. A tale scopo, usa l'interfaccia [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) di EVR, ottenuta quando EVR chiama il metodo [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del Presenter. (L'interfaccia **IMediaEventSink** è in origine un'interfaccia DirectShow, ma viene usata sia in DirectShow EVR che in Media Foundation). Il codice seguente illustra come inviare un evento a EVR:


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



La tabella seguente elenca gli eventi inviati dal Presenter, insieme ai parametri dell'evento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Event</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>Il relatore ha completato il rendering di tutti i frame dopo il MFVP_MESSAGE_ENDOFSTREAM messaggio.<br/>
<ul>
<li><em>Param1</em>: HRESULT che indica lo stato dell'operazione.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul>
Per ulteriori informazioni, vedere la <a href="#end-of-stream">fine del flusso</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>Il dispositivo Direct3D è stato modificato.<br/>
<ul>
<li><em>Param1</em>: non utilizzato.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul>
Per ulteriori informazioni, vedere <a href="#managing-the-direct3d-device">gestione del dispositivo Direct3D</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Si è verificato un errore che richiede l'arresto del flusso.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT</strong> che indica l'errore che si è verificato.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Specifica la quantità di tempo che il Presenter sta prendendo per eseguire il rendering di ogni fotogramma. Facoltativo.<br/>
<ul>
<li><em>Param1</em>: puntatore a un valore costante di <strong>LONGLONG</strong> che contiene la quantità di tempo per l'elaborazione del frame, in unità di 100 nanosecondi.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul>
Per ulteriori informazioni, vedere <a href="#processing-output">elaborazione dell'output</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Specifica il tempo di ritardo corrente negli esempi di rendering. Se il valore è positivo, gli esempi sono dietro la pianificazione. Se il valore è negativo, gli esempi sono avanti rispetto alla pianificazione. Facoltativo.<br/>
<ul>
<li><em>Param1</em>: puntatore a un valore costante di <strong>LONGLONG</strong> che contiene il tempo di ritardo, in unità di 100 nanosecondi.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Inviato immediatamente dopo <strong>EC_STEP_COMPLETE</strong> se la velocità di riproduzione è zero. Questo evento contiene l'indicatore di data e ora del frame visualizzato.<br/>
<ul>
<li><em>Param1</em>: 32 bit inferiori del timestamp.</li>
<li><em>Param2</em>: 32 bit superiori del timestamp.</li>
</ul>
Per altre informazioni, vedere <a href="#frame-stepping">esecuzione del frame</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>Il presentatore ha completato o annullato un passaggio del frame.<br/>
<ul>
<li><em>Param1</em>: non utilizzato.</li>
<li><em>Param2</em>: non utilizzato.</li>
</ul>
Per altre informazioni, vedere <a href="#frame-stepping">esecuzione del frame</a>.<br/>
<blockquote>
[!Note]<br />
Una versione precedente della documentazione descrive <em>param1</em> in modo errato. Questo parametro non viene utilizzato per questo evento.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Formati di negoziazione

Ogni volta che il Presenter riceve un messaggio di **MFVP_MESSAGE_INVALIDATEMEDIATYPE** da EVR, deve impostare il formato di output nel mixer, come indicato di seguito:

1.  Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) nel mixer per ottenere un possibile tipo di output. Questo tipo descrive un formato che il mixer può produrre dato i flussi di input e le funzionalità di elaborazione video del dispositivo grafico.
2.  Controllare se il Presenter può utilizzare questo tipo di supporto come formato di rendering. Di seguito sono riportati alcuni aspetti da verificare, anche se l'implementazione potrebbe avere requisiti specifici:

    -   Il video deve essere decompresso.
    -   Il video deve contenere solo frame progressivi. Verificare che l'attributo [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) sia uguale a **MFVideoInterlace_Progressive**.
    -   Il formato deve essere compatibile con il dispositivo Direct3D.

    Se il tipo non è accettabile, tornare al passaggio 1 e ottenere il tipo proposto successivo del mixer.

3.  Creare un nuovo tipo di supporto che sia un clone del tipo originale, quindi modificare gli attributi seguenti:

    -   Impostare l'attributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) uguale alla larghezza e all'altezza desiderate per le superfici Direct3D che si desidera allocare.
    -   Impostare l'attributo [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) su **false**.
    -   Impostare l'attributo [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) uguale alla par dello schermo (in genere 1:1).
    -   Impostare l'apertura geometrica (attributo [**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) ) uguale a un rettangolo all'interno della superficie Direct3D. Quando il mixer genera un frame di output, Blits l'immagine di origine su questo rettangolo. Il diaframma geometrico può essere di grandi dimensioni della superficie oppure può essere un sottorettangolo all'interno della superficie. Per altre informazioni, vedere [rettangoli di origine e di destinazione](#source-and-destination-rectangles).

4.  Per verificare se il mixer accetterà il tipo di output modificato, chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con il flag **MFT_SET_TYPE_TEST_ONLY** . Se il mixer rifiuta il tipo, tornare al passaggio 1 e ottenere il tipo successivo.
5.  Allocare un pool di superfici Direct3D, come descritto in [allocazione di superfici Direct3D](#allocating-direct3d-surfaces). Il mixer utilizzerà queste superfici quando disegna i fotogrammi video compositi.
6.  Impostare il tipo di output sul mixer chiamando [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) senza flag. Se la prima chiamata a **SetOutputType** ha avuto esito positivo nel passaggio 4, il metodo dovrebbe riuscire.

Se il mixer esaurisce i tipi, il metodo [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) restituisce **MF_E_NO_MORE_TYPES**. Se il presentatore non riesce a trovare un tipo di output adatto per il mixer, non è possibile eseguire il rendering del flusso. In tal caso, è possibile che DirectShow o Media Foundation provi a usare un altro formato di flusso. Il Presenter potrebbe pertanto ricevere diversi messaggi di **MFVP_MESSAGE_INVALIDATEMEDIATYPE** in una riga fino a quando non viene trovato un tipo valido.

Il mixer esegue automaticamente il letterboxing del video, prendendo in considerazione le proporzioni in pixel (PAR) dell'origine e della destinazione. Per ottenere risultati ottimali, la larghezza e l'altezza della superficie e l'apertura geometrica devono essere uguali alle dimensioni effettive che si desidera che il video venga visualizzato sullo schermo. Questo processo è illustrato nella figura seguente.

![diagramma che mostra un Fram composto che conduce a una superficie Direct3D, che conduce a una finestra](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

Nel codice seguente viene illustrata la struttura del processo. Alcuni passaggi sono posizionati in funzioni helper, i cui dettagli esatti dipendono dai requisiti del Presenter.


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



Per ulteriori informazioni sui tipi di supporti video, vedere [tipi di supporti video](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Gestione del dispositivo Direct3D

Il relatore crea il dispositivo Direct3D e gestisce eventuali perdite di dispositivi durante il flusso. Il Presenter ospita anche gestione dispositivi Direct3D, che consente ad altri componenti di usare lo stesso dispositivo. Ad esempio, il mixer usa il dispositivo Direct3D per combinare sottoflussi, deinterlacciare ed eseguire regolazioni dei colori. I decodificatori possono usare il dispositivo Direct3D per la decodifica video accelerata. (Per altre informazioni sull'accelerazione video, vedere [accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)).

Per configurare il dispositivo Direct3D, seguire questa procedura:

1.  Creare l'oggetto Direct3D chiamando **Direct3DCreate9** o **Direct3DCreate9Ex**.
2.  Creare il dispositivo chiamando **IDirect3D9:: CreateDevice** o **IDirect3D9Ex:: CreateDevice**.
3.  Creare Gestione dispositivi chiamando [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Impostare il dispositivo su Gestione dispositivi chiamando [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Se un altro componente della pipeline necessita di gestione dispositivi, viene chiamato [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in EVR, specificando **MR_VIDEO_ACCELERATION_SERVICE** per il GUID del servizio. Il EVR passa la richiesta al Presenter. Dopo che l'oggetto ha ottenuto il puntatore [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , può ottenere un handle per il dispositivo chiamando [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Quando l'oggetto deve usare il dispositivo, passa l'handle del dispositivo al metodo [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , che restituisce un puntatore **IDirect3DDevice9** .

Dopo la creazione del dispositivo, se il relatore elimina il dispositivo e ne crea uno nuovo, il relatore deve chiamare nuovamente [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) . Il metodo **ResetDevice** invalida qualsiasi handle di dispositivo esistente, che fa sì che [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) restituisca **DXVA2_E_NEW_VIDEO_DEVICE**. Questo codice di errore segnala ad altri oggetti che usano il dispositivo di aprire un nuovo handle di dispositivo. Per ulteriori informazioni sull'utilizzo di gestione dispositivi, vedere [Direct3D gestione dispositivi](direct3d-device-manager.md).

Il presentatore può creare il dispositivo in modalità a finestra o in modalità esclusiva a schermo intero. Per la modalità finestra, è necessario fornire un modo per consentire all'applicazione di specificare la finestra del video. Il Presenter standard implementa il metodo [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) a questo scopo. È necessario creare il dispositivo quando il Presenter viene creato per la prima volta. In questo momento non si conoscono tutti i parametri del dispositivo, ad esempio la finestra o il formato del buffer nascosto. È possibile creare un dispositivo temporaneo e sostituirlo in un secondo momento&\# ; è sufficiente ricordare di chiamare [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) in gestione dispositivi.

Se si crea un nuovo dispositivo o si chiama **IDirect3DDevice9:: Reset** o **IDirect3DDevice9Ex:: ResetEx** in un dispositivo esistente, inviare un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) a EVR. Questo evento notifica a EVR di rinegoziare il tipo di supporto. EVR ignora i parametri evento per questo evento.

### <a name="allocating-direct3d-surfaces"></a>Allocazione di superfici Direct3D

Quando il relatore imposta il tipo di supporto, può allocare le superfici Direct3D, che verrà usata dal mixer per scrivere i fotogrammi video. La superficie deve corrispondere al tipo di supporto del relatore:

-   Il formato della superficie deve corrispondere al sottotipo di supporto. Se, ad esempio, il sottotipo è **MFVideoFormat_RGB24**, il formato della superficie deve essere **D3DFMT_X8R8G8B8**. Per altre informazioni sui sottotipi e i formati Direct3D, vedere [GUID del sottotipo video](video-subtype-guids.md).
-   La larghezza e l'altezza della superficie devono corrispondere alle dimensioni specificate nell'attributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) del tipo di supporto.

Il modo consigliato per allocare le superfici dipende dal fatto che il Presenter venga eseguito a finestra o a schermo intero.

Se il dispositivo Direct3D è a finestra, è possibile creare diverse catene di scambio, ognuna con un singolo buffer nascosto. Utilizzando questo approccio, è possibile presentare ogni superficie in modo indipendente, perché la presentazione di una catena di scambio non interferisce con le altre catene di scambio. Il mixer può scrivere dati in una superficie mentre è pianificata un'altra superficie per la presentazione.

Per prima cosa, decidere il numero di catene di scambio da creare. È consigliabile un minimo di tre. Per ogni catena di scambio, procedere come segue:

1.  Chiamare **IDirect3DDevice9:: CreateAdditionalSwapChain** per creare la catena di scambio.
2.  Chiamare **IDirect3DSwapChain9:: GetBackBuffer** per ottenere un puntatore alla superficie del buffer indietro della catena di scambio.
3.  Chiamare [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) e passare un puntatore alla superficie. Questa funzione restituisce un puntatore a un oggetto video di esempio. L'oggetto di esempio video implementa l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e il Presenter usa questa interfaccia per distribuire la superficie al mixer quando il Presenter chiama il metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer. Per ulteriori informazioni sull'oggetto di esempio video, vedere [esempi video](video-samples.md).
4.  Archiviare il puntatore [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una coda. Il relatore eseguirà il pull degli esempi da questa coda durante l'elaborazione come descritto in [elaborazione dell'output](#processing-output).
5.  Mantiene un riferimento al puntatore **IDirect3DSwapChain9** in modo che la catena di scambio non venga rilasciata.

In modalità esclusiva a schermo intero, il dispositivo non può avere più di una catena di scambio. Questa catena di scambio viene creata in modo implicito quando si crea il dispositivo a schermo intero. La catena di scambio può avere più di un buffer nascosto. Sfortunatamente, tuttavia, se si presenta un buffer nascosto quando si scrive in un altro buffer nascosto nella stessa catena di scambio, non esiste un modo semplice per coordinare le due operazioni. Questo è dovuto al modo in cui Direct3D implementa il capovolgimento della superficie. Quando si chiama present, il driver di grafica aggiorna i puntatori alla superficie nella memoria grafica. Se si mantengono i puntatori **IDirect3DSurface9** quando si chiama **present**, questi punteranno a buffer diversi dopo la restituzione della chiamata **corrente** .

L'opzione più semplice consiste nel creare un esempio video per la catena di scambio. Se si sceglie questa opzione, attenersi alla stessa procedura indicata per la modalità con finestra. L'unica differenza è che la coda di esempio contiene un singolo esempio di video. Un'altra opzione consiste nel creare superfici Offscreen e quindi blit nel buffer nascosto. Le superfici create devono supportare il metodo [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , usato dal mixer per comporre i frame di output.

### <a name="tracking-samples"></a>Esempi di rilevamento

Quando il Presenter alloca prima di tutto gli esempi video, li inserisce in una coda. Il presentatore disegna da questa coda ogni volta che è necessario ottenere un nuovo frame dal mixer. Quando il mixer restituisce il frame, il relatore sposta l'esempio in una seconda coda. La seconda coda è destinata ad esempi in attesa dell'ora di presentazione pianificata.

Per semplificare la traccia dello stato di ogni esempio, l'oggetto video di esempio implementa l'interfaccia [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . È possibile usare questa interfaccia come indicato di seguito:

1.  Implementare l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) nel relatore.
2.  Prima di inserire un campione nella coda pianificata, eseguire una query sull'oggetto video di esempio per l'interfaccia [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .

3.  Chiamare [**IMFTrackedSample:: Seallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntatore all'interfaccia di callback.
4.  Quando l'esempio è pronto per la presentazione, rimuoverlo dalla coda pianificata, presentarlo e rilasciare tutti i riferimenti all'esempio.
5.  Nell'esempio viene richiamato il callback. L'oggetto di esempio non viene eliminato in questo caso, perché include un conteggio dei riferimenti su se stesso fino a quando non viene richiamato il callback.
6.  All'interno del callback, restituire l'esempio alla coda disponibile.

Non è necessario un presentatore per usare [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) per tenere traccia degli esempi; è possibile implementare qualsiasi tecnica che funzioni meglio per la progettazione. Un vantaggio di **IMFTrackedSample** è che è possibile spostare le funzioni di pianificazione e rendering del relatore in oggetti helper e questi oggetti non necessitano di alcun meccanismo speciale per richiamare il presentatore quando rilasciano esempi video perché l'oggetto di esempio fornisce tale meccanismo.

Nel codice seguente viene illustrato come impostare il callback:


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



Nel callback, chiamare [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) sull'oggetto risultato asincrono per recuperare un puntatore all'esempio:


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

    /*** Begin lock **_/

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

    /_*_ End lock _*_/

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

Ogni volta che il mixer riceve un nuovo esempio di input, EVR Invia un messaggio _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY** al Presenter. Questo messaggio indica che il mixer potrebbe avere un nuovo fotogramma video da recapitare. In risposta, il Presenter chiama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer. Se il metodo ha esito positivo, il relatore pianifica l'esempio per la presentazione.

Per ottenere l'output dal mixer, seguire questa procedura:

1.  Controllare lo stato dell'orologio. Se il clock è sospeso, ignorare il messaggio di **MFVP_MESSAGE_PROCESSINPUTNOTIFY** a meno che non si tratti del primo fotogramma video. Se il clock è in esecuzione o se è il primo fotogramma video, continuare.
2.  Ottenere un esempio dalla coda degli esempi disponibili. Se la coda è vuota, significa che tutti gli esempi allocati sono attualmente pianificati per la presentazione. In tal caso, ignorare il messaggio di **MFVP_MESSAGE_PROCESSINPUTNOTIFY** al momento. Quando l'esempio successivo diventa disponibile, ripetere i passaggi elencati di seguito.
3.  (Facoltativo). Se l'orologio è disponibile, ottenere l'ora dell'orologio corrente (*T1*) chiamando [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer. Se **ProcessOutput** ha esito positivo, l'esempio contiene un frame video. Se il metodo ha esito negativo, controllare il codice restituito. I codici di errore seguenti di **ProcessOutput** non sono errori critici:

    

    | Codice di errore                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Il mixer necessita di un maggiore input prima che possa produrre un nuovo frame di output.<br/> Se si ottiene questo codice di errore, controllare se il EVR ha raggiunto la fine del flusso e rispondere di conseguenza, come descritto alla [fine del flusso](#end-of-stream). In caso contrario, ignorare questo messaggio **MF_E_TRANSFORM_NEED_MORE_INPUT** . Il EVR invierà un altro oggetto quando il mixer otterrà un maggiore input.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Il tipo di output del mixer è diventato non valido, probabilmente a causa di una modifica del formato upstream.<br/> Se si ottiene questo codice di errore, impostare il tipo di supporto del relatore su **null**. Il EVR richiederà un nuovo formato.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Il mixer richiede un nuovo tipo di supporto.<br/> Se si ottiene questo codice di errore, rinegoziare il tipo di output del mixer come descritto in [formati di negoziazione](#negotiating-formats).<br/>                                                                                                                                                                                                        |

    

     

    Se [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ha esito positivo, continuare.

5.  (Facoltativo). Se l'orologio è disponibile, ottenere l'ora dell'orologio corrente (*T2*). La quantità di latenza introdotta dal mixer è (*T2*  -  *T1*). Inviare un evento **EC_PROCESSING_LATENCY** con questo valore a EVR. EVR utilizza questo valore per il controllo qualità. Se non è disponibile alcun clock, non esiste alcun motivo per inviare l'evento **EC_PROCESSING_LATENCY** .
6.  (Facoltativo). Eseguire una query sull'esempio per [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) e chiamare [**IMFTrackedSample:: seallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) come descritto in [Tracking Samples](#tracking-samples).
7.  Pianificare l'esempio per la presentazione.

Questa sequenza di passaggi può terminare prima che il relatore ottenga qualsiasi output dal mixer. Per assicurarsi che nessuna richiesta venga eliminata, è necessario ripetere gli stessi passaggi quando si verifica quanto segue:

-   Viene chiamato il metodo [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink:: OnClockStart** del relatore. Questo consente di gestire il caso in cui il mixer ignora l'input perché il clock è sospeso (passaggio 1).
-   Viene richiamato il callback [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Questo consente di gestire il caso in cui il mixer riceve l'input ma tutti gli esempi video del Presenter sono in uso (passaggio 2).

I successivi diversi esempi di codice illustrano questi passaggi in modo più dettagliato. Il Presenter chiama il `ProcessInputNotify` Metodo (illustrato nell'esempio seguente) quando ottiene il messaggio di **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .


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



Questo `ProcessInputNotify` metodo imposta un flag booleano per registrare il fatto che il mixer ha un nuovo input. Chiama quindi il `ProcessOutputLoop` metodo, illustrato nell'esempio successivo. Questo metodo tenta di estrarre il maggior numero possibile di campioni dal mixer:


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



Il `ProcessOutput` metodo, illustrato nell'esempio successivo, tenta di ottenere un singolo fotogramma video dal mixer. Se non è disponibile alcun fotogramma video, `ProcessSample` restituisce S_FALSE o un codice di errore, che interrompe il ciclo in `ProcessOutputLoop` . La maggior parte del lavoro viene eseguita all'interno del `ProcessOutput` Metodo:


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



Di seguito sono riportate alcune osservazioni sull'esempio:

-   Si presuppone che la variabile *m_SamplePool* sia un oggetto raccolta che include la coda degli esempi video disponibili. Il metodo dell'oggetto `GetSample` restituisce **MF_E_SAMPLEALLOCATOR_EMPTY** se la coda è vuota.
-   Se il metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer restituisce MF_E_TRANSFORM_NEED_MORE_INPUT, significa che il mixer non può produrre altro output, quindi il relatore Cancella il flag di *m_fSampleNotify* .
-   Il `TrackSample` metodo, che imposta il callback [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , viene illustrato nella sezione [esempi di rilevamento](#tracking-samples).

### <a name="repainting-frames"></a>Ridisegno di frame

Occasionalmente il presentatore potrebbe dover ridisegnare il frame video più recente. Il presentatore standard, ad esempio, ridisegna il frame nelle situazioni seguenti:

-   In modalità finestra, in risposta a **WM_PAINT** messaggi ricevuti dalla finestra dell'applicazione. Vedere [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Se il rettangolo di destinazione viene modificato quando l'applicazione chiama [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Usare la procedura seguente per richiedere al mixer di ricreare il frame più recente:

1.  Ottenere un esempio video dalla coda.
2.  Eseguire una query sull'esempio per l'interfaccia [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .
3.  Chiamare [**IMFDesiredSample:: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Specificare il timestamp del fotogramma video più recente. (Sarà necessario memorizzare nella cache questo valore e aggiornarlo per ciascun frame).
4.  Chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer.

Quando si ridisegna un frame, è possibile ignorare il clock di presentazione e presentare immediatamente il frame.

### <a name="scheduling-samples"></a>Esempi di pianificazione

I frame video possono raggiungere il EVR in qualsiasi momento. Il relatore è responsabile della presentazione di ogni fotogramma all'ora corretta, in base al timestamp del frame. Quando il presentatore ottiene un nuovo campione dal mixer, inserisce l'esempio nella coda pianificata. In un thread separato, il relatore ottiene continuamente il primo campione dall'inizio della coda e determina se:

-   Presentare l'esempio.
-   Mantieni l'esempio nella coda perché è in anticipo.
-   Rimuovere l'esempio perché è in ritardo. Anche se è consigliabile evitare di eliminare frame, se possibile, potrebbe essere necessario se il presentatore sta continuando a rimanere indietro.

Per ottenere il timestamp per un fotogramma video, chiamare [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) nell'esempio video. Il timestamp è relativo al clock di presentazione di EVR. Per ottenere l'ora dell'orologio corrente, chiamare [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Se il EVR non dispone di un clock di presentazione o se un campione non ha un timestamp, è possibile presentare l'esempio immediatamente dopo averlo ottenuto.

Per ottenere la durata di ogni esempio, chiamare [**IMFSample:: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Se l'esempio non ha una durata, è possibile usare la funzione [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) per calcolare la durata della frequenza dei fotogrammi.

Quando si pianificano gli esempi, tenere presente quanto segue:

-   Se la velocità di riproduzione è più veloce o più lenta della velocità normale, il clock viene eseguito a una velocità più veloce o più lenta. Ciò significa che il timestamp di un campione fornisce sempre l'ora di destinazione corretta rispetto al clock di presentazione. Tuttavia, se si traducono i tempi di presentazione in un altro orario (ad esempio, il contatore delle prestazioni ad alta risoluzione), è necessario ridimensionare le ore in base alla velocità di clock. Se la velocità di clock viene modificata, EVR chiama il metodo [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del Presenter.
-   La velocità di riproduzione può essere negativa per la riproduzione inversa. Quando la velocità di riproduzione è negativa, il clock di presentazione viene eseguito all'indietro. In altre parole, l'ora *n* + 1 si verifica prima dell'ora *n*.

Nell'esempio seguente viene calcolato l'inizio o la fine di un campione rispetto al clock di presentazione:


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



Il clock di presentazione viene in genere gestito dall'orologio di sistema o dal renderer audio. (Il renderer audio deriva l'ora della frequenza con cui la scheda audio utilizza l'audio.) In generale, il clock di presentazione non è sincronizzato con la frequenza di aggiornamento del monitoraggio.

Se i parametri di presentazione Direct3D specificano **D3DPRESENT_INTERVAL_DEFAULT** o **D3DPRESENT_INTERVAL_ONE** per l'intervallo di presentazione, l'operazione **attuale** attende la ritraccia verticale del monitoraggio. Si tratta di un modo semplice per impedire lo strappo, ma riduce l'accuratezza dell'algoritmo di pianificazione. Viceversa, se l'intervallo di presentazione è **D3DPRESENT_INTERVAL_IMMEDIATE**, il metodo **presente** viene eseguito immediatamente, causando la disattivazione, a meno che l'algoritmo di pianificazione non sia sufficientemente preciso da chiamare **present** solo durante il periodo di ritraccia verticale.

Le funzioni seguenti consentono di ottenere informazioni accurate sugli intervalli:

-   **IDirect3DDevice9:: GetRasterStatus** restituisce informazioni sul raster, inclusa la riga di analisi corrente e se il raster si trova nel periodo di vuoto verticale.
-   **DwmGetCompositionTimingInfo** restituisce le informazioni di temporizzazione per gestione finestre desktop. Queste informazioni sono utili se la composizione del desktop è abilitata.

### <a name="presenting-samples"></a>Presentazione di esempi

In questa sezione si presuppone che sia stata creata una catena di scambio separata per ogni superficie, come descritto in [allocazione di superfici Direct3D](#allocating-direct3d-surfaces). Per presentare un esempio, ottenere la catena di scambio dall'esempio video, come indicato di seguito:

1.  Chiamare [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) nell'esempio video per ottenere il buffer.
2.  Eseguire una query sul buffer per l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
3.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere l'interfaccia **IDirect3DSurface9** della superficie Direct3D. È possibile combinare questo passaggio e il passaggio precedente in uno chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).
4.  Chiamare **IDirect3DSurface9:: GetContainer** sulla superficie per ottenere un puntatore alla catena di scambio.
5.  Chiamare **IDirect3DSwapChain9::P inviato nuovamente** nella catena di scambio.

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



### <a name="source-and-destination-rectangles"></a>Rettangoli di origine e di destinazione

Il *rettangolo di origine* è la parte del fotogramma video da visualizzare. Viene definito in relazione a un sistema di coordinate normalizzato, in cui l'intero frame video occupa un rettangolo con le coordinate {0, 0, 1, 1}. Il *rettangolo di destinazione* è l'area all'interno della superficie di destinazione in cui viene disegnato il frame del video. Il presentatore standard consente a un'applicazione di impostare questi rettangoli chiamando [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Sono disponibili diverse opzioni per l'applicazione di rettangoli di origine e di destinazione. La prima opzione consiste nel consentire al mixer di applicarle:

-   Impostare il rettangolo di origine utilizzando l'attributo [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) . Il mixer applicherà il rettangolo di origine quando Blits il video alla superficie di destinazione. Il rettangolo di origine predefinito del mixer è l'intero frame.
-   Impostare il rettangolo di destinazione come apertura geometrica nel tipo di output del mixer. Per ulteriori informazioni, vedere la pagina relativa ai [formati di negoziazione](#negotiating-formats).

La seconda opzione consiste nell'applicare i rettangoli quando si **IDirect3DSwapChain9::P** di inviare nuovamente i rettangoli specificando i parametri *pSourceRect* e *pDestRect* nel metodo **presente** . È possibile combinare queste opzioni. Ad esempio, è possibile impostare il rettangolo di origine sul mixer, ma applicare il rettangolo di destinazione nel metodo **presente** .

Se l'applicazione modifica il rettangolo di destinazione o ridimensiona la finestra, potrebbe essere necessario allocare nuove superfici. In tal caso, è necessario prestare attenzione a sincronizzare questa operazione con il thread di pianificazione. Svuotare la coda di pianificazione ed eliminare gli esempi precedenti prima di allocare nuove superfici.

### <a name="end-of-stream"></a>Fine del flusso

Al termine di ogni flusso di input in EVR, EVR Invia un messaggio di **MFVP_MESSAGE_ENDOFSTREAM** al Presenter. Nel momento in cui si riceve il messaggio, tuttavia, potrebbero essere presenti alcuni fotogrammi video ancora da elaborare. Prima di rispondere al messaggio di fine flusso, è necessario svuotare tutto l'output dal mixer e presentare tutti i frame rimanenti. Dopo la presentazione dell'ultimo frame, inviare un evento **EC_COMPLETE** a EVR.

Nell'esempio seguente viene illustrato un metodo che invia l'evento **EC_COMPLETE** se vengono soddisfatte diverse condizioni. In caso contrario, restituisce S_OK senza inviare l'evento:


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



Questo metodo controlla gli Stati seguenti:

-   Se la *m_fSampleNotify* variabile è **true**, significa che il mixer contiene uno o più frame che non sono stati ancora elaborati. Per informazioni dettagliate, vedere [elaborazione dell'output](#processing-output).
-   La variabile *m_fEndStreaming* è un flag Boolean il cui valore iniziale è **false**. Il relatore imposta il flag su **true** quando EVR invia il messaggio di **MFVP_MESSAGE_ENDOFSTREAM** .
-   `AreSamplesPending`Si presuppone che il metodo restituisca **true** purché uno o più frame siano in attesa nella coda pianificata.

Nel metodo [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) impostare *m_fEndStreaming* su **true** e chiamare `CheckEndOfStream` quando il EVR invia il messaggio di **MFVP_MESSAGE_ENDOFSTREAM** :


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



Inoltre, chiamare `CheckEndOfStream` se il metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer restituisce **MF_E_TRANSFORM_NEED_MORE_INPUT**. Questo codice di errore indica che il mixer non contiene altri esempi di input (vedere [elaborazione dell'output](#processing-output)).

## <a name="frame-stepping"></a>Esecuzione del frame

EVR è progettato per supportare l'esecuzione dei frame in DirectShow e lo scrubbing in Media Foundation. L'esecuzione del frame e lo scrubbing sono concettualmente simili. In entrambi i casi, l'applicazione richiede un frame video alla volta. Internamente, il Presenter usa lo stesso meccanismo per implementare entrambe le funzionalità.

L'esecuzione del frame in DirectShow funziona nel modo seguente:

-   L'applicazione chiama [**IVideoFrameStep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). Il numero di passaggi viene specificato nel parametro *dwSteps* . EVR Invia un messaggio di **MFVP_MESSAGE_STEP** al presentatore, dove il parametro del messaggio (*ulParam*) è il numero di passaggi.
-   Se l'applicazione chiama [**IVideoFrameStep:: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o modifica lo stato del grafico (in esecuzione, in pausa o arrestato), il EVR Invia un messaggio **MFVP_MESSAGE_CANCELSTEP** .

Lo scrubbing in Media Foundation funziona nel modo seguente:

-   L'applicazione imposta la velocità di riproduzione su zero chiamando [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).
-   Per eseguire il rendering di un nuovo frame, l'applicazione chiama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione desiderata. EVR Invia un messaggio di **MFVP_MESSAGE_STEP** con *ulParam* uguale a 1.
-   Per arrestare lo scrubbing, l'applicazione imposta la velocità di riproduzione su un valore diverso da zero. Il EVR invia il messaggio **MFVP_MESSAGE_CANCELSTEP** .

Dopo la ricezione del messaggio di **MFVP_MESSAGE_STEP** , il relatore attende l'arrivo del frame di destinazione. Se il numero di passaggi è *N*, il relatore elimina gli esempi successivi (*n* -1) e presenta l'esempio *n* . Quando il Presenter completa il passaggio del frame, invia un evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) a EVR con *LParam1* impostato su **false**. Inoltre, se la velocità di riproduzione è zero, il Presenter Invia un evento [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) . Se il EVR Annulla l'esecuzione del frame mentre è ancora in sospeso un'operazione del frame, il Presenter Invia un evento **EC_STEP_COMPLETE** con *LParam1* impostato su **true**.

L'applicazione può eseguire il frame o la pulitura più volte, quindi il presentatore potrebbe ricevere più messaggi di **MFVP_MESSAGE_STEP** prima di ottenere un messaggio di **MFVP_MESSAGE_CANCELSTEP** . Inoltre, il relatore può ricevere il messaggio di **MFVP_MESSAGE_STEP** prima dell'avvio del clock o durante l'esecuzione del clock.

### <a name="implementing-frame-stepping"></a>Implementazione dell'esecuzione del frame

Questa sezione descrive un algoritmo per implementare l'esecuzione del frame. L'algoritmo frame stepping usa le variabili seguenti:

-   *step_count*. Unsigned Integer che specifica il numero di passaggi nell'operazione di esecuzione del frame corrente.
-   *step_queue*. Coda di puntatori [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
-   *step_state*. In qualsiasi momento, il presentatore può trovarsi in uno degli Stati seguenti rispetto all'esecuzione dei frame: 

    | State         | Descrizione                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Non esecuzione del frame.                                                                                                                                                                                             |
    | WAITING       | Il relatore ha ricevuto il messaggio di **MFVP_MESSAGE_STEP** , ma l'orologio non è stato avviato.                                                                                                                  |
    | PENDING       | Il relatore ha ricevuto il messaggio di **MFVP_MESSAGE_STEP** e l'orologio è stato avviato, ma il relatore è in attesa di ricevere il frame di destinazione.                                                             |
    | PIANIFICATO     | Il presentatore ha ricevuto il frame di destinazione e ha pianificato la presentazione, ma il frame non è stato presentato.                                                                                        |
    | COMPLETARE      | Il presentatore ha presentato il frame di destinazione e ha inviato l'evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) ed è in attesa del successivo **MFVP_MESSAGE_STEP** o **MFVP_MESSAGE_CANCELSTEP** messaggio. |

    

     

    Questi Stati sono indipendenti dagli Stati del relatore elencati nella sezione [Stati del relatore](#presenter-states).

Per l'algoritmo di esecuzione dei frame sono definite le procedure seguenti:

Procedura PrepareFrameStep

1.  Incrementa *step_count*.
2.  Impostare *step_state* su Waiting.
3.  Se il clock è in esecuzione, chiamare StartFrameStep.

Procedura StartFrameStep

1.  Se *step_state* è uguale a Waiting, impostare *step_state* su pending. Per ogni esempio in *step_queue*, chiamare DeliverFrameStepSample.
2.  Se *step_state* è uguale a NOT_STEPPING, rimuovere gli esempi da *step_queue* e pianificarli per la presentazione.

Procedura CompleteFrameStep

1.  Impostare *step_state* per il completamento.
2.  Inviare l'evento EC_STEP_COMPLETE con *lParam1*  =  **false**.
3.  Se la frequenza di clock è zero, inviare l'evento **EC_SCRUB_TIME** con l'ora di esempio.

Procedura DeliverFrameStepSample

1.  Se la frequenza di clock è pari a zero e ora di *campionamento*  +  *durata campione*  <  , eliminare l'esempio. Exit.
2.  Se *step_state* è uguale a scheduled o complete, aggiungere l'esempio al *step_queue*. Exit.
3.  Decrementa *step_count*.
4.  Se *step_count* > 0, eliminare l'esempio. Exit.
5.  Se *step_state* è uguale a Waiting, aggiungere l'esempio al *step_queue*. Exit.
6.  Pianificare l'esempio per la presentazione.
7.  Impostare *step_state* su pianificato.

Procedura CancelFrameStep

1.  Imposta *step_state* su NOT_STEPPING
2.  Reimposta *step_count* su zero.
3.  Se il valore precedente di *step_state* era in attesa, in sospeso o pianificato, inviare EC_STEP_COMPLETE con *lParam1*  =  **true**.

Chiamare queste procedure come segue:



| Messaggio o metodo del Presenter                                                   | Procedura           |
|-------------------------------------------------------------------------------|---------------------|
| Messaggio **MFVP_MESSAGE_STEP**                                               | `PrepareFrameStep`  |
| Messaggio **MFVP_MESSAGE_STEP**                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| Callback [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

Il diagramma di flusso seguente mostra le procedure per l'esecuzione dei frame.

![diagramma di flusso che mostra i percorsi che iniziano con il \- \- passaggio del messaggio mfvp e il \- messaggio mfvp \- processinputnotify e terminano con "stato = completo"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Impostazione del Presenter in EVR

Dopo l'implementazione del Presenter, il passaggio successivo consiste nel configurare il EVR per usarlo.

### <a name="setting-the-presenter-in-directshow"></a>Impostazione del Presenter in DirectShow

In un'applicazione DirectShow impostare il Presenter in EVR come segue:

1.  Creare il filtro EVR chiamando **CoCreateInstance**. Il CLSID è **CLSID_EnhancedVideoRenderer**.
2.  Aggiungere EVR al grafico dei filtri.
3.  Creare un'istanza del Presenter. Il presentatore può supportare la creazione di oggetti COM standard tramite **IClassFactory**, ma questa operazione non è obbligatoria.
4.  Eseguire una query sul filtro EVR per l'interfaccia [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
5.  Chiamare [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

### <a name="setting-the-presenter-in-media-foundation"></a>Impostazione del Presenter in Media Foundation

In Media Foundation sono disponibili diverse opzioni, a seconda che venga creato il sink di supporto EVR o l'oggetto attivazione di EVR. Per ulteriori informazioni sugli oggetti attivazione, vedere [oggetti Activation](activation-objects.md).

Per il sink di supporto EVR, eseguire le operazioni seguenti:

1.  Chiamare [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) per creare il sink multimediale.
2.  Creare un'istanza del Presenter.
3.  Eseguire una query sul sink multimediale EVR per l'interfaccia [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
4.  Chiamare [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

Per l'oggetto attivazione di EVR, eseguire le operazioni seguenti:

1.  Chiamare [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto Activation.
2.  Impostare uno degli attributi seguenti nell'oggetto Activation: 

    | Attributo                                                                                                         | Descrizione                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Puntatore a un oggetto di attivazione per il presentatore.<br/> Con questo flag, è necessario fornire un oggetto attivazione per il relatore. L'oggetto Activation deve implementare l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID del Presenter.<br/> Con questo flag, il relatore deve supportare la creazione di oggetti COM standard tramite **IClassFactory**.<br/>                                                                                         |

    

     

3.  Facoltativamente, impostare l'attributo [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) sull'oggetto Activation.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> <dt>

[Esempio EVRPresenter](evrpresenter-sample.md)
</dt> </dl>

 

 
