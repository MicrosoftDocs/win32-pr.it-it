---
description: Impostare le proprietà dell'allocatore come parte della scrittura di un filtro di trasformazione. Il pin di output del filtro di trasformazione seleziona l'allocatore downstream.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Passaggio 4. Impostare le proprietà dell'allocatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406824"
---
# <a name="step-4-set-allocator-properties"></a>Passaggio 4. Impostare le proprietà dell'allocatore

Questo è il passaggio 4 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter.**

 

Quando due pin concordano su un tipo di supporto, selezionano un allocatore per la connessione e negoziano le proprietà dell'allocatore, ad esempio le dimensioni del buffer e il numero di buffer.

Nella classe **CTransformFilter** sono presenti due allocatori, uno per la connessione pin upstream e uno per la connessione pin downstream. Il filtro upstream seleziona l'allocatore upstream e sceglie anche le proprietà dell'allocatore. Il pin di input accetta qualsiasi decisione del filtro upstream. Se è necessario modificare questo comportamento, eseguire l'override del [**metodo CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)

Il pin di output del filtro di trasformazione seleziona l'allocatore downstream. Esegue i passaggi seguenti:

1.  Se il filtro downstream può fornire un allocatore, il pin di output usa tale allocatore. In caso contrario, il pin di output crea un nuovo allocatore.
2.  Il pin di output ottiene i requisiti dell'allocatore del filtro downstream (se presenti) chiamando [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  Il pin di output chiama il metodo [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) del filtro di trasformazione, che è virtuale puro. I parametri di questo metodo sono un puntatore all'allocatore e una struttura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con i requisiti del filtro downstream. Se il filtro downstream non ha requisiti di allocatore, la struttura viene azzerato.
4.  Nel metodo **DecideBufferSize** la classe derivata imposta le proprietà dell'allocatore chiamando [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

In genere, la classe derivata selezionerà le proprietà dell'allocatore in base al formato di output, ai requisiti del filtro downstream e ai requisiti specifici del filtro. Provare a selezionare le proprietà compatibili con la richiesta del filtro downstream. In caso contrario, il filtro downstream potrebbe rifiutare la connessione.

Nell'esempio seguente il codificatore RLE imposta i valori minimi per le dimensioni del buffer, l'allineamento del buffer e il numero di buffer. Per il prefisso, usa qualsiasi valore richiesto dal filtro downstream. Il prefisso è in genere zero byte, ma alcuni filtri lo richiedono. Ad esempio, il [filtro Mux AVI](avi-mux-filter.md) usa il prefisso per scrivere le intestazioni RIFF.


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



L'allocatore potrebbe non essere in grado di corrispondere esattamente alla richiesta. Di conseguenza, **il metodo SetProperties** restituisce il risultato effettivo in una struttura **ALLOCATOR \_ PROPERTIES** separata *(il parametro Actual* nell'esempio precedente). Anche quando **SetProperties** ha esito positivo, è necessario controllare il risultato per assicurarsi che soddisfino i requisiti minimi del filtro.

**Allocatori personalizzati**

Per impostazione predefinita, tutte le classi di filtro usano la [**classe CMemAllocator**](cmemallocator.md) per i relativi allocatori. Questa classe alloca memoria dallo spazio degli indirizzi virtuali del processo client (usando **VirtualAlloc).** Se il filtro deve usare un altro tipo di memoria, ad esempio le superfici DirectDraw, è possibile implementare un allocatore personalizzato. È possibile usare la [**classe CBaseAllocator**](cbaseallocator.md) o scrivere una classe allocatore completamente nuova. Se il filtro ha un allocatore personalizzato, eseguire l'override dei metodi seguenti, a seconda del pin che usa l'allocatore:

-   Pin di input: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Pin di output: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

Se l'altro filtro rifiuta di connettersi usando l'allocatore personalizzato, il filtro può non riuscire o connettersi all'allocatore dell'altro filtro. Nel secondo caso, potrebbe essere necessario impostare un flag interno che indica il tipo di allocatore. Per un esempio di questo approccio, vedere [**Classe CDrawImage**](cdrawimage.md).

Passaggio [5. Trasformare l'immagine](step-5--transform-the-image.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectMostra filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



