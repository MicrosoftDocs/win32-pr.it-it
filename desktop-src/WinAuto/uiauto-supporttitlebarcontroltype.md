---
title: Tipo di controllo barra di titolo
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo barra del titolo. Un controllo barra del titolo rappresenta una barra del titolo o della didascalia in una finestra.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo barra di titolo
- Automazione interfaccia utente, tipo di controllo barra di titolo
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo barra del titolo
- Automazione interfaccia utente, proprietà per il tipo di controllo barra di titolo
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo barra del titolo
- Automazione interfaccia utente, eventi per il tipo di controllo barra di titolo
- strutture ad albero, tipo di controllo barra di titolo
- Proprietà, tipo di controllo barra di titolo
- pattern di controllo, tipo di controllo barra di titolo
- eventi, tipo di controllo barra di titolo
- supporto per il tipo di controllo barra di titolo
- Tipo di controllo barra di titolo
- tipi di controllo, struttura ad albero per il tipo di controllo barra del titolo
- tipi di controllo, pattern di controllo per il tipo di controllo barra del titolo
- tipi di controllo, supporto per la barra del titolo
- tipi di controllo, barra di titolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955798"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="62c8d-120">Tipo di controllo barra di titolo</span><span class="sxs-lookup"><span data-stu-id="62c8d-120">TitleBar Control Type</span></span>

<span data-ttu-id="62c8d-121">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **barra** del titolo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="62c8d-122">Un controllo barra del titolo rappresenta una barra del titolo o della didascalia in una finestra.</span><span class="sxs-lookup"><span data-stu-id="62c8d-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="62c8d-123">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **barra** del titolo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="62c8d-124">I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra del titolo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="62c8d-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="62c8d-125">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="62c8d-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="62c8d-126">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="62c8d-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="62c8d-127">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="62c8d-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="62c8d-128">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="62c8d-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="62c8d-129">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="62c8d-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="62c8d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62c8d-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="62c8d-131">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="62c8d-131">Typical Tree Structure</span></span>

<span data-ttu-id="62c8d-132">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra del titolo e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62c8d-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="62c8d-133">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="62c8d-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62c8d-134">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="62c8d-134">Control View</span></span></th>
<th><span data-ttu-id="62c8d-135">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="62c8d-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="62c8d-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="62c8d-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="62c8d-137">Menu (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="62c8d-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="62c8d-138">Button (0 o più)</span><span class="sxs-lookup"><span data-stu-id="62c8d-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="62c8d-139">(Non applicabile; il controllo barra del titolo non include contenuto)</span><span class="sxs-lookup"><span data-stu-id="62c8d-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="62c8d-140">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="62c8d-140">Relevant Properties</span></span>

<span data-ttu-id="62c8d-141">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo della **barra** del titolo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="62c8d-142">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="62c8d-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="62c8d-143">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62c8d-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="62c8d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="62c8d-144">Value</span></span>        | <span data-ttu-id="62c8d-145">Note</span><span class="sxs-lookup"><span data-stu-id="62c8d-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c8d-146">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="62c8d-147">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="62c8d-147">See notes.</span></span>   | <span data-ttu-id="62c8d-148">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62c8d-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="62c8d-149">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="62c8d-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="62c8d-150">See notes.</span></span>   | <span data-ttu-id="62c8d-151">Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.</span><span class="sxs-lookup"><span data-stu-id="62c8d-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="62c8d-152">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="62c8d-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="62c8d-153">See notes.</span></span>   | <span data-ttu-id="62c8d-154">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="62c8d-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="62c8d-155">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="62c8d-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="62c8d-156">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="62c8d-157">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="62c8d-157">**TitleBar**</span></span> | <span data-ttu-id="62c8d-158">Questo valore è uguale per tutti i framework dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62c8d-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="62c8d-159">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="62c8d-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="62c8d-160">FALSE</span></span>        | <span data-ttu-id="62c8d-161">Il controllo barra del titolo non viene mai incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62c8d-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="62c8d-162">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="62c8d-163">true</span><span class="sxs-lookup"><span data-stu-id="62c8d-163">TRUE</span></span>         | <span data-ttu-id="62c8d-164">Il controllo barra del titolo viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="62c8d-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="62c8d-165">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="62c8d-166">FALSE</span><span class="sxs-lookup"><span data-stu-id="62c8d-166">FALSE</span></span>        | <span data-ttu-id="62c8d-167">Un controllo barra del titolo non ha mai lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="62c8d-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="62c8d-168">**\_ISOFFSCREENPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="62c8d-169">Dipende da</span><span class="sxs-lookup"><span data-stu-id="62c8d-169">Depends</span></span>      | <span data-ttu-id="62c8d-170">Un controllo barra del titolo restituisce un valore a seconda che sia visibile sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="62c8d-171">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="62c8d-172">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="62c8d-172">See notes.</span></span>   | <span data-ttu-id="62c8d-173">Un controllo barra del titolo in genere non dispone di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="62c8d-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="62c8d-174">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="62c8d-175">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="62c8d-175">See notes.</span></span>   | <span data-ttu-id="62c8d-176">Stringa localizzata corrispondente al tipo di controllo TitleBar.</span><span class="sxs-lookup"><span data-stu-id="62c8d-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="62c8d-177">Il valore predefinito è "barra del titolo" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="62c8d-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="62c8d-178">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="62c8d-179">""</span><span class="sxs-lookup"><span data-stu-id="62c8d-179">""</span></span>           | <span data-ttu-id="62c8d-180">Una barra del titolo non è contenuto; le informazioni testuali sono esposte dal nome della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="62c8d-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="62c8d-181">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="62c8d-181">Required Control Patterns</span></span>

<span data-ttu-id="62c8d-182">Il tipo di controllo **barra** del titolo non è necessario per supportare alcun pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="62c8d-183">La relativa funzionalità viene esposta tramite il pattern di controllo [Window](uiauto-implementingwindow.md) sul tipo di controllo [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="62c8d-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="62c8d-184">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="62c8d-184">Required Events</span></span>

<span data-ttu-id="62c8d-185">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli della barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="62c8d-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="62c8d-186">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="62c8d-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="62c8d-187">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62c8d-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="62c8d-188">Note</span><span class="sxs-lookup"><span data-stu-id="62c8d-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c8d-189">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="62c8d-190">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="62c8d-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="62c8d-191">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="62c8d-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="62c8d-192">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="62c8d-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="62c8d-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="62c8d-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="62c8d-194">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="62c8d-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="62c8d-195">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="62c8d-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="62c8d-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62c8d-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62c8d-197">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="62c8d-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62c8d-198">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62c8d-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="62c8d-199">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="62c8d-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




