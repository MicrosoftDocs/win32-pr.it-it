---
title: Pattern di controllo ScrollItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IScrollItemProvider, incluse informazioni sui metodi.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo ScrollItem
- Automazione interfaccia utente, pattern di controllo ScrollItem
- Automazione interfaccia utente, IScrollItemProvider
- IScrollItemProvider
- implementazione di pattern di controllo ScrollItem di automazione interfaccia utente
- Pattern di controllo ScrollItem
- pattern di controllo, IScrollItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente ScrollItem
- pattern di controllo, ScrollItem
- interfacce, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221568"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="3a3e6-113">Pattern di controllo ScrollItem</span><span class="sxs-lookup"><span data-stu-id="3a3e6-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="3a3e6-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluse informazioni sui metodi.</span><span class="sxs-lookup"><span data-stu-id="3a3e6-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="3a3e6-115">Il pattern di controllo **ScrollItem** viene usato per supportare singoli controlli figlio di contenitori che implementano [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span><span class="sxs-lookup"><span data-stu-id="3a3e6-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="3a3e6-116">L'esistenza del pattern di controllo **ScrollItem** in un controllo non implica che il relativo contenitore o qualsiasi predecessore debba implementare il pattern di controllo **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="3a3e6-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="3a3e6-117">Quando il contenitore implementa il pattern di controllo **Scroll** , il pattern di controllo **ScrollItem** funge da canale di comunicazione tra un controllo figlio e il relativo contenitore per garantire che il contenitore possa modificare il contenuto o l'area attualmente visibile all'interno del viewport per visualizzare il controllo figlio.</span><span class="sxs-lookup"><span data-stu-id="3a3e6-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="3a3e6-118">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3a3e6-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3a3e6-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a3e6-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a3e6-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="3a3e6-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3a3e6-121">Membri obbligatori per **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3a3e6-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="3a3e6-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a3e6-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3a3e6-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="3a3e6-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3a3e6-124">Quando si implementa il pattern di controllo **ScrollItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a3e6-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3a3e6-125">Gli elementi contenuti in una [finestra](uiauto-supportwindowcontroltype.md) o in un controllo **Canvas** non sono necessari per implementare l'interfaccia [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="3a3e6-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="3a3e6-126">In alternativa, tuttavia, devono esporre un percorso valido per la proprietà [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (o [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)).</span><span class="sxs-lookup"><span data-stu-id="3a3e6-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="3a3e6-127">Ciò consentirà a un'applicazione client di automazione interfaccia utente Microsoft di usare i metodi del pattern di controllo [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) sul contenitore per visualizzare l'elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="3a3e6-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="3a3e6-128">Membri obbligatori per **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3a3e6-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="3a3e6-129">Il metodo seguente è necessario per implementare l'interfaccia [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="3a3e6-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="3a3e6-130">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="3a3e6-130">Required members</span></span>                                                    | <span data-ttu-id="3a3e6-131">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="3a3e6-131">Member type</span></span> | <span data-ttu-id="3a3e6-132">Note</span><span class="sxs-lookup"><span data-stu-id="3a3e6-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="3a3e6-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="3a3e6-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="3a3e6-134">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a3e6-134">Method</span></span>      | <span data-ttu-id="3a3e6-135">nessuno</span><span class="sxs-lookup"><span data-stu-id="3a3e6-135">None</span></span>  |



 

<span data-ttu-id="3a3e6-136">Questo pattern di controllo non è associato a proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="3a3e6-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a3e6-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a3e6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3e6-138">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="3a3e6-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3a3e6-139">Pattern di controllo Selection</span><span class="sxs-lookup"><span data-stu-id="3a3e6-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="3a3e6-140">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3a3e6-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3a3e6-141">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3a3e6-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




