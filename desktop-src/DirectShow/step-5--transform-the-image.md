---
description: Usare questo esempio per comprendere in che modo il codificatore RLE può implementare il metodo come parte della scrittura di un filtro di trasformazione.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Passaggio 5. Trasformare l'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406784"
---
# <a name="step-5-transform-the-image"></a>Passaggio 5. Trasformare l'immagine

Questo è il passaggio 5 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

Il filtro upstream fornisce esempi di contenuti multimediali al filtro di trasformazione chiamando il metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input del filtro di trasformazione. Per elaborare i dati, il filtro di trasformazione chiama **il metodo Transform,** che è virtuale puro. Le **classi CTransformFilter** **e CTransInPlaceFilter** usano due versioni diverse di questo metodo:

-   [**CTransformFilter::Transform**](ctransformfilter-transform.md) accetta un puntatore all'esempio di input e un puntatore all'esempio di output. Prima che il filtro chiami il metodo , copia le proprietà di esempio dall'esempio di input all'esempio di output, inclusi i timestamp.
-   [**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) accetta un puntatore all'esempio di input. Il filtro modifica i dati sul posto.

Se il **metodo Transform** restituisce S \_ OK, il filtro recapita il campione a valle. Per ignorare un frame, restituire S \_ FALSE. Se si verifica un errore di flusso, restituire un codice di errore.

L'esempio seguente illustra come il codificatore RLE potrebbe implementare questo metodo. L'implementazione potrebbe variare notevolmente, a seconda del filtro.


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



Questo esempio presuppone che EncodeFrame sia un metodo privato che implementa la codifica RLE. L'algoritmo di codifica stesso non è descritto qui. Per informazioni dettagliate, vedere l'argomento "Compressione bitmap" nella documentazione di Platform SDK.

In primo luogo, [**l'esempio chiama IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) per recuperare gli indirizzi dei buffer sottostanti. Li passa al metodo EncoderFrame privato. Chiama quindi [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) per specificare la lunghezza dei dati codificati. Il filtro downstream necessita di queste informazioni per poter gestire correttamente il buffer. Infine, il metodo chiama [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) per impostare il flag del fotogramma chiave su **TRUE.** La codifica della lunghezza di esecuzione non usa fotogrammi differenziali, quindi ogni fotogramma è un fotogramma chiave. Per i frame differenziali, impostare il valore su **FALSE.**

Altri problemi che è necessario considerare includono:

-   Timestamp. La **classe CTransformFilter** indica il timestamp dell'esempio di output prima di chiamare il **metodo Transform.** Copia i valori del timestamp dall'esempio di input, senza modificarli. Se il filtro deve modificare i timestamp, chiamare [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) nell'esempio di output.
-   Modifiche al formato. Il filtro upstream può modificare i formati durante il flusso collegando un tipo di supporto all'esempio. Prima di procedere, chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input del filtro. Nella classe **CTransformFilter** viene generata una chiamata a **CheckInputType** seguita da **CheckTransform.** Il filtro downstream può anche modificare i tipi di supporti, usando lo stesso meccanismo. Nel filtro personalizzato è necessario controllare due elementi:

    -   Assicurarsi che **QueryAccept** non restituirà false accettazioni.
    -   Se il filtro accetta modifiche al formato, verificarle all'interno del **metodo Transform** chiamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se il metodo restituisce S \_ OK, il filtro deve rispondere alla modifica del formato.

    Per altre informazioni, vedere [Modifiche al formato dinamico.](dynamic-format-changes.md)

-   Discussioni. Sia in **CTransformFilter** che **in CTransInPlaceFilter** il filtro di trasformazione fornisce esempi di output in modo sincrono all'interno **del metodo Receive.** Il filtro non crea thread di lavoro per elaborare i dati. In genere, non esiste alcun motivo per cui un filtro di trasformazione crei thread di lavoro.

Passaggio [successivo: Passaggio 6. Aggiunta del supporto per COM.](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectMostra filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



