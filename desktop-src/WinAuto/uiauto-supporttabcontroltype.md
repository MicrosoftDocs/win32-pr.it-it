---
title: Tipo di controllo Tab
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Tab
- Automazione interfaccia utente, tipo di controllo Tab
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Tab
- Automazione interfaccia utente, proprietà per il tipo di controllo Tab
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Tab
- Automazione interfaccia utente, eventi per il tipo di controllo Tab
- strutture ad albero, tipo di controllo Tab
- Proprietà, tipo di controllo Tab
- pattern di controllo, tipo di controllo Tab
- eventi, tipo di controllo Tab
- supporto per il tipo di controllo Tab
- Tab (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Tab
- tipi di controllo, pattern di controllo per il tipo di controllo Tab
- tipi di controllo, supporto per Tab
- tipi di controllo, scheda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955598"
---
# <a name="tab-control-type"></a><span data-ttu-id="b261e-119">Tipo di controllo Tab</span><span class="sxs-lookup"><span data-stu-id="b261e-119">Tab Control Type</span></span>

<span data-ttu-id="b261e-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Tab** .</span><span class="sxs-lookup"><span data-stu-id="b261e-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="b261e-121">Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio.</span><span class="sxs-lookup"><span data-stu-id="b261e-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="b261e-122">L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b261e-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="b261e-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Tab** .</span><span class="sxs-lookup"><span data-stu-id="b261e-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="b261e-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli struttura a schede in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e</span><span class="sxs-lookup"><span data-stu-id="b261e-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="b261e-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b261e-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b261e-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="b261e-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b261e-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="b261e-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b261e-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="b261e-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="b261e-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="b261e-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b261e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b261e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b261e-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="b261e-131">Typical Tree Structure</span></span>

<span data-ttu-id="b261e-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa ai controlli struttura a schede e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b261e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b261e-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b261e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b261e-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="b261e-134">Control View</span></span></th>
<th><span data-ttu-id="b261e-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="b261e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b261e-136">Scheda</span><span class="sxs-lookup"><span data-stu-id="b261e-136">Tab</span></span>
<ul>
<li><span data-ttu-id="b261e-137">TabItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b261e-138">ScrollBar (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="b261e-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="b261e-139">Button (0 o 2)</span><span class="sxs-lookup"><span data-stu-id="b261e-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b261e-140">Scheda</span><span class="sxs-lookup"><span data-stu-id="b261e-140">Tab</span></span>
<ul>
<li><span data-ttu-id="b261e-141">TabItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b261e-142">I controlli struttura a schede hanno elementi di automazione interfaccia utente figlio basati sul tipo di controllo [TabItem](uiauto-supporttabitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="b261e-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="b261e-143">Quando gli elementi della scheda sono raggruppati, ad esempio in Microsoft Office applicazioni, il tipo di controllo **Tab** **può ospitare anche** tipi di controllo per gli elementi di scheda raggruppati, come illustrato nella struttura ad albero seguente.</span><span class="sxs-lookup"><span data-stu-id="b261e-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b261e-144">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="b261e-144">Control View</span></span></th>
<th><span data-ttu-id="b261e-145">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="b261e-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b261e-146">Scheda</span><span class="sxs-lookup"><span data-stu-id="b261e-146">Tab</span></span>
<ul>
<li><span data-ttu-id="b261e-147">TabItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b261e-148">Group (0 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="b261e-149">TabItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="b261e-150">ScrollBar (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="b261e-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="b261e-151">Button (0 o 2)</span><span class="sxs-lookup"><span data-stu-id="b261e-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b261e-152">Scheda</span><span class="sxs-lookup"><span data-stu-id="b261e-152">Tab</span></span>
<ul>
<li><span data-ttu-id="b261e-153">TabItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b261e-154">Group (0 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="b261e-155">TabItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="b261e-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="b261e-156">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="b261e-156">Relevant Properties</span></span>

<span data-ttu-id="b261e-157">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b261e-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="b261e-158">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="b261e-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b261e-159">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b261e-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b261e-160">Valore</span><span class="sxs-lookup"><span data-stu-id="b261e-160">Value</span></span>      | <span data-ttu-id="b261e-161">Note</span><span class="sxs-lookup"><span data-stu-id="b261e-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b261e-162">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="b261e-163">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-163">See notes.</span></span> | <span data-ttu-id="b261e-164">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b261e-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b261e-165">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b261e-166">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-166">See notes.</span></span> | <span data-ttu-id="b261e-167">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="b261e-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="b261e-168">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="b261e-169">No</span><span class="sxs-lookup"><span data-stu-id="b261e-169">No</span></span>         | <span data-ttu-id="b261e-170">Il controllo struttura a schede non dispone di punti selezionabili.</span><span class="sxs-lookup"><span data-stu-id="b261e-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b261e-171">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b261e-172">**TAB**</span><span class="sxs-lookup"><span data-stu-id="b261e-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b261e-173">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b261e-174">true</span><span class="sxs-lookup"><span data-stu-id="b261e-174">TRUE</span></span>       | <span data-ttu-id="b261e-175">Il controllo struttura a schede viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b261e-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b261e-176">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b261e-177">true</span><span class="sxs-lookup"><span data-stu-id="b261e-177">TRUE</span></span>       | <span data-ttu-id="b261e-178">Il controllo struttura a schede viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b261e-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b261e-179">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b261e-180">true</span><span class="sxs-lookup"><span data-stu-id="b261e-180">TRUE</span></span>       | <span data-ttu-id="b261e-181">Il tipo di controllo Tab deve essere in grado di ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b261e-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="b261e-182">In genere, un client di automazione interfaccia utente chiama [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) su un controllo struttura a schede e uno dei relativi elementi inoltrerà lo stato attivo al controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b261e-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="b261e-183">È possibile che alcuni contenitori di schede assumano lo stato attivo senza che lo stato attivo venga impostato su uno dei relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="b261e-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="b261e-184">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b261e-185">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-185">See notes.</span></span> | <span data-ttu-id="b261e-186">I controlli Struttura a schede in genere includono un'etichetta di testo statico che viene esposta tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b261e-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="b261e-187">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b261e-188">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-188">See notes.</span></span> | <span data-ttu-id="b261e-189">Stringa localizzata corrispondente al tipo di controllo **Tab** .</span><span class="sxs-lookup"><span data-stu-id="b261e-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="b261e-190">Il valore predefinito è "tab" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="b261e-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b261e-191">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b261e-192">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-192">See notes.</span></span> | <span data-ttu-id="b261e-193">Il controllo struttura a schede raramente richiede una proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="b261e-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="b261e-194">**\_ORIENTATIONPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b261e-195">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="b261e-195">See notes.</span></span> | <span data-ttu-id="b261e-196">Il controllo Struttura a schede deve sempre indicare se è posizionato orizzontalmente o verticalmente.</span><span class="sxs-lookup"><span data-stu-id="b261e-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="b261e-197">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="b261e-197">Required Control Patterns</span></span>

<span data-ttu-id="b261e-198">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b261e-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="b261e-199">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b261e-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="b261e-200">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="b261e-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="b261e-201">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="b261e-201">Support/Value</span></span> | <span data-ttu-id="b261e-202">Note</span><span class="sxs-lookup"><span data-stu-id="b261e-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b261e-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="b261e-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="b261e-204">Necessario</span><span class="sxs-lookup"><span data-stu-id="b261e-204">Required</span></span>      | <span data-ttu-id="b261e-205">Tutti i controlli struttura a schede devono supportare il pattern di controllo [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="b261e-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="b261e-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="b261e-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="b261e-207">true</span><span class="sxs-lookup"><span data-stu-id="b261e-207">TRUE</span></span>          | <span data-ttu-id="b261e-208">I controlli Struttura a schede richiedono sempre una selezione.</span><span class="sxs-lookup"><span data-stu-id="b261e-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="b261e-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="b261e-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="b261e-210">FALSE</span><span class="sxs-lookup"><span data-stu-id="b261e-210">FALSE</span></span>         | <span data-ttu-id="b261e-211">I controlli Struttura a schede sono sempre contenitori a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="b261e-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="b261e-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="b261e-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="b261e-213">Dipende da</span><span class="sxs-lookup"><span data-stu-id="b261e-213">Depends</span></span>       | <span data-ttu-id="b261e-214">Il pattern di controllo [Scroll](uiauto-implementingscroll.md) deve essere supportato se il controllo struttura a schede include widget che consentono lo scorrimento di un set di elementi di schede.</span><span class="sxs-lookup"><span data-stu-id="b261e-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="b261e-215">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="b261e-215">Required Events</span></span>

<span data-ttu-id="b261e-216">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b261e-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="b261e-217">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b261e-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b261e-218">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b261e-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="b261e-219">Note</span><span class="sxs-lookup"><span data-stu-id="b261e-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b261e-220">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="b261e-221">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="b261e-222">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="b261e-223">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="b261e-224">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="b261e-225">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="b261e-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="b261e-227">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b261e-228">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="b261e-229">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b261e-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="b261e-231">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b261e-232">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="b261e-233">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b261e-234">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="b261e-235">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b261e-236">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b261e-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="b261e-237">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="b261e-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="b261e-238">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="b261e-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="b261e-239">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b261e-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b261e-240">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b261e-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b261e-241">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b261e-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b261e-242">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b261e-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




