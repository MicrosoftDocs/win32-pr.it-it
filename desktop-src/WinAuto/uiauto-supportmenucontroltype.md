---
title: Tipo di controllo menu
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo menu
- Automazione interfaccia utente, tipo di controllo menu
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo menu
- Automazione interfaccia utente, proprietà per il tipo di controllo menu
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo menu
- Automazione interfaccia utente, eventi per il tipo di controllo menu
- strutture ad albero, tipo di controllo menu
- Proprietà, tipo di controllo menu
- pattern di controllo, tipo di controllo menu
- eventi, tipo di controllo menu
- supporto per il tipo di controllo menu
- Menu (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo menu
- tipi di controllo, pattern di controllo per il tipo di controllo menu
- tipi di controllo, supporto per menu
- tipi di controllo, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044606"
---
# <a name="menu-control-type"></a><span data-ttu-id="0bfbb-119">Tipo di controllo menu</span><span class="sxs-lookup"><span data-stu-id="0bfbb-119">Menu Control Type</span></span>

<span data-ttu-id="0bfbb-120">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **menu** .</span><span class="sxs-lookup"><span data-stu-id="0bfbb-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="0bfbb-121">Un controllo menu consente l'organizzazione gerarchica degli elementi associati a comandi e gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="0bfbb-122">In una tipica applicazione di Microsoft Windows, una barra dei menu contiene diversi pulsanti di menu (ad esempio **file**, **modifica** e **finestra**), mentre ogni pulsante di menu Visualizza un menu.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="0bfbb-123">Un menu contiene una raccolta di voci di menu (ad esempio **Nuovo**, **Apri** e **Chiudi**), che può essere espansa per visualizzare altre voci di menu che, se selezionate, consentono di eseguire un'azione specifica.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="0bfbb-124">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **menu** .</span><span class="sxs-lookup"><span data-stu-id="0bfbb-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="0bfbb-125">I requisiti di automazione interfaccia utente si applicano a tutti i controlli menu in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern</span><span class="sxs-lookup"><span data-stu-id="0bfbb-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0bfbb-126">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0bfbb-127">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0bfbb-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0bfbb-128">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0bfbb-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0bfbb-129">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0bfbb-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0bfbb-130">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0bfbb-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0bfbb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bfbb-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0bfbb-132">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="0bfbb-132">Typical Tree Structure</span></span>

<span data-ttu-id="0bfbb-133">Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli menu e viene descritto il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0bfbb-134">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0bfbb-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0bfbb-135">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="0bfbb-135">Control View</span></span></th>
<th><span data-ttu-id="0bfbb-136">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="0bfbb-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0bfbb-137">Menu</span><span class="sxs-lookup"><span data-stu-id="0bfbb-137">Menu</span></span>
<ul>
<li><span data-ttu-id="0bfbb-138">MenuItem (1 o molti)</span><span class="sxs-lookup"><span data-stu-id="0bfbb-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="0bfbb-139">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="0bfbb-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0bfbb-140">Menu</span><span class="sxs-lookup"><span data-stu-id="0bfbb-140">Menu</span></span>
<ul>
<li><span data-ttu-id="0bfbb-141">MenuItem (1 o molti)</span><span class="sxs-lookup"><span data-stu-id="0bfbb-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="0bfbb-142">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="0bfbb-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0bfbb-143">I controlli menu vengono sempre visualizzati nella visualizzazione controlli e nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="0bfbb-144">I controlli menu devono essere visualizzati sotto il controllo a cui si riferiscono le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="0bfbb-145">I client di automazione interfaccia utente possono restare in ascolto dei [**\_ MenuOpenedEventId**](uiauto-event-ids.md) dell'interfaccia utente per assicurarsi che ottengano costantemente informazioni trasmesse dai controlli menu.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="0bfbb-146">I controlli menu di scelta rapida rappresentano un caso speciale.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-146">Context menu controls are a special case.</span></span> <span data-ttu-id="0bfbb-147">Possono apparire come elementi figlio del desktop o di una finestra dell'applicazione di primo livello.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="0bfbb-148">Un controllo menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="0bfbb-149">Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati nella tabella precedente nelle visualizzazioni controlli e contenuto.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="0bfbb-150">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="0bfbb-150">Relevant Properties</span></span>

<span data-ttu-id="0bfbb-151">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **menu** .</span><span class="sxs-lookup"><span data-stu-id="0bfbb-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="0bfbb-152">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0bfbb-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0bfbb-153">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0bfbb-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="0bfbb-154">Valore</span><span class="sxs-lookup"><span data-stu-id="0bfbb-154">Value</span></span>      | <span data-ttu-id="0bfbb-155">Note</span><span class="sxs-lookup"><span data-stu-id="0bfbb-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bfbb-156">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="0bfbb-157">**Menu**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="0bfbb-158">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0bfbb-159">true</span><span class="sxs-lookup"><span data-stu-id="0bfbb-159">TRUE</span></span>       | <span data-ttu-id="0bfbb-160">Il controllo menu viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="0bfbb-161">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0bfbb-162">true</span><span class="sxs-lookup"><span data-stu-id="0bfbb-162">TRUE</span></span>       | <span data-ttu-id="0bfbb-163">Il controllo menu viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="0bfbb-164">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="0bfbb-165">NULL</span><span class="sxs-lookup"><span data-stu-id="0bfbb-165">NULL</span></span>       | <span data-ttu-id="0bfbb-166">Non è prevista alcuna etichetta con un controllo menu standard.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="0bfbb-167">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="0bfbb-168">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-168">See notes.</span></span> | <span data-ttu-id="0bfbb-169">Il controllo menu non richiede l'impostazione di una proprietà **Name** o potrebbe avere lo stesso nome del controllo associato, ad esempio una voce di menu che ha aperto il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0bfbb-170">Pattern di controllo obbligatori</span><span class="sxs-lookup"><span data-stu-id="0bfbb-170">Required Control Patterns</span></span>

<span data-ttu-id="0bfbb-171">Non sono presenti pattern di controllo obbligatori per il tipo di controllo Menu.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="0bfbb-172">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="0bfbb-172">Required Events</span></span>

<span data-ttu-id="0bfbb-173">I controlli menu devono generare l'evento [**\_ MenuOpenedEventId di UIA**](uiauto-event-ids.md) quando vengono visualizzati sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="0bfbb-174">L' **evento \_ MenuOpenedEventId di UIA** includerà il testo del controllo.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="0bfbb-175">L' [**evento \_ MenuClosedEventId di UIA**](uiauto-event-ids.md) deve essere generato quando un menu scompare dallo schermo.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="0bfbb-176">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli menu.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="0bfbb-177">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0bfbb-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0bfbb-178">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0bfbb-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="0bfbb-179">Note</span><span class="sxs-lookup"><span data-stu-id="0bfbb-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bfbb-180">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="0bfbb-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="0bfbb-182">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="0bfbb-183">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0bfbb-184">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0bfbb-185">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0bfbb-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0bfbb-186">**\_MENUCLOSEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="0bfbb-187">**\_MENUOPENEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="0bfbb-188">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0bfbb-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bfbb-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0bfbb-190">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0bfbb-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0bfbb-191">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0bfbb-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0bfbb-192">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0bfbb-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




