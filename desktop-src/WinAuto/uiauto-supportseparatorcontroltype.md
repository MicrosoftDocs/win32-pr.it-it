---
title: Tipo di controllo Separator
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Separator
- Automazione interfaccia utente, tipo di controllo Separator
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Separator
- Automazione interfaccia utente, proprietà per il tipo di controllo Separator
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Separator
- Automazione interfaccia utente, eventi per il tipo di controllo Separator
- strutture ad albero, tipo di controllo Separator
- Proprietà, tipo di controllo Separator
- pattern di controllo, tipo di controllo Separator
- eventi, tipo di controllo Separator
- supporto per il tipo di controllo Separator
- Separator (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Separator
- tipi di controllo, pattern di controllo per il tipo di controllo Separator
- tipi di controllo, supporto per il separatore
- tipi di controllo, separatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515931"
---
# <a name="separator-control-type"></a><span data-ttu-id="c7494-119">Tipo di controllo Separator</span><span class="sxs-lookup"><span data-stu-id="c7494-119">Separator Control Type</span></span>

<span data-ttu-id="c7494-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **separator** .</span><span class="sxs-lookup"><span data-stu-id="c7494-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="c7494-121">I controlli separatore vengono usati per dividere visivamente uno spazio in due aree.</span><span class="sxs-lookup"><span data-stu-id="c7494-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="c7494-122">Ad esempio, un controllo separatore può essere una barra che definisce due riquadri in una finestra.</span><span class="sxs-lookup"><span data-stu-id="c7494-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="c7494-123">Se il separatore può essere spostato, il controllo deve essere esposto come il tipo di controllo Thumb.</span><span class="sxs-lookup"><span data-stu-id="c7494-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="c7494-124">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **separator** .</span><span class="sxs-lookup"><span data-stu-id="c7494-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="c7494-125">I requisiti di automazione interfaccia utente si applicano a tutti i controlli separatore in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern</span><span class="sxs-lookup"><span data-stu-id="c7494-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c7494-126">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7494-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c7494-127">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="c7494-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c7494-128">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="c7494-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c7494-129">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="c7494-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c7494-130">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="c7494-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c7494-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7494-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c7494-132">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="c7494-132">Typical Tree Structure</span></span>

<span data-ttu-id="c7494-133">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli separatore e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c7494-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c7494-134">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7494-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7494-135">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="c7494-135">Control View</span></span></th>
<th><span data-ttu-id="c7494-136">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="c7494-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c7494-137">Separatore</span><span class="sxs-lookup"><span data-stu-id="c7494-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c7494-138">Il tipo di controllo <strong>separator</strong> non dispone mai di contenuto.</span><span class="sxs-lookup"><span data-stu-id="c7494-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="c7494-139">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="c7494-139">Relevant Properties</span></span>

<span data-ttu-id="c7494-140">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli separatore.</span><span class="sxs-lookup"><span data-stu-id="c7494-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="c7494-141">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c7494-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c7494-142">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c7494-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c7494-143">Valore</span><span class="sxs-lookup"><span data-stu-id="c7494-143">Value</span></span>         | <span data-ttu-id="c7494-144">Note</span><span class="sxs-lookup"><span data-stu-id="c7494-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7494-145">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c7494-146">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c7494-146">See notes.</span></span>    | <span data-ttu-id="c7494-147">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c7494-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="c7494-148">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c7494-149">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c7494-149">See notes.</span></span>    | <span data-ttu-id="c7494-150">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="c7494-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="c7494-151">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c7494-152">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c7494-152">See notes.</span></span>    | <span data-ttu-id="c7494-153">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="c7494-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="c7494-154">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="c7494-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="c7494-155">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c7494-156">**Separatore**</span><span class="sxs-lookup"><span data-stu-id="c7494-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="c7494-157">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c7494-158">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7494-158">FALSE</span></span>         | <span data-ttu-id="c7494-159">Il controllo separatore non è mai un contenuto.</span><span class="sxs-lookup"><span data-stu-id="c7494-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="c7494-160">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c7494-161">true</span><span class="sxs-lookup"><span data-stu-id="c7494-161">TRUE</span></span>          | <span data-ttu-id="c7494-162">Il controllo separatore deve essere sempre un controllo.</span><span class="sxs-lookup"><span data-stu-id="c7494-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="c7494-163">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c7494-164">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c7494-164">See notes.</span></span>    | <span data-ttu-id="c7494-165">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7494-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="c7494-166">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c7494-167">NULL</span><span class="sxs-lookup"><span data-stu-id="c7494-167">NULL</span></span>          | <span data-ttu-id="c7494-168">Il controllo separatore non dispone di un'etichetta statica.</span><span class="sxs-lookup"><span data-stu-id="c7494-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="c7494-169">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c7494-170">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="c7494-170">See notes.</span></span>    | <span data-ttu-id="c7494-171">Stringa localizzata corrispondente al tipo di controllo **separator** .</span><span class="sxs-lookup"><span data-stu-id="c7494-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="c7494-172">Il valore predefinito è "Separator" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="c7494-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="c7494-173">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c7494-174">""</span><span class="sxs-lookup"><span data-stu-id="c7494-174">""</span></span>            | <span data-ttu-id="c7494-175">Il controllo separatore non richiede una proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="c7494-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c7494-176">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="c7494-176">Required Control Patterns</span></span>

<span data-ttu-id="c7494-177">Il controllo separatore non deve supportare qualsiasi pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="c7494-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="c7494-178">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7494-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="c7494-179">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="c7494-179">Required Events</span></span>

<span data-ttu-id="c7494-180">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli separatore.</span><span class="sxs-lookup"><span data-stu-id="c7494-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="c7494-181">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c7494-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c7494-182">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c7494-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="c7494-183">Note</span><span class="sxs-lookup"><span data-stu-id="c7494-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7494-184">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="c7494-185">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7494-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="c7494-186">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7494-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="c7494-187">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c7494-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="c7494-188">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c7494-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="c7494-189">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c7494-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="c7494-190">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="c7494-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="c7494-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7494-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c7494-192">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c7494-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7494-193">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c7494-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c7494-194">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c7494-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




