---
title: Tipo di controllo Text
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Text
- Automazione interfaccia utente, tipo di controllo Text
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Text
- Automazione interfaccia utente, proprietà per il tipo di controllo Text
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Text
- Automazione interfaccia utente, eventi per il tipo di controllo Text
- strutture ad albero, tipo di controllo Text
- Proprietà, tipo di controllo Text
- pattern di controllo, tipo di controllo Text
- eventi, tipo di controllo Text
- supporto per il tipo di controllo Text
- Text (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Text
- tipi di controllo, pattern di controllo per il tipo di controllo Text
- tipi di controllo, supporto del testo
- tipi di controllo, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331100"
---
# <a name="text-control-type"></a><span data-ttu-id="8f87f-119">Tipo di controllo Text</span><span class="sxs-lookup"><span data-stu-id="8f87f-119">Text Control Type</span></span>

<span data-ttu-id="8f87f-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Text** .</span><span class="sxs-lookup"><span data-stu-id="8f87f-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="8f87f-121">Un controllo testo è un elemento di base dell'interfaccia utente che rappresenta una parte di testo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="8f87f-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Text** .</span><span class="sxs-lookup"><span data-stu-id="8f87f-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="8f87f-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli struttura ad albero in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e</span><span class="sxs-lookup"><span data-stu-id="8f87f-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="8f87f-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8f87f-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8f87f-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="8f87f-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="8f87f-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="8f87f-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="8f87f-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f87f-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="8f87f-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f87f-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="8f87f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f87f-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="8f87f-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="8f87f-130">Typical Tree Structure</span></span>

<span data-ttu-id="8f87f-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli testo e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8f87f-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="8f87f-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8f87f-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f87f-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="8f87f-133">Control View</span></span></th>
<th><span data-ttu-id="8f87f-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="8f87f-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8f87f-135">Testo</span><span class="sxs-lookup"><span data-stu-id="8f87f-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8f87f-136">Testo (se contenuto)</span><span class="sxs-lookup"><span data-stu-id="8f87f-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8f87f-137">Un controllo testo può essere usato da solo come etichetta o come testo statico in un form.</span><span class="sxs-lookup"><span data-stu-id="8f87f-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="8f87f-138">Può anche essere contenuto all'interno della struttura di uno degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f87f-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="8f87f-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="8f87f-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="8f87f-140">ListItem</span><span class="sxs-lookup"><span data-stu-id="8f87f-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="8f87f-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="8f87f-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="8f87f-142">I controlli testo potrebbero non essere visualizzati nella visualizzazione contenuto dell'albero di automazione interfaccia utente perché il testo viene spesso visualizzato tramite la proprietà **Name** di un altro controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="8f87f-143">Ad esempio, il testo usato per etichettare un controllo casella combinata viene esposto tramite la proprietà **Name** del controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="8f87f-144">Poiché il controllo casella combinata si trova nella visualizzazione contenuto dell'albero di automazione interfaccia utente, il controllo testo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8f87f-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="8f87f-145">I controlli testo possono avere elementi figlio nella visualizzazione contenuto se è presente un oggetto incorporato, ad esempio un collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="8f87f-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="8f87f-146">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="8f87f-146">Relevant Properties</span></span>

<span data-ttu-id="8f87f-147">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli testo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="8f87f-148">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="8f87f-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="8f87f-149">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f87f-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="8f87f-150">Valore</span><span class="sxs-lookup"><span data-stu-id="8f87f-150">Value</span></span>      | <span data-ttu-id="8f87f-151">Note</span><span class="sxs-lookup"><span data-stu-id="8f87f-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f87f-152">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="8f87f-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-153">See notes.</span></span> | <span data-ttu-id="8f87f-154">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="8f87f-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="8f87f-155">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="8f87f-156">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-156">See notes.</span></span> | <span data-ttu-id="8f87f-157">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="8f87f-158">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="8f87f-159">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-159">See notes.</span></span> | <span data-ttu-id="8f87f-160">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="8f87f-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="8f87f-161">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="8f87f-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="8f87f-162">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="8f87f-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="8f87f-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8f87f-164">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8f87f-165">Dipende da</span><span class="sxs-lookup"><span data-stu-id="8f87f-165">Depends</span></span>    | <span data-ttu-id="8f87f-166">Il controllo testo è contenuto se contiene informazioni non esposte nella proprietà Name di un altro controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8f87f-167">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8f87f-168">true</span><span class="sxs-lookup"><span data-stu-id="8f87f-168">TRUE</span></span>       | <span data-ttu-id="8f87f-169">Il controllo testo deve essere sempre un controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="8f87f-170">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="8f87f-171">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-171">See notes.</span></span> | <span data-ttu-id="8f87f-172">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f87f-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8f87f-173">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="8f87f-174">NULL</span><span class="sxs-lookup"><span data-stu-id="8f87f-174">NULL</span></span>       | <span data-ttu-id="8f87f-175">I controlli Text non hanno un'etichetta di testo statico.</span><span class="sxs-lookup"><span data-stu-id="8f87f-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="8f87f-176">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="8f87f-177">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-177">See notes.</span></span> | <span data-ttu-id="8f87f-178">Stringa localizzata corrispondente al tipo di controllo **Text** .</span><span class="sxs-lookup"><span data-stu-id="8f87f-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="8f87f-179">Il valore predefinito è "Text" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="8f87f-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="8f87f-180">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="8f87f-181">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="8f87f-181">See notes.</span></span> | <span data-ttu-id="8f87f-182">Il nome di un controllo testo può essere il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8f87f-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="8f87f-183">Tuttavia, se il controllo supporta anche il modello di [testo](uiauto-implementingtextandtextrange.md) e il testo è esteso, non usare il contenuto full-text come valore del **nome** .</span><span class="sxs-lookup"><span data-stu-id="8f87f-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="8f87f-184">Fornire invece un valore di **nome** più breve, derivato da altre proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="8f87f-185">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f87f-185">Required Control Patterns</span></span>

<span data-ttu-id="8f87f-186">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli testo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="8f87f-187">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8f87f-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="8f87f-188">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="8f87f-188">Control Pattern</span></span>                                         | <span data-ttu-id="8f87f-189">Supporto</span><span class="sxs-lookup"><span data-stu-id="8f87f-189">Support</span></span> | <span data-ttu-id="8f87f-190">Note</span><span class="sxs-lookup"><span data-stu-id="8f87f-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f87f-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="8f87f-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="8f87f-192">Dipende da</span><span class="sxs-lookup"><span data-stu-id="8f87f-192">Depends</span></span> | <span data-ttu-id="8f87f-193">Se il controllo di testo è contenuto in un controllo Table, è necessario che il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia supportato.</span><span class="sxs-lookup"><span data-stu-id="8f87f-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="8f87f-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="8f87f-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="8f87f-195">Dipende da</span><span class="sxs-lookup"><span data-stu-id="8f87f-195">Depends</span></span> | <span data-ttu-id="8f87f-196">Se il controllo testo è contenuto in un controllo Table, è necessario che il pattern di controllo [TableItem](uiauto-implementingtableitem.md) sia supportato.</span><span class="sxs-lookup"><span data-stu-id="8f87f-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="8f87f-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="8f87f-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="8f87f-198">Dipende da</span><span class="sxs-lookup"><span data-stu-id="8f87f-198">Depends</span></span> | <span data-ttu-id="8f87f-199">Il testo deve supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) per una migliore accessibilità; Tuttavia, non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f87f-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="8f87f-200">Il pattern di controllo Text è utile quando il testo ha stili di formattazione e attributi, ad esempio colore, grassetto e corsivo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="8f87f-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="8f87f-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="8f87f-202">Mai</span><span class="sxs-lookup"><span data-stu-id="8f87f-202">Never</span></span>   | <span data-ttu-id="8f87f-203">Un controllo di testo non supporta mai il pattern di controllo [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="8f87f-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="8f87f-204">Se il testo è modificabile, è il tipo di controllo [Edit](uiauto-supporteditcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="8f87f-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="8f87f-205">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="8f87f-205">Required Events</span></span>

<span data-ttu-id="8f87f-206">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli testo.</span><span class="sxs-lookup"><span data-stu-id="8f87f-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="8f87f-207">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8f87f-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="8f87f-208">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f87f-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="8f87f-209">Note</span><span class="sxs-lookup"><span data-stu-id="8f87f-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f87f-210">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="8f87f-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="8f87f-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="8f87f-212">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="8f87f-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="8f87f-213">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="8f87f-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="8f87f-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="8f87f-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="8f87f-215">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="8f87f-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="8f87f-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="8f87f-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="8f87f-217">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="8f87f-218">**\_TextChangedEventId testo \_ UIA**</span><span class="sxs-lookup"><span data-stu-id="8f87f-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="8f87f-219">Se il controllo supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="8f87f-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="8f87f-220">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f87f-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8f87f-221">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8f87f-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f87f-222">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f87f-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="8f87f-223">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8f87f-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




