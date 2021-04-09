---
description: In questo argomento viene illustrata in dettaglio l'esempio MPEG-1 Media Source SDK.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Case Study: origine supporto MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058430"
---
# <a name="case-study-mpeg-1-media-source"></a>Case Study: origine supporto MPEG-1

In Microsoft Media Foundation, l'oggetto che introduce i dati multimediali nella pipeline di dati viene chiamato *origine multimediale*. In questo argomento viene illustrata in dettaglio l'esempio [MPEG-1 media source](mpeg1source-sample.md) SDK.

-   [Prerequisiti](#prerequisites)
-   [Classi C++ usate nell'origine MPEG-1](#c-classes-used-in-the-mpeg-1-source)
-   [Gestore del flusso di byte](#byte-stream-handler)
-   [Descrittore presentazione](#presentation-descriptor)
-   [Stati di streaming](#streaming-states)
    -   [Inizia](#start)
    -   [Sospendi](#pause)
    -   [Stop](#stop)
-   [Richieste di esempio](#sample-requests)
-   [Fine del flusso](#end-of-stream)
-   [Operazioni asincrone](#asynchronous-operations)
    -   [Coda operazioni](#operation-queue)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Prima di leggere questo argomento, è necessario comprendere i concetti seguenti Media Foundation:

-   [Modello a oggetti di origine multimediale](media-source-object-model.md)
-   [Metodi di callback asincroni](asynchronous-callback-methods.md).
-   [Code di lavoro](work-queues.md)
-   [Generatori di eventi multimediali](media-event-generators.md)
-   [Buffer multimediali](media-buffers.md)
-   [Esempi di supporti](media-samples.md)
-   [Tipi di supporto](media-types.md)

È anche necessario avere una conoscenza di base dell'architettura Media Foundation, in particolare il ruolo delle origini multimediali nella pipeline. Per altre informazioni, vedere [origini multimediali](media-sources.md).

Inoltre, è possibile leggere l'argomento [scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md), che fornisce una panoramica più generale dei passaggi descritti qui.

Questo argomento non riproduce tutto il codice dell'esempio SDK, perché l'esempio è piuttosto grande.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>Classi C++ usate nell'origine MPEG-1

L'origine MPEG-1 di esempio viene implementata con le classi C++ seguenti:

-   `MPEG1ByteStreamHandler`. Implementa il gestore del flusso di byte per l'origine multimediale. Dato un flusso di byte, il gestore del flusso di byte crea un'istanza dell'origine.
-   `MPEG1Source`. Implementa l'origine del supporto.
-   `MPEG1Stream`. Implementa gli oggetti del flusso multimediale. L'origine multimediale crea un `MPEG1Stream` oggetto per ogni flusso audio o video nel file Bitstream MPEG-1.
-   `Parser`. Analizza il Bitstream MPEG-1. Nella maggior parte dei casi, i dettagli di questa classe non sono rilevanti per le API Media Foundation.
-   SourceOp, OpQueue: queste due classi gestiscono le operazioni asincrone nell'origine multimediale. (Vedere [operazioni asincrone](#asynchronous-operations)).

Altre classi helper varie sono descritte più avanti in questo argomento.

## <a name="byte-stream-handler"></a>Gestore Byte-Stream

Il gestore del *flusso di byte* è l'oggetto che crea l'origine multimediale. Il gestore del flusso di byte viene creato dal resolver di origine; le applicazioni non interagiscono direttamente con il gestore del flusso di byte. Il resolver di origine individua il gestore del flusso di byte cercando nel registro di sistema. Il gestore viene registrato dall'estensione del nome file o dal tipo MIME. Per l'origine MPEG-1, il gestore del flusso di byte viene registrato per l'estensione del nome file ". mpg".

> [!Note]  
> Se si desidera supportare schemi URL personalizzati, è anche possibile scrivere un *gestore dello schema*. L'origine MPEG-1 è progettata per i file locali e Media Foundation fornisce già un gestore dello schema per gli URL "file://".

 

Il gestore del flusso di byte implementa l'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Questa interfaccia dispone di due metodi più importanti che devono essere implementati:

-   [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Avvia un'operazione asincrona per creare l'origine multimediale.
-   [**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Completa la chiamata asincrona.

Altri due metodi sono facoltativi e non sono implementati nell'esempio SDK:

-   [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Annulla il metodo [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) . Questo metodo è utile per un'origine di rete che può avere una latenza elevata all'avvio.
-   [**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Ottiene il numero massimo di byte che il gestore leggerà dal flusso di origine. Implementare questo metodo se si conosce la quantità di dati che il gestore del flusso di byte prima può creare l'origine multimediale. In caso contrario, restituire semplicemente **E \_ NOTIMPL**.

Di seguito è illustrata l'implementazione del metodo [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



Il metodo esegue i passaggi seguenti:

1.  Crea una nuova istanza dell'oggetto `MPEG1Source`.
2.  Creare un oggetto risultato asincrono. Questo oggetto viene usato in un secondo momento per richiamare il metodo di callback del resolver di origine.
3.  Chiama `MPEG1Source::BeginOpen` un metodo asincrono definito nella `MPEG1Source` classe.
4.  Imposta *ppIUnknownCancelCookie* su **null**, che informa il chiamante che [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) non è supportato.

Il `MPEG1Source::BeginOpen` metodo esegue l'operazione effettiva di lettura del flusso di byte e di inizializzazione dell' `MPEG1Source` oggetto. Questo metodo non fa parte dell'API pubblica. È possibile definire qualsiasi meccanismo tra il gestore e l'origine multimediale più adatta alle proprie esigenze. L'inserimento della maggior parte della logica nell'origine multimediale mantiene il gestore del flusso di byte relativamente semplice.

In breve, `BeginOpen` esegue le operazioni seguenti:

1.  Chiama [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) per verificare che il flusso di byte di origine sia leggibile e ricercabile.
2.  Chiama [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) per avviare una richiesta di I/O asincrona.

Il resto dell'inizializzazione si verifica in modo asincrono. L'origine multimediale legge dati sufficienti dal flusso per analizzare le intestazioni di sequenza MPEG-1. Viene quindi creato un *descrittore di presentazione*, ovvero l'oggetto usato per descrivere i flussi audio e video nel file. Per ulteriori informazioni, vedere [descrittore della presentazione](#presentation-descriptor). Al `BeginOpen` termine dell'operazione, il gestore del flusso di byte richiama il metodo di callback del resolver di origine. A questo punto, il resolver di origine chiama [**IMFByteStreamHandler:: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Il metodo **EndCreateObject** restituisce lo stato dell'operazione.


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



Se si verifica un errore in qualsiasi momento durante questo processo, il callback viene richiamato con un codice di stato di errore.

## <a name="presentation-descriptor"></a>Descrittore presentazione

Il descrittore della presentazione descrive il contenuto del file MPEG-1, incluse le informazioni seguenti:

-   Numero di flussi.
-   Formato di ogni flusso.
-   Identificatori di flusso.
-   Stato di selezione di ogni flusso (selezionato o deselezionato).

In termini di architettura Media Foundation, il descrittore di presentazione contiene uno o più descrittori di *flusso*. Ogni descrittore di flusso contiene un *gestore di tipo di supporto*, che viene usato per ottenere o impostare i tipi di supporto nel flusso. Media Foundation fornisce implementazioni predefinite per il descrittore di presentazione e il descrittore del flusso; sono adatti per la maggior parte delle origini multimediali.

Per creare un descrittore di presentazione, seguire questa procedura:

1.  Per ogni flusso:
    1.  Fornire un ID flusso e una matrice di tipi di supporti possibili. Se il flusso supporta più di un tipo di supporto, ordinare l'elenco dei tipi di supporto in base alla preferenza, se disponibile. (Inserire prima il tipo ottimale e il tipo meno ottimale).
    2.  Chiamare [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) per creare il descrittore del flusso.
    3.  Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso appena creato.
    4.  Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato predefinito per il flusso. Se è presente più di un tipo di supporto, è in genere necessario impostare il primo tipo nell'elenco.
2.  Chiamare [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e passare la matrice di puntatori del descrittore di flusso.
3.  Per ogni flusso, chiamare [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) o [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) per impostare lo stato di selezione predefinito. Se è presente più di un flusso dello stesso tipo (audio o video), per impostazione predefinita è necessario selezionarne solo uno.

L' `MPEG1Source` oggetto crea il descrittore della presentazione nel `InitPresentationDescriptor` Metodo:


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



L'applicazione ottiene il descrittore di presentazione chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Questo metodo crea una copia superficiale del descrittore di presentazione chiamando [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). La copia contiene i puntatori ai descrittori di flusso originali. L'applicazione può usare il descrittore della presentazione per impostare il tipo di supporto, selezionare un flusso o deselezionare un flusso.

Facoltativamente, i descrittori di presentazione e i descrittori di flusso possono contenere attributi che forniscono informazioni aggiuntive sull'origine. Per un elenco di tali attributi, vedere gli argomenti seguenti:

-   [Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
-   [Attributi del descrittore di flusso](stream-descriptor-attributes.md)

Un attributo merita menzione speciale: l'attributo della [**\_ \_ durata MF PD**](mf-pd-duration-attribute.md) contiene la durata totale dell'origine. Impostare questo attributo se si conosce la durata di inizio; è ad esempio possibile specificare la durata nelle intestazioni dei file, a seconda del formato di file. L'applicazione può visualizzare questo valore o usarlo per impostare un indicatore di stato o una barra di ricerca.

## <a name="streaming-states"></a>Stati di streaming

Un'origine multimediale definisce gli Stati seguenti:



| State    | Descrizione                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Avviato  | L'origine accetta ed elabora le richieste di esempio.                                                               |
| Paused   | L'origine accetta richieste di esempio, ma non le elabora. Le richieste vengono accodate fino a quando l'origine non viene avviata. |
| Arrestato. | L'origine rifiuta le richieste di esempio.                                                                             |



 

### <a name="start"></a>Avvio

Il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) avvia l'origine del supporto. È necessario specificare i seguenti parametri:

-   Descrittore di presentazione.
-   GUID del formato di ora.
-   Posizione iniziale.

L'applicazione deve ottenere il descrittore di presentazione chiamando [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) nell'origine. Non esiste alcun meccanismo definito per la convalida di un descrittore di presentazione. Se l'applicazione specifica il descrittore di presentazione errato, i risultati non sono definiti.

Il GUID del formato di ora specifica come interpretare la posizione iniziale. Il formato standard è 100 unità di nanosecondi (NS), indicate dal GUID \_ null. Ogni origine multimediale deve supportare unità 100-ns. Facoltativamente, un'origine può supportare altre unità di tempo, ad esempio il numero di frame o il codice temporale. Tuttavia, non esiste un modo standard per eseguire una query su un'origine multimediale per l'elenco dei formati di tempo supportati.

La posizione iniziale viene specificata come **PROPVARIANT**, consentendo tipi di dati diversi a seconda del formato dell'ora. Per 100-ns, il tipo **PROPVARIANT** è **VT \_ i8** o **VT \_ empty**. Se **VT \_ i8**, il **PROPVARIANT** contiene la posizione iniziale in unità 100-ns. Il valore **VT \_ vuoto** ha il significato speciale "inizia alla posizione corrente".

Implementare il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) come segue:

1.  Convalida parametri e stato:
    -   Verificare la presenza di parametri **null** .
    -   Controllare il GUID del formato di ora. Se il valore non è valido, restituire il **\_ formato di \_ \_ ora non \_ supportato**.
    -   Controllare il tipo di dati di **PROPVARIANT** che include la posizione iniziale.
    -   Convalidare la posizione iniziale. Se non è valido, restituire **MF \_ E \_ INVALIDREQUEST**.
    -   Se l'origine è stata arrestata, restituire **MF \_ E \_ Shutdown**.
2.  Se non si verificano errori nel passaggio 1, accodare un'operazione asincrona. Tutti gli elementi dopo questo passaggio si verificano in un thread della coda di lavoro.
3.  Per ogni flusso:
    1.  Controllare se il flusso è già attivo da una precedente richiesta di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) .
    2.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per verificare se l'applicazione ha selezionato o deselezionato il flusso.
    3.  Se un flusso selezionato in precedenza è ora deselezionato, scaricare tutti gli esempi non recapitati per tale flusso.
    4.  Se il flusso è attivo, l'origine del supporto (non il flusso) Invia uno degli eventi seguenti:
        -   Invia [MEUpdatedStream](meupdatedstream.md) se il flusso era precedentemente attivo.
        -   In caso contrario, invia [MENewStream](menewstream.md).

        Per entrambi gli eventi, i dati dell'evento sono il puntatore [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) per il flusso.
    5.  Se l'origine viene riavviata dallo stato sospeso, potrebbero essere presenti richieste di esempio in sospeso. In tal caso, è possibile recapitarli adesso.
    6.  Se l'origine sta cercando in una nuova posizione, ogni oggetto flusso Invia un evento [MEStreamSeeked](mestreamseeked.md) . In caso contrario, ogni flusso Invia un evento [MEStreamStarted](mestreamstarted.md) .
4.  Se l'origine sta cercando in una nuova posizione, l'origine multimediale Invia un evento [MESourceSeeked](mesourceseeked.md) . In caso contrario, invia un evento [MESourceStarted](mesourcestarted.md) .

Se si verifica un errore in qualsiasi momento dopo il passaggio 2, l'origine invia un evento [MESourceStarted](mesourcestarted.md) con un codice di errore. Viene avvisato l'applicazione che il metodo di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) non è riuscito in modo asincrono.

Il codice seguente illustra i passaggi da 1 a 2:


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



I passaggi rimanenti sono illustrati nell'esempio seguente:


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>Sospendi

Il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) mette in pausa l'origine del supporto. Implementare questo metodo come segue:

1.  Accoda un'operazione asincrona.
2.  Ogni flusso attivo Invia un evento [MEStreamPaused](mestreampaused.md) .
3.  L'origine multimediale Invia un evento [MESourcePaused](mesourcepaused.md) .

Durante la sospensione, le code di origine vengono richieste di esempio senza elaborarle. (Vedere [le richieste di esempio](#sample-requests)).

### <a name="stop"></a>Interrompere

Il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) interrompe l'origine del supporto. Implementare questo metodo come segue:

1.  Accoda un'operazione asincrona.
2.  Ogni flusso attivo Invia un evento [MEStreamStopped](mestreamstopped.md) .
3.  Cancellare tutti gli esempi in coda e le richieste di esempio.
4.  L'origine multimediale Invia un evento [MESourceStopped](mesourcestopped.md) .

Durante l'arresto, l'origine rifiuta tutte le richieste per gli esempi.

Se l'origine viene arrestata mentre è in corso una richiesta di I/O, la richiesta di I/O può essere completata dopo che l'origine entra nello stato interrotto. In tal caso, l'origine deve eliminare il risultato della richiesta di I/O.

## <a name="sample-requests"></a>Richieste di esempio

Media Foundation usare un modello *pull* , in cui la pipeline richiede esempi dall'origine multimediale. Questo comportamento è diverso rispetto al modello usato da DirectShow, in cui sono presenti gli esempi "push" delle origini.

Per richiedere un nuovo esempio, la pipeline Media Foundation chiama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Questo metodo accetta un puntatore **IUnknown** che rappresenta un oggetto *token* . L'implementazione dell'oggetto token spetta al chiamante. fornisce semplicemente un modo per il chiamante per tenere traccia delle richieste di esempio. Anche il parametro del token può essere **null**.

Supponendo che l'origine usi richieste di I/O asincrone per leggere i dati, la generazione di esempio non verrà sincronizzata con le richieste di esempio. Per sincronizzare le richieste di esempio con la generazione di esempio, un'origine multimediale esegue le operazioni seguenti:

1.  I token della richiesta vengono inseriti in una coda.
2.  Man mano che vengono generati esempi, vengono inseriti in una seconda coda.
3.  L'origine multimediale completa una richiesta di esempio estraendo un token di richiesta dalla prima coda e un campione dalla seconda coda.
4.  L'origine multimediale Invia un evento MEMediaSample. L'evento contiene un puntatore all'esempio e l'esempio contiene un puntatore al token.

Il diagramma seguente illustra la relazione tra l'evento [MEMediaSample](memediasample.md) , l'esempio e il token della richiesta.

![diagramma che mostra memediasample e una coda di esempio che punta a IMFSample; IMFSample e la coda di richieste puntano a IUnknown](images/mediasourceimpl01.png)

L'origine MPEG-1 di esempio implementa questo processo nel modo seguente:

1.  Il metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) inserisce la richiesta in una coda FIFO.
2.  Quando le richieste di I/O vengono completate, l'origine multimediale crea nuovi esempi e li inserisce in una seconda coda FIFO. Questa coda ha una dimensione massima per impedire che l'origine legga troppo a lungo.
3.  Ogni volta che entrambe le code hanno almeno un elemento (una richiesta e un campione), l'origine multimediale completa la prima richiesta dalla coda delle richieste inviando il primo esempio dalla coda di esempio.
4.  Per recapitare un esempio, l'oggetto flusso (non l'oggetto di origine) Invia un evento [MEMediaSample](memediasample.md) .
    -   I dati dell'evento sono un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dell'esempio.
    -   Se la richiesta include un token, allegare il token all'esempio impostando l'attributo del [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) nell'esempio.

A questo punto, sono disponibili tre possibilità:

-   È presente un altro esempio nella coda di esempio, ma nessuna richiesta corrispondente.
-   È presente una richiesta, ma non un campione.
-   Entrambe le code sono vuote. non sono presenti esempi e richieste.

Se la coda di esempio è vuota, l'origine controlla la fine del flusso (vedere la [fine del flusso](#end-of-stream)). In caso contrario, viene avviata un'altra richiesta di I/O per i dati. Se si verifica un errore durante questo processo, il flusso Invia un evento [MEError](meerror.md) .

Il codice seguente implementa il metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



Il `DispatchSamples` metodo estrae gli esempi dalla coda di esempio, li associa alle richieste di esempio in sospeso e gli eventi [MEMediaSample](memediasample.md) di Accodamento:


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



Il `DispatchSamples` metodo viene chiamato nelle circostanze seguenti:

-   All'interno del metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .
-   Quando l'origine multimediale viene riavviata dallo stato sospeso.
-   Quando viene completata una richiesta di I/O.

## <a name="end-of-stream"></a>Fine del flusso

Quando un flusso non contiene più dati e tutti gli esempi per tale flusso sono stati recapitati, gli oggetti flusso inviano un evento [MEEndOfStream](meendofstream.md) .

Quando tutti i flussi attivi vengono eseguiti, l'origine multimediale Invia un evento [MEEndOfPresentation](meendofpresentation.md) .

## <a name="asynchronous-operations"></a>Operazioni asincrone

Probabilmente la parte più difficile della scrittura di un'origine multimediale consiste nel comprendere il Media Foundation modello asincrono.

Tutti i metodi in un'origine multimediale che controllano il flusso sono asincroni. In ogni caso, il metodo esegue una convalida iniziale, ad esempio il controllo dei parametri. L'origine invia quindi il resto del lavoro a una coda di lavoro. Al termine dell'operazione, l'origine multimediale Invia un evento al chiamante tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) dell'origine multimediale. È quindi importante comprendere le code di lavoro.

Per inserire un elemento in una coda di lavoro, è possibile chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). L'origine MPEG-1 USA **MFPutWorkItem**, ma le due funzioni eseguono la stessa operazione. La funzione **MFPutWorkItem** accetta i parametri seguenti:

-   Valore **DWORD** che identifica la coda di lavoro. È possibile creare una coda di lavoro privata o usare lo **\_ standard della \_ coda \_ di callback MFASYNC**.
-   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Questa interfaccia di callback viene richiamata per eseguire il lavoro.
-   Oggetto di stato facoltativo, che deve implementare **IUnknown**.

La coda di lavoro viene gestita da uno o più thread di lavoro che effettuano il pull continuo del successivo elemento di lavoro dalla coda e richiamano il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'interfaccia di callback.

Non è garantito che gli elementi di lavoro vengano eseguiti nello stesso ordine in cui sono stati inseriti nella coda. Si tenga presente che più thread possono servire la stessa coda di lavoro, quindi le chiamate [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) possono sovrapporsi o non essere presenti in ordine. Pertanto, spetta all'origine multimediale mantenere lo stato interno corretto inviando elementi della coda di lavoro nell'ordine corretto. Solo quando l'operazione precedente è completa, l'origine avvia l'operazione successiva.

Per rappresentare le operazioni in sospeso, l'origine MPEG-1 definisce una classe denominata `SourceOp` :


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



L' `Operation` enumerazione identifica l'operazione in sospeso. La classe contiene anche un **PROPVARIANT** per fornire dati aggiuntivi per l'operazione.

### <a name="operation-queue"></a>Coda operazioni

Per serializzare le operazioni, l'origine multimediale mantiene una coda di `SourceOp` oggetti. Usa una classe helper per gestire la coda:


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



La `OpQueue` classe è progettata per essere ereditata dal componente che esegue gli elementi di lavoro asincroni. Il parametro del modello di *\_ tipo op* è il tipo di oggetto usato per rappresentare gli elementi di lavoro nella coda, in questo caso il *\_ tipo op* sarà `SourceOp` . La `OpQueue` classe implementa i metodi seguenti:

-   `QueueOperation` inserisce un nuovo elemento nella coda.
-   `ProcessQueue` Invia l'operazione successiva dalla coda. Questo metodo è asincrono.
-   `ProcessQueueAsync` completa il metodo asincrono `ProcessQueue` .

Altri due metodi devono essere implementati dalla classe derivata:

-   `ValidateOperation` Verifica se è valido per eseguire un'operazione specificata, dato lo stato corrente dell'origine del supporto.
-   `DispatchOperation` esegue l'elemento di lavoro asincrono.

La coda delle operazioni viene utilizzata come segue:

1.  La pipeline Media Foundation chiama un metodo asincrono sull'origine multimediale, ad esempio [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Il metodo asincrono chiama `QueueOperation` , che inserisce l'operazione di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) nella coda e chiama `ProcessQueue` (sotto forma di `SourceOp` oggetto).
3.  `ProcessQueue` chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).
4.  Il thread della coda di lavoro chiama `ProcessQueueAsync` .
5.  Il `ProcessQueueAsync` metodo chiama `ValidateOperation` e `DispatchOperation` .

Il codice seguente Accoda una nuova operazione sull'origine MPEG-1:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



Il codice seguente elabora la coda:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



Il `ValidateOperation` metodo controlla se l'origine MPEG-1 può inviare l'operazione successiva nella coda. Se è in corso un'altra operazione, `ValidateOperation` restituisce **MF \_ E \_ NOTACCEPTING**. Ciò garantisce che `DispatchOperation` non venga chiamato mentre è in sospeso un'altra operazione.


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



Il metodo DispatchOperation passa al tipo di operazione:


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Per concludere:

1.  La pipeline chiama un metodo asincrono, ad esempio [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Il metodo asincrono chiama `OpQueue::QueueOperation` , passando un puntatore a un `SourceOp` oggetto.
3.  Il `QueueOperation` metodo inserisce l'operazione sulla coda *m \_ OpQueue* e chiama `OpQueue::ProcessQueue` .
4.  Il `ProcessQueue` metodo chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem). Da questo punto, tutto avviene in un Media Foundation thread della coda di lavoro. Il metodo asincrono restituisce al chiamante.
5.  Il thread della coda di lavoro chiama il `OpQueue::ProcessQueueAsync` metodo.
6.  Il `ProcessQueueAsync` metodo chiama `MPEG1Source:ValidateOperation` per convalidare l'operazione.
7.  Il `ProcessQueueAsync` metodo chiama `MPEG1Source::DispatchOperation` per elaborare l'operazione.

Questa progettazione presenta diversi vantaggi:

-   I metodi sono asincroni, quindi non bloccano il thread dell'applicazione chiamante.
-   Le operazioni vengono inviate in un thread della coda di lavoro Media Foundation, condiviso tra i componenti della pipeline. Pertanto, l'origine multimediale non crea il proprio thread, riducendo il numero totale di thread creati.
-   L'origine multimediale non si blocca durante l'attesa del completamento delle operazioni. In questo modo si riduce la probabilità che un'origine multimediale provochi accidentalmente un deadlock e contribuisca a ridurre il cambio del contesto.
-   L'origine multimediale può usare l'I/O asincrono per leggere il file di origine (chiamando [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). Non è necessario bloccare l'origine multimediale durante l'attesa del completamento della routine di I/O.

Se si segue il modello illustrato nell'esempio SDK, è possibile concentrarsi sui dettagli specifici dell'origine multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)
</dt> </dl>

 

 



