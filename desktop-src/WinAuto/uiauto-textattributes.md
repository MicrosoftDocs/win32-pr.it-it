---
title: Attributi di testo di automazione interfaccia utente
description: Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft espone le proprietà di formato e stile (attributi di testo) del contenuto testuale e fornisce un elenco di attributi di testo supportati.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automazione interfaccia utente, attributi di testo
- attributi di testo, informazioni
- attributi di testo, tipi Variant
- attributi di testo, tipi di dati
- Automazione interfaccia utente, elenco di attributi
- Automazione interfaccia utente, elenco di attributi di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300120"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="5a1aa-109">Attributi di testo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="5a1aa-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="5a1aa-110">Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft espone le proprietà di formato e stile (*attributi di testo*) del contenuto testuale e fornisce un elenco di attributi di testo supportati.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="5a1aa-111">I provider di automazione interfaccia utente espongono gli attributi di testo tramite i metodi [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del pattern di controllo [TextRange](uiauto-about-text-and-textrange-patterns.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1aa-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="5a1aa-112">Le applicazioni client usano il metodo [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) per recuperare il valore di un attributo di testo specifico per un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="5a1aa-113">I client possono usare il metodo [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) per eseguire la ricerca in un intervallo di testo per il testo con un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="5a1aa-114">Se viene trovato un testo corrispondente, il metodo crea un nuovo intervallo di testo che contiene il testo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="5a1aa-115">Gli attributi di testo nell'elenco seguente sono supportati dal pattern di controllo **TextRange** .</span><span class="sxs-lookup"><span data-stu-id="5a1aa-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="5a1aa-116">I nomi di attributo sono derivati dagli identificatori degli attributi di testo di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="5a1aa-117">Ad esempio, l'attributo **AnimationStyle** viene identificato dai client come [**\_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definito in UIAutomationClient. h) e dai provider come **testo \_ \_ \_ GUID dell'attributo AnimationStyle** (definito in Uiautomationcoreapi. h).</span><span class="sxs-lookup"><span data-stu-id="5a1aa-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="5a1aa-118">Per altre informazioni su ogni attributo di testo supportato, vedere [**identificatori di attributi di testo**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="5a1aa-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="5a1aa-119">Alcuni degli attributi elencati sono supportati a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="5a1aa-120">Vedere [**identificatori di attributi di testo**](uiauto-textattribute-ids.md) per note sul supporto della versione.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="5a1aa-121">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a1aa-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5a1aa-122">Attributi di annotazione</span><span class="sxs-lookup"><span data-stu-id="5a1aa-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="5a1aa-123">Attributi dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="5a1aa-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="5a1aa-124">Attributi del linguaggio</span><span class="sxs-lookup"><span data-stu-id="5a1aa-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="5a1aa-125">Attributo link</span><span class="sxs-lookup"><span data-stu-id="5a1aa-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="5a1aa-126">Attributi del margine della pagina</span><span class="sxs-lookup"><span data-stu-id="5a1aa-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="5a1aa-127">Attributi di allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="5a1aa-128">Attributi colore testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="5a1aa-129">Attributi di decorazione testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="5a1aa-130">Attributi di stile testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="5a1aa-131">Attributi di interazione e selezione</span><span class="sxs-lookup"><span data-stu-id="5a1aa-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="5a1aa-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a1aa-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="5a1aa-133">Attributi di annotazione</span><span class="sxs-lookup"><span data-stu-id="5a1aa-133">Annotation Attributes</span></span>

<span data-ttu-id="5a1aa-134">Gli oggetti Annotation e i tipi di annotazione sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="5a1aa-135">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-135">Attribute</span></span>             | <span data-ttu-id="5a1aa-136">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="5a1aa-138">**\_ANNOTATIONOBJECTSATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="5a1aa-140">**\_ANNOTATIONTYPESATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="5a1aa-141">Attributi dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="5a1aa-141">Font Attributes</span></span>

<span data-ttu-id="5a1aa-142">Il nome, le dimensioni e il peso di un tipo di carattere sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="5a1aa-143">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-143">Attribute</span></span>      | <span data-ttu-id="5a1aa-144">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-145">**FontName**</span></span>   | [<span data-ttu-id="5a1aa-146">**\_FONTNAMEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="5a1aa-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-147">**FontSize**</span></span>   | [<span data-ttu-id="5a1aa-148">**\_FONTSIZEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="5a1aa-149">**SpessoreCarattere**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-149">**FontWeight**</span></span> | [<span data-ttu-id="5a1aa-150">**\_FONTWEIGHTATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="5a1aa-151">Attributi del linguaggio</span><span class="sxs-lookup"><span data-stu-id="5a1aa-151">Language Attributes</span></span>

<span data-ttu-id="5a1aa-152">Le informazioni sulla lingua del testo sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="5a1aa-153">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-153">Attribute</span></span>              | <span data-ttu-id="5a1aa-154">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-155">**culture**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-155">**Culture**</span></span>            | [<span data-ttu-id="5a1aa-156">**\_CULTUREATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="5a1aa-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="5a1aa-158">**\_TEXTFLOWDIRECTIONSATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="5a1aa-159">Attributo link</span><span class="sxs-lookup"><span data-stu-id="5a1aa-159">Link Attribute</span></span>

<span data-ttu-id="5a1aa-160">L'attributo seguente fornisce l'intervallo di testo che rappresenta la destinazione di un collegamento in un documento.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="5a1aa-161">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-161">Attribute</span></span> | <span data-ttu-id="5a1aa-162">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-163">**Collegamento**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-163">**Link**</span></span>  | [<span data-ttu-id="5a1aa-164">**\_LINKATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="5a1aa-165">Attributi del margine della pagina</span><span class="sxs-lookup"><span data-stu-id="5a1aa-165">Page Margin Attributes</span></span>

<span data-ttu-id="5a1aa-166">I rettangoli di delimitazione di un intervallo di testo non espongono le coordinate del testo nella pagina.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="5a1aa-167">Tuttavia, un provider può esporre le informazioni sul margine della pagina usando gli attributi di testo seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="5a1aa-168">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-168">Attribute</span></span>          | <span data-ttu-id="5a1aa-169">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-170">**MarginBottom**</span></span>   | [<span data-ttu-id="5a1aa-171">**\_MARGINBOTTOMATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="5a1aa-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-172">**MarginLeading**</span></span>  | [<span data-ttu-id="5a1aa-173">**\_MARGINLEADINGATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="5a1aa-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-174">**MarginTop**</span></span>      | [<span data-ttu-id="5a1aa-175">**\_MARGINTOPATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-176">**MarginTrailing**</span></span> | [<span data-ttu-id="5a1aa-177">**\_MARGINTRAILINGATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="5a1aa-178">Attributi di allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-178">Text Alignment Attributes</span></span>

<span data-ttu-id="5a1aa-179">Le informazioni sull'allineamento del testo, ad esempio il rientro, le impostazioni di tabulazione e l'allineamento orizzontale, sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="5a1aa-180">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-180">Attribute</span></span>                   | <span data-ttu-id="5a1aa-181">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="5a1aa-183">**\_HORIZONTALTEXTALIGNMENTATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="5a1aa-185">**\_INDENTATIONFIRSTLINEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="5a1aa-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="5a1aa-187">**\_INDENTATIONLEADINGATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-188">**IndentationTrailing**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="5a1aa-189">**\_INDENTATIONTRAILINGATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="5a1aa-190">**Schede**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-190">**Tabs**</span></span>                    | [<span data-ttu-id="5a1aa-191">**\_TABSATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="5a1aa-192">Attributi colore testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-192">Text Color Attributes</span></span>

<span data-ttu-id="5a1aa-193">I colori del testo in primo piano e in background sono disponibili tramite gli attributi di testo seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="5a1aa-194">Entrambi i colori sono specificati come tipo di dati [**COLORREF**](/windows/desktop/gdi/colorref) .</span><span class="sxs-lookup"><span data-stu-id="5a1aa-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="5a1aa-195">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-195">Attribute</span></span>           | <span data-ttu-id="5a1aa-196">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-197">**BackgroundColor**</span></span> | [<span data-ttu-id="5a1aa-198">**\_BACKGROUNDCOLORATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-199">**ForegroundColor**</span></span> | [<span data-ttu-id="5a1aa-200">**\_FOREGROUNDCOLORATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="5a1aa-201">Attributi di decorazione testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-201">Text Decoration Attributes</span></span>

<span data-ttu-id="5a1aa-202">Gli effetti di testo includono aree quali elenchi puntati, sottolinee e animazioni.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="5a1aa-203">Se il testo include punti elenco o numeri iniziali, il simbolo o il testo utilizzato per il punto elenco o il numero deve essere incluso nel flusso di testo, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="5a1aa-204">Le informazioni sugli effetti di testo sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="5a1aa-205">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-205">Attribute</span></span>              | <span data-ttu-id="5a1aa-206">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="5a1aa-208">**\_ANIMATIONSTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="5a1aa-209">**BulletStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-209">**BulletStyle**</span></span>        | [<span data-ttu-id="5a1aa-210">**\_BULLETSTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="5a1aa-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="5a1aa-212">**\_OUTLINESTYLESATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-213">**OverlineColor**</span></span>      | [<span data-ttu-id="5a1aa-214">**\_OVERLINECOLORATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="5a1aa-216">**\_OVERLINESTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="5a1aa-218">**\_STRIKETHROUGHCOLORATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="5a1aa-220">**\_STRIKETHROUGHSTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="5a1aa-222">**\_UNDERLINECOLORATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="5a1aa-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="5a1aa-224">**\_UNDERLINESTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="5a1aa-225">Attributi di stile testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-225">Text Style Attributes</span></span>

<span data-ttu-id="5a1aa-226">Le informazioni sugli stili di testo sono disponibili anche con gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="5a1aa-227">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-227">Attribute</span></span>         | <span data-ttu-id="5a1aa-228">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-229">**CapStyle**</span></span>      | [<span data-ttu-id="5a1aa-230">**\_CAPSTYLEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-231">**IsHidden**</span></span>      | [<span data-ttu-id="5a1aa-232">**\_ISHIDDENATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-233">**IsItalic**</span></span>      | [<span data-ttu-id="5a1aa-234">**\_ISITALICATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="5a1aa-236">**\_ISREADONLYATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="5a1aa-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-237">**IsSuperscript**</span></span> | [<span data-ttu-id="5a1aa-238">**\_ISSUPERSCRIPTATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-239">**IsSubscript**</span></span>   | [<span data-ttu-id="5a1aa-240">**\_ISSUBSCRIPTATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="5a1aa-241">Attributi di interazione e selezione</span><span class="sxs-lookup"><span data-stu-id="5a1aa-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="5a1aa-242">Le informazioni sulla selezione di testo corrente nello stato intervallo e stato attivo sono disponibili anche se gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a1aa-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="5a1aa-243">Attributo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-243">Attribute</span></span>              | <span data-ttu-id="5a1aa-244">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5a1aa-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1aa-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-245">**IsActive**</span></span>           | [<span data-ttu-id="5a1aa-246">**\_ISACTIVEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="5a1aa-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="5a1aa-248">**\_SELECTIONACTIVEENDATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="5a1aa-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-249">**CaretPosition**</span></span>      | [<span data-ttu-id="5a1aa-250">**\_CARETPOSITIONATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="5a1aa-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="5a1aa-252">**\_CARETBIDIMODEATTRIBUTEID UIA**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="5a1aa-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a1aa-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5a1aa-254">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5a1aa-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5a1aa-255">Informazioni sul testo di automazione interfaccia utente e sui pattern di controllo TextRange</span><span class="sxs-lookup"><span data-stu-id="5a1aa-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="5a1aa-256">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="5a1aa-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="5a1aa-257">Utilizzo di controlli basati su testo</span><span class="sxs-lookup"><span data-stu-id="5a1aa-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 