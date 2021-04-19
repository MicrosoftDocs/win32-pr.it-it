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
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Utilizzo dell'indicizzatore per la ricerca all'interno di un file ASF

L' *indicizzatore* ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF). In questo argomento vengono fornite informazioni sull'utilizzo dell'indicizzatore ASF per la ricerca all'interno di un file ASF.

-   [Inizializzazione dell'indicizzatore per la ricerca](#initializing-the-indexer-for-seeking)
-   [Recupero della posizione di ricerca.](#getting-the-seek-position)
-   [Argomenti correlati](#related-topics)

Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Inizializzazione dell'indicizzatore per la ricerca

Per inizializzare l'indicizzatore ASF per la ricerca:

1.  Chiamare [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) per creare una nuova istanza dell'indicizzatore ASF.
2.  Chiamare [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) per inizializzare l'indicizzatore. Questo metodo ottiene le informazioni dall'intestazione ASF per determinare quali flussi ASF sono indicizzati. Per impostazione predefinita, l'oggetto indicizzatore è configurato per la ricerca.
3.  Chiamare [**IMFASFIndexer:: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) per trovare l'offset dell'indice all'interno del file ASF.
4.  Chiamare la funzione [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) per creare un flusso di byte per la lettura dell'indice. L'input per questa funzione è un puntatore a un flusso di byte che contiene il file ASF e l'offset dell'indice (dal passaggio precedente).
5.  Chiamare [**IMFASFIndexer:: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) per impostare il flusso di byte di indice nell'indicizzatore.

Il codice seguente illustra questi passaggi:


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



## <a name="getting-the-seek-position"></a>Recupero della posizione di ricerca.

1.  Per determinare se un determinato flusso è indicizzato, chiamare [**IMFASFIndexer:: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Se il flusso è indicizzato, il parametro *pfIsIndexed* riceve il valore **true**; in caso contrario, riceve il valore **false**.
2.  Per impostazione predefinita, l'indicizzatore usa la ricerca in diretta. Per la ricerca inversa, ovvero la ricerca dalla fine del file, chiamare [**IMFASFIndexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) e impostare l' **\_ indicizzatore MFASF \_ Read \_ per \_ REVERSEPLAYBACK** flag. In caso contrario, ignorare questo passaggio.
3.  Se il flusso è indicizzato, ottenere la posizione di ricerca per un'ora di presentazione specificata chiamando [**IMFASFIndexer:: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Questo metodo legge l'indice ASF e trova la voce di indice più vicina al tempo richiesto. Il metodo restituisce l'offset dei byte del pacchetto di dati specificato dalla voce di indice. L'offset dei byte è relativo all'inizio dell'oggetto dati ASF.

Il metodo [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) accetta un puntatore alla struttura [**dell' \_ \_ identificatore di indice ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) . Questa struttura specifica un tipo di indice e un identificatore di flusso. Attualmente, il tipo di indice deve essere un GUID \_ null, che specifica l'indicizzazione basata sul tempo.

Il codice seguente ottiene una posizione di ricerca, dati un identificatore del flusso e l'ora di presentazione di destinazione. Se la chiamata ha esito positivo, restituisce l'offset dei dati nel parametro *pcbDataOffset* e il tempo di ricerca effettivo approssimativo in *phnsApproxSeekTime*.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzatore ASF](asf-index-object.md)
</dt> </dl>

 

 



