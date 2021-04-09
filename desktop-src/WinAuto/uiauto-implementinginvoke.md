---
title: Pattern di controllo Invoke
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IInvokeProvider, incluse informazioni sui metodi.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Invoke
- Automazione interfaccia utente, pattern di controllo Invoke
- Automazione interfaccia utente, IInvokeProvider
- IInvokeProvider
- implementazione di pattern di controllo Invoke di automazione interfaccia utente
- Richiama pattern di controllo
- pattern di controllo, IInvokeProvider
- pattern di controllo, implementazione di Invoke di automazione interfaccia utente
- pattern di controllo, Invoke
- interfacce, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855922"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="57bba-113">Pattern di controllo Invoke</span><span class="sxs-lookup"><span data-stu-id="57bba-113">Invoke Control Pattern</span></span>

<span data-ttu-id="57bba-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluse informazioni sui metodi.</span><span class="sxs-lookup"><span data-stu-id="57bba-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="57bba-115">Il pattern di controllo **Invoke** viene usato per supportare i controlli che non mantengono lo stato quando sono attivati, bensì avviano o eseguono una singola azione non ambigua.</span><span class="sxs-lookup"><span data-stu-id="57bba-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="57bba-116">I controlli che mantengono lo stato, ad esempio caselle di controllo e pulsanti di opzione, devono invece implementare rispettivamente [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="57bba-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="57bba-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="57bba-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="57bba-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="57bba-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="57bba-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="57bba-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="57bba-120">Membri obbligatori per **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="57bba-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="57bba-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57bba-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="57bba-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="57bba-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="57bba-123">Quando si implementa il pattern di controllo **Invoke** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57bba-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="57bba-124">I controlli implementano [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se lo stesso comportamento non viene esposto tramite un altro provider di pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="57bba-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="57bba-125">Se, ad esempio, il metodo [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) su un controllo esegue la stessa azione del metodo [**IUIAutomationExpandCollapsePattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) o [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , il controllo non deve implementare **IInvokeProvider**.</span><span class="sxs-lookup"><span data-stu-id="57bba-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="57bba-126">La chiamata di un controllo viene in genere eseguita facendo clic o doppio clic oppure premendo INVIO, una scelta rapida predefinita da tastiera o una combinazione alternativa di tasti.</span><span class="sxs-lookup"><span data-stu-id="57bba-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="57bba-127">L'evento **richiamato** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) viene generato su un controllo che è stato attivato (come risposta a un controllo che esegue l'azione associata).</span><span class="sxs-lookup"><span data-stu-id="57bba-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="57bba-128">Se possibile, l'evento deve essere generato dopo che il controllo ha completato l'azione ed è stato restituito senza alcun blocco.</span><span class="sxs-lookup"><span data-stu-id="57bba-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="57bba-129">L'evento **richiamato** (**UIA \_ Invoke \_ InvokedEventId**) deve essere generato prima della manutenzione della richiesta **Invoke** negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="57bba-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="57bba-130">Non è possibile o conveniente attendere il completamento dell'azione.</span><span class="sxs-lookup"><span data-stu-id="57bba-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="57bba-131">L'azione richiede l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="57bba-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="57bba-132">L'azione è dispendiosa a livello di tempo e comporta il blocco del client chiamante un periodo di tempo significativo.</span><span class="sxs-lookup"><span data-stu-id="57bba-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="57bba-133">Se il richiamo del controllo è caratterizzato da effetti collaterali significativi, tali effetti collaterali devono essere esposti tramite la proprietà **HelpText** .</span><span class="sxs-lookup"><span data-stu-id="57bba-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="57bba-134">Ad esempio, anche se [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) non è associato alla selezione, **Invoke** può causare la selezione di un altro controllo.</span><span class="sxs-lookup"><span data-stu-id="57bba-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="57bba-135">Gli effetti del passaggio del mouse (o del mouse su) in genere non costituiscono un evento **richiamato** .</span><span class="sxs-lookup"><span data-stu-id="57bba-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="57bba-136">Tuttavia, i controlli che eseguono un'azione, anziché causare un effetto visivo, basati sullo stato del passaggio del mouse devono supportare il pattern di controllo **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="57bba-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="57bba-137">Questa implementazione viene considerata un problema di accessibilità se il controllo può essere chiamato solo come risultato di un effetto collaterale relativo al mouse.</span><span class="sxs-lookup"><span data-stu-id="57bba-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="57bba-138">La chiamata di un controllo è diversa dalla selezione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="57bba-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="57bba-139">Tuttavia, a seconda del controllo, come effetto collaterale la chiamata potrebbe causare la selezione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="57bba-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="57bba-140">Ad esempio, la chiamata di un elemento dell'elenco di documenti di Microsoft Word nella cartella documenti seleziona l'elemento e apre il documento.</span><span class="sxs-lookup"><span data-stu-id="57bba-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="57bba-141">Un elemento può scomparire dall'albero di automazione interfaccia utente Microsoft immediatamente dopo essere stato richiamato.</span><span class="sxs-lookup"><span data-stu-id="57bba-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="57bba-142">Di conseguenza, la richiesta di informazioni dall'elemento fornito dal callback di evento potrebbe avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="57bba-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="57bba-143">La prelettura delle informazioni memorizzate nella cache rappresenta la soluzione alternativa consigliata.</span><span class="sxs-lookup"><span data-stu-id="57bba-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="57bba-144">I controlli possono implementare più pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="57bba-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="57bba-145">Ad esempio, il controllo **colore riempimento** sulla barra degli strumenti di Microsoft Excel implementa sia il pattern di controllo Invoke che il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="57bba-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="57bba-146">Il pattern di controllo ExpandCollapse espone il menu e il pattern di controllo **Invoke** riempie la selezione attiva con il colore scelto.</span><span class="sxs-lookup"><span data-stu-id="57bba-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="57bba-147">Membri obbligatori per **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="57bba-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="57bba-148">Il metodo seguente è necessario per implementare l'interfaccia [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="57bba-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="57bba-149">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="57bba-149">Required members</span></span>                                | <span data-ttu-id="57bba-150">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="57bba-150">Member type</span></span> | <span data-ttu-id="57bba-151">Note</span><span class="sxs-lookup"><span data-stu-id="57bba-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57bba-152">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="57bba-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="57bba-153">Metodo</span><span class="sxs-lookup"><span data-stu-id="57bba-153">Method</span></span>      | <span data-ttu-id="57bba-154">**Invoke** è una chiamata asincrona e deve restituire immediatamente un valore senza blocco.</span><span class="sxs-lookup"><span data-stu-id="57bba-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="57bba-155">Questo comportamento è particolarmente critico per i controlli che direttamente o indirettamente avviano una finestra di dialogo quando vengono chiamati.</span><span class="sxs-lookup"><span data-stu-id="57bba-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="57bba-156">Qualsiasi client di automazione interfaccia utente che ha generato l'evento rimarrà bloccato fino a quando non viene chiusa la finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="57bba-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="57bba-157">Questo pattern di controllo non è associato a proprietà o eventi.</span><span class="sxs-lookup"><span data-stu-id="57bba-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57bba-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57bba-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57bba-159">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="57bba-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="57bba-160">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="57bba-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="57bba-161">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="57bba-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="57bba-162">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="57bba-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





