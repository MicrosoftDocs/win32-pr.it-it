---
title: Tipo di controllo Spinner
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Spinner
- Automazione interfaccia utente, tipo di controllo Spinner
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Spinner
- Automazione interfaccia utente, proprietà per il tipo di controllo Spinner
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Spinner
- Automazione interfaccia utente, eventi per il tipo di controllo Spinner
- strutture ad albero, tipo di controllo Spinner
- Proprietà, tipo di controllo Spinner
- pattern di controllo, tipo di controllo Spinner
- eventi, tipo di controllo Spinner
- supporto per il tipo di controllo Spinner
- Spinner (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Spinner
- tipi di controllo, pattern di controllo per il tipo di controllo Spinner
- tipi di controllo, supporto per Spinner
- tipi di controllo, casella di selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712700"
---
# <a name="spinner-control-type"></a><span data-ttu-id="1dc26-119">Tipo di controllo Spinner</span><span class="sxs-lookup"><span data-stu-id="1dc26-119">Spinner Control Type</span></span>

<span data-ttu-id="1dc26-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="1dc26-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="1dc26-121">I controlli casella di selezione vengono usati per effettuare selezioni da un dominio di elementi o un intervallo di numeri.</span><span class="sxs-lookup"><span data-stu-id="1dc26-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="1dc26-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="1dc26-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="1dc26-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli casella di selezione in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e</span><span class="sxs-lookup"><span data-stu-id="1dc26-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="1dc26-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1dc26-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1dc26-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="1dc26-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="1dc26-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="1dc26-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="1dc26-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="1dc26-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="1dc26-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="1dc26-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="1dc26-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc26-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="1dc26-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="1dc26-130">Typical Tree Structure</span></span>

<span data-ttu-id="1dc26-131">La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli casella di selezione quando supportano i pattern di controllo **RangeValue** e **Selection** e descrive il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="1dc26-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1dc26-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="1dc26-133">**Pattern di controllo RangeValue**</span><span class="sxs-lookup"><span data-stu-id="1dc26-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1dc26-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="1dc26-134">Control View</span></span></th>
<th><span data-ttu-id="1dc26-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="1dc26-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1dc26-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="1dc26-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="1dc26-137">Edit (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="1dc26-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="1dc26-138">Button (2)</span><span class="sxs-lookup"><span data-stu-id="1dc26-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1dc26-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="1dc26-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1dc26-140">**Selection (pattern di controllo)**</span><span class="sxs-lookup"><span data-stu-id="1dc26-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1dc26-141">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="1dc26-141">Control View</span></span></th>
<th><span data-ttu-id="1dc26-142">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="1dc26-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1dc26-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="1dc26-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="1dc26-144">Edit (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="1dc26-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="1dc26-145">Button (2)</span><span class="sxs-lookup"><span data-stu-id="1dc26-145">Button (2)</span></span></li>
<li><span data-ttu-id="1dc26-146">Elemento elenco (0 o più)</span><span class="sxs-lookup"><span data-stu-id="1dc26-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1dc26-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="1dc26-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="1dc26-148">ListItem (0 o più)</span><span class="sxs-lookup"><span data-stu-id="1dc26-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1dc26-149">Per assicurarsi che i due pulsanti nel sottoalbero della visualizzazione controlli possano essere distinti dagli strumenti di test automatici, assegnare il valore **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) alla proprietà **AutomationId** nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="1dc26-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="1dc26-150">Per alcune implementazioni il controllo di modifica associato può essere un peer del controllo casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="1dc26-151">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="1dc26-151">Relevant Properties</span></span>

<span data-ttu-id="1dc26-152">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="1dc26-153">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="1dc26-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="1dc26-154">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1dc26-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="1dc26-155">Valore</span><span class="sxs-lookup"><span data-stu-id="1dc26-155">Value</span></span>       | <span data-ttu-id="1dc26-156">Note</span><span class="sxs-lookup"><span data-stu-id="1dc26-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dc26-157">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="1dc26-158">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-158">See notes.</span></span>  | <span data-ttu-id="1dc26-159">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1dc26-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="1dc26-160">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="1dc26-161">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-161">See notes.</span></span>  | <span data-ttu-id="1dc26-162">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="1dc26-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="1dc26-163">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="1dc26-164">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-164">See notes.</span></span>  | <span data-ttu-id="1dc26-165">Il punto selezionabile del controllo casella di selezione fornisce lo stato attivo alla parte modificabile del controllo.</span><span class="sxs-lookup"><span data-stu-id="1dc26-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="1dc26-166">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="1dc26-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="1dc26-167">**Spinner**</span></span> | <span data-ttu-id="1dc26-168">Questo valore è uguale per tutti i framework.</span><span class="sxs-lookup"><span data-stu-id="1dc26-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="1dc26-169">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="1dc26-170">true</span><span class="sxs-lookup"><span data-stu-id="1dc26-170">TRUE</span></span>        | <span data-ttu-id="1dc26-171">Il controllo casella di selezione deve essere sempre di tipo contenuto.</span><span class="sxs-lookup"><span data-stu-id="1dc26-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="1dc26-172">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="1dc26-173">true</span><span class="sxs-lookup"><span data-stu-id="1dc26-173">TRUE</span></span>        | <span data-ttu-id="1dc26-174">Il controllo casella di selezione deve essere sempre un controllo.</span><span class="sxs-lookup"><span data-stu-id="1dc26-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1dc26-175">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="1dc26-176">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-176">See notes.</span></span>  | <span data-ttu-id="1dc26-177">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="1dc26-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="1dc26-178">Un controllo casella di selezione assume raramente lo stato attivo, ma, in questo caso, lo stato attivo deve rimanere sul controllo casella di selezione, non sui pulsanti figlio.</span><span class="sxs-lookup"><span data-stu-id="1dc26-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="1dc26-179">L'utente deve essere in grado di eseguire tutte le azioni di scorrimento usando i tasti freccia su e freccia giù.</span><span class="sxs-lookup"><span data-stu-id="1dc26-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="1dc26-180">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="1dc26-181">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-181">See notes.</span></span>  | <span data-ttu-id="1dc26-182">I controlli casella di selezione hanno un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="1dc26-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="1dc26-183">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="1dc26-184">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-184">See notes.</span></span>  | <span data-ttu-id="1dc26-185">Stringa localizzata corrispondente al tipo di controllo **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="1dc26-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="1dc26-186">Il valore predefinito è "Spinner" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="1dc26-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="1dc26-187">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="1dc26-188">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="1dc26-188">See notes.</span></span>  | <span data-ttu-id="1dc26-189">Il controllo casella di selezione in genere ricava il proprio nome da un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="1dc26-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="1dc26-190">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="1dc26-190">Required Control Patterns</span></span>

<span data-ttu-id="1dc26-191">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="1dc26-192">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1dc26-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="1dc26-193">Pattern di controllo/proprietà del pattern</span><span class="sxs-lookup"><span data-stu-id="1dc26-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="1dc26-194">Supporto/valore</span><span class="sxs-lookup"><span data-stu-id="1dc26-194">Support/Value</span></span> | <span data-ttu-id="1dc26-195">Note</span><span class="sxs-lookup"><span data-stu-id="1dc26-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dc26-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="1dc26-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="1dc26-197">Dipende da</span><span class="sxs-lookup"><span data-stu-id="1dc26-197">Depends</span></span>       | <span data-ttu-id="1dc26-198">I controlli casella di selezione che si estendono su un intervallo numerico possono supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc26-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="1dc26-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="1dc26-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="1dc26-200">Dipende da</span><span class="sxs-lookup"><span data-stu-id="1dc26-200">Depends</span></span>       | <span data-ttu-id="1dc26-201">I controlli casella di selezione che dispongono di un elenco di elementi da selezionare devono supportare il pattern di controllo [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc26-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="1dc26-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="1dc26-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="1dc26-203">FALSE</span><span class="sxs-lookup"><span data-stu-id="1dc26-203">FALSE</span></span>         | <span data-ttu-id="1dc26-204">I controlli casella di selezione sono sempre contenitori a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="1dc26-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="1dc26-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="1dc26-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="1dc26-206">Dipende da</span><span class="sxs-lookup"><span data-stu-id="1dc26-206">Depends</span></span>       | <span data-ttu-id="1dc26-207">I controlli casella di selezione che si estendono su un set descrete di opzioni o numeri possono supportare il pattern di controllo [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc26-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="1dc26-208">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="1dc26-208">Required Events</span></span>

<span data-ttu-id="1dc26-209">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="1dc26-210">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="1dc26-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="1dc26-211">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1dc26-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="1dc26-212">Note</span><span class="sxs-lookup"><span data-stu-id="1dc26-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dc26-213">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="1dc26-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1dc26-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="1dc26-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="1dc26-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="1dc26-216">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1dc26-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="1dc26-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="1dc26-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="1dc26-218">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1dc26-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="1dc26-219">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1dc26-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="1dc26-220">Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1dc26-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="1dc26-221">[**UIA \_ Evento \_**](uiauto-event-ids.md) di modifica della proprietà InvalidatedEventId di selezione.</span><span class="sxs-lookup"><span data-stu-id="1dc26-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="1dc26-222">Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1dc26-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="1dc26-223">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="1dc26-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="1dc26-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="1dc26-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="1dc26-225">Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="1dc26-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="1dc26-226">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc26-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1dc26-227">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1dc26-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1dc26-228">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1dc26-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="1dc26-229">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1dc26-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




