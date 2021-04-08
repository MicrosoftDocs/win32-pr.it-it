---
title: Come abilitare la navigazione in un provider di frammenti di automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come abilitare la navigazione in un provider di automazione interfaccia utente Microsoft per un elemento in un frammento.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044189"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="a66d9-103">Come abilitare la navigazione in un provider di frammenti di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a66d9-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="a66d9-104">Questo argomento contiene codice di esempio che illustra come abilitare la navigazione in un provider di automazione interfaccia utente Microsoft per un elemento in un frammento.</span><span class="sxs-lookup"><span data-stu-id="a66d9-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="a66d9-105">Il codice di esempio seguente implementa il metodo [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) per una voce di elenco in un controllo elenco personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a66d9-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="a66d9-106">L'elemento padre è il controllo elenco personalizzato, mentre gli elementi di pari livello sono altri elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a66d9-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="a66d9-107">Il metodo imposta il parametro *pRetVal* su **null** se non è presente alcun elemento nella direzione specificata.</span><span class="sxs-lookup"><span data-stu-id="a66d9-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a><span data-ttu-id="a66d9-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a66d9-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a66d9-109">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a66d9-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a66d9-110">Implementazione di un provider di automazione interfaccia utente Server-Side</span><span class="sxs-lookup"><span data-stu-id="a66d9-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="a66d9-111">Procedure per i provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a66d9-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




