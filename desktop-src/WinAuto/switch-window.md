---
title: Finestra switch (riferimento all'elemento dell'interfaccia utente MSAA)
description: La finestra di commutazione viene visualizzata ogni volta che un utente preme ALT + TAB per passare a un'altra applicazione. La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714128"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="814d0-104">Finestra switch (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="814d0-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="814d0-105">La finestra di commutazione viene visualizzata ogni volta che un utente preme ALT + TAB per passare a un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="814d0-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="814d0-106">La finestra switch contiene un'icona per ogni applicazione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="814d0-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="814d0-107">Il nome della classe di finestra per la finestra switch è " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="814d0-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="814d0-108">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="814d0-108">IAccessible Methods</span></span>

<span data-ttu-id="814d0-109">La finestra switch supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="814d0-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="814d0-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="814d0-110">Method</span></span>                                                                    | <span data-ttu-id="814d0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="814d0-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="814d0-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="814d0-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="814d0-113">L'oggetto finestra switch non dispone di una proprietà **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="814d0-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="814d0-114">Il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per ogni elemento nella finestra switch attiva l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="814d0-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="814d0-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="814d0-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="814d0-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="814d0-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="814d0-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="814d0-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="814d0-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="814d0-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="814d0-119">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="814d0-119">IAccessible Properties</span></span>

<span data-ttu-id="814d0-120">La finestra switch supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="814d0-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="814d0-121">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="814d0-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="814d0-122">La proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="814d0-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="814d0-123">**ottenere \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="814d0-123">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="814d0-124">L'oggetto finestra switch non dispone di una proprietà **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="814d0-124">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="814d0-125">La proprietà **DefaultAction** per ogni elemento nella finestra switch è "switch".</span><span class="sxs-lookup"><span data-stu-id="814d0-125">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="814d0-126">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="814d0-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="814d0-127">L'oggetto padre della finestra switch non può ricevere lo stato attivo; solo i singoli figli possono ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="814d0-127">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="814d0-128">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="814d0-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="814d0-129">L'oggetto finestra switch non dispone di una proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="814d0-129">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="814d0-130">La proprietà **Name** per ogni icona dell'applicazione nella finestra switch corrisponde al nome dell'applicazione visualizzato.</span><span class="sxs-lookup"><span data-stu-id="814d0-130">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="814d0-131">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="814d0-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="814d0-132">L'oggetto finestra switch ha una proprietà **Role** di "window \[ 32771 \] ".</span><span class="sxs-lookup"><span data-stu-id="814d0-132">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="814d0-133">Inoltre, ogni icona dell'applicazione nella finestra del commutire presenta il ruolo proprietà del ruolo proprietà **del ruolo.** [**\_ \_**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="814d0-133">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="814d0-134">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="814d0-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="814d0-135">L'oggetto finestra switch non supporta la proprietà **state** .</span><span class="sxs-lookup"><span data-stu-id="814d0-135">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="814d0-136">Il valore **dello stato** per gli elementi della visualizzazione elenco è [**stato \_ \_ attivabile dal sistema di stato**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="814d0-136">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="814d0-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="814d0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="814d0-138">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="814d0-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




