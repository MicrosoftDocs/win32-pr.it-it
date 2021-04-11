---
title: Tipo di controllo gruppo
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Group
- Automazione interfaccia utente, tipo di controllo gruppo
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Group
- Automazione interfaccia utente, proprietà per il tipo di controllo Group
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Group
- Automazione interfaccia utente, eventi per il tipo di controllo Group
- strutture ad albero, tipo di controllo Group
- Proprietà, tipo di controllo gruppo
- pattern di controllo, tipo di controllo Group
- eventi, tipo di controllo gruppo
- supporto per il tipo di controllo Group
- Group (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Group
- tipi di controllo, pattern di controllo per il tipo di controllo Group
- tipi di controllo, supporto per il gruppo
- tipi di controllo, gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395858"
---
# <a name="group-control-type"></a><span data-ttu-id="c9738-119">Tipo di controllo gruppo</span><span class="sxs-lookup"><span data-stu-id="c9738-119">Group Control Type</span></span>

<span data-ttu-id="c9738-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Group** .</span><span class="sxs-lookup"><span data-stu-id="c9738-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="c9738-121">Un controllo gruppo rappresenta un nodo all'interno di una gerarchia.</span><span class="sxs-lookup"><span data-stu-id="c9738-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="c9738-122">Il tipo di controllo **Group** crea una separazione nell'albero di automazione interfaccia utente in modo che gli elementi raggruppati abbiano una divisione logica all'interno dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c9738-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="c9738-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Group** .</span><span class="sxs-lookup"><span data-stu-id="c9738-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="c9738-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli gruppo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="c9738-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c9738-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9738-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9738-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="c9738-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c9738-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="c9738-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c9738-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="c9738-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c9738-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="c9738-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c9738-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9738-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c9738-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="c9738-131">Typical Tree Structure</span></span>

<span data-ttu-id="c9738-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli gruppo e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9738-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c9738-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9738-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9738-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="c9738-134">Control View</span></span></th>
<th><span data-ttu-id="c9738-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="c9738-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c9738-136">Group</span><span class="sxs-lookup"><span data-stu-id="c9738-136">Group</span></span>
<ul>
<li><span data-ttu-id="c9738-137">0 o molti controlli</span><span class="sxs-lookup"><span data-stu-id="c9738-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9738-138">Group</span><span class="sxs-lookup"><span data-stu-id="c9738-138">Group</span></span>
<ul>
<li><span data-ttu-id="c9738-139">0 o molti controlli</span><span class="sxs-lookup"><span data-stu-id="c9738-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c9738-140">I controlli gruppo includono in genere il supporto di automazione interfaccia utente per i tipi di controllo trovati sotto di essi nel sottoalbero, inclusi i tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9738-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="c9738-141">Poiché un controllo gruppo è un contenitore generico, è possibile che qualsiasi tipo di controllo si trovi sotto il controllo gruppo nell'albero.</span><span class="sxs-lookup"><span data-stu-id="c9738-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="c9738-142">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="c9738-142">Relevant Properties</span></span>

<span data-ttu-id="c9738-143">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli gruppo.</span><span class="sxs-lookup"><span data-stu-id="c9738-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="c9738-144">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c9738-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c9738-145">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9738-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c9738-146">Valore</span><span class="sxs-lookup"><span data-stu-id="c9738-146">Value</span></span>      | <span data-ttu-id="c9738-147">Note</span><span class="sxs-lookup"><span data-stu-id="c9738-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9738-148">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c9738-149">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-149">See notes.</span></span> | <span data-ttu-id="c9738-150">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c9738-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="c9738-151">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c9738-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-152">See notes.</span></span> | <span data-ttu-id="c9738-153">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="c9738-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="c9738-154">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c9738-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-155">See notes.</span></span> | <span data-ttu-id="c9738-156">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="c9738-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="c9738-157">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="c9738-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="c9738-158">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c9738-159">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="c9738-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="c9738-160">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c9738-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c9738-161">**TRUE**</span></span>   | <span data-ttu-id="c9738-162">Il controllo gruppo viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c9738-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="c9738-163">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c9738-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c9738-164">**TRUE**</span></span>   | <span data-ttu-id="c9738-165">Il controllo gruppo viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c9738-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="c9738-166">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c9738-167">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-167">See notes.</span></span> | <span data-ttu-id="c9738-168">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9738-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="c9738-169">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c9738-170">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-170">See notes.</span></span> | <span data-ttu-id="c9738-171">I controlli gruppo sono in genere associati a un'etichetta automatica.</span><span class="sxs-lookup"><span data-stu-id="c9738-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="c9738-172">In questi casi, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="c9738-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="c9738-173">Se il gruppo ha un'etichetta di testo statico, restituire l'etichetta come valore della proprietà **LabeledBy** .</span><span class="sxs-lookup"><span data-stu-id="c9738-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="c9738-174">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c9738-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-175">See notes.</span></span> | <span data-ttu-id="c9738-176">Stringa localizzata corrispondente al tipo di controllo **Group** .</span><span class="sxs-lookup"><span data-stu-id="c9738-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="c9738-177">Il valore predefinito è "Group" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="c9738-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="c9738-178">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c9738-179">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c9738-179">See notes.</span></span> | <span data-ttu-id="c9738-180">Il controllo gruppo in genere ricava il proprio nome dal testo dell'etichetta applicata al controllo.</span><span class="sxs-lookup"><span data-stu-id="c9738-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c9738-181">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="c9738-181">Required Control Patterns</span></span>

<span data-ttu-id="c9738-182">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per il tipo di controllo **gruppo** .</span><span class="sxs-lookup"><span data-stu-id="c9738-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="c9738-183">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9738-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c9738-184">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="c9738-184">Control Pattern</span></span>                                                   | <span data-ttu-id="c9738-185">Supporto</span><span class="sxs-lookup"><span data-stu-id="c9738-185">Support</span></span> | <span data-ttu-id="c9738-186">Note</span><span class="sxs-lookup"><span data-stu-id="c9738-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9738-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="c9738-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="c9738-188">Dipende da</span><span class="sxs-lookup"><span data-stu-id="c9738-188">Depends</span></span> | <span data-ttu-id="c9738-189">I controlli gruppo che possono essere usati per mostrare o nascondere le informazioni devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="c9738-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="c9738-190">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="c9738-190">Required Events</span></span>

<span data-ttu-id="c9738-191">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c9738-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="c9738-192">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9738-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c9738-193">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9738-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="c9738-194">Note</span><span class="sxs-lookup"><span data-stu-id="c9738-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9738-195">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="c9738-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9738-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="c9738-197">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9738-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="c9738-198">Se il controllo supporta il pattern di controllo pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c9738-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="c9738-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9738-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="c9738-200">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c9738-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="c9738-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9738-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="c9738-202">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c9738-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="c9738-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9738-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="c9738-204">Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c9738-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="c9738-205">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="c9738-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="c9738-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9738-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c9738-207">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c9738-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9738-208">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9738-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c9738-209">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c9738-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




