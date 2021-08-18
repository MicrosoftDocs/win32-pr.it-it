---
description: Rimuovere tutti i filtri nel Graph
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Rimuovere tutti i filtri nel Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10b76bb5f5bc3cff2bfb989c422f177ef0d2ee4d09acff3c2f895ef9984b7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072735"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Rimuovere tutti i filtri nel Graph

Il modo più semplice per rimuovere tutti i filtri in un grafo di filtro è semplicemente rilasciare filter Graph Manager e crearne uno nuovo. Assicurarsi di rilasciare ogni puntatore dell'applicazione a qualsiasi interfaccia in Filter Graph Managers, nonché puntatori a oggetti nel grafico, inclusi filtri, pin, clock di riferimento e così via.

In alternativa, è possibile rimuovere i filtri uno alla volta usando il [**metodo IFilterGraph::RemoveFilter:**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter)


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



In questo esempio viene [**utilizzato il metodo IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) per enumerare i filtri nel grafico. La rimozione di un filtro causa la non sincronizzazione dell'oggetto enumeratore con il grafico. Usare il [**metodo IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) per reimpostare l'enumeratore. In caso contrario, qualsiasi chiamata successiva a [**IEnumFilters::Next avrà**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) esito negativo.

 

 



