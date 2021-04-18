---
description: Passaggio 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Passaggio 4. Imposta proprietà allocatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316326"
---
# <a name="step-4-set-allocator-properties"></a>Passaggio 4. Imposta proprietà allocatore

Questo è il passaggio 4 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.

 

Dopo aver accettato due pin per un tipo di supporto, selezionare un allocatore per la connessione e negoziare le proprietà dell'allocatore, ad esempio la dimensione del buffer e il numero di buffer.

Nella classe **CTransformFilter** sono disponibili due allocatori, uno per la connessione pin upstream e uno per la connessione pin downstream. Il filtro upstream seleziona l'allocatore upstream e sceglie anche le proprietà dell'allocatore. Il pin di input accetta qualsiasi cosa venga deciso dal filtro upstream. Se è necessario modificare questo comportamento, eseguire l'override del metodo [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .

Il pin di output del filtro di trasformazione seleziona l'allocatore downstream. Esegue i passaggi seguenti:

1.  Se il filtro downstream può fornire un allocatore, il pin di output lo utilizzerà. In caso contrario, il pin di output crea un nuovo allocatore.
2.  Il pin di output ottiene i requisiti dell'allocatore del filtro downstream chiamando [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  Il pin di output chiama il metodo [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) del filtro di trasformazione, che è virtuale puro. I parametri di questo metodo sono un puntatore all'allocatore e una struttura delle [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con i requisiti del filtro downstream. Se il filtro downstream non presenta requisiti per l'allocatore, la struttura viene azzerata.
4.  Nel metodo **DecideBufferSize** la classe derivata imposta le proprietà dell'allocatore chiamando [**IMemAllocator::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)SetValue.

In genere, la classe derivata selezionerà le proprietà dell'allocatore in base al formato di output, i requisiti del filtro downstream e i requisiti del filtro. Provare a selezionare le proprietà compatibili con la richiesta del filtro downstream. In caso contrario, il filtro downstream potrebbe rifiutare la connessione.

Nell'esempio seguente il codificatore RLE imposta i valori minimi per le dimensioni del buffer, l'allineamento del buffer e il numero di buffer. Per il prefisso, USA qualsiasi valore richiesto dal filtro downstream. Il prefisso è in genere pari a zero byte, ma alcuni filtri lo richiedono. Ad esempio, il filtro [Mux AVI](avi-mux-filter.md) usa il prefisso per scrivere le intestazioni riff.


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



L'allocatore potrebbe non essere in grado di soddisfare esattamente la richiesta. Pertanto, il metodo **seproperties** restituisce il risultato effettivo in una struttura **di \_ Proprietà allocatore** separata (il parametro *effettivo* nell'esempio precedente). Anche in caso di esito positivo delle **Proprietà** , è necessario controllare il risultato per assicurarsi che soddisfino i requisiti minimi del filtro.

**Allocatori personalizzati**

Per impostazione predefinita, tutte le classi di filtro utilizzano la classe [**CMemAllocator**](cmemallocator.md) per gli allocatori. Questa classe alloca memoria dallo spazio degli indirizzi virtuali del processo client (tramite **VirtualAlloc**). Se il filtro deve usare un altro tipo di memoria, ad esempio le superfici DirectDraw, è possibile implementare un allocatore personalizzato. È possibile usare la classe [**CBaseAllocator**](cbaseallocator.md) o scrivere una classe allocator completamente nuova. Se il filtro ha un allocatore personalizzato, eseguire l'override dei metodi seguenti, a seconda del PIN che usa l'allocatore:

-   Pin di input: [**CBaseInputPin:: Getallocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Pin di output: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

Se l'altro filtro si rifiuta di connettersi usando l'allocatore personalizzato, il filtro può interrompere la connessione oppure connettersi con l'allocatore dell'altro filtro. Nel secondo caso, potrebbe essere necessario impostare un flag interno che indichi il tipo di allocatore. Per un esempio di questo approccio, vedere [**classe CDrawImage**](cdrawimage.md).

Successivo: [passaggio 5. Trasformare l'immagine](step-5--transform-the-image.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



