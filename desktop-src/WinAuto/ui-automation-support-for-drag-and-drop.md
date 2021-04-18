---
title: Supporto di automazione interfaccia utente per il trascinamento della selezione
description: Questo argomento descrive i pattern di controllo che espongono informazioni sulla funzionalità di trascinamento della selezione di un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automazione interfaccia utente, supporto del trascinamento della selezione
- Automazione interfaccia utente, panoramica del modello di trascinamento
- Automazione interfaccia utente, panoramica del modello DropTarget
- Automazione interfaccia utente, panoramica del trascinamento della selezione
- modelli di trascinamento della selezione, informazioni
- Trascinare il pattern di controllo
- Pattern di controllo DropTarget
- pattern di controllo, trascinamento
- pattern di controllo, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300061"
---
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="67347-112">Supporto di automazione interfaccia utente per il trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="67347-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="67347-113">Automazione interfaccia utente Microsoft definisce due pattern di controllo per supportare gli scenari di trascinamento della selezione, il pattern di controllo di [trascinamento](/windows/desktop/WinAuto/uiauto-implementingdrag) e il pattern di controllo [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="67347-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="67347-114">Si implementa il pattern di controllo di trascinamento per un elemento che può essere trascinato e il pattern di controllo DropTarget per un elemento che può ricevere un elemento trascinato; ovvero una destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="67347-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="67347-115">I due pattern di controllo espongono informazioni che possono essere usate da una tecnologia per l'accessibilità per consentire a un utente di accessibilità di completare un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="67347-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="67347-116">Stili di trascinamento</span><span class="sxs-lookup"><span data-stu-id="67347-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="67347-117">Stile di origine/destinazione</span><span class="sxs-lookup"><span data-stu-id="67347-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="67347-118">Stile di solo origine</span><span class="sxs-lookup"><span data-stu-id="67347-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="67347-119">Trascinamento di più elementi</span><span class="sxs-lookup"><span data-stu-id="67347-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="67347-120">Interfacce client per il trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="67347-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="67347-121">Stili di trascinamento</span><span class="sxs-lookup"><span data-stu-id="67347-121">Dragging Styles</span></span>

<span data-ttu-id="67347-122">Quando si implementa il pattern [di controllo di trascinamento](/windows/desktop/WinAuto/uiauto-implementingdrag) per un elemento trascinabile, è necessario decidere se implementare lo stile di trascinamento di *origine/destinazione* oppure lo stile di trascinamento *solo di origine* .</span><span class="sxs-lookup"><span data-stu-id="67347-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="67347-123">Stile di origine/destinazione</span><span class="sxs-lookup"><span data-stu-id="67347-123">Source/target Style</span></span>

