---
title: Accesso ai server Microsoft Active Accessibility
description: Microsoft Active Accessibility al proxy di automazione interfaccia utente è un componente software che consente ai client di automazione interfaccia utente Microsoft di interagire con i server Microsoft Active Accessibility che implementano l'interfaccia IAccessible in modo nativo.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automazione interfaccia utente, accesso Active Accessibility
- Automazione interfaccia utente, Active Accessibility
- Proxy di automazione interfaccia utente
- Automazione interfaccia utente, proxy di automazione interfaccia utente
- Pattern di controllo LegacyIAccessible
- Automazione interfaccia utente, pattern di controllo LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- client, accesso a server Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044413"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="16fa7-112">Accesso ai server Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="16fa7-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="16fa7-113">Microsoft Active Accessibility al proxy di automazione interfaccia utente è un componente software che consente ai client di automazione interfaccia utente Microsoft di interagire con i server Microsoft Active Accessibility che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="16fa7-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="16fa7-114">Il proxy supporta il pattern di controllo [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) e fornisce un'istanza dell'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) per ogni server Active Accessibility Microsoft rilevato.</span><span class="sxs-lookup"><span data-stu-id="16fa7-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="16fa7-115">I client di automazione interfaccia utente usano i metodi esposti da **IUIAutomationLegacyIAccessiblePattern** per accedere alle proprietà e agli oggetti di Microsoft Active Accessibility supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="16fa7-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="16fa7-116">Se un elemento di automazione interfaccia utente dispone di un'implementazione di Microsoft Active Accessibility sottostante, un client può ottenere un puntatore di interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) per l'elemento passando l'ID del pattern di controllo [**\_ LegacyIAccessiblePatternId di UIA**](uiauto-controlpattern-ids.md) a uno dei seguenti metodi [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :</span><span class="sxs-lookup"><span data-stu-id="16fa7-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="16fa7-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="16fa7-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="16fa7-118">**GetCachedPatternAs**</span><span class="sxs-lookup"><span data-stu-id="16fa7-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="16fa7-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="16fa7-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="16fa7-120">**GetCurrentPatternAs**</span><span class="sxs-lookup"><span data-stu-id="16fa7-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="16fa7-121">L'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) non è disponibile per i controlli basati sull'automazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="16fa7-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="16fa7-122">L'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) consente ai client di automazione interfaccia utente di accedere all'implementazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sottostante di un elemento Active Accessibility Microsoft.</span><span class="sxs-lookup"><span data-stu-id="16fa7-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="16fa7-123">Tuttavia, l'interfaccia non supporta i metodi obsoleti o ridondanti con le funzionalità di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="16fa7-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="16fa7-124">Ad esempio, **IUIAutomationLegacyIAccessiblePattern** non dispone di un metodo equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché la posizione corrente di un elemento dell'interfaccia utente è disponibile dalla proprietà BoundingRectangle di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="16fa7-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="16fa7-125">Il metodo [**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) consente a un client di recuperare un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da un elemento di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="16fa7-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="16fa7-126">Il contrario è possibile anche usando i metodi [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .</span><span class="sxs-lookup"><span data-stu-id="16fa7-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="16fa7-127">[**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) restituisce **null** se l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento viene fornita da un oggetto proxy da OLEACC.dll o dall'automazione interfaccia utente a Microsoft Active Accessibility Bridge.</span><span class="sxs-lookup"><span data-stu-id="16fa7-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16fa7-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16fa7-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="16fa7-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="16fa7-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="16fa7-130">Automazione interfaccia utente e Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="16fa7-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="16fa7-131">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="16fa7-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




