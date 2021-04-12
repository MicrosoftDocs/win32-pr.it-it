---
title: Tipo di controllo AppBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo AppBar
- Automazione interfaccia utente, tipo di controllo AppBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo AppBar
- pattern di controllo, tipo di controllo AppBar
- supporto per il tipo di controllo AppBar
- Tipo di controllo AppBar
- tipi di controllo, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473859"
---
# <a name="appbar-control-type"></a><span data-ttu-id="3388b-110">Tipo di controllo AppBar</span><span class="sxs-lookup"><span data-stu-id="3388b-110">AppBar Control Type</span></span>

<span data-ttu-id="3388b-111">In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="3388b-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="3388b-112">Una barra dell'app è un elemento dell'interfaccia utente che presenta la navigazione, i comandi e gli strumenti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="3388b-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="3388b-113">Per le app di Windows Store, è possibile visualizzare le barre dell'app per le app premendo il tasto Windows + Z.</span><span class="sxs-lookup"><span data-stu-id="3388b-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="3388b-114">Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="3388b-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="3388b-115">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3388b-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3388b-116">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="3388b-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3388b-117">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="3388b-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3388b-118">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="3388b-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3388b-119">Eventi rilevanti</span><span class="sxs-lookup"><span data-stu-id="3388b-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="3388b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3388b-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3388b-121">Struttura ad albero tipica</span><span class="sxs-lookup"><span data-stu-id="3388b-121">Typical Tree Structure</span></span>

<span data-ttu-id="3388b-122">La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli **AppBar** e descrive il possibile contenuto di ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3388b-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="3388b-123">Il **pulsante** è l'elemento più comune all'interno di un **AppBar** , ma sono possibili anche altri controlli che richiamano azioni per un'app.</span><span class="sxs-lookup"><span data-stu-id="3388b-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="3388b-124">Un **AppBar** può anche avere 0 o più separatori (tipo di controllo **separator** ), che vengono visualizzati nella visualizzazione controlli come posizionati tra gli altri controlli.</span><span class="sxs-lookup"><span data-stu-id="3388b-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="3388b-125">Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3388b-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3388b-126">Visualizzazione controlli</span><span class="sxs-lookup"><span data-stu-id="3388b-126">Control View</span></span></th>
<th><span data-ttu-id="3388b-127">Visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="3388b-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3388b-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="3388b-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="3388b-129">Button (0 o più)</span><span class="sxs-lookup"><span data-stu-id="3388b-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="3388b-130">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="3388b-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3388b-131">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="3388b-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="3388b-132">Button (0 o più)</span><span class="sxs-lookup"><span data-stu-id="3388b-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="3388b-133">Altri controlli (0 o molti)</span><span class="sxs-lookup"><span data-stu-id="3388b-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="3388b-134">Proprietà rilevanti</span><span class="sxs-lookup"><span data-stu-id="3388b-134">Relevant Properties</span></span>