<span data-ttu-id="67347-124">Nello stile di origine/destinazione del trascinamento della selezione, l'elemento trascinato ("origine") e l'elemento di destinazione finale ("destinazione") sono distinti e ognuno di essi genera un set di eventi distinto.</span><span class="sxs-lookup"><span data-stu-id="67347-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="67347-125">Ecco il ciclo di vita di un'operazione di trascinamento che usa lo stile di origine/destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="67347-126">Quando l'utente avvia un'operazione di trascinamento:</span><span class="sxs-lookup"><span data-stu-id="67347-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="67347-127">L'origine genera l'evento DragStart [**( \_ \_ DragStartEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-128">Il codice sorgente imposta la proprietà [**IDragProvider:: grabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.</span><span class="sxs-lookup"><span data-stu-id="67347-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="67347-129">Le destinazioni aggiornano le proprietà [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .</span><span class="sxs-lookup"><span data-stu-id="67347-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="67347-130">Quando l'operazione di trascinamento entra in un'area di destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="67347-131">La destinazione genera l'evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="67347-132">Quando l'operazione di trascinamento esce da un'area di destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="67347-133">La destinazione genera l'evento DragLeave [**( \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="67347-134">Quando l'utente rilascia l'elemento trascinato su un non target:</span><span class="sxs-lookup"><span data-stu-id="67347-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="67347-135">L'origine genera l'evento DragCancel [**( \_ \_ DragCancelEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-136">L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.</span><span class="sxs-lookup"><span data-stu-id="67347-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="67347-137">Quando l'utente rilascia l'elemento trascinato su una destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="67347-138">L'origine genera l'evento DragComplete [**( \_ \_ DragCompleteEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-139">L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.</span><span class="sxs-lookup"><span data-stu-id="67347-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="67347-140">La destinazione imposta la proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) per indicare l'effetto che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="67347-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="67347-141">La destinazione genera l'evento [**\_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)eliminato.</span><span class="sxs-lookup"><span data-stu-id="67347-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="67347-142">Gli eventi degli oggetti di origine e di destinazione sono strettamente correlati, ma distinti.</span><span class="sxs-lookup"><span data-stu-id="67347-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="67347-143">I dati relativi a ciò che viene trascinato provengono dall'origine, mentre i dati relativi a "cosa può accadere" e "cosa è accaduto" provengono dalla destinazione.</span><span class="sxs-lookup"><span data-stu-id="67347-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="67347-144">Quando è in corso un'operazione di trascinamento, l'elemento trascinato può essere trascinato all'interno e all'esterno delle aree di destinazione un numero qualsiasi di volte prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="67347-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="67347-145">Qualsiasi destinazione di rilascio che deve aggiornare la relativa proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) in tempo reale deve generare un evento di modifica proprietà aggiuntivo sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="67347-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="67347-146">Stile di solo origine</span><span class="sxs-lookup"><span data-stu-id="67347-146">Source-only Style</span></span>

<span data-ttu-id="67347-147">Lo stile di trascinamento solo origine consente a un provider di evitare di implementare destinazioni di rilascio.</span><span class="sxs-lookup"><span data-stu-id="67347-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="67347-148">La mancata implementazione degli obiettivi di rilascio contribuisce a ridurre il costo di implementazione, ma non fornisce alle applicazioni client di accessibilità informazioni sull'oggetto che ha ricevuto l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="67347-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="67347-149">Ecco il ciclo di vita di un'operazione di trascinamento che usa lo stile di sola origine:</span><span class="sxs-lookup"><span data-stu-id="67347-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="67347-150">Quando l'utente avvia un'operazione di trascinamento:</span><span class="sxs-lookup"><span data-stu-id="67347-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="67347-151">L'origine genera l'evento DragStart [**( \_ \_ DragStartEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-152">Il codice sorgente imposta la proprietà [**IDragProvider:: grabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.</span><span class="sxs-lookup"><span data-stu-id="67347-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="67347-153">Quando l'operazione di trascinamento entra in un'area di destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="67347-154">L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="67347-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="67347-155">Quando l'operazione di trascinamento esce da un'area di destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="67347-156">L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sul valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="67347-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="67347-157">Quando l'utente rilascia l'elemento trascinato su un non target:</span><span class="sxs-lookup"><span data-stu-id="67347-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="67347-158">L'origine genera l'evento DragCancel [**( \_ \_ DragCancelEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-159">L'origine imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **false**.</span><span class="sxs-lookup"><span data-stu-id="67347-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="67347-160">Quando l'utente rilascia l'elemento trascinato su una destinazione:</span><span class="sxs-lookup"><span data-stu-id="67347-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="67347-161">L'origine genera l'evento DragComplete [**( \_ \_ DragCompleteEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-162">L'origine imposta la proprietà [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) per indicare l'effetto che si è verificato quando l'elemento è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="67347-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="67347-163">Trascinamento di più elementi</span><span class="sxs-lookup"><span data-stu-id="67347-163">Dragging Multiple Items</span></span>

<span data-ttu-id="67347-164">Se un provider implementa operazioni di trascinamento della selezione in cui l'utente può trascinare contemporaneamente più oggetti, il provider utilizza gli stili di origine/destinazione o solo origine, come descritto nella sezione precedente, ma con una piccola differenza.</span><span class="sxs-lookup"><span data-stu-id="67347-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="67347-165">Quando l'utente inizia l'operazione di trascinamento, il provider crea un elemento di origine master che rappresenta il set completo di elementi trascinati.</span><span class="sxs-lookup"><span data-stu-id="67347-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="67347-166">L'elemento di origine master genera tutti gli eventi per conto del set di elementi trascinati; gli elementi non generano alcun evento autonomo.</span><span class="sxs-lookup"><span data-stu-id="67347-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="67347-167">Quando l'utente avvia un'operazione di trascinamento:</span><span class="sxs-lookup"><span data-stu-id="67347-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="67347-168">Il provider crea l'elemento di origine master.</span><span class="sxs-lookup"><span data-stu-id="67347-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="67347-169">L'elemento di origine master genera l'evento DragStart ([**\_ \_ DragStartEventId drag**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="67347-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="67347-170">L'elemento di origine master imposta la proprietà [**IDragProvider:: ungrabbing**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) su **true**.</span><span class="sxs-lookup"><span data-stu-id="67347-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="67347-171">L'elemento di origine master aggiorna l'elenco di elementi catturati per includere tutti gli elementi trascinati in modo che il metodo [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) possa recuperare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="67347-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="67347-172">Per questo punto, l'elemento di origine master esegue lo stesso ruolo dell'elemento di origine, come descritto nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="67347-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="67347-173">Interfacce client per il trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="67347-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="67347-174">Le applicazioni client di automazione interfaccia utente usano le interfacce [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) e [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) per accedere alle informazioni relative al trascinamento della selezione dagli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="67347-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 