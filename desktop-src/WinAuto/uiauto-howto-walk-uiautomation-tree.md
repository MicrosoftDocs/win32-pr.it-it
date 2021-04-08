---
title: Come esaminare l'albero di automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come usare l'interfaccia IUIAutomationTreeWalker per esaminare ed esaminare gli elementi nell'albero di automazione interfaccia utente Microsoft.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855993"
---
# <a name="how-to-walk-the-ui-automation-tree"></a><span data-ttu-id="8d021-103">Come esaminare l'albero di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8d021-103">How to Walk the UI Automation Tree</span></span>

<span data-ttu-id="8d021-104">Questo argomento contiene codice di esempio che illustra come usare l'interfaccia [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) per esaminare ed esaminare gli elementi nell'albero di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d021-104">This topic contains example code that shows how to use the [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface to walk through and examine the elements in the Microsoft UI Automation tree.</span></span> <span data-ttu-id="8d021-105">Vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d021-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="8d021-106">Scorrere i discendenti di un elemento</span><span class="sxs-lookup"><span data-stu-id="8d021-106">Walking through Descendants of an Element</span></span>](#walking-through-descendants-of-an-element)
-   [<span data-ttu-id="8d021-107">Esplorazione degli elementi predecessore</span><span class="sxs-lookup"><span data-stu-id="8d021-107">Walking through Ancestor Elements</span></span>](#walking-through-ancestor-elements)
-   [<span data-ttu-id="8d021-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d021-108">Related topics</span></span>](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a><span data-ttu-id="8d021-109">Scorrere i discendenti di un elemento</span><span class="sxs-lookup"><span data-stu-id="8d021-109">Walking through Descendants of an Element</span></span>

<span data-ttu-id="8d021-110">L'esempio di codice seguente è una funzione ricorsiva che analizza tutti i discendenti di un elemento dell'interfaccia utente e Visualizza i relativi tipi di controllo in un elenco gerarchico.</span><span class="sxs-lookup"><span data-stu-id="8d021-110">The following code example is a recursive function that walks through all the descendants of a UI element and displays their control types in a hierarchical list.</span></span>


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



## <a name="walking-through-ancestor-elements"></a><span data-ttu-id="8d021-111">Esplorazione degli elementi predecessore</span><span class="sxs-lookup"><span data-stu-id="8d021-111">Walking through Ancestor Elements</span></span>

<span data-ttu-id="8d021-112">L'esempio di codice seguente è una funzione che analizza i predecessori di un elemento per identificare l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="8d021-112">The following code example is a function that walks through the ancestors of a element to identify the parent element.</span></span> <span data-ttu-id="8d021-113">Questa operazione è utile quando è necessario identificare la finestra padre di un controllo.</span><span class="sxs-lookup"><span data-stu-id="8d021-113">This is useful when you need to identify the parent window of a control.</span></span> <span data-ttu-id="8d021-114">La funzione restituisce **null** per gli elementi di primo livello. ovvero gli elementi il cui padre è il desktop.</span><span class="sxs-lookup"><span data-stu-id="8d021-114">The function returns **NULL** for top-level elements; that is, elements whose parent is the desktop.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8d021-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d021-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d021-116">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8d021-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d021-117">Ottenere elementi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8d021-117">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="8d021-118">Procedure per i client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8d021-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




