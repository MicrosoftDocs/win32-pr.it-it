---
title: Tipo di controllo DataGrid
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo DataGrid
- Automazione interfaccia utente, tipo di controllo DataGrid
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo DataGrid
- Automazione interfaccia utente, proprietà per il tipo di controllo DataGrid
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo DataGrid
- Automazione interfaccia utente, eventi per il tipo di controllo DataGrid
- strutture ad albero, tipo di controllo DataGrid
- Proprietà, tipo di controllo DataGrid
- pattern di controllo, tipo di controllo DataGrid
- eventi, tipo di controllo DataGrid
- supporto per il tipo di controllo DataGrid
- Tipo di controllo DataGrid
- tipi di controllo, struttura ad albero per il tipo di controllo DataGrid
- tipi di controllo, pattern di controllo per il tipo di controllo DataGrid
- tipi di controllo, supporto per DataGrid
- tipi di controllo, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955405"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="0c878-119">Tipo di controllo DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c878-119">DataGrid Control Type</span></span>

<span data-ttu-id="0c878-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="0c878-121">Il tipo di controllo **DataGrid** consente a un utente di usare facilmente gli elementi contenenti dati o elementi di automazione presentati in colonne o righe.</span><span class="sxs-lookup"><span data-stu-id="0c878-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="0c878-122">I controlli griglia dati contengono righe di elementi e colonne di informazioni su tali elementi.</span><span class="sxs-lookup"><span data-stu-id="0c878-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="0c878-123">Un controllo visualizzazione elenco in Esplora risorse di Windows Vista è un esempio che supporta il tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="0c878-124">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="0c878-125">I requisiti di automazione interfaccia utente si applicano a tutti i controlli griglia di dati in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="0c878-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0c878-126">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0c878-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0c878-127">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0c878-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0c878-128">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0c878-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0c878-129">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0c878-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0c878-130">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0c878-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0c878-131">Esempio di tipo di controllo DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c878-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="0c878-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c878-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0c878-133">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0c878-133">Typical Tree Structure</span></span>

<span data-ttu-id="0c878-134">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli griglia dati e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c878-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0c878-135">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c878-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c878-136">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="0c878-136">Control View</span></span></th>
<th><span data-ttu-id="0c878-137">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="0c878-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0c878-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c878-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="0c878-139">Header (0, 1 o 2)</span><span class="sxs-lookup"><span data-stu-id="0c878-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="0c878-140">HeaderItem (numero di colonne o righe)</span><span class="sxs-lookup"><span data-stu-id="0c878-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="0c878-141">DataItem (0 o più, può essere strutturato in una gerarchia)</span><span class="sxs-lookup"><span data-stu-id="0c878-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0c878-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c878-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="0c878-143">DataItem (0 o più, può essere strutturato in una gerarchia)</span><span class="sxs-lookup"><span data-stu-id="0c878-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0c878-144">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0c878-144">Relevant Properties</span></span>

