---
description: Trovare un'interfaccia su un filtro o un pin
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Trovare un'interfaccia su un filtro o un pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225311"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Trovare un'interfaccia su un filtro o un pin

Per molte operazioni in DirectShow, l'applicazione chiama i metodi in gestione grafico dei filtri. In alcune situazioni, tuttavia, l'applicazione deve chiamare un metodo direttamente su un filtro o un PIN. Molti filtri, ad esempio, espongono interfacce specializzate che vengono usate per configurare il filtro.

Nel caso di un'interfaccia di filtro, è possibile che si disponga già di un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro. In tal caso, usare semplicemente **QueryInterface** per ottenere l'altra interfaccia. Tuttavia, è possibile che alcuni filtri vengano aggiunti al grafico dal gestore del grafico dei filtri. Per informazioni dettagliate, vedere [connessione intelligente](intelligent-connect.md). In tal caso, usare l'interfaccia [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) per scorrere in ciclo tutti i filtri nel grafico ed eseguire una query su ognuno di essi. Nella funzione seguente viene illustrato quanto segue:


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



Per trovare un'interfaccia su un PIN, usare l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per scorrere in ciclo i pin di un filtro. La funzione seguente mostra come eseguire questa operazione:


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



La funzione successiva cerca un'interfaccia su un filtro o un PIN:


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



Si noti che tutte le funzioni mostrate qui si arrestano al primo **QueryInterface** riuscito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei filtri](enumerating-filters.md)
</dt> <dt>

[Enumerazione dei pin](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



