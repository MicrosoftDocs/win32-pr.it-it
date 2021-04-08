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
# <a name="enumerating-pins"></a><span data-ttu-id="346f4-103">Enumerazione dei pin</span><span class="sxs-lookup"><span data-stu-id="346f4-103">Enumerating Pins</span></span>

<span data-ttu-id="346f4-104">I filtri supportano il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , che enumera i pin disponibili sul filtro.</span><span class="sxs-lookup"><span data-stu-id="346f4-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="346f4-105">Restituisce un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="346f4-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="346f4-106">Il metodo [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera i puntatori dell'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="346f4-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="346f4-107">Nell'esempio seguente viene illustrata una funzione che individua un pin con una determinata direzione (input o output) su un filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="346f4-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="346f4-108">Usa l'enumerazione [**di \_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) per specificare la direzione del PIN e il metodo [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per trovare la direzione di ogni pin enumerato.</span><span class="sxs-lookup"><span data-stu-id="346f4-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="346f4-109">Se questa funzione trova un pin corrispondente, restituisce un puntatore a interfaccia **Ipin** con un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="346f4-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="346f4-110">Il chiamante è responsabile del rilascio dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="346f4-110">The caller is responsible for releasing the interface.</span></span>


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



<span data-ttu-id="346f4-111">Questa funzione può essere facilmente modificata per restituire l'ennesimo pin con la direzione specificata *o il pin* non connesso.</span><span class="sxs-lookup"><span data-stu-id="346f4-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="346f4-112">Per sapere se un PIN è connesso a un altro pin, chiamare il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="346f4-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="346f4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="346f4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346f4-114">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="346f4-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="346f4-115">Trovare un PIN non connesso in un filtro</span><span class="sxs-lookup"><span data-stu-id="346f4-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="346f4-116">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="346f4-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="346f4-117">Imposta la proprietà pin</span><span class="sxs-lookup"><span data-stu-id="346f4-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



