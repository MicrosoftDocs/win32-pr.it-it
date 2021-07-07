---
title: Automazione interfaccia utente di testo
description: Questo argomento descrive come Microsoft Automazione interfaccia utente il formato e le proprietà di stile (attributi di testo) del contenuto testuale e fornisce un elenco di attributi di testo supportati.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automazione interfaccia utente,attributi di testo
- attributi di testo, informazioni
- attributi di testo, tipi variant
- attributi di testo, tipi di dati
- Automazione interfaccia utente,elenco di attributi
- Automazione interfaccia utente,elenco di attributi di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353624"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="c5a65-109">Automazione interfaccia utente di testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="c5a65-110">Questo argomento descrive come Microsoft Automazione interfaccia utente il formato e le proprietà di stile *(* attributi di testo ) del contenuto testuale e fornisce un elenco di attributi di testo supportati.</span><span class="sxs-lookup"><span data-stu-id="c5a65-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="c5a65-111">Automazione interfaccia utente provider di testo espongono attributi di testo tramite [**i metodi GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) [**e FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del [pattern di controllo TextRange.](uiauto-about-text-and-textrange-patterns.md)</span><span class="sxs-lookup"><span data-stu-id="c5a65-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="c5a65-112">Le applicazioni client usano [**il metodo IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) per recuperare il valore di un particolare attributo di testo per un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="c5a65-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="c5a65-113">I client possono usare [**il metodo IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) per cercare testo con un attributo specifico in un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="c5a65-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="c5a65-114">Se viene trovato un testo corrispondente, il metodo crea un nuovo intervallo di testo contenente il testo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c5a65-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="c5a65-115">Gli attributi di testo nell'elenco seguente sono supportati dal pattern **di controllo TextRange.**</span><span class="sxs-lookup"><span data-stu-id="c5a65-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="c5a65-116">I nomi degli attributi derivano dagli identificatori Automazione interfaccia utente degli attributi di testo.</span><span class="sxs-lookup"><span data-stu-id="c5a65-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="c5a65-117">Ad esempio, l'attributo **AnimationStyle** viene identificato dai client come [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definito in Uiautomationclient.h) e dai provider come GUID dell'attributo **Text \_ \_ \_ AnimationStyle** (definito in Uiautomationcoreapi.h).</span><span class="sxs-lookup"><span data-stu-id="c5a65-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="c5a65-118">Per altre informazioni su ogni attributo di testo supportato, vedere [**Identificatori di attributi di testo**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="c5a65-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="c5a65-119">Alcuni degli attributi elencati sono supportati a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c5a65-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="c5a65-120">Per le note sul supporto [**della versione,**](uiauto-textattribute-ids.md) vedere Identificatori di attributi di testo.</span><span class="sxs-lookup"><span data-stu-id="c5a65-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="c5a65-121">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5a65-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c5a65-122">Attributi di annotazione</span><span class="sxs-lookup"><span data-stu-id="c5a65-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="c5a65-123">Attributi dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="c5a65-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="c5a65-124">Attributi del linguaggio</span><span class="sxs-lookup"><span data-stu-id="c5a65-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="c5a65-125">Attributo di collegamento</span><span class="sxs-lookup"><span data-stu-id="c5a65-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="c5a65-126">Attributi del margine di pagina</span><span class="sxs-lookup"><span data-stu-id="c5a65-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="c5a65-127">Attributi di allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="c5a65-128">Attributi di colore del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="c5a65-129">Attributi di decorazione del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="c5a65-130">Attributi di stile del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="c5a65-131">Attributi di interazione e selezione</span><span class="sxs-lookup"><span data-stu-id="c5a65-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="c5a65-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5a65-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="c5a65-133">Attributi di annotazione</span><span class="sxs-lookup"><span data-stu-id="c5a65-133">Annotation Attributes</span></span>

<span data-ttu-id="c5a65-134">Gli oggetti annotazione e i tipi di annotazione sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="c5a65-135">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-135">Attribute</span></span>             | <span data-ttu-id="c5a65-136">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c5a65-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="c5a65-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="c5a65-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-annotation-type-identifiers.md) |
| <span data-ttu-id="c5a65-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="c5a65-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="c5a65-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="c5a65-141">Attributi dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="c5a65-141">Font Attributes</span></span>

<span data-ttu-id="c5a65-142">Il nome, la dimensione e lo spessore di un tipo di carattere sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="c5a65-143">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-143">Attribute</span></span>      | <span data-ttu-id="c5a65-144">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="c5a65-145">**FontName**</span></span>   | [<span data-ttu-id="c5a65-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="c5a65-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="c5a65-147">**FontSize**</span></span>   | [<span data-ttu-id="c5a65-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="c5a65-149">**SpessoreCarattere**</span><span class="sxs-lookup"><span data-stu-id="c5a65-149">**FontWeight**</span></span> | [<span data-ttu-id="c5a65-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="c5a65-151">Attributi del linguaggio</span><span class="sxs-lookup"><span data-stu-id="c5a65-151">Language Attributes</span></span>

<span data-ttu-id="c5a65-152">Le informazioni sulla lingua del testo sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="c5a65-153">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-153">Attribute</span></span>              | <span data-ttu-id="c5a65-154">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-155">**culture**</span><span class="sxs-lookup"><span data-stu-id="c5a65-155">**Culture**</span></span>            | [<span data-ttu-id="c5a65-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="c5a65-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="c5a65-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="c5a65-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="c5a65-159">Attributo di collegamento</span><span class="sxs-lookup"><span data-stu-id="c5a65-159">Link Attribute</span></span>

<span data-ttu-id="c5a65-160">L'attributo seguente fornisce l'intervallo di testo che rappresenta la destinazione di un collegamento in un documento.</span><span class="sxs-lookup"><span data-stu-id="c5a65-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="c5a65-161">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-161">Attribute</span></span> | <span data-ttu-id="c5a65-162">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-163">**Collegamento**</span><span class="sxs-lookup"><span data-stu-id="c5a65-163">**Link**</span></span>  | [<span data-ttu-id="c5a65-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="c5a65-165">Attributi del margine di pagina</span><span class="sxs-lookup"><span data-stu-id="c5a65-165">Page Margin Attributes</span></span>

<span data-ttu-id="c5a65-166">I rettangoli di delimitazione di un intervallo di testo non espongono le coordinate del testo nella pagina.</span><span class="sxs-lookup"><span data-stu-id="c5a65-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="c5a65-167">Tuttavia, un provider può esporre le informazioni sul margine della pagina usando gli attributi di testo seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="c5a65-168">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-168">Attribute</span></span>          | <span data-ttu-id="c5a65-169">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="c5a65-170">**MarginBottom**</span></span>   | [<span data-ttu-id="c5a65-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="c5a65-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="c5a65-172">**MarginLeading**</span></span>  | [<span data-ttu-id="c5a65-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="c5a65-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="c5a65-174">**MarginTop**</span></span>      | [<span data-ttu-id="c5a65-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="c5a65-176">**MarginTrailing**</span></span> | [<span data-ttu-id="c5a65-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="c5a65-178">Attributi di allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-178">Text Alignment Attributes</span></span>

<span data-ttu-id="c5a65-179">Informazioni sull'allineamento del testo, ad esempio rientro, impostazioni di tabulazione e allineamento orizzontale, sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="c5a65-180">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-180">Attribute</span></span>                   | <span data-ttu-id="c5a65-181">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="c5a65-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="c5a65-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="c5a65-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="c5a65-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="c5a65-186">**RientroLeading**</span><span class="sxs-lookup"><span data-stu-id="c5a65-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="c5a65-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-188">**RientroTrailing**</span><span class="sxs-lookup"><span data-stu-id="c5a65-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="c5a65-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="c5a65-190">**Schede**</span><span class="sxs-lookup"><span data-stu-id="c5a65-190">**Tabs**</span></span>                    | [<span data-ttu-id="c5a65-191">**Schede dell'interfaccia \_ utenteAAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="c5a65-192">Attributi di colore del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-192">Text Color Attributes</span></span>

<span data-ttu-id="c5a65-193">I colori del testo in primo piano e di sfondo sono disponibili tramite gli attributi di testo seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="c5a65-194">Entrambi i colori vengono specificati come [**tipo di dati COLORREF.**](/windows/desktop/gdi/colorref)</span><span class="sxs-lookup"><span data-stu-id="c5a65-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="c5a65-195">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-195">Attribute</span></span>           | <span data-ttu-id="c5a65-196">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="c5a65-197">**BackgroundColor**</span></span> | [<span data-ttu-id="c5a65-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="c5a65-199">**ForegroundColor**</span></span> | [<span data-ttu-id="c5a65-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="c5a65-201">Attributi di decorazione del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-201">Text Decoration Attributes</span></span>

<span data-ttu-id="c5a65-202">Le decorazione di testo includono aree come elenchi puntati, sottolineatura e animazioni.</span><span class="sxs-lookup"><span data-stu-id="c5a65-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="c5a65-203">Se il testo include punti elenco o numeri iniziali, il simbolo o il testo usato per il punto elenco o il numero deve essere incluso nel flusso di testo, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="c5a65-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="c5a65-204">Le informazioni sulle decorazione di testo sono disponibili tramite gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="c5a65-205">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-205">Attribute</span></span>              | <span data-ttu-id="c5a65-206">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="c5a65-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="c5a65-209">**Bulletstyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-209">**BulletStyle**</span></span>        | [<span data-ttu-id="c5a65-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="c5a65-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="c5a65-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="c5a65-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="c5a65-213">**OverlineColor**</span></span>      | [<span data-ttu-id="c5a65-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="c5a65-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="c5a65-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="c5a65-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="c5a65-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="c5a65-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="c5a65-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="c5a65-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="c5a65-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="c5a65-225">Attributi di stile del testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-225">Text Style Attributes</span></span>

<span data-ttu-id="c5a65-226">Le informazioni sugli stili di testo sono disponibili anche con gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="c5a65-227">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-227">Attribute</span></span>         | <span data-ttu-id="c5a65-228">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="c5a65-229">**CapStyle**</span></span>      | [<span data-ttu-id="c5a65-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="c5a65-231">**IsHidden**</span></span>      | [<span data-ttu-id="c5a65-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="c5a65-233">**IsItalic**</span></span>      | [<span data-ttu-id="c5a65-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c5a65-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="c5a65-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="c5a65-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="c5a65-237">**IsSuperscript**</span></span> | [<span data-ttu-id="c5a65-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="c5a65-239">**IsSubscript**</span></span>   | [<span data-ttu-id="c5a65-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="c5a65-241">Attributi di interazione e selezione</span><span class="sxs-lookup"><span data-stu-id="c5a65-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="c5a65-242">Le informazioni sulla selezione del testo corrente nell'intervallo e nello stato attivo sono disponibili negli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5a65-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="c5a65-243">Attributo</span><span class="sxs-lookup"><span data-stu-id="c5a65-243">Attribute</span></span>              | <span data-ttu-id="c5a65-244">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c5a65-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a65-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="c5a65-245">**IsActive**</span></span>           | [<span data-ttu-id="c5a65-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="c5a65-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="c5a65-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="c5a65-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="c5a65-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="c5a65-249">**CaretPosition**</span></span>      | [<span data-ttu-id="c5a65-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="c5a65-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="c5a65-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="c5a65-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="c5a65-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="c5a65-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5a65-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c5a65-254">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c5a65-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5a65-255">Informazioni sui pattern Automazione interfaccia utente di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="c5a65-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="c5a65-256">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="c5a65-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="c5a65-257">Uso di controlli basati su testo</span><span class="sxs-lookup"><span data-stu-id="c5a65-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 