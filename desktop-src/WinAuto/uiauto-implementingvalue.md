---
title: Pattern di controllo value
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IValueProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo value
- Automazione interfaccia utente, pattern di controllo value
- Automazione interfaccia utente, IValueProvider
- IValueProvider
- implementazione di pattern di controllo Value di automazione interfaccia utente
- Pattern di controllo value
- pattern di controllo, IValueProvider
- pattern di controllo, implementazione del valore di automazione interfaccia utente
- pattern di controllo, valore
- interfacce, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399364"
---
# <a name="value-control-pattern"></a><span data-ttu-id="c8e99-113">Pattern di controllo value</span><span class="sxs-lookup"><span data-stu-id="c8e99-113">Value Control Pattern</span></span>

<span data-ttu-id="c8e99-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="c8e99-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="c8e99-115">Il pattern di controllo **value** viene usato per supportare i controlli con un valore intrinseco che non si estende su un intervallo e che può essere rappresentato come stringa.</span><span class="sxs-lookup"><span data-stu-id="c8e99-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="c8e99-116">La stringa di valore può essere modificabile, a seconda del controllo e delle relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="c8e99-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="c8e99-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c8e99-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="c8e99-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8e99-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c8e99-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c8e99-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c8e99-120">Membri obbligatori per **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="c8e99-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="c8e99-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8e99-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c8e99-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="c8e99-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c8e99-123">Quando si implementa il pattern di controllo **value** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8e99-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c8e99-124">I controlli, ad esempio un elemento elenco o un elemento albero, devono supportare il pattern di controllo **value** se il valore di uno degli elementi è modificabile, indipendentemente dalla modalità di modifica corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="c8e99-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="c8e99-125">Il controllo padre deve supportare anche il pattern di controllo **value** se gli elementi figlio sono modificabili.</span><span class="sxs-lookup"><span data-stu-id="c8e99-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="c8e99-126">Nell'immagine seguente viene illustrato un esempio di elemento di elenco modificabile.</span><span class="sxs-lookup"><span data-stu-id="c8e99-126">The following image shows an example of an editable list item.</span></span>

    ![illustrazione che mostra l'elemento elenco modificabile](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="c8e99-128">I controlli di modifica a riga singola e a più righe devono implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) per esporre il contenuto di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c8e99-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="c8e99-129">I controlli di modifica a più righe devono implementare [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) se il relativo contenuto può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="c8e99-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="c8e99-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) non supporta il recupero delle informazioni di formattazione o dei valori della sottostringa.</span><span class="sxs-lookup"><span data-stu-id="c8e99-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="c8e99-131">Implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in questi scenari.</span><span class="sxs-lookup"><span data-stu-id="c8e99-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="c8e99-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) deve essere implementato da controlli come il controllo di selezione della selezione colori di Microsoft Word (vedere l'immagine seguente), che supporta il mapping delle stringhe tra un valore di colore (ad esempio, "Yellow") e un valore [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.</span><span class="sxs-lookup"><span data-stu-id="c8e99-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![illustrazione che mostra il mapping del campione di colore delle stringhe](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="c8e99-134">Una proprietà **IsEnabled** di un controllo deve essere impostata su **true** e la relativa proprietà [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) è impostata su **false** prima di consentire una chiamata a [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span><span class="sxs-lookup"><span data-stu-id="c8e99-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="c8e99-135">Membri obbligatori per **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="c8e99-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="c8e99-136">Per l'implementazione dell'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) sono necessari i metodi e le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8e99-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="c8e99-137">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="c8e99-137">Required members</span></span>                                       | <span data-ttu-id="c8e99-138">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="c8e99-138">Member type</span></span> | <span data-ttu-id="c8e99-139">Note</span><span class="sxs-lookup"><span data-stu-id="c8e99-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c8e99-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c8e99-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="c8e99-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8e99-141">Property</span></span>    | <span data-ttu-id="c8e99-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="c8e99-142">None</span></span>  |
| [<span data-ttu-id="c8e99-143">**Valore**</span><span class="sxs-lookup"><span data-stu-id="c8e99-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="c8e99-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8e99-144">Property</span></span>    | <span data-ttu-id="c8e99-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="c8e99-145">None</span></span>  |
| [<span data-ttu-id="c8e99-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="c8e99-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="c8e99-147">Metodo</span><span class="sxs-lookup"><span data-stu-id="c8e99-147">Method</span></span>      | <span data-ttu-id="c8e99-148">nessuno</span><span class="sxs-lookup"><span data-stu-id="c8e99-148">None</span></span>  |



 

<span data-ttu-id="c8e99-149">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="c8e99-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8e99-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8e99-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8e99-151">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="c8e99-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c8e99-152">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c8e99-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c8e99-153">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="c8e99-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="c8e99-154">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="c8e99-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 