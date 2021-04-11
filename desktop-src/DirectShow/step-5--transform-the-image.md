---
description: Passaggio 5.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Passaggio 5. Trasforma l'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232984"
---
# <a name="step-5-transform-the-image"></a>Passaggio 5. Trasforma l'immagine

Questo è il passaggio 5 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

Il filtro upstream recapita gli esempi multimediali al filtro di trasformazione chiamando il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input del filtro di trasformazione. Per elaborare i dati, il filtro di trasformazione chiama il metodo **Transform** , che è virtuale puro. Le classi **CTransformFilter** e **CTransInPlaceFilter** usano due versioni diverse di questo metodo:

-   [**CTransformFilter:: Transform**](ctransformfilter-transform.md) accetta un puntatore all'esempio di input e un puntatore all'esempio di output. Prima che il filtro chiami il metodo, copia le proprietà di esempio dall'esempio di input nell'esempio di output, inclusi i timestamp.
-   [**CTransInPlaceFilter:: Transform**](ctransinplacefilter-transform.md) accetta un puntatore all'esempio di input. Il filtro modifica i dati sul posto.

Se il metodo **Transform** restituisce S \_ OK, il filtro recapita l'esempio downstream. Per ignorare un frame, restituire S \_ false. Se si verifica un errore di streaming, restituire un codice di errore.

Nell'esempio seguente viene illustrato come il codificatore RLE può implementare questo metodo. Una propria implementazione può variare notevolmente, a seconda del tipo di filtro.


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



Questo esempio presuppone che EncodeFrame sia un metodo privato che implementa la codifica RLE. L'algoritmo di codifica non è descritto in questo articolo. per informazioni dettagliate, vedere l'argomento "compressione bitmap" nella documentazione di Platform SDK.

In primo luogo, nell'esempio viene chiamato [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) per recuperare gli indirizzi dei buffer sottostanti. Vengono passati al metodo EncoderFrame privato. Chiama quindi [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) per specificare la lunghezza dei dati codificati. Il filtro downstream necessita di queste informazioni in modo che sia in grado di gestire correttamente il buffer. Infine, il metodo chiama [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) per impostare il flag del fotogramma chiave su **true**. La codifica di lunghezza di esecuzione non usa alcun frame Delta, quindi ogni frame è un fotogramma chiave. Per i frame Delta, impostare il valore su **false**.

Altri problemi che è necessario considerare includono:

-   Timestamp. La classe **CTransformFilter** timestamp l'esempio di output prima di chiamare il metodo **Transform** . Copia i valori timestamp dall'esempio di input, senza modificarli. Se il filtro deve modificare i timestamp, chiamare [**IMediaSample:: Setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) nell'esempio di output.
-   Modificare il formato. Il filtro upstream può modificare i formati a metà flusso connettendo un tipo di supporto all'esempio. Prima di procedere, viene chiamato [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input del filtro. Nella classe **CTransformFilter** , il risultato è una chiamata a **CheckInputType** seguito da **CheckTransform**. Il filtro downstream può anche modificare i tipi di supporto, usando lo stesso meccanismo. Nel filtro è necessario tenere presenti due aspetti:

    -   Verificare che **QueryAccept** non restituisca false accettazioni.
    -   Se il filtro accetta modifiche al formato, verificarle all'interno del metodo **Transform** chiamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se il metodo restituisce S \_ OK, il filtro deve rispondere alla modifica del formato.

    Per altre informazioni, vedere [Dynamic Format Changes](dynamic-format-changes.md).

-   Thread. In **CTransformFilter** e **CTransInPlaceFilter** il filtro di trasformazione recapita gli esempi di output in modo sincrono all'interno del metodo **Receive** . Il filtro non crea alcun thread di lavoro per elaborare i dati. In genere, non esiste alcun motivo per cui un filtro di trasformazione crei thread di lavoro.

[Passaggio 6: Aggiungere il supporto per COM](step-6--add-support-for-com.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



