---
description: Enumerazione dei pin
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumerazione dei pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876482"
---
# <a name="enumerating-pins"></a>Enumerazione dei pin

I filtri supportano il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , che enumera i pin disponibili sul filtro. Restituisce un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Il metodo [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera i puntatori dell'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

Nell'esempio seguente viene illustrata una funzione che individua un pin con una determinata direzione (input o output) su un filtro specificato. Usa l'enumerazione [**di \_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) per specificare la direzione del PIN e il metodo [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per trovare la direzione di ogni pin enumerato. Se questa funzione trova un pin corrispondente, restituisce un puntatore a interfaccia **Ipin** con un conteggio dei riferimenti in attesa. Il chiamante è responsabile del rilascio dell'interfaccia.


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



Questa funzione può essere facilmente modificata per restituire l'ennesimo pin con la direzione specificata *o il pin* non connesso. Per sapere se un PIN è connesso a un altro pin, chiamare il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti in un grafico di filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Trovare un PIN non connesso in un filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[Imposta la proprietà pin](pin-property-set.md)
</dt> </dl>

 

 



