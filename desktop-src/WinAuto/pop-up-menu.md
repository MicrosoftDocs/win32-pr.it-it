---
title: Menu a comparsa (riferimento all'elemento dell'interfaccia utente MSAA)
description: Un menu a comparsa Visualizza un elenco di comandi di menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856497"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="7b64f-103">Menu a comparsa (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="7b64f-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="7b64f-104">Questo argomento descrive gli oggetti **menu popup** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="7b64f-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="7b64f-105">La creazione di oggetti **menu popup** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="7b64f-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="7b64f-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="7b64f-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="7b64f-107">Un menu a comparsa Visualizza un elenco di comandi di menu.</span><span class="sxs-lookup"><span data-stu-id="7b64f-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="7b64f-108">Microsoft Active Accessibility crea un oggetto popup del menu quando viene aperta una voce di menu in una barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="7b64f-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="7b64f-109">Microsoft Active Accessibility crea anche oggetti popup del menu per i menu di scelta rapida, che vengono visualizzati quando l'utente fa clic con il pulsante destro del mouse su un elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7b64f-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="7b64f-110">Il nome della classe della finestra per un menu di scelta rapida è " \# 32768".</span><span class="sxs-lookup"><span data-stu-id="7b64f-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="7b64f-111">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="7b64f-111">IAccessible Methods</span></span>

<span data-ttu-id="7b64f-112">Un menu popup supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="7b64f-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7b64f-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7b64f-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7b64f-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7b64f-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="7b64f-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7b64f-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="7b64f-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="7b64f-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="7b64f-117">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="7b64f-117">IAccessible Properties</span></span>

<span data-ttu-id="7b64f-118">Un menu popup supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b64f-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="7b64f-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b64f-119">Property</span></span>                                                                 | <span data-ttu-id="7b64f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b64f-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b64f-121">**ottenere \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="7b64f-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="7b64f-122">Recupera il [**IDispatch**](idispatch-interface.md) per la voce di menu specificata.</span><span class="sxs-lookup"><span data-stu-id="7b64f-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="7b64f-123">Gli ID figlio per le voci di menu sono numerati in sequenza dall'alto verso il basso iniziando da uno.</span><span class="sxs-lookup"><span data-stu-id="7b64f-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7b64f-124">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="7b64f-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="7b64f-125">La proprietà **childCount** è il numero di voci di menu nel menu, inclusi i separatori di menu.</span><span class="sxs-lookup"><span data-stu-id="7b64f-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7b64f-126">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="7b64f-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7b64f-127">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="7b64f-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="7b64f-128">La proprietà **Name** di un menu di scelta rapida corrisponde al nome del menu.</span><span class="sxs-lookup"><span data-stu-id="7b64f-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="7b64f-129">La proprietà **Name** di un menu di scelta rapida è "context".</span><span class="sxs-lookup"><span data-stu-id="7b64f-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7b64f-130">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="7b64f-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="7b64f-131">La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il menu di scelta rapida e ha la stessa proprietà **Name** e il nome della classe di finestra del menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="7b64f-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7b64f-132">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="7b64f-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="7b64f-133">La proprietà **Role** è [**\_ \_ MENUPOPUP del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b64f-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7b64f-134">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="7b64f-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="7b64f-135">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="7b64f-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="7b64f-136">Note</span><span class="sxs-lookup"><span data-stu-id="7b64f-136">Notes</span></span>

-   <span data-ttu-id="7b64f-137">Gli oggetti menu popup non attivano gli eventi di [**\_ \_ creazione**](event-constants.md) di oggetti evento e [**\_ \_ eliminazione di oggetti evento**](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="7b64f-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="7b64f-138">I menu a più colonne non supportano i flag [**NAVDIR \_ Left**](navigation-constants.md) o [**NAVDIR \_ right**](navigation-constants.md) del metodo [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .</span><span class="sxs-lookup"><span data-stu-id="7b64f-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="7b64f-139">Gli eventi [**\_ \_ MENUPOPUPSTART**](event-constants.md) e [**\_ \_ MENUPOPUPEND**](event-constants.md) del sistema eventi non vengono inviati in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="7b64f-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="7b64f-140">Si tratta di un problema noto che viene risolto.</span><span class="sxs-lookup"><span data-stu-id="7b64f-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b64f-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b64f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b64f-142">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="7b64f-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="7b64f-143">**Barra dei menu**</span><span class="sxs-lookup"><span data-stu-id="7b64f-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="7b64f-144">**Voce di menu**</span><span class="sxs-lookup"><span data-stu-id="7b64f-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





