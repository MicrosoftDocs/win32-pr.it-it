---
description: In questo argomento vengono illustrate alcune funzioni helper per la connessione di filtri DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Connetti due filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124869"
---
# <a name="connect-two-filters"></a>Connetti due filtri

In questo argomento vengono illustrate alcune funzioni helper per la connessione di filtri DirectShow.

Per connettere due filtri, è necessario trovare un pin di output non connesso sul filtro upstream e un pin di input non connesso sul filtro downstream.

Se sono già presenti puntatori a entrambi i pin, chiamare il metodo [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connetterli. Se i pin non possono connettersi direttamente tra loro, il metodo **IGraphBuilder:: Connect** potrebbe inserire filtri aggiuntivi per completare la connessione. Per ulteriori informazioni, vedere la pagina relativa alla [connessione intelligente](intelligent-connect.md).

Se è presente un puntatore ai filtri, ma non ai pin, è necessario usare il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare i pin. (Vedere [enumerazione dei pin](enumerating-pins.md)). Questa tecnica è illustrata nelle funzioni helper di questo argomento.

### <a name="output-pin-to-filter"></a>Pin di output da filtrare

La funzione seguente accetta due parametri: un puntatore a un pin di output e un puntatore a un filtro. La funzione connette il pin di output al primo pin di input disponibile sul filtro.


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

1.  Chiama la `FindUnconnectedPin` funzione per ottenere un pin di input non connesso. Questa funzione è illustrata nell'argomento [trovare un PIN non connesso in un filtro](find-an-unconnected-pin-on-a-filter.md).
2.  Chiama [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connettere i due pin.

### <a name="filter-to-input-pin"></a>Filtrare al pin di input

La funzione successiva accetta un puntatore a un filtro e un puntatore a un pin di input. Connette il pin di input al primo pin di output disponibile sul filtro.


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

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



