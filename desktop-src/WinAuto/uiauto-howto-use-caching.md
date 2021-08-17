---
title: Come usare il Servizio di memorizzazione nella cache
description: Questo argomento contiene codice di esempio che illustra come usare le funzionalità di memorizzazione nella cache (o recupero bulk) di Microsoft Automazione interfaccia utente albero.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a020f200384f88e1e4f06f9418676e8fc567851424ed03b1c36e2e6299f98e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133254"
---
# <a name="how-to-use-caching"></a>Come usare il Servizio di memorizzazione nella cache

Questo argomento contiene codice di esempio che illustra come usare le funzionalità di memorizzazione nella cache (o recupero bulk) di Microsoft Automazione interfaccia utente albero. Vengono illustrati gli argomenti seguenti:

-   [Recupero di proprietà e pattern di controllo nella cache](#fetching-properties-and-control-patterns-into-the-cache)
-   [Recupero di proprietà e pattern di controllo dalla cache](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Argomenti correlati](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Recupero di proprietà e pattern di controllo nella cache

Nell'esempio di codice seguente viene illustrata una funzione che recupera elementi da un controllo elenco e memorizza nella cache il pattern di controllo SelectionItem e la proprietà Name per ogni elemento. Per impostazione predefinita, gli elementi dell'elenco vengono restituiti con un riferimento completo, in modo che tutte le proprietà correnti siano ancora disponibili.


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



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Recupero di proprietà e pattern di controllo dalla cache

Nel codice seguente viene illustrato come recuperare proprietà e pattern di controllo dalla cache. Recupera il pattern di controllo SelectionItem e la proprietà Name per un elemento dell'elenco.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Caching Automazione interfaccia utente proprietà e pattern di controllo](uiauto-cachingforclients.md)
</dt> <dt>

[Procedure per i Automazione interfaccia utente client](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




