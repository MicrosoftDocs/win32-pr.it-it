---
description: Enumerazione dei pin
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumerazione dei pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748711"
---
# <a name="enumerating-pins"></a>Enumerazione dei pin

I filtri [**supportano il metodo IBaseFilter::EnumPins,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) che enumera i pin disponibili nel filtro. Restituisce un puntatore [**all'interfaccia IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) Il [**metodo IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera i [**puntatori a interfaccia IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

Nell'esempio seguente viene illustrata una funzione che individua un segnaposto con una direzione specificata (input o output) in un determinato filtro. Usa [**l'enumerazione \_ PIN DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) per specificare la direzione del pin e il metodo [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per trovare la direzione di ogni pin enumerato. Se questa funzione trova un pin corrispondente, restituisce un puntatore a interfaccia **IPin** con un conteggio dei riferimenti in sospeso. Il chiamante è responsabile del rilascio dell'interfaccia.


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



Questa funzione può essere modificata facilmente per restituire l'eesimo pin con la direzione specificata o *l'eesimo* pin non associato. Per determinare se un pin è connesso a un altro pin, chiamare il metodo [**IPin::ConnectedTo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti in un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Trovare un pin non interconnesso in un filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Tecniche Graph-Building generale](general-graph-building-techniques.md)
</dt> <dt>

[Impostare la proprietà Pin](pin-property-set.md)
</dt> </dl>

 

 



