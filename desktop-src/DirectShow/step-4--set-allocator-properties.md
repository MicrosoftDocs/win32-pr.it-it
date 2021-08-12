---
description: Impostare le proprietà dell'allocatore come parte della scrittura di un filtro di trasformazione. Il pin di output del filtro di trasformazione seleziona l'allocatore downstream.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Passaggio 4. Impostare le proprietà dell'allocatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33376cff0e6c0674edfadcffed59d16d8d7dccb9f48384a22ec4c69fc48d8eb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652131"
---
# <a name="step-4-set-allocator-properties"></a>Passaggio 4. Impostare le proprietà dell'allocatore

Questo è il passaggio 4 dell'esercitazione [Scrittura di filtri di trasformazione](writing-transform-filters.md).

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.

 

Dopo che due pin concordano su un tipo di supporto, selezionano un allocatore per la connessione e negoziano le proprietà dell'allocatore, ad esempio le dimensioni del buffer e il numero di buffer.

Nella classe **CTransformFilter** sono disponibili due allocatori, uno per la connessione del pin upstream e uno per la connessione del pin downstream. Il filtro upstream seleziona l'allocatore upstream e sceglie anche le proprietà dell'allocatore. Il pin di input accetta qualsiasi cosa decida il filtro upstream. Se è necessario modificare questo comportamento, eseguire l'override del [**metodo CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)

Il pin di output del filtro di trasformazione seleziona l'allocatore downstream. Esegue i passaggi seguenti:

1.  Se il filtro downstream può fornire un allocatore, il pin di output lo usa. In caso contrario, il pin di output crea un nuovo allocatore.
2.  Il pin di output ottiene i requisiti di allocatore del filtro downstream (se presenti) chiamando [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  Il pin di output chiama il metodo [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) del filtro di trasformazione, che è virtuale puro. I parametri di questo metodo sono un puntatore all'allocatore e una struttura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con i requisiti del filtro downstream. Se il filtro downstream non ha requisiti di allocatore, la struttura viene azzerato.
4.  Nel metodo **DecideBufferSize** la classe derivata imposta le proprietà dell'allocatore chiamando [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

In genere, la classe derivata selezionerà le proprietà dell'allocatore in base al formato di output, ai requisiti del filtro downstream e ai requisiti del filtro stesso. Provare a selezionare le proprietà compatibili con la richiesta del filtro downstream. In caso contrario, il filtro downstream potrebbe rifiutare la connessione.

Nell'esempio seguente il codificatore RLE imposta i valori minimi per le dimensioni del buffer, l'allineamento del buffer e il numero di buffer. Per il prefisso, usa qualsiasi valore richiesto dal filtro downstream. Il prefisso è in genere zero byte, ma alcuni filtri lo richiedono. Ad esempio, il [filtro AVI Mux](avi-mux-filter.md) usa il prefisso per scrivere intestazioni RIFF.


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



L'allocatore potrebbe non essere in grado di soddisfare esattamente la richiesta. Pertanto, il **metodo SetProperties** restituisce il risultato effettivo in una struttura **ALLOCATOR \_ PROPERTIES** separata *(il parametro Actual,* nell'esempio precedente). Anche quando **SetProperties** ha esito positivo, è necessario controllare il risultato per assicurarsi che soddisfino i requisiti minimi del filtro.

**Allocatori personalizzati**

Per impostazione predefinita, tutte le classi di filtro usano la [**classe CMemAllocator**](cmemallocator.md) per i relativi allocatori. Questa classe alloca memoria dallo spazio degli indirizzi virtuali del processo client (usando **VirtualAlloc**). Se il filtro deve usare un altro tipo di memoria, ad esempio superfici DirectDraw, è possibile implementare un allocatore personalizzato. È possibile usare la [**classe CBaseAllocator**](cbaseallocator.md) o scrivere una classe allocatore completamente nuova. Se il filtro ha un allocatore personalizzato, eseguire l'override dei metodi seguenti, a seconda del pin che usa l'allocatore:

-   Pin di input: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Pin di output: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

Se l'altro filtro rifiuta di connettersi usando l'allocatore personalizzato, il filtro può non riuscire oppure connettersi all'allocatore dell'altro filtro. In quest'ultimo caso potrebbe essere necessario impostare un flag interno che indica il tipo di allocatore. Per un esempio di questo approccio, vedere [**Classe CDrawImage**](cdrawimage.md).

Successivo: [Passaggio 5. Trasformare l'immagine](step-5--transform-the-image.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



