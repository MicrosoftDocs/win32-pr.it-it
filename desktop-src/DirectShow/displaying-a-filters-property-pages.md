---
description: Visualizzazione delle pagine delle proprietà di un filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Visualizzazione delle pagine delle proprietà di un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0e29654983ee51b98666411a11f7130eb896c380ec754b5576862c313dcbc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016138"
---
# <a name="displaying-a-filters-property-pages"></a>Visualizzazione delle pagine delle proprietà di un filtro

Una pagina delle proprietà è un modo per un filtro per supportare le proprietà che l'utente può impostare. Questo articolo descrive come visualizzare le pagine delle proprietà di un filtro in un'applicazione. Per altre informazioni sulle pagine delle proprietà, vedere la documentazione di Platform SDK.

> [!Note]  
> Sebbene molti dei filtri forniti con le pagine DirectShow supportino le pagine delle proprietà, sono destinati al debug e non sono consigliati per l'uso dell'applicazione. Nella maggior parte dei casi la funzionalità equivalente viene fornita tramite un'interfaccia personalizzata nel filtro. Un'applicazione deve controllare questi filtri a livello di codice, anziché esporre le pagine delle proprietà agli utenti.

 

I filtri con pagine delle proprietà **espongono l'interfaccia ISpecifyPropertyPages.** Per determinare se un filtro definisce una pagina delle proprietà, eseguire una query sul filtro per questa interfaccia usando **QueryInterface**.

Se è stata creata direttamente un'istanza di un filtro (chiamando **CoCreateInstance**), è già presente un puntatore al filtro. In caso contrario, è possibile enumerare i filtri nel grafico usando il [**metodo IFilterGraph::EnumFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) Per informazioni dettagliate, vedere [Enumerazione di oggetti in un filtro Graph](enumerating-objects-in-a-filter-graph.md).

Dopo aver creato il puntatore a interfaccia **ISpecifyPropertyPages,** recuperare le pagine delle proprietà del filtro chiamando il metodo **ISpecifyPropertyPages::GetPages.** Questo metodo riempie una matrice conteggiata di identificatori univoci globali (GUID) con l'identificatore di classe (CLSID) di ogni pagina delle proprietà. Una matrice conteggiata viene definita da una **struttura CAUUID,** che è necessario allocare ma non è necessario inizializzare. Il **metodo GetPages** alloca la matrice, contenuta nel membro **pElems** della **struttura CAUUID.** Al termine, liberare la matrice chiamando la **funzione CoTaskMemFree.**

La **funzione OleCreatePropertyFrame** consente di visualizzare in modo semplice le pagine delle proprietà all'interno di una finestra di dialogo modale.


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

 

 



