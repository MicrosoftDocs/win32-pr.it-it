---
title: Pattern di controllo Transform
description: Descrive le linee guida e le convenzioni per l'implementazione di ITransformProvider e ITransformProvider2, incluse informazioni su proprietà e metodi.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Transform
- Automazione interfaccia utente, pattern di controllo Transform
- Automazione interfaccia utente, ITransformProvider
- ITransformProvider
- implementazione di pattern di controllo Transform di automazione interfaccia utente
- Pattern di controllo Transform
- pattern di controllo, ITransformProvider
- pattern di controllo, implementazione della trasformazione automazione interfaccia utente
- pattern di controllo, trasformazione
- interfacce, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516959"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="1f49e-113">Pattern di controllo Transform</span><span class="sxs-lookup"><span data-stu-id="1f49e-113">Transform Control Pattern</span></span>

<span data-ttu-id="1f49e-114">Descrive le linee guida e le convenzioni per l'implementazione di [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) e [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="1f49e-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="1f49e-115">Il pattern di controllo Transform viene usato per supportare i controlli che possono essere spostati, ridimensionati o ruotati in uno spazio bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="1f49e-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="1f49e-116">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="1f49e-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="1f49e-117">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f49e-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1f49e-118">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="1f49e-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="1f49e-119">Membri obbligatori per **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="1f49e-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="1f49e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f49e-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="1f49e-121">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="1f49e-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="1f49e-122">Quando si implementa il pattern di controllo **Transform** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f49e-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="1f49e-123">Il supporto per questo pattern di controllo non è limitato agli oggetti sul desktop.</span><span class="sxs-lookup"><span data-stu-id="1f49e-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="1f49e-124">Questo pattern di controllo deve essere supportato dagli elementi figlio di un oggetto contenitore se gli elementi figlio possono essere spostati, ridimensionati o ruotati all'interno dei limiti del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1f49e-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="1f49e-125">Un oggetto non può essere spostato, ridimensionato o ruotato in modo che la posizione risultante sullo schermo potrebbe essere completamente esterna alle coordinate del relativo contenitore e pertanto inaccessibile per la tastiera o il mouse (ad esempio, quando una finestra di primo livello viene spostata fuori schermo o un oggetto figlio viene spostato fuori dai limiti del riquadro di visualizzazione del contenitore).</span><span class="sxs-lookup"><span data-stu-id="1f49e-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="1f49e-126">In questi casi, l'oggetto viene posizionato il più vicino possibile alle coordinate richieste dello schermo rispetto alle coordinate in alto e a sinistra entro i limiti del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1f49e-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="1f49e-127">Per sistemi con più monitor, se un oggetto viene spostato, ridimensionato o ruotato completamente al di fuori delle coordinate combinate dello schermo desktop, l'oggetto viene posizionato sul monitor principale il più vicino possibile alle coordinate richieste.</span><span class="sxs-lookup"><span data-stu-id="1f49e-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="1f49e-128">Tutti i parametri e i valori delle proprietà sono assoluti e indipendenti dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="1f49e-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="1f49e-129">Membri obbligatori per **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="1f49e-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="1f49e-130">Per l'implementazione dell'interfaccia [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) sono necessari i metodi e le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f49e-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="1f49e-131">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="1f49e-131">Required members</span></span>                                         | <span data-ttu-id="1f49e-132">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="1f49e-132">Member type</span></span> | <span data-ttu-id="1f49e-133">Note</span><span class="sxs-lookup"><span data-stu-id="1f49e-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1f49e-134">**CanMove**</span><span class="sxs-lookup"><span data-stu-id="1f49e-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="1f49e-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-135">Property</span></span>    | <span data-ttu-id="1f49e-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-136">None</span></span>  |
| [<span data-ttu-id="1f49e-137">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="1f49e-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="1f49e-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-138">Property</span></span>    | <span data-ttu-id="1f49e-139">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-139">None</span></span>  |
| [<span data-ttu-id="1f49e-140">**CanRotate**</span><span class="sxs-lookup"><span data-stu-id="1f49e-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="1f49e-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-141">Property</span></span>    | <span data-ttu-id="1f49e-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-142">None</span></span>  |
| [<span data-ttu-id="1f49e-143">**Spostare**</span><span class="sxs-lookup"><span data-stu-id="1f49e-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="1f49e-144">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f49e-144">Method</span></span>      | <span data-ttu-id="1f49e-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-145">None</span></span>  |
| [<span data-ttu-id="1f49e-146">**Ridimensionamento**</span><span class="sxs-lookup"><span data-stu-id="1f49e-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="1f49e-147">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f49e-147">Method</span></span>      | <span data-ttu-id="1f49e-148">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-148">None</span></span>  |
| [<span data-ttu-id="1f49e-149">**Ruota**</span><span class="sxs-lookup"><span data-stu-id="1f49e-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="1f49e-150">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f49e-150">Method</span></span>      | <span data-ttu-id="1f49e-151">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-151">None</span></span>  |



 

<span data-ttu-id="1f49e-152">Per l'implementazione dell'interfaccia [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) sono necessari i metodi e le proprietà aggiuntive seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f49e-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="1f49e-153">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="1f49e-153">Required members</span></span>                                              | <span data-ttu-id="1f49e-154">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="1f49e-154">Member type</span></span> | <span data-ttu-id="1f49e-155">Note</span><span class="sxs-lookup"><span data-stu-id="1f49e-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1f49e-156">**CanZoom**</span><span class="sxs-lookup"><span data-stu-id="1f49e-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="1f49e-157">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-157">Property</span></span>    | <span data-ttu-id="1f49e-158">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-158">None</span></span>  |
| [<span data-ttu-id="1f49e-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="1f49e-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="1f49e-160">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f49e-160">Method</span></span>      | <span data-ttu-id="1f49e-161">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-161">None</span></span>  |
| [<span data-ttu-id="1f49e-162">**ZoomByUnit**</span><span class="sxs-lookup"><span data-stu-id="1f49e-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="1f49e-163">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f49e-163">Method</span></span>      | <span data-ttu-id="1f49e-164">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-164">None</span></span>  |
| [<span data-ttu-id="1f49e-165">**ZoomLevel**</span><span class="sxs-lookup"><span data-stu-id="1f49e-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="1f49e-166">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-166">Property</span></span>    | <span data-ttu-id="1f49e-167">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-167">None</span></span>  |
| [<span data-ttu-id="1f49e-168">**ZoomMaximum**</span><span class="sxs-lookup"><span data-stu-id="1f49e-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="1f49e-169">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-169">Property</span></span>    | <span data-ttu-id="1f49e-170">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-170">None</span></span>  |
| [<span data-ttu-id="1f49e-171">**ZoomMinimum**</span><span class="sxs-lookup"><span data-stu-id="1f49e-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="1f49e-172">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f49e-172">Property</span></span>    | <span data-ttu-id="1f49e-173">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f49e-173">None</span></span>  |



 

<span data-ttu-id="1f49e-174">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="1f49e-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f49e-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f49e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f49e-176">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="1f49e-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="1f49e-177">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1f49e-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="1f49e-178">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1f49e-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 