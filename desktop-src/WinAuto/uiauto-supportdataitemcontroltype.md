---
title: Tipo di controllo DataItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo DataItem
- Automazione interfaccia utente, tipo di controllo DataItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo DataItem
- Automazione interfaccia utente, proprietà per il tipo di controllo DataItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo DataItem
- Automazione interfaccia utente, eventi per il tipo di controllo DataItem
- Automazione interfaccia utente, elenchi di grandi dimensioni e tipo di controllo DataItem
- strutture ad albero, tipo di controllo DataItem
- Proprietà, tipo di controllo DataItem
- pattern di controllo, tipo di controllo DataItem
- eventi, tipo di controllo DataItem
- elenchi di grandi dimensioni
- supporto per il tipo di controllo DataItem
- Tipo di controllo DataItem
- tipi di controllo, struttura ad albero per il tipo di controllo DataItem
- tipi di controllo, pattern di controllo per il tipo di controllo DataItem
- tipi di controllo, elenchi di grandi dimensioni e tipo di controllo DataItem
- tipi di controllo, supporto per DataItem
- tipi di controllo, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044609"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="056d2-122">Tipo di controllo DataItem</span><span class="sxs-lookup"><span data-stu-id="056d2-122">DataItem Control Type</span></span>

<span data-ttu-id="056d2-123">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="056d2-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="056d2-124">Una voce in un elenco Contatti, ad esempio, è un controllo elemento dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="056d2-125">Un controllo elemento dati contiene informazioni di interesse per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="056d2-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="056d2-126">È più complicato del semplice elemento elenco poiché contiene informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="056d2-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="056d2-127">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="056d2-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="056d2-128">I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento dati in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="056d2-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="056d2-129">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="056d2-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="056d2-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="056d2-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="056d2-131">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="056d2-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="056d2-132">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="056d2-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="056d2-133">Utilizzo di oggetti dataItems in elenchi di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="056d2-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="056d2-134">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="056d2-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="056d2-135">Esempio del tipo di controllo DataItem</span><span class="sxs-lookup"><span data-stu-id="056d2-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="056d2-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="056d2-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="056d2-137">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="056d2-137">Typical Tree Structure</span></span>

<span data-ttu-id="056d2-138">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli elemento dati e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="056d2-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="056d2-139">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="056d2-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="056d2-140">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="056d2-140">Control View</span></span></th>
<th><span data-ttu-id="056d2-141">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="056d2-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="056d2-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="056d2-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="056d2-143">Varia (0 o più, può essere strutturato in una gerarchia)</span><span class="sxs-lookup"><span data-stu-id="056d2-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="056d2-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="056d2-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="056d2-145">Varia (0 o più, può essere strutturato in una gerarchia)</span><span class="sxs-lookup"><span data-stu-id="056d2-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="056d2-146">Un elemento dati in una griglia di dati può contenere vari tipi di oggetti, incluso un altro livello di elementi dati o specifici elementi di griglia quali testo, immagini o controlli di modifica.</span><span class="sxs-lookup"><span data-stu-id="056d2-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="056d2-147">Se l'elemento dati dispone di un ruolo di oggetto specifico, l'elemento deve essere esposto come tipo di controllo specifico; ad esempio, un tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) per un elemento di dati selezionabile nella griglia.</span><span class="sxs-lookup"><span data-stu-id="056d2-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="056d2-148">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="056d2-148">Relevant Properties</span></span>

