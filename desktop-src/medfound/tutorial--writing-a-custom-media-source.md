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
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="9021d-103">Case Study: origine supporto MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9021d-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="9021d-104">In Microsoft Media Foundation, l'oggetto che introduce i dati multimediali nella pipeline di dati viene chiamato *origine multimediale*.</span><span class="sxs-lookup"><span data-stu-id="9021d-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="9021d-105">In questo argomento viene illustrata in dettaglio l'esempio [MPEG-1 media source](mpeg1source-sample.md) SDK.</span><span class="sxs-lookup"><span data-stu-id="9021d-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="9021d-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9021d-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="9021d-107">Classi C++ usate nell'origine MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9021d-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="9021d-108">Gestore del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="9021d-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="9021d-109">Descrittore presentazione</span><span class="sxs-lookup"><span data-stu-id="9021d-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="9021d-110">Stati di streaming</span><span class="sxs-lookup"><span data-stu-id="9021d-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="9021d-111">Inizia</span><span class="sxs-lookup"><span data-stu-id="9021d-111">Start</span></span>](#start)
    -   [<span data-ttu-id="9021d-112">Sospendi</span><span class="sxs-lookup"><span data-stu-id="9021d-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="9021d-113">Stop</span><span class="sxs-lookup"><span data-stu-id="9021d-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="9021d-114">Richieste di esempio</span><span class="sxs-lookup"><span data-stu-id="9021d-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="9021d-115">Fine del flusso</span><span class="sxs-lookup"><span data-stu-id="9021d-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="9021d-116">Operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="9021d-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="9021d-117">Coda operazioni</span><span class="sxs-lookup"><span data-stu-id="9021d-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="9021d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9021d-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="9021d-119">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9021d-119">Prerequisites</span></span>

<span data-ttu-id="9021d-120">Prima di leggere questo argomento, è necessario comprendere i concetti seguenti Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="9021d-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="9021d-121">Modello a oggetti di origine multimediale</span><span class="sxs-lookup"><span data-stu-id="9021d-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="9021d-122">[Metodi di callback asincroni](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9021d-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="9021d-123">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="9021d-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="9021d-124">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="9021d-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="9021d-125">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="9021d-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="9021d-126">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="9021d-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="9021d-127">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="9021d-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="9021d-128">È anche necessario avere una conoscenza di base dell'architettura Media Foundation, in particolare il ruolo delle origini multimediali nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="9021d-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="9021d-129">Per altre informazioni, vedere [origini multimediali](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="9021d-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="9021d-130">Inoltre, è possibile leggere l'argomento [scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md), che fornisce una panoramica più generale dei passaggi descritti qui.</span><span class="sxs-lookup"><span data-stu-id="9021d-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="9021d-131">Questo argomento non riproduce tutto il codice dell'esempio SDK, perché l'esempio è piuttosto grande.</span><span class="sxs-lookup"><span data-stu-id="9021d-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="9021d-132">Classi C++ usate nell'origine MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9021d-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="9021d-133">L'origine MPEG-1 di esempio viene implementata con le classi C++ seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="9021d-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="9021d-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="9021d-135">Implementa il gestore del flusso di byte per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="9021d-136">Dato un flusso di byte, il gestore del flusso di byte crea un'istanza dell'origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="9021d-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="9021d-137">`MPEG1Source`.</span></span> <span data-ttu-id="9021d-138">Implementa l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9021d-138">Implements the media source.</span></span>
-   <span data-ttu-id="9021d-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="9021d-139">`MPEG1Stream`.</span></span> <span data-ttu-id="9021d-140">Implementa gli oggetti del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-140">Implements the media stream objects.</span></span> <span data-ttu-id="9021d-141">L'origine multimediale crea un `MPEG1Stream` oggetto per ogni flusso audio o video nel file Bitstream MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9021d-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="9021d-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="9021d-142">`Parser`.</span></span> <span data-ttu-id="9021d-143">Analizza il Bitstream MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9021d-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="9021d-144">Nella maggior parte dei casi, i dettagli di questa classe non sono rilevanti per le API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9021d-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="9021d-145">SourceOp, OpQueue: queste due classi gestiscono le operazioni asincrone nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="9021d-146">(Vedere [operazioni asincrone](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="9021d-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="9021d-147">Altre classi helper varie sono descritte più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9021d-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="9021d-148">Gestore Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="9021d-148">Byte-Stream Handler</span></span>

<span data-ttu-id="9021d-149">Il gestore del *flusso di byte* è l'oggetto che crea l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="9021d-150">Il gestore del flusso di byte viene creato dal resolver di origine; le applicazioni non interagiscono direttamente con il gestore del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="9021d-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="9021d-151">Il resolver di origine individua il gestore del flusso di byte cercando nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9021d-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="9021d-152">Il gestore viene registrato dall'estensione del nome file o dal tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="9021d-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="9021d-153">Per l'origine MPEG-1, il gestore del flusso di byte viene registrato per l'estensione del nome file ". mpg".</span><span class="sxs-lookup"><span data-stu-id="9021d-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="9021d-154">Se si desidera supportare schemi URL personalizzati, è anche possibile scrivere un *gestore dello schema*.</span><span class="sxs-lookup"><span data-stu-id="9021d-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="9021d-155">L'origine MPEG-1 è progettata per i file locali e Media Foundation fornisce già un gestore dello schema per gli URL "file://".</span><span class="sxs-lookup"><span data-stu-id="9021d-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="9021d-156">Il gestore del flusso di byte implementa l'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="9021d-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="9021d-157">Questa interfaccia dispone di due metodi più importanti che devono essere implementati:</span><span class="sxs-lookup"><span data-stu-id="9021d-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="9021d-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="9021d-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="9021d-159">Avvia un'operazione asincrona per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="9021d-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="9021d-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="9021d-161">Completa la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="9021d-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="9021d-162">Altri due metodi sono facoltativi e non sono implementati nell'esempio SDK:</span><span class="sxs-lookup"><span data-stu-id="9021d-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="9021d-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="9021d-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="9021d-164">Annulla il metodo [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) .</span><span class="sxs-lookup"><span data-stu-id="9021d-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="9021d-165">Questo metodo è utile per un'origine di rete che può avere una latenza elevata all'avvio.</span><span class="sxs-lookup"><span data-stu-id="9021d-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="9021d-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="9021d-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="9021d-167">Ottiene il numero massimo di byte che il gestore leggerà dal flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="9021d-168">Implementare questo metodo se si conosce la quantità di dati che il gestore del flusso di byte prima può creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="9021d-169">In caso contrario, restituire semplicemente **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="9021d-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="9021d-170">Di seguito è illustrata l'implementazione del metodo [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :</span><span class="sxs-lookup"><span data-stu-id="9021d-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


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



<span data-ttu-id="9021d-171">Il metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="9021d-172">Crea una nuova istanza dell'oggetto `MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="9021d-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="9021d-173">Creare un oggetto risultato asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-173">Create an asynchronous result object.</span></span> <span data-ttu-id="9021d-174">Questo oggetto viene usato in un secondo momento per richiamare il metodo di callback del resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="9021d-175">Chiama `MPEG1Source::BeginOpen` un metodo asincrono definito nella `MPEG1Source` classe.</span><span class="sxs-lookup"><span data-stu-id="9021d-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="9021d-176">Imposta *ppIUnknownCancelCookie* su **null**, che informa il chiamante che [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="9021d-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="9021d-177">Il `MPEG1Source::BeginOpen` metodo esegue l'operazione effettiva di lettura del flusso di byte e di inizializzazione dell' `MPEG1Source` oggetto.</span><span class="sxs-lookup"><span data-stu-id="9021d-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="9021d-178">Questo metodo non fa parte dell'API pubblica.</span><span class="sxs-lookup"><span data-stu-id="9021d-178">This method is not part of the public API.</span></span> <span data-ttu-id="9021d-179">È possibile definire qualsiasi meccanismo tra il gestore e l'origine multimediale più adatta alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="9021d-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="9021d-180">L'inserimento della maggior parte della logica nell'origine multimediale mantiene il gestore del flusso di byte relativamente semplice.</span><span class="sxs-lookup"><span data-stu-id="9021d-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="9021d-181">In breve, `BeginOpen` esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="9021d-182">Chiama [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) per verificare che il flusso di byte di origine sia leggibile e ricercabile.</span><span class="sxs-lookup"><span data-stu-id="9021d-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="9021d-183">Chiama [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) per avviare una richiesta di I/O asincrona.</span><span class="sxs-lookup"><span data-stu-id="9021d-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="9021d-184">Il resto dell'inizializzazione si verifica in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="9021d-185">L'origine multimediale legge dati sufficienti dal flusso per analizzare le intestazioni di sequenza MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9021d-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="9021d-186">Viene quindi creato un *descrittore di presentazione*, ovvero l'oggetto usato per descrivere i flussi audio e video nel file.</span><span class="sxs-lookup"><span data-stu-id="9021d-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="9021d-187">Per ulteriori informazioni, vedere [descrittore della presentazione](#presentation-descriptor). Al `BeginOpen` termine dell'operazione, il gestore del flusso di byte richiama il metodo di callback del resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="9021d-188">A questo punto, il resolver di origine chiama [**IMFByteStreamHandler:: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="9021d-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="9021d-189">Il metodo **EndCreateObject** restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-189">The **EndCreateObject** method returns the status of the operation.</span></span>


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



<span data-ttu-id="9021d-190">Se si verifica un errore in qualsiasi momento durante questo processo, il callback viene richiamato con un codice di stato di errore.</span><span class="sxs-lookup"><span data-stu-id="9021d-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="9021d-191">Descrittore presentazione</span><span class="sxs-lookup"><span data-stu-id="9021d-191">Presentation Descriptor</span></span>

<span data-ttu-id="9021d-192">Il descrittore della presentazione descrive il contenuto del file MPEG-1, incluse le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="9021d-193">Numero di flussi.</span><span class="sxs-lookup"><span data-stu-id="9021d-193">The number of the streams.</span></span>
-   <span data-ttu-id="9021d-194">Formato di ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-194">The format of each stream.</span></span>
-   <span data-ttu-id="9021d-195">Identificatori di flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-195">Stream identifiers.</span></span>
-   <span data-ttu-id="9021d-196">Stato di selezione di ogni flusso (selezionato o deselezionato).</span><span class="sxs-lookup"><span data-stu-id="9021d-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="9021d-197">In termini di architettura Media Foundation, il descrittore di presentazione contiene uno o più descrittori di *flusso*.</span><span class="sxs-lookup"><span data-stu-id="9021d-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="9021d-198">Ogni descrittore di flusso contiene un *gestore di tipo di supporto*, che viene usato per ottenere o impostare i tipi di supporto nel flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="9021d-199">Media Foundation fornisce implementazioni predefinite per il descrittore di presentazione e il descrittore del flusso; sono adatti per la maggior parte delle origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="9021d-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="9021d-200">Per creare un descrittore di presentazione, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9021d-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="9021d-201">Per ogni flusso:</span><span class="sxs-lookup"><span data-stu-id="9021d-201">For each stream:</span></span>
    1.  <span data-ttu-id="9021d-202">Fornire un ID flusso e una matrice di tipi di supporti possibili.</span><span class="sxs-lookup"><span data-stu-id="9021d-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="9021d-203">Se il flusso supporta più di un tipo di supporto, ordinare l'elenco dei tipi di supporto in base alla preferenza, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="9021d-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="9021d-204">(Inserire prima il tipo ottimale e il tipo meno ottimale).</span><span class="sxs-lookup"><span data-stu-id="9021d-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="9021d-205">Chiamare [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) per creare il descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="9021d-206">Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso appena creato.</span><span class="sxs-lookup"><span data-stu-id="9021d-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="9021d-207">Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato predefinito per il flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="9021d-208">Se è presente più di un tipo di supporto, è in genere necessario impostare il primo tipo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="9021d-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="9021d-209">Chiamare [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e passare la matrice di puntatori del descrittore di flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="9021d-210">Per ogni flusso, chiamare [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) o [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) per impostare lo stato di selezione predefinito.</span><span class="sxs-lookup"><span data-stu-id="9021d-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="9021d-211">Se è presente più di un flusso dello stesso tipo (audio o video), per impostazione predefinita è necessario selezionarne solo uno.</span><span class="sxs-lookup"><span data-stu-id="9021d-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="9021d-212">L' `MPEG1Source` oggetto crea il descrittore della presentazione nel `InitPresentationDescriptor` Metodo:</span><span class="sxs-lookup"><span data-stu-id="9021d-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


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



<span data-ttu-id="9021d-213">L'applicazione ottiene il descrittore di presentazione chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9021d-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="9021d-214">Questo metodo crea una copia superficiale del descrittore di presentazione chiamando [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span><span class="sxs-lookup"><span data-stu-id="9021d-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="9021d-215">La copia contiene i puntatori ai descrittori di flusso originali. L'applicazione può usare il descrittore della presentazione per impostare il tipo di supporto, selezionare un flusso o deselezionare un flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="9021d-216">Facoltativamente, i descrittori di presentazione e i descrittori di flusso possono contenere attributi che forniscono informazioni aggiuntive sull'origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="9021d-217">Per un elenco di tali attributi, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="9021d-218">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="9021d-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="9021d-219">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="9021d-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="9021d-220">Un attributo merita menzione speciale: l'attributo della [**\_ \_ durata MF PD**](mf-pd-duration-attribute.md) contiene la durata totale dell'origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="9021d-221">Impostare questo attributo se si conosce la durata di inizio; è ad esempio possibile specificare la durata nelle intestazioni dei file, a seconda del formato di file.</span><span class="sxs-lookup"><span data-stu-id="9021d-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="9021d-222">L'applicazione può visualizzare questo valore o usarlo per impostare un indicatore di stato o una barra di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9021d-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="9021d-223">Stati di streaming</span><span class="sxs-lookup"><span data-stu-id="9021d-223">Streaming States</span></span>

<span data-ttu-id="9021d-224">Un'origine multimediale definisce gli Stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-224">A media source defines the following states:</span></span>



| <span data-ttu-id="9021d-225">State</span><span class="sxs-lookup"><span data-stu-id="9021d-225">State</span></span>    | <span data-ttu-id="9021d-226">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9021d-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9021d-227">Avviato</span><span class="sxs-lookup"><span data-stu-id="9021d-227">Started</span></span>  | <span data-ttu-id="9021d-228">L'origine accetta ed elabora le richieste di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="9021d-229">Paused</span><span class="sxs-lookup"><span data-stu-id="9021d-229">Paused</span></span>   | <span data-ttu-id="9021d-230">L'origine accetta richieste di esempio, ma non le elabora.</span><span class="sxs-lookup"><span data-stu-id="9021d-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="9021d-231">Le richieste vengono accodate fino a quando l'origine non viene avviata.</span><span class="sxs-lookup"><span data-stu-id="9021d-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="9021d-232">Arrestato.</span><span class="sxs-lookup"><span data-stu-id="9021d-232">Stopped.</span></span> | <span data-ttu-id="9021d-233">L'origine rifiuta le richieste di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="9021d-234">Avvio</span><span class="sxs-lookup"><span data-stu-id="9021d-234">Start</span></span>

<span data-ttu-id="9021d-235">Il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) avvia l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9021d-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="9021d-236">È necessario specificare i seguenti parametri:</span><span class="sxs-lookup"><span data-stu-id="9021d-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="9021d-237">Descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="9021d-238">GUID del formato di ora.</span><span class="sxs-lookup"><span data-stu-id="9021d-238">A time-format GUID.</span></span>
-   <span data-ttu-id="9021d-239">Posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="9021d-239">A start position.</span></span>

<span data-ttu-id="9021d-240">L'applicazione deve ottenere il descrittore di presentazione chiamando [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) nell'origine.</span><span class="sxs-lookup"><span data-stu-id="9021d-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="9021d-241">Non esiste alcun meccanismo definito per la convalida di un descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="9021d-242">Se l'applicazione specifica il descrittore di presentazione errato, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="9021d-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="9021d-243">Il GUID del formato di ora specifica come interpretare la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="9021d-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="9021d-244">Il formato standard è 100 unità di nanosecondi (NS), indicate dal GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="9021d-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="9021d-245">Ogni origine multimediale deve supportare unità 100-ns.</span><span class="sxs-lookup"><span data-stu-id="9021d-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="9021d-246">Facoltativamente, un'origine può supportare altre unità di tempo, ad esempio il numero di frame o il codice temporale.</span><span class="sxs-lookup"><span data-stu-id="9021d-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="9021d-247">Tuttavia, non esiste un modo standard per eseguire una query su un'origine multimediale per l'elenco dei formati di tempo supportati.</span><span class="sxs-lookup"><span data-stu-id="9021d-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="9021d-248">La posizione iniziale viene specificata come **PROPVARIANT**, consentendo tipi di dati diversi a seconda del formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="9021d-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="9021d-249">Per 100-ns, il tipo **PROPVARIANT** è **VT \_ i8** o **VT \_ empty**.</span><span class="sxs-lookup"><span data-stu-id="9021d-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="9021d-250">Se **VT \_ i8**, il **PROPVARIANT** contiene la posizione iniziale in unità 100-ns.</span><span class="sxs-lookup"><span data-stu-id="9021d-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="9021d-251">Il valore **VT \_ vuoto** ha il significato speciale "inizia alla posizione corrente".</span><span class="sxs-lookup"><span data-stu-id="9021d-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="9021d-252">Implementare il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) come segue:</span><span class="sxs-lookup"><span data-stu-id="9021d-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="9021d-253">Convalida parametri e stato:</span><span class="sxs-lookup"><span data-stu-id="9021d-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="9021d-254">Verificare la presenza di parametri **null** .</span><span class="sxs-lookup"><span data-stu-id="9021d-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="9021d-255">Controllare il GUID del formato di ora.</span><span class="sxs-lookup"><span data-stu-id="9021d-255">Check the time-format GUID.</span></span> <span data-ttu-id="9021d-256">Se il valore non è valido, restituire il **\_ formato di \_ \_ ora non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="9021d-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="9021d-257">Controllare il tipo di dati di **PROPVARIANT** che include la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="9021d-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="9021d-258">Convalidare la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="9021d-258">Validate the start position.</span></span> <span data-ttu-id="9021d-259">Se non è valido, restituire **MF \_ E \_ INVALIDREQUEST**.</span><span class="sxs-lookup"><span data-stu-id="9021d-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="9021d-260">Se l'origine è stata arrestata, restituire **MF \_ E \_ Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="9021d-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="9021d-261">Se non si verificano errori nel passaggio 1, accodare un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9021d-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="9021d-262">Tutti gli elementi dopo questo passaggio si verificano in un thread della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="9021d-263">Per ogni flusso:</span><span class="sxs-lookup"><span data-stu-id="9021d-263">For each stream:</span></span>
    1.  <span data-ttu-id="9021d-264">Controllare se il flusso è già attivo da una precedente richiesta di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) .</span><span class="sxs-lookup"><span data-stu-id="9021d-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="9021d-265">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per verificare se l'applicazione ha selezionato o deselezionato il flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="9021d-266">Se un flusso selezionato in precedenza è ora deselezionato, scaricare tutti gli esempi non recapitati per tale flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="9021d-267">Se il flusso è attivo, l'origine del supporto (non il flusso) Invia uno degli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="9021d-268">Invia [MEUpdatedStream](meupdatedstream.md) se il flusso era precedentemente attivo.</span><span class="sxs-lookup"><span data-stu-id="9021d-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="9021d-269">In caso contrario, invia [MENewStream](menewstream.md).</span><span class="sxs-lookup"><span data-stu-id="9021d-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="9021d-270">Per entrambi gli eventi, i dati dell'evento sono il puntatore [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="9021d-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="9021d-271">Se l'origine viene riavviata dallo stato sospeso, potrebbero essere presenti richieste di esempio in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9021d-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="9021d-272">In tal caso, è possibile recapitarli adesso.</span><span class="sxs-lookup"><span data-stu-id="9021d-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="9021d-273">Se l'origine sta cercando in una nuova posizione, ogni oggetto flusso Invia un evento [MEStreamSeeked](mestreamseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="9021d-274">In caso contrario, ogni flusso Invia un evento [MEStreamStarted](mestreamstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="9021d-275">Se l'origine sta cercando in una nuova posizione, l'origine multimediale Invia un evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="9021d-276">In caso contrario, invia un evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="9021d-277">Se si verifica un errore in qualsiasi momento dopo il passaggio 2, l'origine invia un evento [MESourceStarted](mesourcestarted.md) con un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="9021d-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="9021d-278">Viene avvisato l'applicazione che il metodo di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) non è riuscito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="9021d-279">Il codice seguente illustra i passaggi da 1 a 2:</span><span class="sxs-lookup"><span data-stu-id="9021d-279">The following code shows steps 1–2:</span></span>


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



<span data-ttu-id="9021d-280">I passaggi rimanenti sono illustrati nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9021d-280">The remaining steps are shown in the next example:</span></span>


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



### <a name="pause"></a><span data-ttu-id="9021d-281">Sospendi</span><span class="sxs-lookup"><span data-stu-id="9021d-281">Pause</span></span>

<span data-ttu-id="9021d-282">Il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) mette in pausa l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9021d-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="9021d-283">Implementare questo metodo come segue:</span><span class="sxs-lookup"><span data-stu-id="9021d-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="9021d-284">Accoda un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9021d-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="9021d-285">Ogni flusso attivo Invia un evento [MEStreamPaused](mestreampaused.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="9021d-286">L'origine multimediale Invia un evento [MESourcePaused](mesourcepaused.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="9021d-287">Durante la sospensione, le code di origine vengono richieste di esempio senza elaborarle.</span><span class="sxs-lookup"><span data-stu-id="9021d-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="9021d-288">(Vedere [le richieste di esempio](#sample-requests)).</span><span class="sxs-lookup"><span data-stu-id="9021d-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="9021d-289">Interrompere</span><span class="sxs-lookup"><span data-stu-id="9021d-289">Stop</span></span>

<span data-ttu-id="9021d-290">Il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) interrompe l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9021d-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="9021d-291">Implementare questo metodo come segue:</span><span class="sxs-lookup"><span data-stu-id="9021d-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="9021d-292">Accoda un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9021d-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="9021d-293">Ogni flusso attivo Invia un evento [MEStreamStopped](mestreamstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="9021d-294">Cancellare tutti gli esempi in coda e le richieste di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="9021d-295">L'origine multimediale Invia un evento [MESourceStopped](mesourcestopped.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="9021d-296">Durante l'arresto, l'origine rifiuta tutte le richieste per gli esempi.</span><span class="sxs-lookup"><span data-stu-id="9021d-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="9021d-297">Se l'origine viene arrestata mentre è in corso una richiesta di I/O, la richiesta di I/O può essere completata dopo che l'origine entra nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="9021d-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="9021d-298">In tal caso, l'origine deve eliminare il risultato della richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="9021d-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="9021d-299">Richieste di esempio</span><span class="sxs-lookup"><span data-stu-id="9021d-299">Sample Requests</span></span>

<span data-ttu-id="9021d-300">Media Foundation usare un modello *pull* , in cui la pipeline richiede esempi dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="9021d-301">Questo comportamento è diverso rispetto al modello usato da DirectShow, in cui sono presenti gli esempi "push" delle origini.</span><span class="sxs-lookup"><span data-stu-id="9021d-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="9021d-302">Per richiedere un nuovo esempio, la pipeline Media Foundation chiama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="9021d-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="9021d-303">Questo metodo accetta un puntatore **IUnknown** che rappresenta un oggetto *token* .</span><span class="sxs-lookup"><span data-stu-id="9021d-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="9021d-304">L'implementazione dell'oggetto token spetta al chiamante. fornisce semplicemente un modo per il chiamante per tenere traccia delle richieste di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="9021d-305">Anche il parametro del token può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9021d-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="9021d-306">Supponendo che l'origine usi richieste di I/O asincrone per leggere i dati, la generazione di esempio non verrà sincronizzata con le richieste di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="9021d-307">Per sincronizzare le richieste di esempio con la generazione di esempio, un'origine multimediale esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="9021d-308">I token della richiesta vengono inseriti in una coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="9021d-309">Man mano che vengono generati esempi, vengono inseriti in una seconda coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="9021d-310">L'origine multimediale completa una richiesta di esempio estraendo un token di richiesta dalla prima coda e un campione dalla seconda coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="9021d-311">L'origine multimediale Invia un evento MEMediaSample.</span><span class="sxs-lookup"><span data-stu-id="9021d-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="9021d-312">L'evento contiene un puntatore all'esempio e l'esempio contiene un puntatore al token.</span><span class="sxs-lookup"><span data-stu-id="9021d-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="9021d-313">Il diagramma seguente illustra la relazione tra l'evento [MEMediaSample](memediasample.md) , l'esempio e il token della richiesta.</span><span class="sxs-lookup"><span data-stu-id="9021d-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![diagramma che mostra memediasample e una coda di esempio che punta a IMFSample; IMFSample e la coda di richieste puntano a IUnknown](images/mediasourceimpl01.png)

<span data-ttu-id="9021d-315">L'origine MPEG-1 di esempio implementa questo processo nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="9021d-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="9021d-316">Il metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) inserisce la richiesta in una coda FIFO.</span><span class="sxs-lookup"><span data-stu-id="9021d-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="9021d-317">Quando le richieste di I/O vengono completate, l'origine multimediale crea nuovi esempi e li inserisce in una seconda coda FIFO.</span><span class="sxs-lookup"><span data-stu-id="9021d-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="9021d-318">Questa coda ha una dimensione massima per impedire che l'origine legga troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="9021d-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="9021d-319">Ogni volta che entrambe le code hanno almeno un elemento (una richiesta e un campione), l'origine multimediale completa la prima richiesta dalla coda delle richieste inviando il primo esempio dalla coda di esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="9021d-320">Per recapitare un esempio, l'oggetto flusso (non l'oggetto di origine) Invia un evento [MEMediaSample](memediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="9021d-321">I dati dell'evento sono un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="9021d-322">Se la richiesta include un token, allegare il token all'esempio impostando l'attributo del [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9021d-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="9021d-323">A questo punto, sono disponibili tre possibilità:</span><span class="sxs-lookup"><span data-stu-id="9021d-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="9021d-324">È presente un altro esempio nella coda di esempio, ma nessuna richiesta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9021d-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="9021d-325">È presente una richiesta, ma non un campione.</span><span class="sxs-lookup"><span data-stu-id="9021d-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="9021d-326">Entrambe le code sono vuote. non sono presenti esempi e richieste.</span><span class="sxs-lookup"><span data-stu-id="9021d-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="9021d-327">Se la coda di esempio è vuota, l'origine controlla la fine del flusso (vedere la [fine del flusso](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="9021d-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="9021d-328">In caso contrario, viene avviata un'altra richiesta di I/O per i dati.</span><span class="sxs-lookup"><span data-stu-id="9021d-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="9021d-329">Se si verifica un errore durante questo processo, il flusso Invia un evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="9021d-330">Il codice seguente implementa il metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :</span><span class="sxs-lookup"><span data-stu-id="9021d-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


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



<span data-ttu-id="9021d-331">Il `DispatchSamples` metodo estrae gli esempi dalla coda di esempio, li associa alle richieste di esempio in sospeso e gli eventi [MEMediaSample](memediasample.md) di Accodamento:</span><span class="sxs-lookup"><span data-stu-id="9021d-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


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



<span data-ttu-id="9021d-332">Il `DispatchSamples` metodo viene chiamato nelle circostanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="9021d-333">All'interno del metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="9021d-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="9021d-334">Quando l'origine multimediale viene riavviata dallo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="9021d-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="9021d-335">Quando viene completata una richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="9021d-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="9021d-336">Fine del flusso</span><span class="sxs-lookup"><span data-stu-id="9021d-336">End of Stream</span></span>

<span data-ttu-id="9021d-337">Quando un flusso non contiene più dati e tutti gli esempi per tale flusso sono stati recapitati, gli oggetti flusso inviano un evento [MEEndOfStream](meendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="9021d-338">Quando tutti i flussi attivi vengono eseguiti, l'origine multimediale Invia un evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="9021d-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="9021d-339">Operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="9021d-339">Asynchronous Operations</span></span>

<span data-ttu-id="9021d-340">Probabilmente la parte più difficile della scrittura di un'origine multimediale consiste nel comprendere il Media Foundation modello asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="9021d-341">Tutti i metodi in un'origine multimediale che controllano il flusso sono asincroni.</span><span class="sxs-lookup"><span data-stu-id="9021d-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="9021d-342">In ogni caso, il metodo esegue una convalida iniziale, ad esempio il controllo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9021d-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="9021d-343">L'origine invia quindi il resto del lavoro a una coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="9021d-344">Al termine dell'operazione, l'origine multimediale Invia un evento al chiamante tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="9021d-345">È quindi importante comprendere le code di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="9021d-346">Per inserire un elemento in una coda di lavoro, è possibile chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span><span class="sxs-lookup"><span data-stu-id="9021d-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="9021d-347">L'origine MPEG-1 USA **MFPutWorkItem**, ma le due funzioni eseguono la stessa operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="9021d-348">La funzione **MFPutWorkItem** accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="9021d-349">Valore **DWORD** che identifica la coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="9021d-350">È possibile creare una coda di lavoro privata o usare lo **\_ standard della \_ coda \_ di callback MFASYNC**.</span><span class="sxs-lookup"><span data-stu-id="9021d-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="9021d-351">Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="9021d-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="9021d-352">Questa interfaccia di callback viene richiamata per eseguire il lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="9021d-353">Oggetto di stato facoltativo, che deve implementare **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9021d-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="9021d-354">La coda di lavoro viene gestita da uno o più thread di lavoro che effettuano il pull continuo del successivo elemento di lavoro dalla coda e richiamano il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'interfaccia di callback.</span><span class="sxs-lookup"><span data-stu-id="9021d-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="9021d-355">Non è garantito che gli elementi di lavoro vengano eseguiti nello stesso ordine in cui sono stati inseriti nella coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="9021d-356">Si tenga presente che più thread possono servire la stessa coda di lavoro, quindi le chiamate [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) possono sovrapporsi o non essere presenti in ordine.</span><span class="sxs-lookup"><span data-stu-id="9021d-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="9021d-357">Pertanto, spetta all'origine multimediale mantenere lo stato interno corretto inviando elementi della coda di lavoro nell'ordine corretto.</span><span class="sxs-lookup"><span data-stu-id="9021d-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="9021d-358">Solo quando l'operazione precedente è completa, l'origine avvia l'operazione successiva.</span><span class="sxs-lookup"><span data-stu-id="9021d-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="9021d-359">Per rappresentare le operazioni in sospeso, l'origine MPEG-1 definisce una classe denominata `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="9021d-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


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



<span data-ttu-id="9021d-360">L' `Operation` enumerazione identifica l'operazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9021d-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="9021d-361">La classe contiene anche un **PROPVARIANT** per fornire dati aggiuntivi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="9021d-362">Coda operazioni</span><span class="sxs-lookup"><span data-stu-id="9021d-362">Operation Queue</span></span>

<span data-ttu-id="9021d-363">Per serializzare le operazioni, l'origine multimediale mantiene una coda di `SourceOp` oggetti.</span><span class="sxs-lookup"><span data-stu-id="9021d-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="9021d-364">Usa una classe helper per gestire la coda:</span><span class="sxs-lookup"><span data-stu-id="9021d-364">It uses a helper class to manage the queue:</span></span>


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



<span data-ttu-id="9021d-365">La `OpQueue` classe è progettata per essere ereditata dal componente che esegue gli elementi di lavoro asincroni.</span><span class="sxs-lookup"><span data-stu-id="9021d-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="9021d-366">Il parametro del modello di *\_ tipo op* è il tipo di oggetto usato per rappresentare gli elementi di lavoro nella coda, in questo caso il *\_ tipo op* sarà `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="9021d-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="9021d-367">La `OpQueue` classe implementa i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9021d-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="9021d-368">`QueueOperation` inserisce un nuovo elemento nella coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="9021d-369">`ProcessQueue` Invia l'operazione successiva dalla coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="9021d-370">Questo metodo è asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="9021d-371">`ProcessQueueAsync` completa il metodo asincrono `ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="9021d-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="9021d-372">Altri due metodi devono essere implementati dalla classe derivata:</span><span class="sxs-lookup"><span data-stu-id="9021d-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="9021d-373">`ValidateOperation` Verifica se è valido per eseguire un'operazione specificata, dato lo stato corrente dell'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="9021d-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="9021d-374">`DispatchOperation` esegue l'elemento di lavoro asincrono.</span><span class="sxs-lookup"><span data-stu-id="9021d-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="9021d-375">La coda delle operazioni viene utilizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="9021d-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="9021d-376">La pipeline Media Foundation chiama un metodo asincrono sull'origine multimediale, ad esempio [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="9021d-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="9021d-377">Il metodo asincrono chiama `QueueOperation` , che inserisce l'operazione di [**avvio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) nella coda e chiama `ProcessQueue` (sotto forma di `SourceOp` oggetto).</span><span class="sxs-lookup"><span data-stu-id="9021d-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="9021d-378">`ProcessQueue` chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="9021d-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="9021d-379">Il thread della coda di lavoro chiama `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="9021d-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="9021d-380">Il `ProcessQueueAsync` metodo chiama `ValidateOperation` e `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="9021d-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="9021d-381">Il codice seguente Accoda una nuova operazione sull'origine MPEG-1:</span><span class="sxs-lookup"><span data-stu-id="9021d-381">The following code queues a new operation on the MPEG-1 source:</span></span>


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



<span data-ttu-id="9021d-382">Il codice seguente elabora la coda:</span><span class="sxs-lookup"><span data-stu-id="9021d-382">The following code processes the queue:</span></span>


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



<span data-ttu-id="9021d-383">Il `ValidateOperation` metodo controlla se l'origine MPEG-1 può inviare l'operazione successiva nella coda.</span><span class="sxs-lookup"><span data-stu-id="9021d-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="9021d-384">Se è in corso un'altra operazione, `ValidateOperation` restituisce **MF \_ E \_ NOTACCEPTING**.</span><span class="sxs-lookup"><span data-stu-id="9021d-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="9021d-385">Ciò garantisce che `DispatchOperation` non venga chiamato mentre è in sospeso un'altra operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


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



<span data-ttu-id="9021d-386">Il metodo DispatchOperation passa al tipo di operazione:</span><span class="sxs-lookup"><span data-stu-id="9021d-386">The DispatchOperation method switches on the operation type:</span></span>


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



<span data-ttu-id="9021d-387">Per concludere:</span><span class="sxs-lookup"><span data-stu-id="9021d-387">To summarize:</span></span>

1.  <span data-ttu-id="9021d-388">La pipeline chiama un metodo asincrono, ad esempio [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="9021d-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="9021d-389">Il metodo asincrono chiama `OpQueue::QueueOperation` , passando un puntatore a un `SourceOp` oggetto.</span><span class="sxs-lookup"><span data-stu-id="9021d-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="9021d-390">Il `QueueOperation` metodo inserisce l'operazione sulla coda *m \_ OpQueue* e chiama `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="9021d-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="9021d-391">Il `ProcessQueue` metodo chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="9021d-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="9021d-392">Da questo punto, tutto avviene in un Media Foundation thread della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9021d-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="9021d-393">Il metodo asincrono restituisce al chiamante.</span><span class="sxs-lookup"><span data-stu-id="9021d-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="9021d-394">Il thread della coda di lavoro chiama il `OpQueue::ProcessQueueAsync` metodo.</span><span class="sxs-lookup"><span data-stu-id="9021d-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="9021d-395">Il `ProcessQueueAsync` metodo chiama `MPEG1Source:ValidateOperation` per convalidare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="9021d-396">Il `ProcessQueueAsync` metodo chiama `MPEG1Source::DispatchOperation` per elaborare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9021d-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="9021d-397">Questa progettazione presenta diversi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="9021d-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="9021d-398">I metodi sono asincroni, quindi non bloccano il thread dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="9021d-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="9021d-399">Le operazioni vengono inviate in un thread della coda di lavoro Media Foundation, condiviso tra i componenti della pipeline.</span><span class="sxs-lookup"><span data-stu-id="9021d-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="9021d-400">Pertanto, l'origine multimediale non crea il proprio thread, riducendo il numero totale di thread creati.</span><span class="sxs-lookup"><span data-stu-id="9021d-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="9021d-401">L'origine multimediale non si blocca durante l'attesa del completamento delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="9021d-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="9021d-402">In questo modo si riduce la probabilità che un'origine multimediale provochi accidentalmente un deadlock e contribuisca a ridurre il cambio del contesto.</span><span class="sxs-lookup"><span data-stu-id="9021d-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="9021d-403">L'origine multimediale può usare l'I/O asincrono per leggere il file di origine (chiamando [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="9021d-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="9021d-404">Non è necessario bloccare l'origine multimediale durante l'attesa del completamento della routine di I/O.</span><span class="sxs-lookup"><span data-stu-id="9021d-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="9021d-405">Se si segue il modello illustrato nell'esempio SDK, è possibile concentrarsi sui dettagli specifici dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="9021d-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9021d-406">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9021d-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9021d-407">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="9021d-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="9021d-408">Scrittura di un'origine multimediale personalizzata</span><span class="sxs-lookup"><span data-stu-id="9021d-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



