---
title: Pattern di controllo SelectionItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISelectionItemProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SelectionItem
- Automazione interfaccia utente, pattern di controllo SelectionItem
- Automazione interfaccia utente, ISelectionItemProvider
- ISelectionItemProvider
- implementazione di pattern di controllo SelectionItem di automazione interfaccia utente
- Pattern di controllo SelectionItem
- pattern di controllo, ISelectionItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SelectionItem
- pattern di controllo, SelectionItem
- interfacce, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297837"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="9f63d-113">Pattern di controllo SelectionItem</span><span class="sxs-lookup"><span data-stu-id="9f63d-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="9f63d-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), incluse informazioni su proprietà, metodi ed eventi.</span><span class="sxs-lookup"><span data-stu-id="9f63d-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="9f63d-115">Il pattern di controllo **SelectionItem** viene usato per supportare i controlli che fungono da singoli elementi figlio selezionabili dei controlli contenitore che implementano [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="9f63d-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="9f63d-116">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9f63d-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9f63d-117">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f63d-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9f63d-118">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="9f63d-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9f63d-119">Membri obbligatori per **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="9f63d-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="9f63d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f63d-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9f63d-121">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="9f63d-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9f63d-122">Quando si implementa il pattern di controllo **SelectionItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f63d-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9f63d-123">I controlli a selezione singola che gestiscono i controlli figlio che implementano [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), ad esempio il dispositivo di scorrimento **risoluzione schermo** nella finestra di dialogo **proprietà di visualizzazione** per Windows, devono implementare [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); i relativi elementi figlio devono implementare sia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) che [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="9f63d-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="9f63d-124">Membri obbligatori per **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="9f63d-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="9f63d-125">Le proprietà, i metodi e gli eventi seguenti sono obbligatori per l'implementazione dell'interfaccia [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="9f63d-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="9f63d-126">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="9f63d-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="9f63d-127">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="9f63d-127">Member type</span></span> | <span data-ttu-id="9f63d-128">Note</span><span class="sxs-lookup"><span data-stu-id="9f63d-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9f63d-129">**AddToSelection**</span><span class="sxs-lookup"><span data-stu-id="9f63d-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="9f63d-130">Metodo</span><span class="sxs-lookup"><span data-stu-id="9f63d-130">Method</span></span>      | <span data-ttu-id="9f63d-131">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-131">None</span></span>  |
| [<span data-ttu-id="9f63d-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="9f63d-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="9f63d-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f63d-133">Property</span></span>    | <span data-ttu-id="9f63d-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-134">None</span></span>  |
| [<span data-ttu-id="9f63d-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="9f63d-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="9f63d-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="9f63d-136">Method</span></span>      | <span data-ttu-id="9f63d-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-137">None</span></span>  |
| [<span data-ttu-id="9f63d-138">**Selezionare**</span><span class="sxs-lookup"><span data-stu-id="9f63d-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="9f63d-139">Metodo</span><span class="sxs-lookup"><span data-stu-id="9f63d-139">Method</span></span>      | <span data-ttu-id="9f63d-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-140">None</span></span>  |
| [<span data-ttu-id="9f63d-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="9f63d-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="9f63d-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f63d-142">Property</span></span>    | <span data-ttu-id="9f63d-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-143">None</span></span>  |
| [<span data-ttu-id="9f63d-144">**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="9f63d-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="9f63d-145">Evento</span><span class="sxs-lookup"><span data-stu-id="9f63d-145">Event</span></span>       | <span data-ttu-id="9f63d-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-146">None</span></span>  |
| [<span data-ttu-id="9f63d-147">**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="9f63d-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="9f63d-148">Evento</span><span class="sxs-lookup"><span data-stu-id="9f63d-148">Event</span></span>       | <span data-ttu-id="9f63d-149">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-149">None</span></span>  |
| [<span data-ttu-id="9f63d-150">**\_ElementSelectedEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="9f63d-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="9f63d-151">Evento</span><span class="sxs-lookup"><span data-stu-id="9f63d-151">Event</span></span>       | <span data-ttu-id="9f63d-152">nessuno</span><span class="sxs-lookup"><span data-stu-id="9f63d-152">None</span></span>  |



 

<span data-ttu-id="9f63d-153">Se il risultato di una [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), di [**un AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)o di un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) è un singolo elemento selezionato, è necessario generare un evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)); in caso contrario, generare gli eventi **ElementAddedToSelection** ([**UIA SelectionItem ElementAddedToSelectionEventId) o \_ \_**](uiauto-event-ids.md) **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="9f63d-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f63d-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f63d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f63d-155">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="9f63d-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9f63d-156">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9f63d-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9f63d-157">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9f63d-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




