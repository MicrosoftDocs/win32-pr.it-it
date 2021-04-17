---
title: Tipo di controllo Table
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Table
- Automazione interfaccia utente, tipo di controllo Table
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Table
- Automazione interfaccia utente, proprietà per il tipo di controllo Table
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Table
- Automazione interfaccia utente, eventi per il tipo di controllo Table
- strutture ad albero, tipo di controllo Table
- Proprietà, tipo di controllo Table
- pattern di controllo, tipo di controllo Table
- eventi, tipo di controllo Table
- supporto per il tipo di controllo Table
- Table (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Table
- tipi di controllo, pattern di controllo per il tipo di controllo Table
- tipi di controllo, supporto per la tabella
- tipi di controllo, tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515925"
---
# <a name="table-control-type"></a><span data-ttu-id="d66e4-119">Tipo di controllo Table</span><span class="sxs-lookup"><span data-stu-id="d66e4-119">Table Control Type</span></span>

<span data-ttu-id="d66e4-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Table** .</span><span class="sxs-lookup"><span data-stu-id="d66e4-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="d66e4-121">I controlli tabella contengono righe e colonne di testo e, facoltativamente, intestazioni di riga e intestazioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="d66e4-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="d66e4-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Table** .</span><span class="sxs-lookup"><span data-stu-id="d66e4-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="d66e4-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli tabella in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="d66e4-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d66e4-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d66e4-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d66e4-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="d66e4-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d66e4-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="d66e4-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d66e4-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="d66e4-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d66e4-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="d66e4-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d66e4-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d66e4-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d66e4-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="d66e4-130">Typical Tree Structure</span></span>

<span data-ttu-id="d66e4-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli tabella e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d66e4-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d66e4-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d66e4-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d66e4-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="d66e4-133">Control View</span></span></th>
<th><span data-ttu-id="d66e4-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="d66e4-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d66e4-135">Tabella</span><span class="sxs-lookup"><span data-stu-id="d66e4-135">Table</span></span>
<ul>
<li><span data-ttu-id="d66e4-136">Text (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="d66e4-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="d66e4-137">Header (0 o più)</span><span class="sxs-lookup"><span data-stu-id="d66e4-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="d66e4-138">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="d66e4-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d66e4-139">Tabella</span><span class="sxs-lookup"><span data-stu-id="d66e4-139">Table</span></span>
<ul>
<li><span data-ttu-id="d66e4-140">Testo (1 o più)</span><span class="sxs-lookup"><span data-stu-id="d66e4-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="d66e4-141">Vari controlli (0 o più)</span><span class="sxs-lookup"><span data-stu-id="d66e4-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d66e4-142">Se un controllo tabella include intestazioni di riga o di colonna, queste devono essere esposte nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d66e4-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="d66e4-143">Non è necessario che la visualizzazione contenuto esponga queste informazioni perché è possibile accedervi usando [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span><span class="sxs-lookup"><span data-stu-id="d66e4-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="d66e4-144">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="d66e4-144">Relevant Properties</span></span>

<span data-ttu-id="d66e4-145">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="d66e4-146">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d66e4-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d66e4-147">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d66e4-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d66e4-148">Valore</span><span class="sxs-lookup"><span data-stu-id="d66e4-148">Value</span></span>      | <span data-ttu-id="d66e4-149">Note</span><span class="sxs-lookup"><span data-stu-id="d66e4-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d66e4-150">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d66e4-151">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-151">See notes.</span></span> | <span data-ttu-id="d66e4-152">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d66e4-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="d66e4-153">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d66e4-154">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-154">See notes.</span></span> | <span data-ttu-id="d66e4-155">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="d66e4-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="d66e4-156">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d66e4-157">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-157">See notes.</span></span> | <span data-ttu-id="d66e4-158">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="d66e4-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="d66e4-159">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="d66e4-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="d66e4-160">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d66e4-161">**Tabella**</span><span class="sxs-lookup"><span data-stu-id="d66e4-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d66e4-162">**\_DESCRIBEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d66e4-163">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-163">See notes.</span></span> | <span data-ttu-id="d66e4-164">Se la tabella viene annotata mediante altri elementi dell'interfaccia utente, ad esempio un elemento di testo contenente la descrizione della tabella, la proprietà DescribedBy deve esporre un riferimento all'elemento di automazione del controllo testo.</span><span class="sxs-lookup"><span data-stu-id="d66e4-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="d66e4-165">**\_HELPTEXTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="d66e4-166">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-166">See notes.</span></span> | <span data-ttu-id="d66e4-167">Altre informazioni sullo scopo della tabella devono essere esposte tramite questa proprietà se non sono sufficientemente spiegate dalla proprietà [**\_ NamePropertyId di UIA**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="d66e4-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="d66e4-168">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d66e4-169">true</span><span class="sxs-lookup"><span data-stu-id="d66e4-169">TRUE</span></span>       | <span data-ttu-id="d66e4-170">Il controllo tabella deve essere sempre visualizzato nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d66e4-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="d66e4-171">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d66e4-172">true</span><span class="sxs-lookup"><span data-stu-id="d66e4-172">TRUE</span></span>       | <span data-ttu-id="d66e4-173">Il controllo tabella deve essere sempre visualizzato nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d66e4-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="d66e4-174">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d66e4-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-175">See notes.</span></span> | <span data-ttu-id="d66e4-176">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d66e4-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="d66e4-177">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d66e4-178">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-178">See notes.</span></span> | <span data-ttu-id="d66e4-179">Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento all'elemento di automazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="d66e4-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="d66e4-180">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d66e4-181">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-181">See notes.</span></span> | <span data-ttu-id="d66e4-182">Stringa localizzata corrispondente al tipo di controllo **Table** .</span><span class="sxs-lookup"><span data-stu-id="d66e4-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="d66e4-183">Il valore predefinito è "Table" per en-US o English (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="d66e4-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="d66e4-184">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d66e4-185">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="d66e4-185">See notes.</span></span> | <span data-ttu-id="d66e4-186">Il controllo tabella in genere ottiene il valore per il nome da un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="d66e4-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="d66e4-187">Se non è presente un'etichetta di testo statico, l'elemento deve assegnare una proprietà Name che deve essere sempre disponibile per spiegare lo scopo della tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d66e4-188">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="d66e4-188">Required Control Patterns</span></span>

<span data-ttu-id="d66e4-189">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="d66e4-190">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d66e4-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d66e4-191">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="d66e4-191">Control Pattern</span></span>                                         | <span data-ttu-id="d66e4-192">Supporto</span><span class="sxs-lookup"><span data-stu-id="d66e4-192">Support</span></span>                     | <span data-ttu-id="d66e4-193">Note</span><span class="sxs-lookup"><span data-stu-id="d66e4-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d66e4-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="d66e4-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="d66e4-195">Necessario</span><span class="sxs-lookup"><span data-stu-id="d66e4-195">Required</span></span>                    | <span data-ttu-id="d66e4-196">Poiché il controllo tabella contiene elementi presentati in una griglia, supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) .</span><span class="sxs-lookup"><span data-stu-id="d66e4-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="d66e4-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d66e4-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="d66e4-198">Obbligatorio con oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="d66e4-198">Required with child objects</span></span> | <span data-ttu-id="d66e4-199">Gli oggetti interni di una tabella devono supportare sia il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia il pattern di controllo [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d66e4-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="d66e4-200">La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem, a meno che la tabella non faccia parte di un'altra tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="d66e4-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="d66e4-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="d66e4-202">Necessario</span><span class="sxs-lookup"><span data-stu-id="d66e4-202">Required</span></span>                    | <span data-ttu-id="d66e4-203">Il controllo tabella può sempre avere intestazioni associate al contenuto.</span><span class="sxs-lookup"><span data-stu-id="d66e4-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="d66e4-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d66e4-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="d66e4-205">Obbligatorio con oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="d66e4-205">Required with child objects</span></span> | <span data-ttu-id="d66e4-206">Gli oggetti interni di una tabella devono supportare sia il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia il pattern di controllo [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d66e4-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="d66e4-207">La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem, a meno che la tabella non faccia parte di un'altra tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="d66e4-208">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="d66e4-208">Required Events</span></span>

<span data-ttu-id="d66e4-209">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli tabella.</span><span class="sxs-lookup"><span data-stu-id="d66e4-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="d66e4-210">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d66e4-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d66e4-211">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d66e4-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d66e4-212">Note</span><span class="sxs-lookup"><span data-stu-id="d66e4-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d66e4-213">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d66e4-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d66e4-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d66e4-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d66e4-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d66e4-216">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="d66e4-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d66e4-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d66e4-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d66e4-218">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="d66e4-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="d66e4-219">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="d66e4-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="d66e4-220">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d66e4-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d66e4-221">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d66e4-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d66e4-222">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d66e4-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d66e4-223">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d66e4-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




