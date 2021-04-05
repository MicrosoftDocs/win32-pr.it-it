---
title: Pattern di controllo SpreadsheetItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetItemProvider, incluse informazioni su proprietà e metodi.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SpreadsheetItem
- Automazione interfaccia utente, pattern di controllo SpreadsheetItem
- Automazione interfaccia utente, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implementazione del pattern di controllo SpreadsheetItem di automazione interfaccia utente
- Pattern di controllo SpreadsheetItem
- pattern di controllo, ISpreadsheetItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SpreadsheetItem
- pattern di controllo, SpreadsheetItem
- interfacce, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047232"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="5a692-113">Pattern di controllo SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="5a692-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="5a692-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="5a692-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="5a692-115">Il pattern di controllo **SpreadsheetItem** viene usato per esporre le proprietà di una cella in un foglio di calcolo o in un altro documento basato su griglia.</span><span class="sxs-lookup"><span data-stu-id="5a692-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="5a692-116">Il pattern di controllo **SpreadsheetItem** è strettamente correlato al pattern di controllo [GridItem](uiauto-implementinggriditem.md) . i controlli che implementano il pattern di controllo **SpreadsheetItem** devono anche implementare il pattern di controllo GridItem.</span><span class="sxs-lookup"><span data-stu-id="5a692-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="5a692-117">I controlli possono anche implementare il pattern di controllo [TableItem](uiauto-implementingtableitem.md) , se appropriato.</span><span class="sxs-lookup"><span data-stu-id="5a692-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="5a692-118">Per esempi di controlli che implementano questi pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="5a692-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="5a692-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a692-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5a692-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="5a692-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="5a692-121">Membri obbligatori per **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="5a692-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="5a692-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a692-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="5a692-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="5a692-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="5a692-124">Quando si implementa il pattern di controllo **SpreadsheetItem** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a692-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="5a692-125">Quando si implementano i metodi [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , fare riferimento alla documentazione di [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="5a692-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="5a692-126">Questi metodi restituiscono matrici per consentire ai provider di supportare più annotazioni in una singola cella.</span><span class="sxs-lookup"><span data-stu-id="5a692-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="5a692-127">Alcuni tipi di annotazioni non richiedono un'implementazione completa dell'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="5a692-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="5a692-128">Ad esempio, un indicatore di errore di ortografia semplice può essere rappresentato con [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) che restituisce un identificatore di attributo di testo di [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) restituisce un valore null.</span><span class="sxs-lookup"><span data-stu-id="5a692-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="5a692-129">Membri obbligatori per **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="5a692-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="5a692-130">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="5a692-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="5a692-131">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="5a692-131">Required members</span></span>                                                                         | <span data-ttu-id="5a692-132">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="5a692-132">Member type</span></span> | <span data-ttu-id="5a692-133">Note</span><span class="sxs-lookup"><span data-stu-id="5a692-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a692-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5a692-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="5a692-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a692-135">Property</span></span>    | <span data-ttu-id="5a692-136">L'implementazione di una proprietà della [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) separata è necessaria perché la proprietà [value](value-property.md) di una cella restituisce in genere il valore calcolato della cella.</span><span class="sxs-lookup"><span data-stu-id="5a692-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="5a692-137">La proprietà della **Formula** deve essere **null** se non è impostata alcuna formula.</span><span class="sxs-lookup"><span data-stu-id="5a692-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="5a692-138">**GetAnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="5a692-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="5a692-139">Metodo</span><span class="sxs-lookup"><span data-stu-id="5a692-139">Method</span></span>      | <span data-ttu-id="5a692-140">Restituisce una matrice di provider di elementi che fanno riferimento alle annotazioni collegate a questa cella.</span><span class="sxs-lookup"><span data-stu-id="5a692-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="5a692-141">I puntatori all'interno della matrice possono essere null se un'annotazione non dispone di un provider collegato.</span><span class="sxs-lookup"><span data-stu-id="5a692-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="5a692-142">**GetAnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="5a692-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="5a692-143">Metodo</span><span class="sxs-lookup"><span data-stu-id="5a692-143">Method</span></span>      | <span data-ttu-id="5a692-144">Restituisce una matrice di identificatori del tipo di annotazione che descrivono le annotazioni in questa cella.</span><span class="sxs-lookup"><span data-stu-id="5a692-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="5a692-145">La matrice deve avere le stesse dimensioni della matrice restituita da [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span><span class="sxs-lookup"><span data-stu-id="5a692-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="5a692-146">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="5a692-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a692-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a692-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5a692-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5a692-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5a692-149">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="5a692-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="5a692-150">Pattern di controllo foglio di calcolo</span><span class="sxs-lookup"><span data-stu-id="5a692-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="5a692-151">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="5a692-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="5a692-152">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="5a692-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 