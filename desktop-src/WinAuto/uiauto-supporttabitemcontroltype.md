---
title: Tipo di controllo TabItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo TabItem
- Automazione interfaccia utente, tipo di controllo TabItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo TabItem
- Automazione interfaccia utente, proprietà per il tipo di controllo TabItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo TabItem
- Automazione interfaccia utente, eventi per il tipo di controllo TabItem
- strutture ad albero, tipo di controllo TabItem
- Proprietà, tipo di controllo TabItem
- pattern di controllo, tipo di controllo TabItem
- eventi, tipo di controllo TabItem
- supporto per il tipo di controllo TabItem
- Tipo di controllo TabItem
- tipi di controllo, struttura ad albero per il tipo di controllo TabItem
- tipi di controllo, pattern di controllo per il tipo di controllo TabItem
- tipi di controllo, supporto per TabItem
- tipi di controllo, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221863"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="788ef-119">Tipo di controllo TabItem</span><span class="sxs-lookup"><span data-stu-id="788ef-119">TabItem Control Type</span></span>

<span data-ttu-id="788ef-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="788ef-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="788ef-121">Un controllo voce di scheda viene usato come controllo in un controllo Struttura a schede che seleziona una pagina specifica da visualizzare in una finestra.</span><span class="sxs-lookup"><span data-stu-id="788ef-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="788ef-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="788ef-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="788ef-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli voce di scheda in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="788ef-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="788ef-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="788ef-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="788ef-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="788ef-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="788ef-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="788ef-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="788ef-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="788ef-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="788ef-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="788ef-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="788ef-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="788ef-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="788ef-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="788ef-130">Typical Tree Structure</span></span>

<span data-ttu-id="788ef-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa ai controlli voce di scheda e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="788ef-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="788ef-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="788ef-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="788ef-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="788ef-133">Control View</span></span></th>
<th><span data-ttu-id="788ef-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="788ef-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="788ef-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="788ef-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="788ef-136">Image (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="788ef-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="788ef-137">Testo</span><span class="sxs-lookup"><span data-stu-id="788ef-137">Text</span></span></li>
<li><span data-ttu-id="788ef-138">Riquadro</span><span class="sxs-lookup"><span data-stu-id="788ef-138">Pane</span></span>
<ul>
<li><span data-ttu-id="788ef-139">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="788ef-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="788ef-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="788ef-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="788ef-141">Riquadro</span><span class="sxs-lookup"><span data-stu-id="788ef-141">Pane</span></span>
<ul>
<li><span data-ttu-id="788ef-142">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="788ef-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="788ef-143">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="788ef-143">Relevant Properties</span></span>

<span data-ttu-id="788ef-144">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="788ef-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="788ef-145">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="788ef-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="788ef-146">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="788ef-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="788ef-147">Valore</span><span class="sxs-lookup"><span data-stu-id="788ef-147">Value</span></span>       | <span data-ttu-id="788ef-148">Note</span><span class="sxs-lookup"><span data-stu-id="788ef-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="788ef-149">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="788ef-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-150">See notes.</span></span>  | <span data-ttu-id="788ef-151">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="788ef-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="788ef-152">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="788ef-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-153">See notes.</span></span>  | <span data-ttu-id="788ef-154">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="788ef-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="788ef-155">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="788ef-156">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-156">See notes.</span></span>  | <span data-ttu-id="788ef-157">Il controllo voce di scheda deve avere un punto su cui è possibile fare clic per selezionare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="788ef-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="788ef-158">**\_CONTROLLERFORPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="788ef-159">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-159">See notes.</span></span>  | <span data-ttu-id="788ef-160">Questa proprietà può essere usata come puntatore al riquadro schede associato.</span><span class="sxs-lookup"><span data-stu-id="788ef-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="788ef-161">Ciò risulta utile nel caso in cui non possa ospitare un riquadro come figlio dell'oggetto voce di scheda.</span><span class="sxs-lookup"><span data-stu-id="788ef-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="788ef-162">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="788ef-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="788ef-163">**TabItem**</span></span> | <span data-ttu-id="788ef-164">Questo valore è uguale per tutti i framework dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="788ef-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="788ef-165">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="788ef-166">true</span><span class="sxs-lookup"><span data-stu-id="788ef-166">TRUE</span></span>        | <span data-ttu-id="788ef-167">Il controllo voce di scheda viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="788ef-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="788ef-168">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="788ef-169">true</span><span class="sxs-lookup"><span data-stu-id="788ef-169">TRUE</span></span>        | <span data-ttu-id="788ef-170">Il controllo voce di scheda viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="788ef-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="788ef-171">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="788ef-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-172">See notes.</span></span>  | <span data-ttu-id="788ef-173">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="788ef-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="788ef-174">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="788ef-175">Null</span><span class="sxs-lookup"><span data-stu-id="788ef-175">Null</span></span>        | <span data-ttu-id="788ef-176">Il controllo voce di scheda non ha un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="788ef-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="788ef-177">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="788ef-178">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-178">See notes.</span></span>  | <span data-ttu-id="788ef-179">Stringa localizzata corrispondente al tipo di controllo **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="788ef-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="788ef-180">Il valore predefinito è "Tab Item" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="788ef-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="788ef-181">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="788ef-182">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="788ef-182">See notes.</span></span>  | <span data-ttu-id="788ef-183">Il controllo voce di scheda con etichetta automatica.</span><span class="sxs-lookup"><span data-stu-id="788ef-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="788ef-184">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="788ef-184">Required Control Patterns</span></span>

<span data-ttu-id="788ef-185">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli voce di scheda.</span><span class="sxs-lookup"><span data-stu-id="788ef-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="788ef-186">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="788ef-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="788ef-187">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="788ef-187">Control Pattern</span></span>                                                 | <span data-ttu-id="788ef-188">Supporto</span><span class="sxs-lookup"><span data-stu-id="788ef-188">Support</span></span>  | <span data-ttu-id="788ef-189">Note</span><span class="sxs-lookup"><span data-stu-id="788ef-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="788ef-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="788ef-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="788ef-191">Necessario</span><span class="sxs-lookup"><span data-stu-id="788ef-191">Required</span></span> | <span data-ttu-id="788ef-192">Il controllo voce di scheda deve supportare [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span><span class="sxs-lookup"><span data-stu-id="788ef-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="788ef-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="788ef-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="788ef-194">Mai</span><span class="sxs-lookup"><span data-stu-id="788ef-194">Never</span></span>    | <span data-ttu-id="788ef-195">Il controllo voce di scheda non supporta mai [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="788ef-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="788ef-196">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="788ef-196">Required Events</span></span>

<span data-ttu-id="788ef-197">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli voce di scheda.</span><span class="sxs-lookup"><span data-stu-id="788ef-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="788ef-198">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="788ef-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="788ef-199">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="788ef-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="788ef-200">Note</span><span class="sxs-lookup"><span data-stu-id="788ef-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="788ef-201">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="788ef-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="788ef-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="788ef-203">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="788ef-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="788ef-204">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="788ef-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="788ef-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="788ef-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="788ef-206">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="788ef-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="788ef-207">**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="788ef-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="788ef-208">**\_ElementSelectedEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="788ef-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="788ef-209">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="788ef-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="788ef-210">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="788ef-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="788ef-211">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="788ef-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="788ef-212">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="788ef-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="788ef-213">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="788ef-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