<span data-ttu-id="056d2-149">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo DataItem.</span><span class="sxs-lookup"><span data-stu-id="056d2-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="056d2-150">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="056d2-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="056d2-151">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="056d2-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="056d2-152">Valore</span><span class="sxs-lookup"><span data-stu-id="056d2-152">Value</span></span>        | <span data-ttu-id="056d2-153">Note</span><span class="sxs-lookup"><span data-stu-id="056d2-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="056d2-154">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="056d2-155">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-155">See notes.</span></span>   | <span data-ttu-id="056d2-156">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="056d2-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="056d2-157">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="056d2-158">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-158">See notes.</span></span>   | <span data-ttu-id="056d2-159">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="056d2-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="056d2-160">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="056d2-161">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-161">See notes.</span></span>   | <span data-ttu-id="056d2-162">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="056d2-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="056d2-163">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="056d2-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="056d2-164">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="056d2-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="056d2-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="056d2-166">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="056d2-167">true</span><span class="sxs-lookup"><span data-stu-id="056d2-167">TRUE</span></span>         | <span data-ttu-id="056d2-168">Il controllo elemento dati deve essere sempre un contenuto.</span><span class="sxs-lookup"><span data-stu-id="056d2-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="056d2-169">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="056d2-170">true</span><span class="sxs-lookup"><span data-stu-id="056d2-170">TRUE</span></span>         | <span data-ttu-id="056d2-171">Il controllo elemento dati deve essere sempre un controllo.</span><span class="sxs-lookup"><span data-stu-id="056d2-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="056d2-172">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="056d2-173">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-173">See notes.</span></span>   | <span data-ttu-id="056d2-174">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="056d2-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="056d2-175">**\_ITEMSTATUSPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="056d2-176">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-176">See notes.</span></span>   | <span data-ttu-id="056d2-177">Se il controllo contiene uno stato aggiornato dinamicamente, è necessario che questa proprietà sia supportata in modo che una tecnologia per l'accesso facilitato possa ricevere aggiornamenti quando lo stato dell'elemento cambia.</span><span class="sxs-lookup"><span data-stu-id="056d2-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="056d2-178">**\_ITEMTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="056d2-179">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-179">See notes.</span></span>   | <span data-ttu-id="056d2-180">Si tratta del valore della stringa che indica all'utente finale l'oggetto sottostante rappresentato dall'elemento,</span><span class="sxs-lookup"><span data-stu-id="056d2-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="056d2-181">Gli esempi includono "file multimediale" e "contatto".</span><span class="sxs-lookup"><span data-stu-id="056d2-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="056d2-182">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="056d2-183">Null</span><span class="sxs-lookup"><span data-stu-id="056d2-183">Null</span></span>         | <span data-ttu-id="056d2-184">I controlli elemento dati non hanno un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="056d2-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="056d2-185">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="056d2-186">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-186">See notes.</span></span>   | <span data-ttu-id="056d2-187">Stringa localizzata corrispondente al tipo di controllo **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="056d2-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="056d2-188">Il valore predefinito è "elemento dati" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="056d2-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="056d2-189">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="056d2-190">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="056d2-190">See notes.</span></span>   | <span data-ttu-id="056d2-191">Il controllo elemento dati contiene sempre un elemento di testo primario che l'utente riconosce come identificatore per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="056d2-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="056d2-192">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="056d2-192">Required Control Patterns</span></span>

<span data-ttu-id="056d2-193">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="056d2-194">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="056d2-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="056d2-195">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="056d2-195">Control Pattern</span></span>                                                   | <span data-ttu-id="056d2-196">Supporto</span><span class="sxs-lookup"><span data-stu-id="056d2-196">Support</span></span> | <span data-ttu-id="056d2-197">Note</span><span class="sxs-lookup"><span data-stu-id="056d2-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="056d2-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="056d2-199">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-199">Depends</span></span> | <span data-ttu-id="056d2-200">Se è possibile espandere o comprimere l'elemento dati per visualizzare e nascondere le informazioni, è necessario supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="056d2-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="056d2-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="056d2-202">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-202">Depends</span></span> | <span data-ttu-id="056d2-203">Gli elementi di dati supporteranno il pattern di controllo [GridItem](uiauto-implementinggriditem.md) quando una raccolta di elementi di dati è disponibile all'interno di un contenitore che può essere spostata a livello spaziale da elemento a elemento.</span><span class="sxs-lookup"><span data-stu-id="056d2-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="056d2-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="056d2-205">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-205">Depends</span></span> | <span data-ttu-id="056d2-206">Tutti gli elementi di dati supportano la possibilità di scorrere la visualizzazione con il pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) quando il relativo contenitore di dati contiene più elementi rispetto a quelli che possono essere visualizzati sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="056d2-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="056d2-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="056d2-208">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-208">Depends</span></span> | <span data-ttu-id="056d2-209">La possibilità di selezionare gli elementi di dati dipende dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="056d2-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="056d2-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="056d2-211">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-211">Depends</span></span> | <span data-ttu-id="056d2-212">Se l'elemento dati è contenuto all'interno di un tipo di controllo [DataGrid](uiauto-supportdatagridcontroltype.md) che dispone di un elemento header, deve supportare il pattern di controllo [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="056d2-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="056d2-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="056d2-214">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-214">Depends</span></span> | <span data-ttu-id="056d2-215">Se l'elemento dati contiene uno stato che può essere ciclito tramite, deve supportare il pattern di controllo di [alternanza](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="056d2-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="056d2-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="056d2-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="056d2-217">Dipende da</span><span class="sxs-lookup"><span data-stu-id="056d2-217">Depends</span></span> | <span data-ttu-id="056d2-218">Se il testo primario dell'elemento dati è modificabile, il pattern di controllo [value](uiauto-implementingvalue.md) deve essere supportato.</span><span class="sxs-lookup"><span data-stu-id="056d2-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="056d2-219">Utilizzo di oggetti dataItems in elenchi di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="056d2-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="056d2-220">Poiché gli elenchi di grandi dimensioni sono spesso virtualizzati nei framework dell'interfaccia utente per facilitare le prestazioni, un client di automazione interfaccia utente non può usare la funzionalità di query di automazione interfaccia utente per cercare il contenuto dell'albero completo nello stesso modo in cui è possibile in altri contenitori di elementi.</span><span class="sxs-lookup"><span data-stu-id="056d2-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="056d2-221">Un client deve scorrere l'elemento nella visualizzazione (oppure espandere il controllo per visualizzare tutte le opzioni disponibili) prima di accedere al set completo di informazioni dell'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="056d2-222">Quando si chiama [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sull'elemento di automazione interfaccia utente per l'elemento di dati, Esplora risorse di Microsoft Windows viene restituito correttamente e causa l'impostazione dello stato attivo sul controllo di modifica all'interno del sottoalbero dell'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="056d2-223">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="056d2-223">Required Events</span></span>

