---
title: Tipo di controllo barra dei menu
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo barra dei menu.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo barra dei menu
- Automazione interfaccia utente, tipo di controllo barra dei menu
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo barra dei menu
- Automazione interfaccia utente, proprietà per il tipo di controllo barra dei menu
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo barra dei menu
- Automazione interfaccia utente, eventi per il tipo di controllo barra dei menu
- strutture ad albero, tipo di controllo barra dei menu
- Proprietà, tipo di controllo barra dei menu
- pattern di controllo, tipo di controllo barra dei menu
- eventi, tipo di controllo barra dei menu
- supporto per il tipo di controllo barra dei menu
- Tipo di controllo barra dei menu
- tipi di controllo, struttura ad albero per il tipo di controllo barra dei menu
- tipi di controllo, pattern di controllo per il tipo di controllo barra dei menu
- tipi di controllo, supporto per la barra dei menu
- tipi di controllo, barra dei menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298151"
---
# <a name="menubar-control-type"></a><span data-ttu-id="9a24f-119">Tipo di controllo barra dei menu</span><span class="sxs-lookup"><span data-stu-id="9a24f-119">MenuBar Control Type</span></span>

<span data-ttu-id="9a24f-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **barra dei menu** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="9a24f-121">I controlli barra dei menu sono un esempio di controlli che implementano il tipo di controllo **barra** dei menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="9a24f-122">Le barre dei menu consentono agli utenti di attivare comandi e opzioni contenuti in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a24f-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="9a24f-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **barra dei menu** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="9a24f-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra dei menu in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="9a24f-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9a24f-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a24f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9a24f-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="9a24f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9a24f-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="9a24f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9a24f-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="9a24f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9a24f-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="9a24f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9a24f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a24f-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9a24f-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="9a24f-131">Typical Tree Structure</span></span>

<span data-ttu-id="9a24f-132">La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra dei menu e descrive il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a24f-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9a24f-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a24f-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a24f-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="9a24f-134">Control View</span></span></th>
<th><span data-ttu-id="9a24f-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="9a24f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9a24f-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="9a24f-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="9a24f-137">MenuItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="9a24f-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="9a24f-138">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="9a24f-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9a24f-139">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9a24f-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="9a24f-140">MenuItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="9a24f-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="9a24f-141">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="9a24f-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9a24f-142">Un controllo barra dei menu viene sempre visualizzato nella visualizzazione controlli, ma non nella visualizzazione contenuto, perché in genere non fornisce informazioni significative all'utente finale (a meno che l'applicazione non contenga più di una barra dei menu).</span><span class="sxs-lookup"><span data-stu-id="9a24f-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="9a24f-143">I client di automazione interfaccia utente possono restare in ascolto dell'evento [**\_ MenuModeStartEventId di UIA**](uiauto-event-ids.md) per assicurarsi che vengano informati costantemente quando l'interfaccia utente entra in modalità menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="9a24f-144">Quando l'applicazione è in modalità menu, è possibile acquisire tutti gli input da tastiera per la navigazione dei menu. ad esempio, la digitazione di ' potrebbe richiamare il menu **Salva** anziché digitare il carattere nell'area client dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a24f-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="9a24f-145">L' **evento \_ MenuModeStartEventId di UIA** deve precedere il primo evento [**\_ MenuOpenedEventId di UIA**](uiauto-event-ids.md) per garantire la coerenza logica.</span><span class="sxs-lookup"><span data-stu-id="9a24f-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="9a24f-146">L' [**evento \_ MenuModeEndEventId di UIA**](uiauto-event-ids.md) segue l'ultimo evento [**\_ MenuClosedEventId di UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="9a24f-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="9a24f-147">Se si fa clic su una voce di menu, è possibile attivare immediatamente l'evento **\_ MenuModeStartEventId di UIA** , seguito da un evento **\_ MenuOpenedEventId di UIA** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="9a24f-148">Un controllo barra dei menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura.</span><span class="sxs-lookup"><span data-stu-id="9a24f-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="9a24f-149">Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati sopra nelle visualizzazioni controlli e contenuto.</span><span class="sxs-lookup"><span data-stu-id="9a24f-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9a24f-150">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="9a24f-150">Relevant Properties</span></span>

