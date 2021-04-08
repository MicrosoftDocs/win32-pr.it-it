---
description: In questo argomento viene descritto come trovare un PIN non connesso in un filtro. Trovare un PIN non connesso è utile quando si connettono i filtri.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Trovare un PIN non connesso in un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048873"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="36ce7-104">Trovare un PIN non connesso in un filtro</span><span class="sxs-lookup"><span data-stu-id="36ce7-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="36ce7-105">In questo argomento viene descritto come trovare un PIN non connesso in un filtro.</span><span class="sxs-lookup"><span data-stu-id="36ce7-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="36ce7-106">Trovare un PIN non connesso è utile quando si connettono i filtri.</span><span class="sxs-lookup"><span data-stu-id="36ce7-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="36ce7-107">In uno scenario tipico di creazione di grafici DirectShow è necessario un PIN non connesso che corrisponda a una direzione del pin particolare (input o output).</span><span class="sxs-lookup"><span data-stu-id="36ce7-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="36ce7-108">Ad esempio, quando si connettono due filtri, si connette un pin di output da un filtro a un pin di input dall'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="36ce7-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="36ce7-109">Entrambi i pin devono essere scollegati prima di connetterli.</span><span class="sxs-lookup"><span data-stu-id="36ce7-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="36ce7-110">Per prima cosa, è necessaria una funzione che verifica se un PIN è connesso a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="36ce7-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="36ce7-111">Questa funzione chiama il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) per verificare se il PIN è connesso a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="36ce7-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="36ce7-112">Questo esempio usa la funzione [SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="36ce7-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="36ce7-113">Quindi, è necessaria una funzione che verifica se un PIN corrisponde a una direzione del pin specificata.</span><span class="sxs-lookup"><span data-stu-id="36ce7-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="36ce7-114">Questa funzione chiama il metodo [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per ottenere la direzione del PIN.</span><span class="sxs-lookup"><span data-stu-id="36ce7-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



<span data-ttu-id="36ce7-115">La funzione Next corrisponde a un PIN per entrambi i criteri (direzione del PIN e stato di connessione).</span><span class="sxs-lookup"><span data-stu-id="36ce7-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



<span data-ttu-id="36ce7-116">Infine, la funzione seguente usa l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per eseguire il loop dei pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="36ce7-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="36ce7-117">Il chiamante specifica la direzione del pin desiderata.</span><span class="sxs-lookup"><span data-stu-id="36ce7-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="36ce7-118">Per ogni pin, la funzione chiama `MatchPin` per verificare se il PIN è una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="36ce7-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="36ce7-119">Se la direzione corrisponde e il PIN è scollegato, la funzione restituisce un puntatore al pin corrispondente nel parametro *ppPin* .</span><span class="sxs-lookup"><span data-stu-id="36ce7-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



<span data-ttu-id="36ce7-120">Per un esempio di come è possibile usare questa funzione, vedere [connettere due filtri](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="36ce7-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36ce7-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36ce7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ce7-122">Enumerazione dei pin</span><span class="sxs-lookup"><span data-stu-id="36ce7-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="36ce7-123">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="36ce7-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="36ce7-124">**ICaptureGraphBuilder2::FindPin**</span><span class="sxs-lookup"><span data-stu-id="36ce7-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