<span data-ttu-id="056d2-224">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli elemento dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="056d2-225">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="056d2-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="056d2-226">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="056d2-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="056d2-227">Note</span><span class="sxs-lookup"><span data-stu-id="056d2-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="056d2-228">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="056d2-229">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="056d2-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="056d2-231">Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="056d2-232">**\_Richiama \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="056d2-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="056d2-233">Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="056d2-234">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="056d2-235">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="056d2-236">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="056d2-237">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="056d2-238">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà ItemStatusPropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="056d2-239">Se il controllo supporta la proprietà [**ItemStatus**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="056d2-240">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="056d2-241">**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="056d2-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="056d2-242">Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="056d2-243">**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="056d2-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="056d2-244">Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="056d2-245">**\_ElementSelectedEventId SelectionItem di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="056d2-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="056d2-246">Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="056d2-247">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="056d2-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="056d2-248">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="056d2-249">Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="056d2-250">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="056d2-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="056d2-251">Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="056d2-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="056d2-252">Esempio del tipo di controllo DataItem</span><span class="sxs-lookup"><span data-stu-id="056d2-252">DataItem Control Type Example</span></span>

<span data-ttu-id="056d2-253">Nell'immagine seguente viene illustrato un tipo di controllo DataItem in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="056d2-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![screenshot del controllo visualizzazione elenco con il tipo di controllo DataItem](images/dataitemxmpl.jpg)

<span data-ttu-id="056d2-255">La visualizzazione controlli e la visualizzazione contenuto dell'albero di automazione interfaccia utente che riguarda il controllo elemento dati sono visualizzate di seguito.</span><span class="sxs-lookup"><span data-stu-id="056d2-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="056d2-256">I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="056d2-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="056d2-257">Il **gruppo** "contoso" fa inoltre parte della griglia del controllo host della griglia dati.</span><span class="sxs-lookup"><span data-stu-id="056d2-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="056d2-258">Per un esempio di una struttura di griglia di livello superiore, vedere [tipo di controllo DataGrid](uiauto-supportdatagridcontroltype.md).</span><span class="sxs-lookup"><span data-stu-id="056d2-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="056d2-259">Albero di automazione interfaccia utente-visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="056d2-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="056d2-260">Albero di automazione interfaccia utente-visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="056d2-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="056d2-261">Gruppo &quot; Contoso &quot; (tabella, griglia)</span><span class="sxs-lookup"><span data-stu-id="056d2-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="056d2-262">DataItem &quot; accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="056d2-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="056d2-263">&quot;Receivable.docdi account immagine&quot;</span><span class="sxs-lookup"><span data-stu-id="056d2-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="056d2-264">Modifica &quot; nome &quot; (TableItem, GridItem, valore &quot; accounts Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="056d2-265">Modifica &quot; Data modifica &quot; (TableItem, GridItem, valore &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="056d2-266">Modifica &quot; dimensioni &quot; (GridItem, TableItem, valore &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="056d2-267">DataItem &quot; accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="056d2-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="056d2-268">...</span><span class="sxs-lookup"><span data-stu-id="056d2-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="056d2-269">Gruppo &quot; Contoso &quot; (tabella, griglia)</span><span class="sxs-lookup"><span data-stu-id="056d2-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="056d2-270">DataItem &quot; accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="056d2-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="056d2-271">&quot;Receivable.docdi account immagine&quot;</span><span class="sxs-lookup"><span data-stu-id="056d2-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="056d2-272">Modifica &quot; nome &quot; (TableItem, GridItem, valore &quot; accounts Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="056d2-273">Modifica &quot; Data modifica &quot; (TableItem, GridItem, valore &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="056d2-274">Modifica &quot; dimensioni &quot; (GridItem, TableItem, valore &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="056d2-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="056d2-275">DataItem &quot; accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="056d2-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="056d2-276">...</span><span class="sxs-lookup"><span data-stu-id="056d2-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="056d2-277">Se una griglia rappresenta un elenco di elementi selezionabili, è possibile esporre gli elementi dell'interfaccia utente selezionabili corrispondenti con il tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) anziché con il tipo di controllo DataItem.</span><span class="sxs-lookup"><span data-stu-id="056d2-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="056d2-278">Nell'esempio precedente, gli elementi **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc") in **Group** ("contoso") possono essere migliorati esponendoli come tipi di controllo ListItem, perché il tipo già supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) .</span><span class="sxs-lookup"><span data-stu-id="056d2-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="056d2-279">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="056d2-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="056d2-280">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="056d2-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="056d2-281">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="056d2-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="056d2-282">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="056d2-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




