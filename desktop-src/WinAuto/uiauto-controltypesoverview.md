---
title: Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente
description: I tipi di controllo di automazione interfaccia utente Microsoft sono proprietà che vengono utilizzate come identificatori noti che indicano il tipo di controllo rappresentato da un particolare elemento dell'interfaccia utente, ad esempio una casella combinata o un pulsante.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Automazione interfaccia utente, panoramica sui tipi di controllo
- Automazione interfaccia utente, proprietà UIA_LocalizedControlTypePropertyId
- tipi di controllo, informazioni
- tipi di controllo, requisiti
- tipi di controllo, prerequisiti
- tipi di controllo, predefiniti
- tipi di controllo, proprietà UIA_LocalizedControlTypePropertyId
- tipi di controllo predefiniti
- Proprietà UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516822"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="bc74f-112">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="bc74f-113">I tipi di controllo di automazione interfaccia utente Microsoft sono proprietà che vengono utilizzate come identificatori noti che indicano il tipo di controllo rappresentato da un particolare elemento dell'interfaccia utente, ad esempio una casella combinata o un pulsante.</span><span class="sxs-lookup"><span data-stu-id="bc74f-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="bc74f-114">Le applicazioni client usano il tipo per identificare le funzionalità di un controllo e per determinare come interagire con esso.</span><span class="sxs-lookup"><span data-stu-id="bc74f-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="bc74f-115">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc74f-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bc74f-116">Requisiti per i tipi di controllo per l'automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="bc74f-117">Proprietà LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="bc74f-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="bc74f-118">Tipi di controllo correnti per l'automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="bc74f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc74f-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="bc74f-120">Requisiti per i tipi di controllo per l'automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="bc74f-121">A ogni tipo di controllo di automazione interfaccia utente è associato un set di condizioni.</span><span class="sxs-lookup"><span data-stu-id="bc74f-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="bc74f-122">Quando un provider assegna un tipo di controllo a un controllo, il provider deve garantire che il controllo soddisfi tutte le condizioni associate a tale tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="bc74f-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="bc74f-123">Di seguito sono riportate le condizioni:</span><span class="sxs-lookup"><span data-stu-id="bc74f-123">The conditions include the following:</span></span>

