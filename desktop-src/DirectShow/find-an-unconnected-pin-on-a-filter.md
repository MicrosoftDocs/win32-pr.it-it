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
# <a name="find-an-unconnected-pin-on-a-filter"></a>Trovare un PIN non connesso in un filtro

In questo argomento viene descritto come trovare un PIN non connesso in un filtro. Trovare un PIN non connesso è utile quando si connettono i filtri.

In uno scenario tipico di creazione di grafici DirectShow è necessario un PIN non connesso che corrisponda a una direzione del pin particolare (input o output). Ad esempio, quando si connettono due filtri, si connette un pin di output da un filtro a un pin di input dall'altro filtro. Entrambi i pin devono essere scollegati prima di connetterli.

Per prima cosa, è necessaria una funzione che verifica se un PIN è connesso a un altro pin. Questa funzione chiama il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) per verificare se il PIN è connesso a un altro pin.


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
> Questo esempio usa la funzione [SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare i puntatori a interfaccia.

 

Quindi, è necessaria una funzione che verifica se un PIN corrisponde a una direzione del pin specificata. Questa funzione chiama il metodo [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per ottenere la direzione del PIN.


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



La funzione Next corrisponde a un PIN per entrambi i criteri (direzione del PIN e stato di connessione).


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



Infine, la funzione seguente usa l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per eseguire il loop dei pin sul filtro. Il chiamante specifica la direzione del pin desiderata. Per ogni pin, la funzione chiama `MatchPin` per verificare se il PIN è una corrispondenza. Se la direzione corrisponde e il PIN è scollegato, la funzione restituisce un puntatore al pin corrispondente nel parametro *ppPin* .


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



Per un esempio di come è possibile usare questa funzione, vedere [connettere due filtri](connect-two-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei pin](enumerating-pins.md)
</dt> <dt>

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
