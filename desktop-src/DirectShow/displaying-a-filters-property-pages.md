---
description: Visualizzazione delle pagine delle proprietà di un filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Visualizzazione delle pagine delle proprietà di un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401081"
---
# <a name="displaying-a-filters-property-pages"></a>Visualizzazione delle pagine delle proprietà di un filtro

Una pagina delle proprietà è un modo per un filtro per supportare le proprietà che possono essere impostate dall'utente. Questo articolo descrive come visualizzare le pagine delle proprietà di un filtro in un'applicazione. Per ulteriori informazioni sulle pagine delle proprietà, vedere la documentazione di Platform SDK.

> [!Note]  
> Anche se molti dei filtri forniti con le pagine delle proprietà supportano DirectShow, sono destinati a scopi di debug e non sono consigliati per l'uso da parte dell'applicazione. Nella maggior parte dei casi, la funzionalità equivalente viene fornita tramite un'interfaccia personalizzata sul filtro. Un'applicazione deve controllare questi filtri a livello di codice, anziché esporre le pagine delle proprietà agli utenti.

 

I filtri con le pagine delle proprietà espongono l'interfaccia **ISpecifyPropertyPages** . Per determinare se un filtro definisce una pagina delle proprietà, eseguire una query sul filtro per questa interfaccia utilizzando **QueryInterface**.

Se è stata creata direttamente un'istanza di un filtro (chiamando **CoCreateInstance**), si dispone già di un puntatore al filtro. In caso contrario, è possibile enumerare i filtri nel grafico usando il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) . Per informazioni dettagliate, vedere [enumerazione di oggetti in un grafico a filtro](enumerating-objects-in-a-filter-graph.md).

Una volta ottenuto il puntatore all'interfaccia **ISpecifyPropertyPages** , recuperare le pagine delle proprietà del filtro chiamando il metodo **ISpecifyPropertyPages:: GetPages** . Questo metodo compila una matrice conteggiata di identificatori univoci globali (GUID) con l'identificatore di classe (CLSID) di ogni pagina delle proprietà. Una matrice conteggiata è definita da una struttura **CAUUID** , che è necessario allocare ma che non è necessario inizializzare. Il metodo **GetPages** alloca la matrice, che è contenuta nel membro **pElems** della struttura **CAUUID** . Al termine, liberare la matrice chiamando la funzione **CoTaskMemFree** .

La funzione **OleCreatePropertyFrame** fornisce un modo semplice per visualizzare le pagine delle proprietà all'interno di una finestra di dialogo modale.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 



