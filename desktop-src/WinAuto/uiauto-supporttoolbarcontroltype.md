---
title: Tipo di controllo ToolBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ToolBar. I controlli della barra degli strumenti consentono agli utenti finali di attivare i comandi e gli strumenti contenuti in un'applicazione.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ToolBar
- Automazione interfaccia utente, tipo di controllo ToolBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ToolBar
- Automazione interfaccia utente, proprietà per il tipo di controllo ToolBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ToolBar
- Automazione interfaccia utente, eventi per il tipo di controllo ToolBar
- strutture ad albero, tipo di controllo ToolBar
- Proprietà, tipo di controllo ToolBar
- pattern di controllo, tipo di controllo ToolBar
- eventi, tipo di controllo ToolBar
- supporto per il tipo di controllo ToolBar
- ToolBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ToolBar
- tipi di controllo, pattern di controllo per il tipo di controllo ToolBar
- tipi di controllo, supporto per la barra degli strumenti
- tipi di controllo, barra degli strumenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396742"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="9593e-120">Tipo di controllo ToolBar</span><span class="sxs-lookup"><span data-stu-id="9593e-120">ToolBar Control Type</span></span>

<span data-ttu-id="9593e-121">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="9593e-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="9593e-122">I controlli della barra degli strumenti consentono agli utenti finali di attivare i comandi e gli strumenti contenuti in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9593e-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="9593e-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="9593e-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="9593e-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli della barra degli strumenti in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo</span><span class="sxs-lookup"><span data-stu-id="9593e-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9593e-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9593e-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9593e-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="9593e-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9593e-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="9593e-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9593e-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="9593e-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9593e-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="9593e-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9593e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9593e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9593e-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="9593e-131">Typical Tree Structure</span></span>

<span data-ttu-id="9593e-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli della barra degli strumenti e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9593e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9593e-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9593e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9593e-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="9593e-134">Control View</span></span></th>
<th><span data-ttu-id="9593e-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="9593e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9593e-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="9593e-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="9593e-137">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="9593e-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9593e-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="9593e-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="9593e-139">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="9593e-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9593e-140">Un controllo barra degli strumenti può contenere qualsiasi tipo di controllo all'interno del relativo sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="9593e-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="9593e-141">In genere contengono pulsanti, caselle combinate e pulsanti di menu combinato.</span><span class="sxs-lookup"><span data-stu-id="9593e-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9593e-142">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="9593e-142">Relevant Properties</span></span>

<span data-ttu-id="9593e-143">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="9593e-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="9593e-144">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9593e-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9593e-145">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9593e-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9593e-146">Valore</span><span class="sxs-lookup"><span data-stu-id="9593e-146">Value</span></span>       | <span data-ttu-id="9593e-147">Note</span><span class="sxs-lookup"><span data-stu-id="9593e-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9593e-148">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9593e-149">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9593e-149">See notes.</span></span>  | <span data-ttu-id="9593e-150">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9593e-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="9593e-151">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9593e-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9593e-152">See notes.</span></span>  | <span data-ttu-id="9593e-153">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="9593e-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="9593e-154">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9593e-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9593e-155">See notes.</span></span>  | <span data-ttu-id="9593e-156">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="9593e-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9593e-157">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="9593e-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="9593e-158">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9593e-159">**Barra degli strumenti**</span><span class="sxs-lookup"><span data-stu-id="9593e-159">**ToolBar**</span></span> | <span data-ttu-id="9593e-160">Questo valore è uguale per tutti i framework dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9593e-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="9593e-161">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9593e-162">true</span><span class="sxs-lookup"><span data-stu-id="9593e-162">TRUE</span></span>        | <span data-ttu-id="9593e-163">Il controllo Toolbar viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9593e-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="9593e-164">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9593e-165">true</span><span class="sxs-lookup"><span data-stu-id="9593e-165">TRUE</span></span>        | <span data-ttu-id="9593e-166">Il controllo Toolbar viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9593e-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="9593e-167">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9593e-168">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9593e-168">See notes.</span></span>  | <span data-ttu-id="9593e-169">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9593e-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="9593e-170">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9593e-171">NULL</span><span class="sxs-lookup"><span data-stu-id="9593e-171">NULL</span></span>        | <span data-ttu-id="9593e-172">Un controllo Toolbar non dispone mai di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="9593e-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="9593e-173">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9593e-174">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9593e-174">See notes.</span></span>  | <span data-ttu-id="9593e-175">Stringa localizzata corrispondente al tipo di controllo **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="9593e-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="9593e-176">Il valore predefinito è "barra degli strumenti" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="9593e-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="9593e-177">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9593e-178">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9593e-178">Depends</span></span>     | <span data-ttu-id="9593e-179">Il controllo Toolbar non necessita di un nome a meno che non venga usato più di un oggetto all'interno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9593e-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="9593e-180">Se sono presenti più di uno, ognuno deve avere un nome distinto (ad esempio, "Formatting" o "delining").</span><span class="sxs-lookup"><span data-stu-id="9593e-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9593e-181">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="9593e-181">Required Control Patterns</span></span>

<span data-ttu-id="9593e-182">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="9593e-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="9593e-183">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9593e-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9593e-184">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="9593e-184">Control Pattern</span></span>                                                   | <span data-ttu-id="9593e-185">Supporto</span><span class="sxs-lookup"><span data-stu-id="9593e-185">Support</span></span> | <span data-ttu-id="9593e-186">Note</span><span class="sxs-lookup"><span data-stu-id="9593e-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9593e-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="9593e-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="9593e-188">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9593e-188">Depends</span></span> | <span data-ttu-id="9593e-189">Se la barra degli strumenti può essere ancorata a parti diverse dello schermo, deve supportare il pattern di controllo [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="9593e-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="9593e-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9593e-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9593e-191">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9593e-191">Depends</span></span> | <span data-ttu-id="9593e-192">Se la barra degli strumenti può essere espansa e compressa per visualizzare più elementi, deve supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="9593e-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="9593e-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="9593e-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="9593e-194">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9593e-194">Depends</span></span> | <span data-ttu-id="9593e-195">Se la barra degli strumenti può essere ridimensionata, ruotata o spostata, deve supportare il pattern di controllo [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="9593e-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="9593e-196">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="9593e-196">Required Events</span></span>

<span data-ttu-id="9593e-197">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="9593e-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="9593e-198">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9593e-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9593e-199">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9593e-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="9593e-200">Note</span><span class="sxs-lookup"><span data-stu-id="9593e-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9593e-201">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="9593e-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9593e-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="9593e-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9593e-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="9593e-204">Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9593e-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="9593e-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9593e-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="9593e-206">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9593e-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="9593e-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9593e-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="9593e-208">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9593e-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="9593e-209">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="9593e-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9593e-210">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9593e-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9593e-211">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9593e-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9593e-212">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9593e-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9593e-213">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9593e-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




