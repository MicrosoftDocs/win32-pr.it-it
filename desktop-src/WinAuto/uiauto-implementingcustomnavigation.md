---
title: Pattern di controllo CustomNavigation
description: Vengono descritte le linee guida e le convenzioni per l'implementazione dell'interfaccia ICustomNavigationProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221377"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="8de9c-103">Pattern di controllo CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="8de9c-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="8de9c-104">Vengono descritte le linee guida e le convenzioni per l'implementazione dell'interfaccia **ICustomNavigationProvider** , incluse informazioni su proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="8de9c-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="8de9c-105">Il pattern di controllo **CustomNavigation** viene usato per abilitare la navigazione personalizzata tra i controlli in strutture di tipo gerarchia, ad esempio voci di elenco, elenchi puntati, elenchi numerati e intestazioni.</span><span class="sxs-lookup"><span data-stu-id="8de9c-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="8de9c-106">Questo consente ai provider di descrivere le strutture o definire le relazioni navigabili usando solo l'elemento e non solo il controllo contenitore.</span><span class="sxs-lookup"><span data-stu-id="8de9c-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="8de9c-107">Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="8de9c-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="8de9c-108">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8de9c-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8de9c-109">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8de9c-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8de9c-110">Membri obbligatori per **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="8de9c-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="8de9c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8de9c-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8de9c-112">Linee guida e convenzioni di implementazione</span><span class="sxs-lookup"><span data-stu-id="8de9c-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8de9c-113">Quando si implementa il provider **CustomNavigation** , tenere presenti le linee guida e le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8de9c-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8de9c-114">I valori delle proprietà per **PositionInSet**, **SizeOfSet** e **Level** sono valori integer in base uno.</span><span class="sxs-lookup"><span data-stu-id="8de9c-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="8de9c-115">**ICustomNavigationProvider** non fornisce la manipolazione attiva del controllo, ad esempio lo sviluppo di posizioni, l'aggiunta e la rimozione di elementi o la promozione e il abbassamento dei livelli.</span><span class="sxs-lookup"><span data-stu-id="8de9c-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="8de9c-116">I controlli che implementano **ICustomNavigationProvider** in genere hanno una struttura gerarchica, ma possono ignorare i livelli usando il metodo **Navigate** .</span><span class="sxs-lookup"><span data-stu-id="8de9c-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="8de9c-117">Le proprietà **PositionInSet**, **SizeOfSet** e **Level** sono necessarie per il modello.</span><span class="sxs-lookup"><span data-stu-id="8de9c-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="8de9c-118">Membri obbligatori per **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="8de9c-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="8de9c-119">Le proprietà seguenti sono necessarie per l'implementazione dell'interfaccia **ICustomNavigationProvider** .</span><span class="sxs-lookup"><span data-stu-id="8de9c-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="8de9c-120">Membri obbligatori</span><span class="sxs-lookup"><span data-stu-id="8de9c-120">Required members</span></span>                                                                  | <span data-ttu-id="8de9c-121">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="8de9c-121">Member type</span></span> | <span data-ttu-id="8de9c-122">Note</span><span class="sxs-lookup"><span data-stu-id="8de9c-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8de9c-123">**CachedLevel**</span><span class="sxs-lookup"><span data-stu-id="8de9c-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="8de9c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-124">Property</span></span>    | <span data-ttu-id="8de9c-125">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-126">**CachedPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="8de9c-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="8de9c-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-127">Property</span></span>    | <span data-ttu-id="8de9c-128">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-129">**CachedSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="8de9c-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="8de9c-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-130">Property</span></span>    | <span data-ttu-id="8de9c-131">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-132">**CurrentLevel**</span><span class="sxs-lookup"><span data-stu-id="8de9c-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="8de9c-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-133">Property</span></span>    | <span data-ttu-id="8de9c-134">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-135">**CurrentPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="8de9c-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="8de9c-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-136">Property</span></span>    | <span data-ttu-id="8de9c-137">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-138">**CurrentSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="8de9c-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="8de9c-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8de9c-139">Property</span></span>    | <span data-ttu-id="8de9c-140">Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="8de9c-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="8de9c-141">**Navigare**</span><span class="sxs-lookup"><span data-stu-id="8de9c-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="8de9c-142">Metodo</span><span class="sxs-lookup"><span data-stu-id="8de9c-142">Method</span></span>      | <span data-ttu-id="8de9c-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="8de9c-143">None</span></span>                                                                                |



 

<span data-ttu-id="8de9c-144">Questo pattern di controllo non è associato a metodi o eventi.</span><span class="sxs-lookup"><span data-stu-id="8de9c-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de9c-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8de9c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de9c-146">Tipi di controllo e i pattern di controllo supportati</span><span class="sxs-lookup"><span data-stu-id="8de9c-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8de9c-147">ListItem (controllo)</span><span class="sxs-lookup"><span data-stu-id="8de9c-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="8de9c-148">Controllo HeaderItem</span><span class="sxs-lookup"><span data-stu-id="8de9c-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="8de9c-149">DataItem (controllo)</span><span class="sxs-lookup"><span data-stu-id="8de9c-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="8de9c-150">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="8de9c-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




