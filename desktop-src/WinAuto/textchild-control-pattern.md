---
title: Pattern di controllo TextChild
description: Introduce le linee guida e le convenzioni per l'implementazione di ITextChildProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo TextChild viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo TextChild
- Automazione interfaccia utente, pattern di controllo TextChild
- Automazione interfaccia utente, ITextChildProvider
- ITextChildProvider
- implementazione di pattern di controllo TextChild di automazione interfaccia utente
- Pattern di controllo TextChild
- pattern di controllo, ITextChildProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente TextChild
- pattern di controllo, TextChild
- interfacce, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729954"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="44b21-114">Pattern di controllo TextChild</span><span class="sxs-lookup"><span data-stu-id="44b21-114">TextChild Control Pattern</span></span>

<span data-ttu-id="44b21-115">Introduce le linee guida e le convenzioni per l'implementazione di [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="44b21-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="44b21-116">Il pattern di controllo **TextChild** viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="44b21-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="44b21-117">Si supponga, ad esempio, che il testo in un documento contenga un'immagine incorporata e un collegamento ipertestuale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="44b21-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![screenshot che mostra il testo che contiene un'immagine incorporata e un collegamento ipertestuale](images/textchild-pattern.png)

<span data-ttu-id="44b21-119">Se si usano gli strumenti di automazione interfaccia utente Microsoft per esaminare l'albero di automazione interfaccia utente per questo contenuto del documento, è possibile che venga visualizzato un elemento documento con un elemento figlio che rappresenta l'immagine e un altro elemento figlio che rappresenta il collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="44b21-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="44b21-120">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="44b21-120">For example:</span></span>

![screenshot che Mostra come controllare la creazione di un esempio di albero degli elementi di automazione interfaccia utente](images/textchild-pattern-tree.png)

<span data-ttu-id="44b21-122">In genere, l'elemento Document nell'esempio precedente supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , ma i due elementi figlio dell'elemento document non lo fanno.</span><span class="sxs-lookup"><span data-stu-id="44b21-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="44b21-123">Se un'applicazione client di automazione interfaccia utente contiene un riferimento all'elemento Image o al collegamento ipertestuale, il client può usare il pattern di controllo **TextChild** come modo pratico per accedere al modello TextControl esposto dall'elemento del documento contenitore.</span><span class="sxs-lookup"><span data-stu-id="44b21-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="44b21-124">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="44b21-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="44b21-125">Quando si implementa l'interfaccia [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="44b21-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="44b21-126">Per la proprietà [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) è necessario specificare l'elemento predecessore più vicino che supporta l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , indipendentemente dal fatto che gli elementi superiori nella catena di predecessore supportino anche **ITextProvider**.</span><span class="sxs-lookup"><span data-stu-id="44b21-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="44b21-127">Un elemento non deve supportare sia l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) che l'interfaccia [ITextChildProvider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="44b21-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="44b21-128">Un elemento che implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) deve essere un elemento figlio o discendente di un elemento che implementa [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span><span class="sxs-lookup"><span data-stu-id="44b21-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="44b21-129">Non è necessario che questo elemento implementi anche il [pattern di controllo Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span><span class="sxs-lookup"><span data-stu-id="44b21-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="44b21-130">La proprietà [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) deve specificare lo stesso intervallo di testo restituito dall'elemento del provider di testo contenitore quando la funzione [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) viene chiamata con l'elemento figlio text come elemento figlio racchiuso.</span><span class="sxs-lookup"><span data-stu-id="44b21-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="44b21-131">Membri obbligatori per **ITextChildProvider**</span><span class="sxs-lookup"><span data-stu-id="44b21-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="44b21-132">Queste proprietà e questi metodi sono necessari per implementare l'interfaccia [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="44b21-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="44b21-133">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="44b21-133">Required members</span></span>                                                     | <span data-ttu-id="44b21-134">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="44b21-134">Member type</span></span> | <span data-ttu-id="44b21-135">Note</span><span class="sxs-lookup"><span data-stu-id="44b21-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="44b21-136">**TextContainer**</span><span class="sxs-lookup"><span data-stu-id="44b21-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="44b21-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44b21-137">Property</span></span>    | <span data-ttu-id="44b21-138">nessuno</span><span class="sxs-lookup"><span data-stu-id="44b21-138">None</span></span>  |
| [<span data-ttu-id="44b21-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="44b21-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="44b21-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44b21-140">Property</span></span>    | <span data-ttu-id="44b21-141">nessuno</span><span class="sxs-lookup"><span data-stu-id="44b21-141">None</span></span>  |



 

<span data-ttu-id="44b21-142">Questo pattern di controllo non è associato a metodi o eventi.</span><span class="sxs-lookup"><span data-stu-id="44b21-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44b21-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44b21-143">Related topics</span></span>

<span data-ttu-id="44b21-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="44b21-144">**Conceptual**</span></span>

- [<span data-ttu-id="44b21-145">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="44b21-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="44b21-146">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="44b21-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="44b21-147">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="44b21-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)