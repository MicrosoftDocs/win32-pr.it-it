---
title: Finestra Switch (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: La finestra switch viene visualizzata ogni volta che un utente preme ALT+TAB per passare a un'applicazione diversa. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443982"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="04ce8-104">Finestra Switch (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="04ce8-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="04ce8-105">La finestra switch viene visualizzata ogni volta che un utente preme ALT+TAB per passare a un'applicazione diversa.</span><span class="sxs-lookup"><span data-stu-id="04ce8-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="04ce8-106">La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="04ce8-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="04ce8-107">Il nome della classe della finestra per la finestra switch è \# "32771".</span><span class="sxs-lookup"><span data-stu-id="04ce8-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="04ce8-108">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="04ce8-108">IAccessible Methods</span></span>

<span data-ttu-id="04ce8-109">La finestra switch supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="04ce8-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="04ce8-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="04ce8-110">Method</span></span>                                                                    | <span data-ttu-id="04ce8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="04ce8-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04ce8-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="04ce8-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="04ce8-113">L'oggetto finestra del commutatore stesso non ha una **proprietà DefaultAction.**</span><span class="sxs-lookup"><span data-stu-id="04ce8-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="04ce8-114">Il [**metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per ogni elemento nella finestra switch attiva l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="04ce8-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="04ce8-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="04ce8-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="04ce8-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="04ce8-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="04ce8-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="04ce8-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="04ce8-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="04ce8-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="04ce8-119">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="04ce8-119">IAccessible Properties</span></span>

<span data-ttu-id="04ce8-120">La finestra switch supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="04ce8-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|      <span data-ttu-id="04ce8-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04ce8-121">Property</span></span>                                                                          |      <span data-ttu-id="04ce8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04ce8-122">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04ce8-123">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="04ce8-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="04ce8-124">La **proprietà ChildCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="04ce8-124">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="04ce8-125">**get \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="04ce8-125">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="04ce8-126">L'oggetto finestra del commutatore stesso non ha una **proprietà DefaultAction.**</span><span class="sxs-lookup"><span data-stu-id="04ce8-126">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="04ce8-127">La **proprietà DefaultAction** per ogni elemento nella finestra switch è "Switch".</span><span class="sxs-lookup"><span data-stu-id="04ce8-127">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="04ce8-128">**get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="04ce8-128">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="04ce8-129">L'oggetto padre della finestra di commutazione non può ricevere lo stato attivo. solo i singoli elementi figlio possono ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="04ce8-129">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="04ce8-130">**get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="04ce8-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="04ce8-131">L'oggetto finestra del commutatore non ha una **proprietà** Name.</span><span class="sxs-lookup"><span data-stu-id="04ce8-131">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="04ce8-132">La **proprietà Name** per ogni icona dell'applicazione nella finestra switch corrisponde al nome dell'applicazione visualizzato.</span><span class="sxs-lookup"><span data-stu-id="04ce8-132">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="04ce8-133">**get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="04ce8-133">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="04ce8-134">L'oggetto finestra del commutatore stesso ha una **proprietà Role** "window \[ 32771". \]</span><span class="sxs-lookup"><span data-stu-id="04ce8-134">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="04ce8-135">Inoltre, ogni icona dell'applicazione nella finestra switch ha la **proprietà Role** [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="04ce8-135">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="04ce8-136">**get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="04ce8-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="04ce8-137">L'oggetto finestra del commutatore non supporta la **proprietà** State.</span><span class="sxs-lookup"><span data-stu-id="04ce8-137">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="04ce8-138">Il **valore State** per gli elementi della visualizzazione elenco è STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="04ce8-138">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="04ce8-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04ce8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04ce8-140">Interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="04ce8-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




