---
title: Procedura per l'albero Automazione interfaccia utente dati
description: Questo argomento contiene codice di esempio che illustra come usare l'interfaccia IUIAutomationTreeWalker per esaminare ed esaminare gli elementi nell'albero Automazione interfaccia utente Microsoft.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe6539a24f271f5c1e8042b1be9933a77f1118b27730d510026de1852d7938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324449"
---
# <a name="how-to-walk-the-ui-automation-tree"></a>Procedura per l'albero Automazione interfaccia utente dati

Questo argomento contiene codice di esempio che illustra come usare l'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per esaminare ed esaminare gli elementi nell'albero Automazione interfaccia utente Microsoft. Vengono illustrati gli argomenti seguenti:

-   [Scorrere i discendenti di un elemento](#walking-through-descendants-of-an-element)
-   [Attraversa gli elementi predecessore](#walking-through-ancestor-elements)
-   [Argomenti correlati](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a>Scorrere i discendenti di un elemento

L'esempio di codice seguente è una funzione ricorsiva che illustra tutti i discendenti di un elemento dell'interfaccia utente e visualizza i relativi tipi di controllo in un elenco gerarchico.


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a>Attraversa gli elementi predecessore

L'esempio di codice seguente è una funzione che consente di scorrere i predecessori di un elemento per identificare l'elemento padre. Ciò è utile quando è necessario identificare la finestra padre di un controllo . La funzione restituisce **NULL per** gli elementi di primo livello. elementi il cui padre è il desktop.


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Ottenere elementi di automazione interfaccia utente](uiauto-obtainingelements.md)
</dt> <dt>

[Procedure per i Automazione interfaccia utente client](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




