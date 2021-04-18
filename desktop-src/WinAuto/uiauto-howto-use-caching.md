---
title: Come usare il Servizio di memorizzazione nella cache
description: Questo argomento contiene codice di esempio che illustra come usare le funzionalità di memorizzazione nella cache (o recupero bulk) dell'albero di automazione interfaccia utente Microsoft.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298111"
---
# <a name="how-to-use-caching"></a><span data-ttu-id="6f01b-103">Come usare il Servizio di memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="6f01b-103">How to Use Caching</span></span>

<span data-ttu-id="6f01b-104">Questo argomento contiene codice di esempio che illustra come usare le funzionalità di memorizzazione nella cache (o recupero bulk) dell'albero di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f01b-104">This topic contains example code that shows how to use the caching (or bulk fetching) capabilities of Microsoft UI Automation tree.</span></span> <span data-ttu-id="6f01b-105">Vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f01b-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="6f01b-106">Recupero di proprietà e pattern di controllo nella cache</span><span class="sxs-lookup"><span data-stu-id="6f01b-106">Fetching Properties and Control Patterns into the Cache</span></span>](#fetching-properties-and-control-patterns-into-the-cache)
-   [<span data-ttu-id="6f01b-107">Recupero di proprietà e pattern di controllo dalla cache</span><span class="sxs-lookup"><span data-stu-id="6f01b-107">Retrieving Properties and Control Patterns from the Cache</span></span>](#retrieving-properties-and-control-patterns-from-the-cache)
-   [<span data-ttu-id="6f01b-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f01b-108">Related topics</span></span>](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a><span data-ttu-id="6f01b-109">Recupero di proprietà e pattern di controllo nella cache</span><span class="sxs-lookup"><span data-stu-id="6f01b-109">Fetching Properties and Control Patterns into the Cache</span></span>

<span data-ttu-id="6f01b-110">Nell'esempio di codice seguente viene illustrata una funzione che recupera gli elementi da un controllo elenco e memorizza nella cache il pattern di controllo SelectionItem e la proprietà Name per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="6f01b-110">The following code example shows a function that retrieves items from a list control and caches the SelectionItem control pattern and Name property for each item.</span></span> <span data-ttu-id="6f01b-111">Per impostazione predefinita, gli elementi dell'elenco vengono restituiti con un riferimento completo, in modo che tutte le proprietà correnti siano ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="6f01b-111">By default, the list items are returned with a full reference, so that all current properties are still available.</span></span>


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a><span data-ttu-id="6f01b-112">Recupero di proprietà e pattern di controllo dalla cache</span><span class="sxs-lookup"><span data-stu-id="6f01b-112">Retrieving Properties and Control Patterns from the Cache</span></span>

<span data-ttu-id="6f01b-113">Il codice seguente illustra come recuperare le proprietà e i pattern di controllo dalla cache.</span><span class="sxs-lookup"><span data-stu-id="6f01b-113">The following code demonstrates how to retrieve properties and control patterns from the cache.</span></span> <span data-ttu-id="6f01b-114">Recupera il pattern di controllo SelectionItem e la proprietà Name per un elemento elenco.</span><span class="sxs-lookup"><span data-stu-id="6f01b-114">It retrieves the SelectionItem control pattern and Name property for a list item.</span></span>


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6f01b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f01b-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f01b-116">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6f01b-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f01b-117">Memorizzare nella cache le proprietà e i pattern di controllo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6f01b-117">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
</dt> <dt>

[<span data-ttu-id="6f01b-118">Procedure per i client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6f01b-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




