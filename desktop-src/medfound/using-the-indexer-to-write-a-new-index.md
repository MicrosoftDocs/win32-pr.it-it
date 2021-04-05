---
description: In questo argomento viene illustrato come scrivere un indice per un file di formato Advanced Systems (ASF).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Uso dell'indicizzatore per scrivere un nuovo indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753834"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="31201-103">Uso dell'indicizzatore per scrivere un nuovo indice</span><span class="sxs-lookup"><span data-stu-id="31201-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="31201-104">In questo argomento viene illustrato come scrivere un indice per un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="31201-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="31201-105">Di seguito è riportata la procedura generale per la creazione di un indice ASF:</span><span class="sxs-lookup"><span data-stu-id="31201-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="31201-106">Inizializzare una nuova istanza dell'oggetto indicizzatore ASF, come descritto in [creazione e configurazione dell'indicizzatore](indexer-creation-and-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="31201-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="31201-107">Facoltativamente, configurare l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="31201-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="31201-108">Inviare pacchetti di dati ASF all'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="31201-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="31201-109">Eseguire il commit dell'indice.</span><span class="sxs-lookup"><span data-stu-id="31201-109">Commit the index.</span></span>
5.  <span data-ttu-id="31201-110">Ottenere l'indice completato dall'indicizzatore e scriverlo in un flusso.</span><span class="sxs-lookup"><span data-stu-id="31201-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="31201-111">Configurare l'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="31201-111">Configure the Indexer</span></span>

<span data-ttu-id="31201-112">Per usare l'indicizzatore per scrivere un nuovo oggetto index, l'oggetto indicizzatore deve avere il flag MFASF \_ indexer \_ Write \_ New \_ index set con una chiamata a [**IMFASFIndexer:: Flags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) prima che venga inizializzato con [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="31201-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="31201-113">Quando l'indicizzatore è configurato per la scrittura di un indice, il chiamante sceglie i flussi da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="31201-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="31201-114">Per impostazione predefinita, l'indicizzatore tenta di creare un oggetto indice per tutti i flussi.</span><span class="sxs-lookup"><span data-stu-id="31201-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="31201-115">L'intervallo di tempo predefinito è un secondo.</span><span class="sxs-lookup"><span data-stu-id="31201-115">The default time interval is one second.</span></span>

<span data-ttu-id="31201-116">[**IMFASFIndexer:: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) può essere usato per eseguire l'override della scelta predefinita dei flussi e dei tipi di indice dell'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="31201-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="31201-117">Nell'esempio di codice seguente viene illustrata l'inizializzazione di un \_ descrittore dell'indice ASF e di un \_ \_ \_ identificatore di indice ASF prima di una chiamata a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="31201-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="31201-118">Il tipo di indice GUID dell'identificatore di indice deve essere impostato su GUID \_ null per indicare che il tipo di indice sarà basato sul tempo di presentazione.</span><span class="sxs-lookup"><span data-stu-id="31201-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="31201-119">È inoltre necessario inizializzare l'identificatore di indice con il numero di flusso del flusso ASF da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="31201-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="31201-120">Una volta impostato l'identificatore di indice, utilizzarlo per inizializzare il descrittore dell'indice.</span><span class="sxs-lookup"><span data-stu-id="31201-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="31201-121">La struttura del descrittore di indice dispone di membri che devono essere impostati prima della chiamata a [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="31201-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="31201-122">**Identifier** è una struttura dell' [**\_ \_ identificatore di indice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) che identifica il numero di flusso e il tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="31201-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="31201-123">**cPerEntryBytes** è il numero di byte utilizzati per ogni voce di indice.</span><span class="sxs-lookup"><span data-stu-id="31201-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="31201-124">Se il valore è MFASFINDEXER \_ per \_ ogni \_ byte di immissione \_ dinamica, le voci di indice hanno dimensioni variabili.</span><span class="sxs-lookup"><span data-stu-id="31201-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="31201-125">**dwInterval** è l'intervallo di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="31201-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="31201-126">Il valore MFASFINDEXER \_ senza \_ intervallo fisso \_ indica che non è presente alcun intervallo di indicizzazione fissa.</span><span class="sxs-lookup"><span data-stu-id="31201-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="31201-127">Inviare pacchetti di dati ASF all'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="31201-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="31201-128">Poiché l'indicizzatore è un oggetto a livello di WMContainer, deve essere usato insieme al multiplexer durante la generazione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="31201-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="31201-129">I pacchetti restituiti da [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) possono essere inviati all'oggetto indicizzatore tramite chiamate a [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , in cui vengono create voci di indice per ogni pacchetto inviato.</span><span class="sxs-lookup"><span data-stu-id="31201-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="31201-130">Il codice seguente illustra come eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="31201-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="31201-131">Per ulteriori informazioni, vedere [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="31201-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="31201-132">Eseguire il commit dell'indice</span><span class="sxs-lookup"><span data-stu-id="31201-132">Commit the Index</span></span>

<span data-ttu-id="31201-133">Dopo che per l'ultimo pacchetto è stata creata una voce di indice, è necessario eseguire il commit dell'indice.</span><span class="sxs-lookup"><span data-stu-id="31201-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="31201-134">Questa operazione viene eseguita con una chiamata a [**IMFASFIndexer:: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="31201-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="31201-135">**CommitIndex** accetta un puntatore all'oggetto ContentInfo che descrive il contenuto del file ASF.</span><span class="sxs-lookup"><span data-stu-id="31201-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="31201-136">Il commit dell'indice completa l'indicizzazione e aggiorna l'intestazione con nuove informazioni sulle dimensioni dei file e la ricercabilità.</span><span class="sxs-lookup"><span data-stu-id="31201-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="31201-137">Ottenere l'indice completato</span><span class="sxs-lookup"><span data-stu-id="31201-137">Get the Completed Index</span></span>

<span data-ttu-id="31201-138">Per ottenere l'indice completato dall'indicizzatore, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="31201-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="31201-139">Chiamare [**IMFASFIndexer:: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) per ottenere le dimensioni dell'indice.</span><span class="sxs-lookup"><span data-stu-id="31201-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="31201-140">Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="31201-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="31201-141">È possibile allocare un buffer sufficientemente grande da mantenere l'intero indice, allocare un buffer più piccolo e ottenere l'indice in blocchi.</span><span class="sxs-lookup"><span data-stu-id="31201-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="31201-142">Chiamare [**IMFASFIndexer:: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) per ottenere i dati dell'indice.</span><span class="sxs-lookup"><span data-stu-id="31201-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="31201-143">Alla prima chiamata, impostare il parametro *cbOffsetWithinIndex* su zero.</span><span class="sxs-lookup"><span data-stu-id="31201-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="31201-144">Se si ottiene l'indice in blocchi, incrementare *cbOffsetWithinIndex* ogni volta per la dimensione dei dati della chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="31201-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="31201-145">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore ai dati dell'indice e le dimensioni dei dati.</span><span class="sxs-lookup"><span data-stu-id="31201-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="31201-146">Scrivere i dati dell'indice nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="31201-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="31201-147">Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="31201-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="31201-148">Ripetere i passaggi da 3 a 6 fino a quando non si scrive l'intero indice.</span><span class="sxs-lookup"><span data-stu-id="31201-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="31201-149">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="31201-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="31201-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31201-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31201-151">Indicizzatore ASF</span><span class="sxs-lookup"><span data-stu-id="31201-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



