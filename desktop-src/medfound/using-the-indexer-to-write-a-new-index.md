---
description: Questo argomento illustra come scrivere un indice per un file ASF (Advanced Systems Format).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Uso dell'indicizzatore per scrivere un nuovo indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fbc604a9493f7feea61e34500e0f620a051b05b1431ec2d4917df9f8ed15b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034529"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>Uso dell'indicizzatore per scrivere un nuovo indice

Questo argomento illustra come scrivere un indice per un file ASF (Advanced Systems Format).

Di seguito è riportata la procedura generale per la creazione di un indice asf:

1.  Inizializzare una nuova istanza dell'oggetto indicizzatore ASF, come descritto in Creazione e configurazione [dell'indicizzatore.](indexer-creation-and-configuration.md)
2.  Facoltativamente, configurare l'indicizzatore.
3.  Inviare pacchetti di dati ASF all'indicizzatore.
4.  Eseguire il commit dell'indice.
5.  Ottenere l'indice completato dall'indicizzatore e scriverlo in un flusso.

## <a name="configure-the-indexer"></a>Configurare l'indicizzatore

Per usare l'indicizzatore per scrivere un nuovo oggetto indice, l'oggetto indicizzatore deve avere il flag MFASF INDEXER WRITE NEW INDEX impostato con una chiamata \_ \_ a \_ \_ [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) prima di essere inizializzato con [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).

Quando l'indicizzatore è configurato per la scrittura di un indice, il chiamante sceglie i flussi da indicizzare. Per impostazione predefinita, l'indicizzatore tenta di creare un oggetto indice per tutti i flussi. L'intervallo di tempo predefinito è un secondo.

[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) può essere usato per eseguire l'override della scelta predefinita di flussi e tipi di indice dell'oggetto indicizzatore.

Nell'esempio di codice seguente viene illustrata l'inizializzazione di un DESCRITTOre DI INDICE ASF e di un IDENTIFICATORE DI INDICE ASF prima \_ di una chiamata a \_ \_ \_ [**SetIndexStatus.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)


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



Il tipo di indice GUID dell'identificatore deve essere impostato su GUID NULL per indicare che il tipo di indice sarà basato sul \_ tempo di presentazione. L'identificatore di indice deve anche essere inizializzato con il numero di flusso del flusso ASF da indicizzare. Dopo aver impostato l'identificatore di indice, usarlo per inizializzare il descrittore di indice.

La struttura del descrittore di indice ha membri che devono essere impostati prima della chiamata a [**SetIndexStatus.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) **Identifier** è una [**struttura ASF \_ INDEX \_ IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) che identifica il numero di flusso e il tipo di indice. **cPerEntryBytes è** il numero di byte usati per ogni voce di indice. Se il valore è MFASFINDEXER \_ PER \_ ENTRY BYTES \_ \_ DYNAMIC, le voci di indice hanno dimensioni variabili. **dwInterval è** l'intervallo di indicizzazione. Il valore MFASFINDEXER NO FIXED INTERVAL indica che non esiste \_ alcun intervallo di indicizzazione \_ \_ fisso.

## <a name="send-asf-data-packets-to-the-indexer"></a>Inviare pacchetti di dati ASF all'indicizzatore

Poiché l'indicizzatore è un oggetto di livello WMContainer, deve essere usato insieme al multiplexer durante la generazione di pacchetti.

I pacchetti restituiti da [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) possono essere inviati all'oggetto indicizzatore tramite chiamate [**a GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) in cui vengono create voci di indice per ogni pacchetto inviato.

Il codice seguente illustra come eseguire questa operazione:


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



Per altre informazioni, vedere [Generating New ASF Data Packets](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Eseguire il commit dell'indice

Dopo aver creato una voce di indice per l'ultimo pacchetto, è necessario eseguire il commit dell'indice. Questa operazione viene eseguita con una chiamata a [**IMFASFIndexer::CommitIndex.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex) **CommitIndex** accetta un puntatore all'oggetto ContentInfo che descrive il contenuto del file ASF. Il commit dell'indice completa l'indicizzazione e aggiorna l'intestazione con nuove informazioni sulle dimensioni e la ricerca del file.

## <a name="get-the-completed-index"></a>Ottenere l'indice completato

Per ottenere l'indice completato dall'indicizzatore, seguire questa procedura:

1.  Chiamare [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) per ottenere le dimensioni dell'indice.
2.  Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un buffer multimediale. È possibile allocare un buffer sufficientemente grande da contenere l'intero indice, allocare un buffer più piccolo e ottenere l'indice in blocchi.
3.  Chiamare [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) per ottenere i dati dell'indice. Nella prima chiamata impostare il *parametro cbOffsetWithinIndex* su zero. Se si ottiene l'indice in blocchi, incrementare *cbOffsetWithinIndex* ogni volta in base alle dimensioni dei dati della chiamata precedente.
4.  Chiamare [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore ai dati dell'indice e le dimensioni dei dati.
5.  Scrivere i dati dell'indice nel file ASF.
6.  Chiamare [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer multimediale.
7.  Ripetere i passaggi da 3 a 6 fino a quando non è stato scritto l'intero indice.

Il codice seguente illustra questi passaggi:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzatore ASF](asf-index-object.md)
</dt> </dl>

 

 



