---
title: Tipo di controllo StatusBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo StatusBar
- Automazione interfaccia utente, tipo di controllo StatusBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo StatusBar
- Automazione interfaccia utente, proprietà per il tipo di controllo StatusBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo StatusBar
- Automazione interfaccia utente, eventi per il tipo di controllo StatusBar
- strutture ad albero, tipo di controllo StatusBar
- Proprietà, tipo di controllo StatusBar
- pattern di controllo, tipo di controllo StatusBar
- eventi, tipo di controllo StatusBar
- supporto per il tipo di controllo StatusBar
- StatusBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo StatusBar
- tipi di controllo, pattern di controllo per il tipo di controllo StatusBar
- tipi di controllo, supporto per StatusBar
- tipi di controllo, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331103"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="a3738-119">Tipo di controllo StatusBar</span><span class="sxs-lookup"><span data-stu-id="a3738-119">StatusBar Control Type</span></span>

<span data-ttu-id="a3738-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="a3738-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="a3738-121">In un controllo barra di stato sono in genere presenti informazioni su un oggetto visualizzato in una finestra di un'applicazione, i componenti dell'oggetto o informazioni contestuali collegate alle operazioni di tale oggetto all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3738-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="a3738-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="a3738-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="a3738-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra di stato in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="a3738-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a3738-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3738-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a3738-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="a3738-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a3738-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="a3738-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a3738-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="a3738-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a3738-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="a3738-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a3738-129">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="a3738-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="a3738-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3738-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a3738-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="a3738-131">Typical Tree Structure</span></span>

