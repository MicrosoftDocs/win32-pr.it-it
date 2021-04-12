---
title: Tipo di controllo Header
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Header
- Automazione interfaccia utente, tipo di controllo Header
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Header
- Automazione interfaccia utente, proprietà per il tipo di controllo Header
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Header
- Automazione interfaccia utente, eventi per il tipo di controllo Header
- strutture ad albero, tipo di controllo Header
- Proprietà, tipo di controllo Header
- pattern di controllo, tipo di controllo Header
- eventi, tipo di controllo Header
- supporto per il tipo di controllo Header
- Header (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Header
- tipi di controllo, pattern di controllo per il tipo di controllo Header
- tipi di controllo, supporto per l'intestazione
- tipi di controllo, intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395854"
---
# <a name="header-control-type"></a><span data-ttu-id="7131a-119">Tipo di controllo Header</span><span class="sxs-lookup"><span data-stu-id="7131a-119">Header Control Type</span></span>

<span data-ttu-id="7131a-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **header** .</span><span class="sxs-lookup"><span data-stu-id="7131a-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="7131a-121">Il controllo intestazione fornisce un contenitore visivo per le etichette di righe o colonne di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7131a-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="7131a-122">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **header** .</span><span class="sxs-lookup"><span data-stu-id="7131a-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="7131a-123">I requisiti di automazione interfaccia utente si applicano a tutti i controlli intestazione in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="7131a-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="7131a-124">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7131a-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7131a-125">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="7131a-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="7131a-126">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="7131a-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="7131a-127">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="7131a-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="7131a-128">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="7131a-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="7131a-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7131a-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="7131a-130">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="7131a-130">Typical Tree Structure</span></span>

<span data-ttu-id="7131a-131">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli intestazione e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="7131a-132">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7131a-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7131a-133">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="7131a-133">Control View</span></span></th>
<th><span data-ttu-id="7131a-134">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="7131a-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="7131a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7131a-135">Header</span></span>
<ul>
<li><span data-ttu-id="7131a-136">HeaderItem (1 o più)</span><span class="sxs-lookup"><span data-stu-id="7131a-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="7131a-137">(Non applicabile)</span><span class="sxs-lookup"><span data-stu-id="7131a-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7131a-138">I controlli intestazione hanno sempre uno o più elementi figlio nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7131a-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="7131a-139">I controlli intestazione hanno zero elementi figlio nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7131a-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="7131a-140">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="7131a-140">Relevant Properties</span></span>

<span data-ttu-id="7131a-141">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli intestazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="7131a-142">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="7131a-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="7131a-143">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7131a-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="7131a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="7131a-144">Value</span></span>                                                            | <span data-ttu-id="7131a-145">Note</span><span class="sxs-lookup"><span data-stu-id="7131a-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7131a-146">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="7131a-147">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-147">See notes.</span></span>                                                       | <span data-ttu-id="7131a-148">Il valore di questa proprietà deve essere univoco in tutti i controlli in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="7131a-149">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="7131a-150">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-150">See notes.</span></span>                                                       | <span data-ttu-id="7131a-151">Il rettangolo più esterno che contiene l'intero controllo.</span><span class="sxs-lookup"><span data-stu-id="7131a-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="7131a-152">**\_CLICKABLEPOINTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="7131a-153">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-153">See notes.</span></span>                                                       | <span data-ttu-id="7131a-154">Supportata se è presente un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="7131a-155">Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.</span><span class="sxs-lookup"><span data-stu-id="7131a-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="7131a-156">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="7131a-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="7131a-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="7131a-158">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7131a-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="7131a-159">FALSE</span></span>                                                            | <span data-ttu-id="7131a-160">Il controllo intestazione non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7131a-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="7131a-161">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="7131a-162">true</span><span class="sxs-lookup"><span data-stu-id="7131a-162">TRUE</span></span>                                                             | <span data-ttu-id="7131a-163">Il controllo intestazione viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7131a-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="7131a-164">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="7131a-165">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-165">See notes.</span></span>                                                       | <span data-ttu-id="7131a-166">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="7131a-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="7131a-167">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="7131a-168">NULL</span><span class="sxs-lookup"><span data-stu-id="7131a-168">NULL</span></span>                                                             | <span data-ttu-id="7131a-169">I controlli intestazione in genere non hanno un'etichetta statica.</span><span class="sxs-lookup"><span data-stu-id="7131a-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7131a-170">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="7131a-171">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-171">See notes.</span></span>                                                       | <span data-ttu-id="7131a-172">Il valore predefinito è "header" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="7131a-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="7131a-173">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="7131a-174">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="7131a-174">See notes.</span></span>                                                       | <span data-ttu-id="7131a-175">Il controllo intestazione richiede un nome se è presente più di un'intestazione di riga o più di un'intestazione di colonna.</span><span class="sxs-lookup"><span data-stu-id="7131a-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="7131a-176">Identifica le informazioni all'interno dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="7131a-177">**\_ORIENTATIONPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="7131a-178">**OrientationType \_ Orizzontale** o **OrientationType \_ verticale**</span><span class="sxs-lookup"><span data-stu-id="7131a-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="7131a-179">Il valore di questa proprietà espone la posizione del controllo intestazione, indipendentemente dal fatto che sia un'intestazione di riga (**OrientationType \_ orizzontale**) o un'intestazione di colonna (**OrientationType \_ Vertical**).</span><span class="sxs-lookup"><span data-stu-id="7131a-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="7131a-180">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="7131a-180">Required Control Patterns</span></span>

<span data-ttu-id="7131a-181">La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per i controlli intestazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="7131a-182">Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7131a-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="7131a-183">Pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="7131a-183">Control Pattern</span></span>                                         | <span data-ttu-id="7131a-184">Supporto</span><span class="sxs-lookup"><span data-stu-id="7131a-184">Support</span></span> | <span data-ttu-id="7131a-185">Note</span><span class="sxs-lookup"><span data-stu-id="7131a-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7131a-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="7131a-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="7131a-187">Dipende da</span><span class="sxs-lookup"><span data-stu-id="7131a-187">Depends</span></span> | <span data-ttu-id="7131a-188">Implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) se il controllo intestazione può essere ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="7131a-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="7131a-189">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="7131a-189">Required Events</span></span>

<span data-ttu-id="7131a-190">La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli intestazione.</span><span class="sxs-lookup"><span data-stu-id="7131a-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="7131a-191">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7131a-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="7131a-192">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7131a-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="7131a-193">Note</span><span class="sxs-lookup"><span data-stu-id="7131a-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7131a-194">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="7131a-195">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="7131a-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="7131a-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7131a-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="7131a-197">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="7131a-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="7131a-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="7131a-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="7131a-199">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="7131a-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="7131a-200">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="7131a-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="7131a-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7131a-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7131a-202">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7131a-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7131a-203">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7131a-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="7131a-204">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7131a-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




