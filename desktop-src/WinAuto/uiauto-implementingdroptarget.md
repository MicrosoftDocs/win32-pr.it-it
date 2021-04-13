---
title: Pattern di controllo DropTarget
description: Fornisce linee guida e convenzioni per l'implementazione del pattern di controllo DropTarget usando IDropTargetProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo DropTarget
- Automazione interfaccia utente, pattern di controllo DropTarget
- Automazione interfaccia utente, IDropTargetProvider
- IDropTargetProvider
- implementazione di pattern di controllo DropTarget di automazione interfaccia utente
- Pattern di controllo DropTarget
- pattern di controllo, IDropTargetProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente DropTarget
- pattern di controllo, DropTarget
- interfacce, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338190"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="a010a-113">Pattern di controllo DropTarget</span><span class="sxs-lookup"><span data-stu-id="a010a-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="a010a-114">Fornisce linee guida e convenzioni per l'implementazione del pattern di controllo **DropTarget** usando [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluse le informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="a010a-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="a010a-115">Il pattern di controllo **DropTarget** viene usato per supportare i controlli che possono essere la destinazione di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="a010a-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a010a-116">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="a010a-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a010a-117">Quando si implementa il pattern di controllo **DropTarget** , usare le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a010a-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a010a-118">Il pattern **DropTarget** deve essere supportato mentre è in corso un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="a010a-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="a010a-119">Può essere supportata anche quando non è in corso un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="a010a-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="a010a-120">La proprietà [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="a010a-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="a010a-121">La proprietà [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) è obbligatoria quando è disponibile più di un effetto di rilascio per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="a010a-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="a010a-122">L'elemento deve generare eventi di modifica di proprietà per le proprietà **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) e **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) quando cambiano.</span><span class="sxs-lookup"><span data-stu-id="a010a-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="a010a-123">Membri obbligatori per **IDropTargetProvider**</span><span class="sxs-lookup"><span data-stu-id="a010a-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="a010a-124">Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .</span><span class="sxs-lookup"><span data-stu-id="a010a-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="a010a-125">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="a010a-125">Required members</span></span>                                                                              | <span data-ttu-id="a010a-126">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="a010a-126">Member type</span></span> | <span data-ttu-id="a010a-127">Note</span><span class="sxs-lookup"><span data-stu-id="a010a-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="a010a-128">**DropTargetEffect**</span><span class="sxs-lookup"><span data-stu-id="a010a-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="a010a-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a010a-129">Property</span></span>    | <span data-ttu-id="a010a-130">nessuno</span><span class="sxs-lookup"><span data-stu-id="a010a-130">None</span></span>                                                                     |
| [<span data-ttu-id="a010a-131">**DropTargetEffects**</span><span class="sxs-lookup"><span data-stu-id="a010a-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="a010a-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a010a-132">Property</span></span>    | <span data-ttu-id="a010a-133">Obbligatorio se la destinazione di rilascio supporta più di un possibile effetto di rilascio.</span><span class="sxs-lookup"><span data-stu-id="a010a-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="a010a-134">**\_DragEnterEventId DropTarget di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="a010a-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="a010a-135">Evento</span><span class="sxs-lookup"><span data-stu-id="a010a-135">Event</span></span>       | <span data-ttu-id="a010a-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="a010a-136">None</span></span>                                                                     |
| [<span data-ttu-id="a010a-137">**\_DragLeaveEventId DropTarget di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="a010a-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="a010a-138">Evento</span><span class="sxs-lookup"><span data-stu-id="a010a-138">Event</span></span>       | <span data-ttu-id="a010a-139">nessuno</span><span class="sxs-lookup"><span data-stu-id="a010a-139">None</span></span>                                                                     |
| [<span data-ttu-id="a010a-140">**\_DroppedEventId DropTarget di UIA \_**</span><span class="sxs-lookup"><span data-stu-id="a010a-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="a010a-141">Evento</span><span class="sxs-lookup"><span data-stu-id="a010a-141">Event</span></span>       | <span data-ttu-id="a010a-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="a010a-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a010a-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a010a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a010a-144">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="a010a-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a010a-145">Trascinare il pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="a010a-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="a010a-146">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a010a-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a010a-147">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a010a-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="a010a-148">Supporto di automazione interfaccia utente per il trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="a010a-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 