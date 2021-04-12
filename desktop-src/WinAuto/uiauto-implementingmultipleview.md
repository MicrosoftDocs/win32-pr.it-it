---
title: Pattern di controllo MultipleView
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IMultipleViewProvider, incluse informazioni su proprietà e metodi.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo MultipleView
- Automazione interfaccia utente, pattern di controllo MultipleView
- Automazione interfaccia utente, IMultipleViewProvider
- IMultipleViewProvider
- implementazione di pattern di controllo MultipleView di automazione interfaccia utente
- Pattern di controllo MultipleView
- pattern di controllo, IMultipleViewProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente MultipleView
- pattern di controllo, MultipleView
- interfacce, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396270"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="f2586-113">Pattern di controllo MultipleView</span><span class="sxs-lookup"><span data-stu-id="f2586-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="f2586-114">Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="f2586-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="f2586-115">Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f2586-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="f2586-116">Il pattern di controllo **MultipleView** viene usato per supportare i controlli che forniscono e sono in grado di passare tra più rappresentazioni delle stesse informazioni o dello stesso set di controlli figlio.</span><span class="sxs-lookup"><span data-stu-id="f2586-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="f2586-117">Esempi di controlli che possono presentare più viste includono la visualizzazione elenco, che può mostrare il contenuto come anteprime, riquadri, icone o dettagli), grafici di Microsoft Excel (a torta, a linee, a barre, valore della cella con una formula), documenti di Microsoft Word (normale, layout Web, layout di stampa, layout di lettura, struttura), calendario di Microsoft Outlook (anno, mese, settimana, giorno) e interfacce di Media Player di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f2586-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="f2586-118">Le visualizzazioni supportate sono determinate dallo sviluppatore del controllo e sono specifiche di ogni controllo.</span><span class="sxs-lookup"><span data-stu-id="f2586-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="f2586-119">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2586-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f2586-120">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="f2586-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f2586-121">Membri obbligatori per **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="f2586-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="f2586-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2586-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f2586-123">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="f2586-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f2586-124">Quando si implementa il pattern di controllo **MultipleView** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2586-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f2586-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) deve essere implementato anche in un contenitore che gestisce la visualizzazione corrente se è diverso da un controllo che fornisce la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f2586-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="f2586-126">Ad esempio, Esplora risorse contiene un controllo elenco per il contenuto della cartella corrente, mentre la visualizzazione per il controllo viene gestita dall'applicazione Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="f2586-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="f2586-127">Un controllo in grado di ordinare il relativo contenuto non supporta più visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f2586-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="f2586-128">La raccolta di visualizzazioni deve essere identica tra istanze.</span><span class="sxs-lookup"><span data-stu-id="f2586-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="f2586-129">I nomi delle visualizzazioni devono essere adatti per l'uso in sintesi vocale, Braille e altre applicazioni leggibili.</span><span class="sxs-lookup"><span data-stu-id="f2586-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="f2586-130">Membri obbligatori per **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="f2586-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="f2586-131">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .</span><span class="sxs-lookup"><span data-stu-id="f2586-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="f2586-132">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="f2586-132">Required members</span></span>                                                            | <span data-ttu-id="f2586-133">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="f2586-133">Member type</span></span> | <span data-ttu-id="f2586-134">Note</span><span class="sxs-lookup"><span data-stu-id="f2586-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f2586-135">**CurrentView**</span><span class="sxs-lookup"><span data-stu-id="f2586-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="f2586-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2586-136">Property</span></span>    | <span data-ttu-id="f2586-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="f2586-137">None</span></span>  |
| [<span data-ttu-id="f2586-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="f2586-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="f2586-139">Metodo</span><span class="sxs-lookup"><span data-stu-id="f2586-139">Method</span></span>      | <span data-ttu-id="f2586-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="f2586-140">None</span></span>  |
| [<span data-ttu-id="f2586-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="f2586-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="f2586-142">Metodo</span><span class="sxs-lookup"><span data-stu-id="f2586-142">Method</span></span>      | <span data-ttu-id="f2586-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="f2586-143">None</span></span>  |
| [<span data-ttu-id="f2586-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="f2586-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="f2586-145">Metodo</span><span class="sxs-lookup"><span data-stu-id="f2586-145">Method</span></span>      | <span data-ttu-id="f2586-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="f2586-146">None</span></span>  |



 

<span data-ttu-id="f2586-147">Questo pattern di controllo non è associato a eventi.</span><span class="sxs-lookup"><span data-stu-id="f2586-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2586-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2586-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2586-149">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="f2586-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f2586-150">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f2586-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f2586-151">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f2586-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="f2586-152">Pattern di controllo ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="f2586-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