<span data-ttu-id="9a24f-151">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **barra dei menu** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="9a24f-152">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9a24f-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9a24f-153">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9a24f-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9a24f-154">Valore</span><span class="sxs-lookup"><span data-stu-id="9a24f-154">Value</span></span>       | <span data-ttu-id="9a24f-155">Note</span><span class="sxs-lookup"><span data-stu-id="9a24f-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a24f-156">**\_ACCELERATORKEYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9a24f-157">NULL</span><span class="sxs-lookup"><span data-stu-id="9a24f-157">NULL</span></span>        | <span data-ttu-id="9a24f-158">Le barre dei menu in genere non dispongono di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="9a24f-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="9a24f-159">**\_ACCESSKEYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9a24f-160">"ALT"</span><span class="sxs-lookup"><span data-stu-id="9a24f-160">"ALT"</span></span>       | <span data-ttu-id="9a24f-161">La pressione del tasto ALT dovrebbe in genere spostare lo stato attivo sulla barra dei menu all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a24f-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="9a24f-162">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9a24f-163">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9a24f-163">See notes.</span></span>  | <span data-ttu-id="9a24f-164">Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.</span><span class="sxs-lookup"><span data-stu-id="9a24f-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="9a24f-165">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9a24f-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="9a24f-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="9a24f-167">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9a24f-168">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a24f-168">FALSE</span></span>       | <span data-ttu-id="9a24f-169">Il controllo barra dei menu non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9a24f-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="9a24f-170">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9a24f-171">true</span><span class="sxs-lookup"><span data-stu-id="9a24f-171">TRUE</span></span>        | <span data-ttu-id="9a24f-172">Il controllo barra dei menu viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9a24f-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="9a24f-173">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9a24f-174">true</span><span class="sxs-lookup"><span data-stu-id="9a24f-174">TRUE</span></span>        | <span data-ttu-id="9a24f-175">I controlli barra dei menu hanno lo stato attivabile perché i controlli che contengono possono prendere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="9a24f-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="9a24f-176">**\_ISOFFSCREENPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9a24f-177">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9a24f-177">See notes.</span></span>  | <span data-ttu-id="9a24f-178">Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="9a24f-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="9a24f-179">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9a24f-180">NULL</span><span class="sxs-lookup"><span data-stu-id="9a24f-180">NULL</span></span>        | <span data-ttu-id="9a24f-181">I controlli barra dei menu in genere non hanno un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="9a24f-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="9a24f-182">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9a24f-183">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9a24f-183">See notes.</span></span>  | <span data-ttu-id="9a24f-184">Stringa localizzata corrispondente al tipo di controllo **barra dei menu** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="9a24f-185">Il valore predefinito è "barra dei menu" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="9a24f-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="9a24f-186">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9a24f-187">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="9a24f-187">See notes.</span></span>  | <span data-ttu-id="9a24f-188">Il controllo barra dei menu non necessita di un nome a meno che un'applicazione non abbia più di una barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="9a24f-189">Se in un'applicazione è presente più di una barra dei menu, utilizzare questa proprietà per esporre i nomi distinti, ad esempio "formattazione" o "struttura".</span><span class="sxs-lookup"><span data-stu-id="9a24f-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="9a24f-190">**\_ORIENTATIONPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9a24f-191">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9a24f-191">Depends</span></span>     | <span data-ttu-id="9a24f-192">Questa proprietà espone l'orientamento orizzontale o verticale del controllo barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9a24f-193">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="9a24f-193">Required Control Patterns</span></span>

<span data-ttu-id="9a24f-194">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="9a24f-195">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a24f-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9a24f-196">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="9a24f-196">Control Pattern</span></span>                                                   | <span data-ttu-id="9a24f-197">Supporto</span><span class="sxs-lookup"><span data-stu-id="9a24f-197">Support</span></span> | <span data-ttu-id="9a24f-198">Note</span><span class="sxs-lookup"><span data-stu-id="9a24f-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a24f-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9a24f-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9a24f-200">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9a24f-200">Depends</span></span> | <span data-ttu-id="9a24f-201">Se il controllo può essere espanso o compresso, deve implementare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="9a24f-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="9a24f-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="9a24f-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="9a24f-203">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9a24f-203">Depends</span></span> | <span data-ttu-id="9a24f-204">Se il controllo può essere ancorato a parti diverse dello schermo, deve implementare il pattern di controllo [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="9a24f-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="9a24f-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="9a24f-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="9a24f-206">Dipende da</span><span class="sxs-lookup"><span data-stu-id="9a24f-206">Depends</span></span> | <span data-ttu-id="9a24f-207">Se il controllo può essere ridimensionato, ruotato o spostato, deve implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="9a24f-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="9a24f-208">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="9a24f-208">Required Events</span></span>

<span data-ttu-id="9a24f-209">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="9a24f-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="9a24f-210">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9a24f-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9a24f-211">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9a24f-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="9a24f-212">Note</span><span class="sxs-lookup"><span data-stu-id="9a24f-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a24f-213">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="9a24f-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a24f-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="9a24f-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a24f-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="9a24f-216">Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9a24f-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="9a24f-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a24f-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="9a24f-218">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9a24f-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="9a24f-219">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9a24f-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="9a24f-220">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="9a24f-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="9a24f-221">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="9a24f-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9a24f-222">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a24f-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9a24f-223">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9a24f-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9a24f-224">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9a24f-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9a24f-225">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9a24f-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




