---
description: Trovare un'interfaccia in un filtro o un segnaposto
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Trovare un'interfaccia in un filtro o un segnaposto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819563"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Trovare un'interfaccia in un filtro o un segnaposto

Per molte operazioni in DirectShow, l'applicazione chiama i metodi in Filter Graph Manager. In alcune situazioni, tuttavia, l'applicazione deve chiamare un metodo direttamente su un filtro o un pin. Ad esempio, molti filtri espongono interfacce specializzate usate per configurare il filtro.

Nel caso di un'interfaccia di filtro, potrebbe essere già presente un puntatore [**all'interfaccia IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro. In tal caso, è sufficiente usare **QueryInterface** per ottenere l'altra interfaccia. Tuttavia, alcuni filtri potrebbero essere aggiunti al grafico da Filter Graph Manager. Per informazioni dettagliate, vedere [Intelligent Connessione](intelligent-connect.md). In tal caso, usare [**l'interfaccia IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) per eseguire il ciclo di tutti i filtri nel grafico ed eseguire una query su ognuno di essi. La funzione seguente illustra questa operazione:


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



Per trovare un'interfaccia su un segnaposto, usare [**l'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per scorrere i segnaposto in un filtro. La funzione seguente illustra come eseguire questa operazione:


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



La funzione successiva cerca un'interfaccia in un filtro o un segnaposto:


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



Si noti che tutte le funzioni illustrate qui si arrestano in corrispondenza della prima **query QueryInterface riuscita.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei filtri](enumerating-filters.md)
</dt> <dt>

[Enumerazione dei pin](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



