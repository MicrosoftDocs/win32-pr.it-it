---
description: Questo argomento descrive come trovare un pin non correlato in un filtro. La ricerca di un pin non connesso è utile quando si connettono i filtri.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Trovare un segnaposto non interconnesso in un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a76100622f0398c58eb10f2dda041ba074f4610efbd1c649d48199ea2c676eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401755"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Trovare un segnaposto non interconnesso in un filtro

Questo argomento descrive come trovare un pin non correlato in un filtro. La ricerca di un pin non connesso è utile quando si connettono i filtri.

In un tipico scenario DirectShow di creazione di grafi, è necessario un segnaposto non interconnesso che corrisponda a una particolare direzione del pin (input o output). Ad esempio, quando si connettono due filtri, si connette un pin di output da un filtro a un pin di input dall'altro filtro. Entrambi i pin devono essere scollegati prima di connetterli.

In primo luogo, è necessaria una funzione che verifica se un pin è connesso a un altro pin. Questa funzione chiama il [**metodo IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) per verificare se il pin è connesso a un altro pin.


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
> Questo esempio usa la [funzione SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare i puntatori a interfaccia.

 

Successivamente, è necessaria una funzione che verifica se un segnaposto corrisponde a una direzione del pin specificata. Questa funzione chiama il [**metodo IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per ottenere la direzione del segnaposto.


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



La funzione successiva corrisponde a un pin in base a entrambi i criteri (direzione del pin e stato della connessione).


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



Infine, la funzione seguente usa [**l'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per scorrere i segnaposto nel filtro. Il chiamante specifica la direzione del pin desiderata. Per ogni pin, la funzione chiama `MatchPin` per verificare se il segnaposto è una corrispondenza. Se la direzione corrisponde e il segnaposto non è interconnesso, la funzione restituisce un puntatore al segnaposto corrispondente nel *parametro ppPin.*


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



Per un esempio di come è possibile usare questa funzione, vedere Connessione [Two Filters](connect-two-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei pin](enumerating-pins.md)
</dt> <dt>

[Tecniche Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
