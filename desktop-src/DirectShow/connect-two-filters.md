---
description: Questo argomento illustra alcune funzioni helper per la connessione DirectShow filtri.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Connessione Due filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83e8608c088fde6d06c0a44621f1c066f177ecf76cbc8ba3f55d31218b49ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954210"
---
# <a name="connect-two-filters"></a>Connessione Due filtri

Questo argomento illustra alcune funzioni helper per la connessione DirectShow filtri.

Per connettere due filtri, è necessario trovare un pin di output non connesso nel filtro upstream e un pin di input non connesso nel filtro downstream.

Se sono già presenti puntatori a entrambi i pin, chiamare il metodo [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connetterli. Se i pin non possono connettersi direttamente tra loro, il metodo **IGraphBuilder::Connessione** potrebbe inserire filtri aggiuntivi per completare la connessione. Per altre informazioni, vedere [Intelligent Connessione](intelligent-connect.md).

Se è disponibile un puntatore ai filtri ma non ai segnaposto, è necessario usare il metodo [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare i segnaposto. Vedere [Enumerazione dei pin.](enumerating-pins.md) Le funzioni helper in questo argomento illustrano questa tecnica.

### <a name="output-pin-to-filter"></a>Aggiunta dell'output al filtro

La funzione seguente accetta due parametri: un puntatore a un pin di output e un puntatore a un filtro. La funzione connette il pin di output al primo pin di input disponibile nel filtro.


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



Questa funzione esegue le operazioni seguenti:

1.  Chiama la `FindUnconnectedPin` funzione per ottenere un pin di input non interconnesso. Questa funzione è illustrata nell'argomento [Trovare un pin non connessa in un filtro.](find-an-unconnected-pin-on-a-filter.md)
2.  Chiama [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connettere i due segnaposto.

### <a name="filter-to-input-pin"></a>Filtrare in base al pin di input

La funzione successiva accetta un puntatore a un filtro e un puntatore a un pin di input. Connette il pin di input al primo pin di output disponibile nel filtro.


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a>Filtrare per filtrare

La terza funzione accetta un puntatore a un filtro upstream e un puntatore a un filtro downstream e tenta di connettere entrambi i filtri.


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



