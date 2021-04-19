---
description: L'indicizzatore ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF). In questo argomento vengono fornite informazioni sull'utilizzo dell'indicizzatore ASF per la ricerca all'interno di un file ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Utilizzo dell'indicizzatore per la ricerca all'interno di un file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310171"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="855b5-104">Utilizzo dell'indicizzatore per la ricerca all'interno di un file ASF</span><span class="sxs-lookup"><span data-stu-id="855b5-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="855b5-105">L' *indicizzatore* ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="855b5-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="855b5-106">In questo argomento vengono fornite informazioni sull'utilizzo dell'indicizzatore ASF per la ricerca all'interno di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="855b5-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="855b5-107">Inizializzazione dell'indicizzatore per la ricerca</span><span class="sxs-lookup"><span data-stu-id="855b5-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="855b5-108">Recupero della posizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="855b5-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="855b5-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="855b5-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="855b5-110">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="855b5-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="855b5-111">Inizializzazione dell'indicizzatore per la ricerca</span><span class="sxs-lookup"><span data-stu-id="855b5-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="855b5-112">Per inizializzare l'indicizzatore ASF per la ricerca:</span><span class="sxs-lookup"><span data-stu-id="855b5-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="855b5-113">Chiamare [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) per creare una nuova istanza dell'indicizzatore ASF.</span><span class="sxs-lookup"><span data-stu-id="855b5-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="855b5-114">Chiamare [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) per inizializzare l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="855b5-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="855b5-115">Questo metodo ottiene le informazioni dall'intestazione ASF per determinare quali flussi ASF sono indicizzati.</span><span class="sxs-lookup"><span data-stu-id="855b5-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="855b5-116">Per impostazione predefinita, l'oggetto indicizzatore è configurato per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="855b5-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="855b5-117">Chiamare [**IMFASFIndexer:: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) per trovare l'offset dell'indice all'interno del file ASF.</span><span class="sxs-lookup"><span data-stu-id="855b5-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="855b5-118">Chiamare la funzione [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) per creare un flusso di byte per la lettura dell'indice.</span><span class="sxs-lookup"><span data-stu-id="855b5-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="855b5-119">L'input per questa funzione è un puntatore a un flusso di byte che contiene il file ASF e l'offset dell'indice (dal passaggio precedente).</span><span class="sxs-lookup"><span data-stu-id="855b5-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="855b5-120">Chiamare [**IMFASFIndexer:: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) per impostare il flusso di byte di indice nell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="855b5-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="855b5-121">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="855b5-121">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a><span data-ttu-id="855b5-122">Recupero della posizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="855b5-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="855b5-123">Per determinare se un determinato flusso è indicizzato, chiamare [**IMFASFIndexer:: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span><span class="sxs-lookup"><span data-stu-id="855b5-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="855b5-124">Se il flusso è indicizzato, il parametro *pfIsIndexed* riceve il valore **true**; in caso contrario, riceve il valore **false**.</span><span class="sxs-lookup"><span data-stu-id="855b5-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="855b5-125">Per impostazione predefinita, l'indicizzatore usa la ricerca in diretta.</span><span class="sxs-lookup"><span data-stu-id="855b5-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="855b5-126">Per la ricerca inversa, ovvero la ricerca dalla fine del file, chiamare [**IMFASFIndexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) e impostare l' **\_ indicizzatore MFASF \_ Read \_ per \_ REVERSEPLAYBACK** flag.</span><span class="sxs-lookup"><span data-stu-id="855b5-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="855b5-127">In caso contrario, ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="855b5-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="855b5-128">Se il flusso è indicizzato, ottenere la posizione di ricerca per un'ora di presentazione specificata chiamando [**IMFASFIndexer:: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span><span class="sxs-lookup"><span data-stu-id="855b5-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="855b5-129">Questo metodo legge l'indice ASF e trova la voce di indice più vicina al tempo richiesto.</span><span class="sxs-lookup"><span data-stu-id="855b5-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="855b5-130">Il metodo restituisce l'offset dei byte del pacchetto di dati specificato dalla voce di indice.</span><span class="sxs-lookup"><span data-stu-id="855b5-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="855b5-131">L'offset dei byte è relativo all'inizio dell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="855b5-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="855b5-132">Il metodo [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) accetta un puntatore alla struttura [**dell' \_ \_ identificatore di indice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) .</span><span class="sxs-lookup"><span data-stu-id="855b5-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="855b5-133">Questa struttura specifica un tipo di indice e un identificatore di flusso.</span><span class="sxs-lookup"><span data-stu-id="855b5-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="855b5-134">Attualmente, il tipo di indice deve essere un GUID \_ null, che specifica l'indicizzazione basata sul tempo.</span><span class="sxs-lookup"><span data-stu-id="855b5-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="855b5-135">Il codice seguente ottiene una posizione di ricerca, dati un identificatore del flusso e l'ora di presentazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="855b5-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="855b5-136">Se la chiamata ha esito positivo, restituisce l'offset dei dati nel parametro *pcbDataOffset* e il tempo di ricerca effettivo approssimativo in *phnsApproxSeekTime*.</span><span class="sxs-lookup"><span data-stu-id="855b5-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="855b5-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="855b5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855b5-138">Indicizzatore ASF</span><span class="sxs-lookup"><span data-stu-id="855b5-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