<span data-ttu-id="a3738-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra di stato e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a3738-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a3738-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3738-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3738-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="a3738-134">Control View</span></span></th>
<th><span data-ttu-id="a3738-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="a3738-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a3738-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="a3738-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="a3738-137">Edit (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="a3738-138">ProgressBar (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="a3738-139">Image (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="a3738-140">Button (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a3738-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="a3738-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="a3738-142">Edit (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="a3738-143">ProgressBar (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="a3738-144">Image (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="a3738-145">Button (0 o più)</span><span class="sxs-lookup"><span data-stu-id="a3738-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="a3738-146">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="a3738-146">Relevant Properties</span></span>

<span data-ttu-id="a3738-147">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli barra di stato.</span><span class="sxs-lookup"><span data-stu-id="a3738-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="a3738-148">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a3738-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a3738-149">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a3738-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a3738-150">Valore</span><span class="sxs-lookup"><span data-stu-id="a3738-150">Value</span></span>         | <span data-ttu-id="a3738-151">Note</span><span class="sxs-lookup"><span data-stu-id="a3738-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3738-152">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="a3738-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="a3738-153">See notes.</span></span>    | <span data-ttu-id="a3738-154">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a3738-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="a3738-155">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a3738-156">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="a3738-156">See notes.</span></span>    | <span data-ttu-id="a3738-157">Il rettangolo di delimitazione di una barra di stato deve includere tutti i controlli in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="a3738-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="a3738-158">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a3738-159">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="a3738-159">See notes.</span></span>    | <span data-ttu-id="a3738-160">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="a3738-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="a3738-161">Se sono presenti aree all'interno del rettangolo di delimitazione che non sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override di questo e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="a3738-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="a3738-162">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a3738-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="a3738-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="a3738-164">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a3738-165">true</span><span class="sxs-lookup"><span data-stu-id="a3738-165">TRUE</span></span>          | <span data-ttu-id="a3738-166">Il controllo barra di stato viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a3738-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="a3738-167">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a3738-168">true</span><span class="sxs-lookup"><span data-stu-id="a3738-168">TRUE</span></span>          | <span data-ttu-id="a3738-169">Il controllo barra di stato viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a3738-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="a3738-170">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a3738-171">Dipende da</span><span class="sxs-lookup"><span data-stu-id="a3738-171">Depends</span></span>       | <span data-ttu-id="a3738-172">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3738-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="a3738-173">**\_ISOFFSCREENPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a3738-174">Dipende da</span><span class="sxs-lookup"><span data-stu-id="a3738-174">Depends</span></span>       | <span data-ttu-id="a3738-175">Se un controllo barra di stato non è attualmente visibile, restituirà TRUE per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3738-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="a3738-176">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a3738-177">NULL</span><span class="sxs-lookup"><span data-stu-id="a3738-177">NULL</span></span>          | <span data-ttu-id="a3738-178">Il controllo barra di stato in genere non dispone di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="a3738-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="a3738-179">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a3738-180">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="a3738-180">See notes.</span></span>    | <span data-ttu-id="a3738-181">Stringa localizzata corrispondente al tipo di controllo **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="a3738-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="a3738-182">Il valore predefinito è "barra di stato" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="a3738-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="a3738-183">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a3738-184">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="a3738-184">See notes.</span></span>    | <span data-ttu-id="a3738-185">Il controllo barra di stato non necessita di un nome a meno che non vengano usati più controlli all'interno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3738-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="a3738-186">In questo caso, distinguere ogni barra con nomi quali "stato Internet" o "stato applicazione".</span><span class="sxs-lookup"><span data-stu-id="a3738-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="a3738-187">**\_ORIENTATIONPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a3738-188">Dipende da</span><span class="sxs-lookup"><span data-stu-id="a3738-188">Depends</span></span>       | <span data-ttu-id="a3738-189">Valore che indica l'orientamento del controllo: orizzontale o verticale.</span><span class="sxs-lookup"><span data-stu-id="a3738-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a3738-190">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="a3738-190">Required Control Patterns</span></span>

<span data-ttu-id="a3738-191">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per i controlli barra di stato.</span><span class="sxs-lookup"><span data-stu-id="a3738-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="a3738-192">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3738-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a3738-193">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="a3738-193">Control Pattern</span></span>                               | <span data-ttu-id="a3738-194">Supporto</span><span class="sxs-lookup"><span data-stu-id="a3738-194">Support</span></span>  | <span data-ttu-id="a3738-195">Note</span><span class="sxs-lookup"><span data-stu-id="a3738-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3738-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="a3738-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="a3738-197">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a3738-197">Optional</span></span> | <span data-ttu-id="a3738-198">I controlli barra di stato devono supportare il pattern di controllo [Grid](uiauto-implementinggrid.md) in modo che sia possibile monitorare e fare facilmente riferimento alle singole parti per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="a3738-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="a3738-199">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="a3738-199">Required Events</span></span>

<span data-ttu-id="a3738-200">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli barra di stato.</span><span class="sxs-lookup"><span data-stu-id="a3738-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="a3738-201">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3738-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a3738-202">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a3738-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="a3738-203">Note</span><span class="sxs-lookup"><span data-stu-id="a3738-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a3738-204">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="a3738-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3738-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="a3738-206">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3738-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="a3738-207">Se il controllo supporta la proprietà **IsEnabled** , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="a3738-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="a3738-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3738-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="a3738-209">Se il controllo supporta la proprietà **IsOffscreen** , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="a3738-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="a3738-210">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="a3738-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a3738-211">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3738-211">Remarks</span></span>

<span data-ttu-id="a3738-212">Si consiglia di usare i controlli di modifica come elementi della griglia figlio in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="a3738-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="a3738-213">Utilizzando i controlli di modifica è più semplice associare lo scopo del campo stato al relativo valore utilizzando il nome dell'elemento e la proprietà del valore.</span><span class="sxs-lookup"><span data-stu-id="a3738-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="a3738-214">Poiché i controlli testo non devono supportare il pattern di controllo **value** , non devono essere usati come elementi Grid figlio.</span><span class="sxs-lookup"><span data-stu-id="a3738-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3738-215">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3738-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3738-216">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a3738-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3738-217">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a3738-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a3738-218">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a3738-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




