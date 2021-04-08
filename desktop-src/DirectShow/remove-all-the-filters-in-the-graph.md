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
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="e4060-103">Rimuovere tutti i filtri nel grafico</span><span class="sxs-lookup"><span data-stu-id="e4060-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="e4060-104">Il modo più semplice per rimuovere tutti i filtri in un grafico di filtro è semplicemente rilasciare Filter Graph Manager e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="e4060-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="e4060-105">Assicurarsi di rilasciare ogni puntatore che l'applicazione deve avere sulle interfacce nei gestori dei grafici del filtro, nonché i puntatori agli oggetti nel grafico, inclusi i filtri, i pin, l'orologio di riferimento e così via.</span><span class="sxs-lookup"><span data-stu-id="e4060-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="e4060-106">In alternativa, è possibile rimuovere i filtri uno alla volta, usando il metodo [**IFilterGraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :</span><span class="sxs-lookup"><span data-stu-id="e4060-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


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



<span data-ttu-id="e4060-107">Questo esempio usa il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) per enumerare i filtri nel grafico.</span><span class="sxs-lookup"><span data-stu-id="e4060-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="e4060-108">Se si rimuove un filtro, l'oggetto enumeratore non sarà sincronizzato con il grafico.</span><span class="sxs-lookup"><span data-stu-id="e4060-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="e4060-109">Usare il metodo [**IEnumFilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) per reimpostare l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="e4060-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="e4060-110">In caso contrario, qualsiasi chiamata successiva a [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e4060-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