<span data-ttu-id="3388b-135">La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="3388b-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="3388b-136">Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="3388b-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="3388b-137">Proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3388b-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="3388b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3388b-138">Value</span></span>      | <span data-ttu-id="3388b-139">Note</span><span class="sxs-lookup"><span data-stu-id="3388b-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3388b-140">**\_AUTOMATIONIDPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="3388b-141">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="3388b-141">See notes.</span></span> | <span data-ttu-id="3388b-142">Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3388b-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="3388b-143">**\_BOUNDINGRECTANGLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="3388b-144">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="3388b-144">See notes.</span></span> | <span data-ttu-id="3388b-145">Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.</span><span class="sxs-lookup"><span data-stu-id="3388b-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="3388b-146">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3388b-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="3388b-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="3388b-148">**\_ISCONTENTELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3388b-149">FALSE</span><span class="sxs-lookup"><span data-stu-id="3388b-149">FALSE</span></span>      | <span data-ttu-id="3388b-150">Un controllo barra dell'app non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3388b-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="3388b-151">**\_ISCONTROLELEMENTPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3388b-152">true</span><span class="sxs-lookup"><span data-stu-id="3388b-152">TRUE</span></span>       | <span data-ttu-id="3388b-153">Un controllo barra dell'app viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3388b-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="3388b-154">**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="3388b-155">Vedere le note</span><span class="sxs-lookup"><span data-stu-id="3388b-155">See notes</span></span>  | <span data-ttu-id="3388b-156">Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="3388b-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="3388b-157">I controlli all'interno della barra dell'app possono in genere assumere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3388b-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="3388b-158">**\_ISOFFSCREENPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3388b-159">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="3388b-159">See notes.</span></span> | <span data-ttu-id="3388b-160">Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="3388b-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="3388b-161">**\_LABELEDBYPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3388b-162">Null</span><span class="sxs-lookup"><span data-stu-id="3388b-162">Null</span></span>       | <span data-ttu-id="3388b-163">I controlli barra dell'app in genere non hanno un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="3388b-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="3388b-164">**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="3388b-165">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="3388b-165">See notes.</span></span> | <span data-ttu-id="3388b-166">Stringa localizzata corrispondente al tipo di controllo **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="3388b-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="3388b-167">Il valore predefinito è "barra app" per en-US o inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="3388b-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="3388b-168">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="3388b-169">Vedere le note.</span><span class="sxs-lookup"><span data-stu-id="3388b-169">See notes.</span></span> | <span data-ttu-id="3388b-170">Il controllo barra dell'app non necessita di un nome a meno che un'applicazione non disponga di più di una barra dell'app.</span><span class="sxs-lookup"><span data-stu-id="3388b-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="3388b-171">Se in un'applicazione sono presenti più barre dell'app, usare questa proprietà per esporre i nomi distinti, ad esempio "Top" o "bottom".</span><span class="sxs-lookup"><span data-stu-id="3388b-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="3388b-172">Eventi obbligatori</span><span class="sxs-lookup"><span data-stu-id="3388b-172">Required Events</span></span>

<span data-ttu-id="3388b-173">La tabella seguente elenca gli eventi di automazione interfaccia utente che devono essere supportati dai controlli barra dell'app.</span><span class="sxs-lookup"><span data-stu-id="3388b-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="3388b-174">Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3388b-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3388b-175">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3388b-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="3388b-176">Note</span><span class="sxs-lookup"><span data-stu-id="3388b-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3388b-177">**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="3388b-178">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="3388b-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="3388b-179">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3388b-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="3388b-180">Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="3388b-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="3388b-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3388b-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="3388b-182">Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.</span><span class="sxs-lookup"><span data-stu-id="3388b-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="3388b-183">**\_STRUCTURECHANGEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="3388b-184">Eventi rilevanti</span><span class="sxs-lookup"><span data-stu-id="3388b-184">Relevant Events</span></span>

<span data-ttu-id="3388b-185">La tabella seguente elenca gli eventi di automazione interfaccia utente che sono particolarmente rilevanti per i controlli che implementano il tipo di controllo **AppBar** , ma non sono strettamente necessari.</span><span class="sxs-lookup"><span data-stu-id="3388b-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="3388b-186">Evento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3388b-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="3388b-187">Note</span><span class="sxs-lookup"><span data-stu-id="3388b-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3388b-188">**\_MENUCLOSEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="3388b-189">Le implementazioni della piattaforma possono generare questo evento quando il controllo barra dell'app è chiuso.</span><span class="sxs-lookup"><span data-stu-id="3388b-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="3388b-190">**\_MENUOPENEDEVENTID UIA**</span><span class="sxs-lookup"><span data-stu-id="3388b-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="3388b-191">Le implementazioni della piattaforma possono generare questo evento quando viene aperto il controllo barra dell'app.</span><span class="sxs-lookup"><span data-stu-id="3388b-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="3388b-192">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="3388b-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="3388b-193">Gestore dell'evento di modifica della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3388b-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3388b-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3388b-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3388b-195">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3388b-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3388b-196">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3388b-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3388b-197">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3388b-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="3388b-198">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3388b-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3388b-199">**AppBar (controllo XAML)**</span><span class="sxs-lookup"><span data-stu-id="3388b-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="3388b-200">[**Oggetto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3388b-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 