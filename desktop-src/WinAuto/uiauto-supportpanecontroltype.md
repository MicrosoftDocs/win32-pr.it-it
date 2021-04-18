---
title: Tipo di controllo pane
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo pane
- Automazione interfaccia utente, tipo di controllo pane
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo pane
- Automazione interfaccia utente, proprietà per il tipo di controllo pane
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo pane
- Automazione interfaccia utente, eventi per il tipo di controllo pane
- strutture ad albero, tipo di controllo pane
- Proprietà, tipo di controllo pane
- pattern di controllo, tipo di controllo pane
- eventi, tipo di controllo pane
- supporto per il tipo di controllo pane
- Pane (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo pane
- tipi di controllo, pattern di controllo per il tipo di controllo pane
- tipi di controllo, supporto per il riquadro
- tipi di controllo, riquadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104565027"
---
# <a name="pane-control-type"></a><span data-ttu-id="29822-119">Tipo di controllo pane</span><span class="sxs-lookup"><span data-stu-id="29822-119">Pane Control Type</span></span>

<span data-ttu-id="29822-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **pane** .</span><span class="sxs-lookup"><span data-stu-id="29822-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="29822-121">Il tipo di controllo **pane** è per aree potenzialmente scorrevoli con contenuto diversi.</span><span class="sxs-lookup"><span data-stu-id="29822-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="29822-122">Viene usato per rappresentare un oggetto all'interno di un frame o di una finestra del documento.</span><span class="sxs-lookup"><span data-stu-id="29822-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="29822-123">Gli utenti possono spostarsi tra i controlli del riquadro e all'interno del contenuto del riquadro corrente.</span><span class="sxs-lookup"><span data-stu-id="29822-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="29822-124">I controlli riquadro rappresentano un livello di raggruppamento inferiore rispetto alle finestre o ai documenti, ma superiore ai singoli controlli.</span><span class="sxs-lookup"><span data-stu-id="29822-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="29822-125">L'utente si sposta tra i riquadri premendo TAB, F6 o CTRL+TAB, a seconda del contesto.</span><span class="sxs-lookup"><span data-stu-id="29822-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="29822-126">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **pane** .</span><span class="sxs-lookup"><span data-stu-id="29822-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="29822-127">I requisiti di automazione interfaccia utente si applicano a tutti i controlli riquadro in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="29822-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="29822-128">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="29822-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="29822-129">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="29822-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="29822-130">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="29822-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="29822-131">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="29822-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="29822-132">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="29822-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="29822-133">Esempio di tipo di controllo Pane</span><span class="sxs-lookup"><span data-stu-id="29822-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="29822-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29822-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="29822-135">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="29822-135">Typical Tree Structure</span></span>

<span data-ttu-id="29822-136">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli riquadro e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="29822-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="29822-137">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29822-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29822-138">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="29822-138">Control View</span></span></th>
<th><span data-ttu-id="29822-139">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="29822-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="29822-140">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="29822-141">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="29822-142">Un controllo riquadro viene sempre visualizzato nelle visualizzazioni controlli e contenuto.</span><span class="sxs-lookup"><span data-stu-id="29822-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="29822-143">Non esporre un oggetto layout come riquadro nel controllo o nella visualizzazione contenuto se l'oggetto viene utilizzato solo per la presentazione visiva.</span><span class="sxs-lookup"><span data-stu-id="29822-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="29822-144">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="29822-144">Relevant Properties</span></span>

<span data-ttu-id="29822-145">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli riquadro.</span><span class="sxs-lookup"><span data-stu-id="29822-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="29822-146">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="29822-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="29822-147">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="29822-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="29822-148">Valore</span><span class="sxs-lookup"><span data-stu-id="29822-148">Value</span></span>      | <span data-ttu-id="29822-149">Note</span><span class="sxs-lookup"><span data-stu-id="29822-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29822-150">**\_ACCESSKEYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="29822-151">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-151">See notes.</span></span> | <span data-ttu-id="29822-152">Se una combinazione di tasti specifica sposta lo stato attivo sul riquadro, le informazioni devono essere esposte tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="29822-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="29822-153">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="29822-154">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-154">See notes.</span></span> | <span data-ttu-id="29822-155">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="29822-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="29822-156">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="29822-157">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-157">See notes.</span></span> | <span data-ttu-id="29822-158">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="29822-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="29822-159">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="29822-160">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-160">See notes.</span></span> | <span data-ttu-id="29822-161">Questa proprietà espone un punto selezionabile del controllo riquadro che fa sì che il riquadro assuma lo stato attivo quando viene selezionato.</span><span class="sxs-lookup"><span data-stu-id="29822-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="29822-162">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="29822-163">**Riquadro**</span><span class="sxs-lookup"><span data-stu-id="29822-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="29822-164">**\_HELPTEXTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="29822-165">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-165">See notes.</span></span> | <span data-ttu-id="29822-166">Il testo della Guida per i controlli riquadro deve illustrare lo scopo del frame e il modo in cui si riferisce ad altri frame.</span><span class="sxs-lookup"><span data-stu-id="29822-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="29822-167">Una descrizione è necessaria se lo scopo e la relazione dei frame non sono deselezionati dal valore della [**proprietà \_ NamePropertyId di UIA**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="29822-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="29822-168">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="29822-169">true</span><span class="sxs-lookup"><span data-stu-id="29822-169">TRUE</span></span>       | <span data-ttu-id="29822-170">Il controllo riquadro viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="29822-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="29822-171">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="29822-172">true</span><span class="sxs-lookup"><span data-stu-id="29822-172">TRUE</span></span>       | <span data-ttu-id="29822-173">Il controllo riquadro viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="29822-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="29822-174">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="29822-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-175">See notes.</span></span> | <span data-ttu-id="29822-176">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="29822-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="29822-177">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="29822-178">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-178">See notes.</span></span> | <span data-ttu-id="29822-179">I controlli riquadro in genere non hanno un'etichetta statica.</span><span class="sxs-lookup"><span data-stu-id="29822-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="29822-180">Se è presente un'etichetta di testo statico, l'etichetta deve essere esposta tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="29822-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="29822-181">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="29822-182">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-182">See notes.</span></span> | <span data-ttu-id="29822-183">Stringa localizzata corrispondente al tipo di controllo **pane** .</span><span class="sxs-lookup"><span data-stu-id="29822-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="29822-184">Il valore predefinito è "pane" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="29822-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="29822-185">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="29822-186">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="29822-186">See notes.</span></span> | <span data-ttu-id="29822-187">Il valore di questa proprietà deve essere sempre un titolo chiaro, conciso e significativo.</span><span class="sxs-lookup"><span data-stu-id="29822-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="29822-188">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="29822-188">Required Control Patterns</span></span>

<span data-ttu-id="29822-189">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli riquadro.</span><span class="sxs-lookup"><span data-stu-id="29822-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="29822-190">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29822-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="29822-191">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="29822-191">Control Pattern</span></span>                                         | <span data-ttu-id="29822-192">Supporto</span><span class="sxs-lookup"><span data-stu-id="29822-192">Support</span></span> | <span data-ttu-id="29822-193">Note</span><span class="sxs-lookup"><span data-stu-id="29822-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29822-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="29822-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="29822-195">Dipende da</span><span class="sxs-lookup"><span data-stu-id="29822-195">Depends</span></span> | <span data-ttu-id="29822-196">Implementare il pattern di controllo [Dock](uiauto-implementingdock.md) se il controllo riquadro può essere ancorato.</span><span class="sxs-lookup"><span data-stu-id="29822-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="29822-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="29822-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="29822-198">Dipende da</span><span class="sxs-lookup"><span data-stu-id="29822-198">Depends</span></span> | <span data-ttu-id="29822-199">Implementare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se è possibile scorrere il controllo riquadro.</span><span class="sxs-lookup"><span data-stu-id="29822-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="29822-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="29822-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="29822-201">Dipende da</span><span class="sxs-lookup"><span data-stu-id="29822-201">Depends</span></span> | <span data-ttu-id="29822-202">Implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) se il controllo riquadro può essere spostato, ridimensionato o ruotato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="29822-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="29822-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="29822-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="29822-204">Mai</span><span class="sxs-lookup"><span data-stu-id="29822-204">Never</span></span>   | <span data-ttu-id="29822-205">Se l'elemento deve implementare il pattern di controllo [Window](uiauto-implementingwindow.md) , il controllo deve essere basato sul tipo di controllo [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="29822-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="29822-206">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="29822-206">Required Events</span></span>

<span data-ttu-id="29822-207">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli riquadro.</span><span class="sxs-lookup"><span data-stu-id="29822-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="29822-208">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="29822-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="29822-209">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="29822-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="29822-210">Note</span><span class="sxs-lookup"><span data-stu-id="29822-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29822-211">**\_ASYNCCONTENTLOADEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="29822-212">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="29822-213">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="29822-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="29822-215">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="29822-216">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="29822-217">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="29822-218">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="29822-219">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="29822-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="29822-221">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="29822-222">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="29822-223">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="29822-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="29822-225">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="29822-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="29822-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="29822-227">Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="29822-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="29822-228">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="29822-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="29822-229">Esempio di tipo di controllo Pane</span><span class="sxs-lookup"><span data-stu-id="29822-229">Pane Control Type Example</span></span>

<span data-ttu-id="29822-230">Nell'immagine seguente viene illustrato un controllo che implementa il tipo di controllo **pane** .</span><span class="sxs-lookup"><span data-stu-id="29822-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![screenshot che mostra l'esempio di un controllo riquadro](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29822-232">Albero di automazione interfaccia utente-visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="29822-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="29822-233">Albero di automazione interfaccia utente-visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="29822-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="29822-234">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-234">Pane</span></span>
<ul>
<li><span data-ttu-id="29822-235">Tree (pattern Scroll)</span><span class="sxs-lookup"><span data-stu-id="29822-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="29822-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="29822-236">TreeItem</span></span></li>
<li><span data-ttu-id="29822-237">...</span><span class="sxs-lookup"><span data-stu-id="29822-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="29822-238">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-238">Pane</span></span>
<ul>
<li><span data-ttu-id="29822-239">Edit (pattern scroll)</span><span class="sxs-lookup"><span data-stu-id="29822-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="29822-240">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-240">Pane</span></span>
<ul>
<li><span data-ttu-id="29822-241">Tree (pattern Scroll)</span><span class="sxs-lookup"><span data-stu-id="29822-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="29822-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="29822-242">TreeItem</span></span></li>
<li><span data-ttu-id="29822-243">...</span><span class="sxs-lookup"><span data-stu-id="29822-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="29822-244">Riquadro</span><span class="sxs-lookup"><span data-stu-id="29822-244">Pane</span></span>
<ul>
<li><span data-ttu-id="29822-245">Edit (pattern scroll)</span><span class="sxs-lookup"><span data-stu-id="29822-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="29822-246">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29822-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="29822-247">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="29822-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29822-248">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="29822-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="29822-249">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="29822-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




