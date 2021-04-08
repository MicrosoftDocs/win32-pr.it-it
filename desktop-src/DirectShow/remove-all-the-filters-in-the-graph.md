---
description: Rimuovere tutti i filtri nel grafico
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Rimuovere tutti i filtri nel grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746303"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Rimuovere tutti i filtri nel grafico

Il modo più semplice per rimuovere tutti i filtri in un grafico di filtro è semplicemente rilasciare Filter Graph Manager e crearne uno nuovo. Assicurarsi di rilasciare ogni puntatore che l'applicazione deve avere sulle interfacce nei gestori dei grafici del filtro, nonché i puntatori agli oggetti nel grafico, inclusi i filtri, i pin, l'orologio di riferimento e così via.

In alternativa, è possibile rimuovere i filtri uno alla volta, usando il metodo [**IFilterGraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :


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



Questo esempio usa il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) per enumerare i filtri nel grafico. Se si rimuove un filtro, l'oggetto enumeratore non sarà sincronizzato con il grafico. Usare il metodo [**IEnumFilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) per reimpostare l'enumeratore. In caso contrario, qualsiasi chiamata successiva a [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) avrà esito negativo.

 

 



