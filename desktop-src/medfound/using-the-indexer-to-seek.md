---
description: L'indicizzatore ASF è un componente del livello WMContainer usato per leggere o scrivere oggetti indice in un file ASF (Advanced Systems Format). In questo argomento vengono fornite informazioni sull'uso dell'indicizzatore ASF per la ricerca all'interno di un file ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Uso dell'indicizzatore per la ricerca all'interno di un file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c674aa809c858856abf0c0e84c5d854b399c6fbc125ac9210e19b695380bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887241"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Uso dell'indicizzatore per la ricerca all'interno di un file ASF

*L'indicizzatore* ASF è un componente del livello WMContainer usato per leggere o scrivere oggetti indice in un file ASF (Advanced Systems Format). In questo argomento vengono fornite informazioni sull'uso dell'indicizzatore ASF per la ricerca all'interno di un file ASF.

-   [Inizializzazione dell'indicizzatore per la ricerca](#initializing-the-indexer-for-seeking)
-   [Recupero della posizione seek.](#getting-the-seek-position)
-   [Argomenti correlati](#related-topics)

Per informazioni sulla struttura di un file ASF, vedere [Struttura del file ASF.](asf-file-structure.md)

## <a name="initializing-the-indexer-for-seeking"></a>Inizializzazione dell'indicizzatore per la ricerca

Per inizializzare l'indicizzatore ASF per la ricerca:

1.  Chiamare [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) per creare una nuova istanza dell'indicizzatore ASF.
2.  Chiamare [**IMFASFIndexer::Initialize per**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) inizializzare l'indicizzatore. Questo metodo ottiene informazioni dall'intestazione ASF per determinare quali flussi asf vengono indicizzati. Per impostazione predefinita, l'oggetto indicizzatore è configurato per la ricerca.
3.  Chiamare [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) per trovare l'offset dell'indice all'interno del file ASF.
4.  Chiamare la [**funzione MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) per creare un flusso di byte per la lettura dell'indice. L'input per questa funzione è un puntatore a un flusso di byte che contiene il file ASF e l'offset dell'indice (dal passaggio precedente).
5.  Chiamare [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) per impostare il flusso di byte dell'indice nell'indicizzatore.

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



## <a name="getting-the-seek-position"></a>Recupero della posizione seek.

1.  Per scoprire se un determinato flusso è indicizzato, chiamare [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Se il flusso è indicizzato, il *parametro pfIsIndexed* riceve il valore **TRUE**; in caso contrario riceve il valore **FALSE.**
2.  Per impostazione predefinita, l'indicizzatore usa la ricerca in avanti. Per la ricerca inversa, ovvero la ricerca dalla fine del file, chiamare [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) e impostare il flag **MFASF \_ INDEXER \_ READ FOR \_ \_ REVERSEPLAYBACK.** In caso contrario, ignorare questo passaggio.
3.  Se il flusso è indicizzato, ottenere la posizione di ricerca per un'ora di presentazione specificata chiamando [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Questo metodo legge l'indice asf e trova la voce di indice più vicina all'ora richiesta. Il metodo restituisce l'offset di byte del pacchetto di dati specificato dalla voce di indice. L'offset dei byte è relativo all'inizio dell'oggetto dati ASF.

Il [**metodo GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) accetta un puntatore alla [**struttura ASF INDEX \_ \_ IDENTIFIER.**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) Questa struttura specifica un tipo di indice e un identificatore di flusso. Attualmente, il tipo di indice deve essere NULL \_ GUID, che specifica l'indicizzazione basata sul tempo.

Il codice seguente ottiene una posizione di ricerca, in base a un identificatore di flusso e all'ora di presentazione di destinazione. Se la chiamata ha esito positivo, restituisce l'offset dei dati nel parametro *pcbDataOffset* e il tempo di ricerca effettivo approssimativo in *phnsApproxSeekTime.*


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

 

 



