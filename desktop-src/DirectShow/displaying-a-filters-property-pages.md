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
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="268be-103">Visualizzazione delle pagine delle proprietà di un filtro</span><span class="sxs-lookup"><span data-stu-id="268be-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="268be-104">Una pagina delle proprietà è un modo per un filtro per supportare le proprietà che possono essere impostate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="268be-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="268be-105">Questo articolo descrive come visualizzare le pagine delle proprietà di un filtro in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="268be-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="268be-106">Per ulteriori informazioni sulle pagine delle proprietà, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="268be-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="268be-107">Anche se molti dei filtri forniti con le pagine delle proprietà supportano DirectShow, sono destinati a scopi di debug e non sono consigliati per l'uso da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="268be-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="268be-108">Nella maggior parte dei casi, la funzionalità equivalente viene fornita tramite un'interfaccia personalizzata sul filtro.</span><span class="sxs-lookup"><span data-stu-id="268be-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="268be-109">Un'applicazione deve controllare questi filtri a livello di codice, anziché esporre le pagine delle proprietà agli utenti.</span><span class="sxs-lookup"><span data-stu-id="268be-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="268be-110">I filtri con le pagine delle proprietà espongono l'interfaccia **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="268be-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="268be-111">Per determinare se un filtro definisce una pagina delle proprietà, eseguire una query sul filtro per questa interfaccia utilizzando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="268be-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="268be-112">Se è stata creata direttamente un'istanza di un filtro (chiamando **CoCreateInstance**), si dispone già di un puntatore al filtro.</span><span class="sxs-lookup"><span data-stu-id="268be-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="268be-113">In caso contrario, è possibile enumerare i filtri nel grafico usando il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) .</span><span class="sxs-lookup"><span data-stu-id="268be-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="268be-114">Per informazioni dettagliate, vedere [enumerazione di oggetti in un grafico a filtro](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="268be-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="268be-115">Una volta ottenuto il puntatore all'interfaccia **ISpecifyPropertyPages** , recuperare le pagine delle proprietà del filtro chiamando il metodo **ISpecifyPropertyPages:: GetPages** .</span><span class="sxs-lookup"><span data-stu-id="268be-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="268be-116">Questo metodo compila una matrice conteggiata di identificatori univoci globali (GUID) con l'identificatore di classe (CLSID) di ogni pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="268be-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="268be-117">Una matrice conteggiata è definita da una struttura **CAUUID** , che è necessario allocare ma che non è necessario inizializzare.</span><span class="sxs-lookup"><span data-stu-id="268be-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="268be-118">Il metodo **GetPages** alloca la matrice, che è contenuta nel membro **pElems** della struttura **CAUUID** .</span><span class="sxs-lookup"><span data-stu-id="268be-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="268be-119">Al termine, liberare la matrice chiamando la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="268be-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="268be-120">La funzione **OleCreatePropertyFrame** fornisce un modo semplice per visualizzare le pagine delle proprietà all'interno di una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="268be-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="268be-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="268be-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="268be-122">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="268be-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



