---
title: Tipo di controllo HeaderItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo HeaderItem
- Automazione interfaccia utente, tipo di controllo HeaderItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo HeaderItem
- Automazione interfaccia utente, proprietà per il tipo di controllo HeaderItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo HeaderItem
- Automazione interfaccia utente, eventi per il tipo di controllo HeaderItem
- strutture ad albero, tipo di controllo HeaderItem
- Proprietà, tipo di controllo HeaderItem
- pattern di controllo, tipo di controllo HeaderItem
- eventi, tipo di controllo HeaderItem
- supporto per il tipo di controllo HeaderItem
- Tipo di controllo HeaderItem
- tipi di controllo, struttura ad albero per il tipo di controllo HeaderItem
- tipi di controllo, pattern di controllo per il tipo di controllo HeaderItem
- tipi di controllo, supporto per HeaderItem
- tipi di controllo, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298153"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="7e16f-119">Tipo di controllo HeaderItem</span><span class="sxs-lookup"><span data-stu-id="7e16f-119">HeaderItem Control Type</span></span>

<span data-ttu-id="7e16f-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="7e16f-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="7e16f-121">Il tipo di controllo **HeaderItem** fornisce un'etichetta visiva per una riga o una colonna di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7e16f-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="7e16f-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="7e16f-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="7e16f-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento intestazione in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="7e16f-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="7e16f-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7e16f-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7e16f-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="7e16f-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="7e16f-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="7e16f-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="7e16f-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="7e16f-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="7e16f-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="7e16f-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="7e16f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e16f-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="7e16f-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="7e16f-130">Typical Tree Structure</span></span>

<span data-ttu-id="7e16f-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa ai controlli elemento intestazione e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7e16f-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="7e16f-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7e16f-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e16f-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="7e16f-133">Control View</span></span></th>
<th><span data-ttu-id="7e16f-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="7e16f-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7e16f-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="7e16f-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="7e16f-136">(Non applicabile)</span><span class="sxs-lookup"><span data-stu-id="7e16f-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="7e16f-137">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="7e16f-137">Relevant Properties</span></span>

<span data-ttu-id="7e16f-138">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="7e16f-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="7e16f-139">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="7e16f-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="7e16f-140">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7e16f-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="7e16f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7e16f-141">Value</span></span>          | <span data-ttu-id="7e16f-142">Note</span><span class="sxs-lookup"><span data-stu-id="7e16f-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e16f-143">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="7e16f-144">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-144">See notes.</span></span>     | <span data-ttu-id="7e16f-145">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e16f-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="7e16f-146">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="7e16f-147">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-147">See notes.</span></span>     | <span data-ttu-id="7e16f-148">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="7e16f-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="7e16f-149">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="7e16f-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-150">See notes.</span></span>     | <span data-ttu-id="7e16f-151">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="7e16f-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="7e16f-152">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="7e16f-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="7e16f-153">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="7e16f-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="7e16f-154">**HeaderItem**</span></span> | <span data-ttu-id="7e16f-155">Questo valore è uguale per tutti i framework dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e16f-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="7e16f-156">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7e16f-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="7e16f-157">FALSE</span></span>          | <span data-ttu-id="7e16f-158">Il controllo elemento intestazione non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e16f-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="7e16f-159">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7e16f-160">true</span><span class="sxs-lookup"><span data-stu-id="7e16f-160">TRUE</span></span>           | <span data-ttu-id="7e16f-161">Il controllo elemento intestazione viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7e16f-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="7e16f-162">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="7e16f-163">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-163">See notes.</span></span>     | <span data-ttu-id="7e16f-164">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e16f-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="7e16f-165">**\_ITEMSTATUSPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="7e16f-166">Vedere le note</span><span class="sxs-lookup"><span data-stu-id="7e16f-166">See notes</span></span>      | <span data-ttu-id="7e16f-167">Questa proprietà fornisce informazioni per i tipi di ordinamento per l'elemento dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="7e16f-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="7e16f-168">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="7e16f-169">NULL</span><span class="sxs-lookup"><span data-stu-id="7e16f-169">NULL</span></span>           | <span data-ttu-id="7e16f-170">I controlli elemento intestazione non hanno un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="7e16f-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="7e16f-171">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="7e16f-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-172">See notes.</span></span>     | <span data-ttu-id="7e16f-173">Stringa localizzata corrispondente al tipo di controllo **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="7e16f-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="7e16f-174">Il valore predefinito è "elemento intestazione" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="7e16f-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="7e16f-175">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="7e16f-176">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7e16f-176">See notes.</span></span>     | <span data-ttu-id="7e16f-177">Il controllo elemento intestazione è sempre associato a un'etichetta automatica.</span><span class="sxs-lookup"><span data-stu-id="7e16f-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="7e16f-178">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="7e16f-178">Required Control Patterns</span></span>

<span data-ttu-id="7e16f-179">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento intestazione.</span><span class="sxs-lookup"><span data-stu-id="7e16f-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="7e16f-180">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7e16f-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="7e16f-181">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="7e16f-181">Control Pattern</span></span>                                         | <span data-ttu-id="7e16f-182">Supporto</span><span class="sxs-lookup"><span data-stu-id="7e16f-182">Support</span></span> | <span data-ttu-id="7e16f-183">Note</span><span class="sxs-lookup"><span data-stu-id="7e16f-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e16f-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="7e16f-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="7e16f-185">Dipende da</span><span class="sxs-lookup"><span data-stu-id="7e16f-185">Depends</span></span> | <span data-ttu-id="7e16f-186">Implementare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) se è possibile fare clic sul controllo elemento intestazione per ordinare i dati.</span><span class="sxs-lookup"><span data-stu-id="7e16f-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="7e16f-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="7e16f-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="7e16f-188">Dipende da</span><span class="sxs-lookup"><span data-stu-id="7e16f-188">Depends</span></span> | <span data-ttu-id="7e16f-189">Implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) se il controllo elemento intestazione può essere ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="7e16f-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="7e16f-190">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="7e16f-190">Required Events</span></span>

<span data-ttu-id="7e16f-191">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli elemento intestazione.</span><span class="sxs-lookup"><span data-stu-id="7e16f-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="7e16f-192">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7e16f-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="7e16f-193">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7e16f-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="7e16f-194">Note</span><span class="sxs-lookup"><span data-stu-id="7e16f-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e16f-195">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="7e16f-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7e16f-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="7e16f-197">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="7e16f-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="7e16f-198">Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="7e16f-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="7e16f-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7e16f-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="7e16f-200">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="7e16f-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="7e16f-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7e16f-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="7e16f-202">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="7e16f-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="7e16f-203">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="7e16f-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="7e16f-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e16f-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7e16f-205">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7e16f-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e16f-206">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7e16f-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="7e16f-207">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7e16f-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