<span data-ttu-id="0c878-145">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="0c878-146">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0c878-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0c878-147">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0c878-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0c878-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0c878-148">Value</span></span>        | <span data-ttu-id="0c878-149">Note</span><span class="sxs-lookup"><span data-stu-id="0c878-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c878-150">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0c878-151">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-151">See notes.</span></span>   | <span data-ttu-id="0c878-152">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0c878-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="0c878-153">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0c878-154">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-154">See notes.</span></span>   | <span data-ttu-id="0c878-155">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="0c878-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="0c878-156">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0c878-157">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-157">See notes.</span></span>   | <span data-ttu-id="0c878-158">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="0c878-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0c878-159">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="0c878-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="0c878-160">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0c878-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="0c878-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0c878-162">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0c878-163">true</span><span class="sxs-lookup"><span data-stu-id="0c878-163">TRUE</span></span>         | <span data-ttu-id="0c878-164">Il valore di questa proprietà deve essere sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="0c878-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="0c878-165">Ciò significa che il controllo griglia dati deve essere sempre presente nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0c878-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0c878-166">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0c878-167">true</span><span class="sxs-lookup"><span data-stu-id="0c878-167">TRUE</span></span>         | <span data-ttu-id="0c878-168">Il valore di questa proprietà deve sempre essere **true**.</span><span class="sxs-lookup"><span data-stu-id="0c878-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="0c878-169">Questo significa che il controllo griglia dati deve essere sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0c878-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="0c878-170">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0c878-171">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-171">See notes.</span></span>   | <span data-ttu-id="0c878-172">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c878-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="0c878-173">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0c878-174">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-174">See notes.</span></span>   | <span data-ttu-id="0c878-175">Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.</span><span class="sxs-lookup"><span data-stu-id="0c878-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="0c878-176">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0c878-177">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-177">See notes.</span></span>   | <span data-ttu-id="0c878-178">Stringa localizzata corrispondente al tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="0c878-179">Il valore predefinito è "griglia dati" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="0c878-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="0c878-180">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0c878-181">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0c878-181">See notes.</span></span>   | <span data-ttu-id="0c878-182">Il controllo griglia dati in genere ottiene il valore per la proprietà **Name** da un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="0c878-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="0c878-183">Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve assegnare un valore a per la proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="0c878-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="0c878-184">Il valore della proprietà **Name** non deve mai essere il contenuto testuale del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="0c878-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0c878-185">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0c878-185">Required Control Patterns</span></span>