-   <span data-ttu-id="bc74f-124">Pattern di controllo di automazione interfaccia utente: ogni tipo di controllo ha un set di pattern di controllo che il controllo deve supportare, un set facoltativo e un set che il controllo non deve supportare.</span><span class="sxs-lookup"><span data-stu-id="bc74f-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="bc74f-125">Valori di proprietà di automazione interfaccia utente: ogni tipo di controllo ha un set di proprietà che il controllo deve supportare.</span><span class="sxs-lookup"><span data-stu-id="bc74f-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="bc74f-126">Eventi di automazione interfaccia utente: ogni tipo di controllo ha un set di eventi che il controllo deve supportare.</span><span class="sxs-lookup"><span data-stu-id="bc74f-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="bc74f-127">Struttura dell'albero di automazione interfaccia utente: ogni tipo di controllo stabilisce il modo in cui il controllo deve apparire nella struttura dell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bc74f-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="bc74f-128">Quando un controllo soddisfa le condizioni per un particolare tipo di controllo, il valore della proprietà [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicherà tale tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="bc74f-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="bc74f-129">Se il controllo non soddisfa le specifiche per un particolare tipo di controllo, usare [**\_ CustomControlTypeId**](uiauto-controltype-ids.md) di gestione dell'interfaccia utente come ID del tipo di controllo e descrivere completamente il controllo usando le proprietà e i pattern di controllo pertinenti.</span><span class="sxs-lookup"><span data-stu-id="bc74f-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="bc74f-130">È anche possibile impostare la [**proprietà \_ LocalizedControlTypePropertyId di UIA**](uiauto-automation-element-propids.md) su una stringa che meglio descrive il tipo del controllo.</span><span class="sxs-lookup"><span data-stu-id="bc74f-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="bc74f-131">Proprietà LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="bc74f-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="bc74f-132">Se si usa un tipo di controllo predefinito per descrivere il controllo, usare il valore predefinito per la [**proprietà \_ LocalizedControlTypePropertyId di UIA**](uiauto-automation-element-propids.md) e consentire all'automazione dell'interfaccia utente di fornire una stringa localizzata per esporre correttamente i provider.</span><span class="sxs-lookup"><span data-stu-id="bc74f-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="bc74f-133">Se non è possibile usare un tipo di controllo predefinito per descrivere il controllo, impostare la proprietà **\_ LocalizedControlTypePropertyId di UIA** su una stringa localizzata che descrive in modo accurato il tipo del controllo.</span><span class="sxs-lookup"><span data-stu-id="bc74f-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="bc74f-134">La stringa deve essere concisa, ma con una precisione sufficiente che una tecnologia per l'accessibilità, ad esempio un'utilità per la lettura dello schermo, possa utilizzarla nell'interfaccia utente per informare l'utente del tipo del controllo.</span><span class="sxs-lookup"><span data-stu-id="bc74f-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="bc74f-135">Tipi di controllo correnti per l'automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="bc74f-136">Negli argomenti seguenti vengono descritti i tipi di controllo di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bc74f-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="bc74f-137">Per ogni tipo di controllo, la descrizione include il set di condizioni che un controllo del tipo specificato deve supportare:</span><span class="sxs-lookup"><span data-stu-id="bc74f-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="bc74f-138">Tipo di controllo AppBar</span><span class="sxs-lookup"><span data-stu-id="bc74f-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="bc74f-139">Tipo di controllo Button</span><span class="sxs-lookup"><span data-stu-id="bc74f-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="bc74f-140">Tipo di controllo Calendar</span><span class="sxs-lookup"><span data-stu-id="bc74f-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="bc74f-141">Tipo di controllo CheckBox</span><span class="sxs-lookup"><span data-stu-id="bc74f-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="bc74f-142">Tipo di controllo ComboBox</span><span class="sxs-lookup"><span data-stu-id="bc74f-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="bc74f-143">Tipo di controllo DataGrid</span><span class="sxs-lookup"><span data-stu-id="bc74f-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="bc74f-144">Tipo di controllo DataItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="bc74f-145">Tipo di controllo Document</span><span class="sxs-lookup"><span data-stu-id="bc74f-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="bc74f-146">Modificare il tipo di controllo</span><span class="sxs-lookup"><span data-stu-id="bc74f-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="bc74f-147">Tipo di controllo gruppo</span><span class="sxs-lookup"><span data-stu-id="bc74f-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="bc74f-148">Tipo di controllo Header</span><span class="sxs-lookup"><span data-stu-id="bc74f-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="bc74f-149">Tipo di controllo HeaderItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="bc74f-150">Tipo di controllo HyperLink</span><span class="sxs-lookup"><span data-stu-id="bc74f-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="bc74f-151">Tipo di controllo Image</span><span class="sxs-lookup"><span data-stu-id="bc74f-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="bc74f-152">Tipo di controllo List</span><span class="sxs-lookup"><span data-stu-id="bc74f-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="bc74f-153">Tipo di controllo ListItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="bc74f-154">Tipo di controllo menu</span><span class="sxs-lookup"><span data-stu-id="bc74f-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="bc74f-155">Tipo di controllo barra dei menu</span><span class="sxs-lookup"><span data-stu-id="bc74f-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="bc74f-156">Tipo di controllo MenuItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="bc74f-157">Tipo di controllo pane</span><span class="sxs-lookup"><span data-stu-id="bc74f-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="bc74f-158">Tipo di controllo ProgressBar</span><span class="sxs-lookup"><span data-stu-id="bc74f-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="bc74f-159">RadioButton (tipo di controllo)</span><span class="sxs-lookup"><span data-stu-id="bc74f-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="bc74f-160">Tipo di controllo ScrollBar</span><span class="sxs-lookup"><span data-stu-id="bc74f-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="bc74f-161">Tipo di controllo SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="bc74f-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="bc74f-162">Tipo di controllo Separator</span><span class="sxs-lookup"><span data-stu-id="bc74f-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="bc74f-163">Tipo di controllo Slider</span><span class="sxs-lookup"><span data-stu-id="bc74f-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="bc74f-164">Tipo di controllo Spinner</span><span class="sxs-lookup"><span data-stu-id="bc74f-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="bc74f-165">Tipo di controllo SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc74f-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="bc74f-166">Tipo di controllo StatusBar</span><span class="sxs-lookup"><span data-stu-id="bc74f-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="bc74f-167">Tipo di controllo Tab</span><span class="sxs-lookup"><span data-stu-id="bc74f-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="bc74f-168">Tipo di controllo TabItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="bc74f-169">Tipo di controllo Table</span><span class="sxs-lookup"><span data-stu-id="bc74f-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="bc74f-170">Tipo di controllo Text</span><span class="sxs-lookup"><span data-stu-id="bc74f-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="bc74f-171">Tipo di controllo Thumb</span><span class="sxs-lookup"><span data-stu-id="bc74f-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="bc74f-172">Tipo di controllo barra di titolo</span><span class="sxs-lookup"><span data-stu-id="bc74f-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="bc74f-173">Tipo di controllo ToolBar</span><span class="sxs-lookup"><span data-stu-id="bc74f-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="bc74f-174">Tipo di controllo ToolTip</span><span class="sxs-lookup"><span data-stu-id="bc74f-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="bc74f-175">Tipo di controllo Tree</span><span class="sxs-lookup"><span data-stu-id="bc74f-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="bc74f-176">Tipo di controllo TreeItem</span><span class="sxs-lookup"><span data-stu-id="bc74f-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="bc74f-177">Tipo di controllo Window</span><span class="sxs-lookup"><span data-stu-id="bc74f-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="bc74f-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc74f-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc74f-179">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bc74f-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc74f-180">Identificatori del tipo di controllo</span><span class="sxs-lookup"><span data-stu-id="bc74f-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="bc74f-181">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bc74f-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc74f-182">Supporto di tipi di controllo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="bc74f-183">Supporto per automazione interfaccia utente dei controlli standard</span><span class="sxs-lookup"><span data-stu-id="bc74f-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="bc74f-184">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bc74f-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 