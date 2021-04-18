---
title: Pattern di controllo RangeValue
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IRangeValueProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo RangeValue viene usato per supportare i controlli che possono essere impostati su un valore compreso in un intervallo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo RangeValue
- Automazione interfaccia utente, pattern di controllo RangeValue
- Automazione interfaccia utente, IRangeValueProvider
- IRangeValueProvider
- implementazione di pattern di controllo RangeValue di automazione interfaccia utente
- Pattern di controllo RangeValue
- pattern di controllo, IRangeValueProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente RangeValue
- pattern di controllo, RangeValue
- interfacce, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298469"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="7acf5-114">Pattern di controllo RangeValue</span><span class="sxs-lookup"><span data-stu-id="7acf5-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="7acf5-115">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="7acf5-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="7acf5-116">Il pattern di controllo **RangeValue** viene usato per supportare i controlli che possono essere impostati su un valore compreso in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="7acf5-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="7acf5-117">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="7acf5-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="7acf5-118">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7acf5-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7acf5-119">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="7acf5-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="7acf5-120">Membri obbligatori per **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="7acf5-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="7acf5-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7acf5-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="7acf5-122">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="7acf5-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="7acf5-123">Quando si implementa il pattern di controllo **RangeValue** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7acf5-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="7acf5-124">I controlli consentono la ricalibrazione delle relative proprietà supportate in base alle preferenze utente o alle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="7acf5-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="7acf5-125">Un esempio di questo è un controllo termometro che può essere impostato per visualizzare la temperatura in gradi Fahrenheit o Celsius.</span><span class="sxs-lookup"><span data-stu-id="7acf5-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="7acf5-126">I controlli che dispongono di valori di intervallo ambigui, ad esempio le barre di avanzamento o i dispositivi di scorrimento, devono avere questi valori normalizzati.</span><span class="sxs-lookup"><span data-stu-id="7acf5-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="7acf5-127">Membri obbligatori per **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="7acf5-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="7acf5-128">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="7acf5-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="7acf5-129">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="7acf5-129">Required members</span></span>                                              | <span data-ttu-id="7acf5-130">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="7acf5-130">Member type</span></span> | <span data-ttu-id="7acf5-131">Note</span><span class="sxs-lookup"><span data-stu-id="7acf5-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="7acf5-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="7acf5-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="7acf5-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-133">Property</span></span>    | <span data-ttu-id="7acf5-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-134">None</span></span>  |
| [<span data-ttu-id="7acf5-135">**Valore**</span><span class="sxs-lookup"><span data-stu-id="7acf5-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="7acf5-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-136">Property</span></span>    | <span data-ttu-id="7acf5-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-137">None</span></span>  |
| [<span data-ttu-id="7acf5-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="7acf5-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="7acf5-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-139">Property</span></span>    | <span data-ttu-id="7acf5-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-140">None</span></span>  |
| [<span data-ttu-id="7acf5-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="7acf5-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="7acf5-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-142">Property</span></span>    | <span data-ttu-id="7acf5-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-143">None</span></span>  |
| [<span data-ttu-id="7acf5-144">**Massimo**</span><span class="sxs-lookup"><span data-stu-id="7acf5-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="7acf5-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-145">Property</span></span>    | <span data-ttu-id="7acf5-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-146">None</span></span>  |
| [<span data-ttu-id="7acf5-147">**Minima**</span><span class="sxs-lookup"><span data-stu-id="7acf5-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="7acf5-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acf5-148">Property</span></span>    | <span data-ttu-id="7acf5-149">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-149">None</span></span>  |
| [<span data-ttu-id="7acf5-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="7acf5-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="7acf5-151">Metodo</span><span class="sxs-lookup"><span data-stu-id="7acf5-151">Method</span></span>      | <span data-ttu-id="7acf5-152">nessuno</span><span class="sxs-lookup"><span data-stu-id="7acf5-152">None</span></span>  |



 

<span data-ttu-id="7acf5-153">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="7acf5-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7acf5-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7acf5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7acf5-155">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="7acf5-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="7acf5-156">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7acf5-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="7acf5-157">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7acf5-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