<span data-ttu-id="0c878-186">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli griglia dati.</span><span class="sxs-lookup"><span data-stu-id="0c878-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="0c878-187">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c878-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0c878-188">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="0c878-188">Control Pattern</span></span>                                         | <span data-ttu-id="0c878-189">Supporto</span><span class="sxs-lookup"><span data-stu-id="0c878-189">Support</span></span>  | <span data-ttu-id="0c878-190">Note</span><span class="sxs-lookup"><span data-stu-id="0c878-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c878-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="0c878-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="0c878-192">Necessario</span><span class="sxs-lookup"><span data-stu-id="0c878-192">Required</span></span> | <span data-ttu-id="0c878-193">Il controllo griglia dati stesso supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) perché gli elementi che contiene contengono metadati disposti in una griglia.</span><span class="sxs-lookup"><span data-stu-id="0c878-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="0c878-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="0c878-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="0c878-195">Dipende da</span><span class="sxs-lookup"><span data-stu-id="0c878-195">Depends</span></span>  | <span data-ttu-id="0c878-196">La possibilità di scorrere la griglia dati dipende dal contenuto e dalla presenza o meno delle barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="0c878-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="0c878-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="0c878-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="0c878-198">Dipende da</span><span class="sxs-lookup"><span data-stu-id="0c878-198">Depends</span></span>  | <span data-ttu-id="0c878-199">La possibilità di selezionare la griglia dati dipende dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="0c878-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="0c878-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="0c878-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="0c878-201">Dipende da</span><span class="sxs-lookup"><span data-stu-id="0c878-201">Depends</span></span>  | <span data-ttu-id="0c878-202">Un controllo griglia di dati che dispone di un'intestazione deve supportare il pattern di controllo [Table](uiauto-implementingtable.md) .</span><span class="sxs-lookup"><span data-stu-id="0c878-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="0c878-203">Gli elementi di dati nei contenitori di griglia dati supporteranno almeno:</span><span class="sxs-lookup"><span data-stu-id="0c878-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="0c878-204">Pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) (se la griglia dati è selezionabile)</span><span class="sxs-lookup"><span data-stu-id="0c878-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="0c878-205">Pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) (se la griglia dati è scorrevole)</span><span class="sxs-lookup"><span data-stu-id="0c878-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="0c878-206">Pattern di controllo [GridItem](uiauto-implementinggriditem.md)</span><span class="sxs-lookup"><span data-stu-id="0c878-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="0c878-207">Pattern di controllo [TableItem](uiauto-implementingtableitem.md) (se la griglia dati ha un'intestazione)</span><span class="sxs-lookup"><span data-stu-id="0c878-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="0c878-208">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0c878-208">Required Events</span></span>

<span data-ttu-id="0c878-209">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli griglia dati.</span><span class="sxs-lookup"><span data-stu-id="0c878-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="0c878-210">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c878-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0c878-211">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0c878-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="0c878-212">Note</span><span class="sxs-lookup"><span data-stu-id="0c878-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c878-213">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="0c878-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="0c878-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="0c878-216">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="0c878-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="0c878-218">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="0c878-219">**\_LAYOUTINVALIDATEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="0c878-220">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="0c878-221">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0c878-222">Se il controllo supporta la proprietà CurrentView del pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="0c878-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="0c878-224">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0c878-225">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="0c878-226">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0c878-227">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="0c878-228">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0c878-229">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="0c878-230">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0c878-231">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="0c878-232">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0c878-233">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c878-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="0c878-234">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0c878-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="0c878-235">**\_InvalidatedEventId selezione \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="0c878-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="0c878-236">Esempio di tipo di controllo DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c878-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="0c878-237">Nell'immagine seguente viene illustrato un controllo visualizzazione elenco che implementa il tipo di controllo **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="0c878-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![screenshot del controllo visualizzazione elenco con il tipo di controllo DataGrid](images/datagridxmpl.jpg)

<span data-ttu-id="0c878-239">La visualizzazione controlli e la visualizzazione contenuto dell'albero di automazione interfaccia utente che riguarda il controllo visualizzazione elenco sono visualizzate di seguito.</span><span class="sxs-lookup"><span data-stu-id="0c878-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="0c878-240">I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="0c878-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c878-241">Albero di automazione interfaccia utente-visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="0c878-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="0c878-242">Albero di automazione interfaccia utente-visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="0c878-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c878-243">DataGrid (ordinamento, tabella, selezione, griglia)</span><span class="sxs-lookup"><span data-stu-id="0c878-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="0c878-244">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c878-244">Header</span></span>
<ul>
<li><span data-ttu-id="0c878-245">&quot;Nome HeaderItem &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c878-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="0c878-246">Data di HeaderItem &quot; modificata &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c878-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="0c878-247">&quot;Dimensioni HeaderItem &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c878-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="0c878-248">Gruppo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="0c878-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="0c878-249">&quot;Receivable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="0c878-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="0c878-250">&quot;Payable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="0c878-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="0c878-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="0c878-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="0c878-252">Gruppo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="0c878-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="0c878-253">&quot;Receivable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="0c878-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="0c878-254">&quot;Payable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="0c878-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0c878-255">\*Nell'esempio precedente viene illustrata una griglia di dati che contiene più livelli di controlli.</span><span class="sxs-lookup"><span data-stu-id="0c878-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="0c878-256">Il controllo **Group** ("contoso") contiene due controlli **DataItem** ("Accounts Receivable.doc" e "Accounts Payable.doc").</span><span class="sxs-lookup"><span data-stu-id="0c878-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="0c878-257">Una  / coppia di **GridItem** DataGrid è indipendente da una coppia in un altro livello.</span><span class="sxs-lookup"><span data-stu-id="0c878-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="0c878-258">I controlli **DataItem** in un **gruppo** possono essere esposti anche come tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) , consentendo loro di essere presentati più chiaramente come oggetti selezionabili, anziché come elementi dati semplici.</span><span class="sxs-lookup"><span data-stu-id="0c878-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="0c878-259">Questo esempio non include i sottoelementi degli elementi di dati raggruppati.</span><span class="sxs-lookup"><span data-stu-id="0c878-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="0c878-260">Per un altro esempio di più livelli di controlli, vedere il tipo di controllo [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="0c878-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c878-261">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c878-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0c878-262">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0c878-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c878-263">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0c878-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0c878-264">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0c878-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




