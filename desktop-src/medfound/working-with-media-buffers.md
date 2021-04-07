---
description: Uso dei buffer multimediali
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Uso dei buffer multimediali (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886000"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Uso dei buffer multimediali (Microsoft Media Foundation)

In questo argomento viene descritto come utilizzare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) per accedere ai dati in un buffer multimediale. Tutti i buffer multimediali espongono **IMFMediaBuffer**, progettato per qualsiasi tipo di dati. I frame video non compressi costituiscono un caso speciale, descritti nell'argomento [buffer video non compressi](uncompressed-video-buffers.md).

## <a name="buffer-size"></a>Dimensione buffer

A un buffer multimediale sono associate due dimensioni:

-   La *lunghezza massima* corrisponde alla dimensione fisica della memoria allocata per il buffer. Questo valore viene impostato quando il buffer viene creato e non viene modificato durante il ciclo di vita del buffer. La lunghezza massima indica la quantità di dati che è possibile archiviare nel buffer. Per trovare le dimensioni massime, chiamare [**IMFMediaBuffer:: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   La *lunghezza corrente* corrisponde alla quantità di dati validi attualmente presenti nel buffer. Quando il buffer viene allocato per la prima volta, la lunghezza corrente è zero, perché non sono presenti dati validi nel buffer. Se si scrivono dati nel buffer, è necessario aggiornare la lunghezza corrente chiamando [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength). Se, ad esempio, si scrivono 100 byte di dati nel buffer, chiamare **SetCurrentLength** con il valore 100. Se si leggono i dati da un buffer multimediale, chiamare [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) per determinare la quantità di dati attualmente presenti nel buffer. Non leggere oltre la lunghezza corrente. La lunghezza corrente non può mai superare la lunghezza massima del buffer.

## <a name="accessing-the-buffer-memory"></a>Accesso alla memoria del buffer

Per accedere alla memoria nel buffer, chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Questo metodo restituisce un puntatore all'inizio del blocco di memoria. Restituisce anche la lunghezza massima e la lunghezza corrente. Al termine dell'utilizzo del puntatore, chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Per scrivere i dati in un buffer multimediale:

1.  Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria. Il metodo restituisce anche la lunghezza massima del buffer.
2.  Scrivere i dati nella memoria, fino alla lunghezza massima del buffer.
3.  Chiamare [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) per aggiornare la lunghezza corrente. Impostare la lunghezza corrente uguale alla quantità di dati scritti nel passaggio 2.
4.  Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.

Per leggere i dati da un buffer multimediale:

1.  Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria. Il metodo restituisce anche la lunghezza corrente del buffer (la quantità di dati validi nel buffer).
2.  Leggere il contenuto della memoria, fino alla lunghezza corrente.
3.  Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.

## <a name="creating-system-memory-buffers"></a>Creazione di buffer di memoria di sistema

Il buffer di memoria di sistema è un buffer multimediale che gestisce un blocco di memoria di sistema. Per creare un'istanza di questo oggetto, chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) o [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) e specificare una dimensione del buffer. Entrambe le funzioni allocano un blocco di memoria e restituiscono un puntatore [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . La memoria viene rilasciata automaticamente quando il conteggio dei riferimenti del buffer multimediale raggiunge lo zero e l'oggetto viene eliminato definitivamente.

Nell'esempio seguente viene illustrato come creare un buffer di memoria di sistema e scrivere nel buffer.


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



