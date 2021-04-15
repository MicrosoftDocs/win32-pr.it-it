---
title: Finestra desktop (riferimento all'elemento dell'interfaccia utente MSAA)
description: Nella finestra del desktop viene visualizzata la visualizzazione elenco dei desktop (che contiene icone come Computer locale) e la barra delle applicazioni che contiene il pulsante Avvia.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395491"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="f3b77-103">Finestra desktop (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="f3b77-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="f3b77-104">Nella finestra del desktop viene visualizzata la visualizzazione elenco dei desktop (che contiene icone come Computer locale) e la barra delle applicazioni che contiene il pulsante **Avvia** .</span><span class="sxs-lookup"><span data-stu-id="f3b77-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="f3b77-105">Questo oggetto viene raramente sottoposto a query dai client perché la visualizzazione elenco e la barra delle applicazioni coprono l'intero desktop.</span><span class="sxs-lookup"><span data-stu-id="f3b77-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="f3b77-106">L'oggetto desktop viene recuperato al momento dell'accesso, prima che la shell del sistema operativo visualizzi la visualizzazione elenco e la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3b77-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="f3b77-107">In alcuni casi, il desktop viene ottenuto quando ci si sposta da altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="f3b77-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="f3b77-108">Il nome della classe di finestra per la finestra del desktop è " \# 32769".</span><span class="sxs-lookup"><span data-stu-id="f3b77-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="f3b77-109">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="f3b77-109">IAccessible Methods</span></span>

<span data-ttu-id="f3b77-110">La finestra desktop supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f3b77-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="f3b77-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="f3b77-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="f3b77-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="f3b77-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="f3b77-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="f3b77-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="f3b77-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="f3b77-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="f3b77-115">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="f3b77-115">IAccessible Properties</span></span>

<span data-ttu-id="f3b77-116">La finestra desktop supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3b77-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="f3b77-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3b77-117">Property</span></span>                                                                 | <span data-ttu-id="f3b77-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3b77-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b77-119">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="f3b77-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f3b77-120">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="f3b77-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f3b77-121">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f3b77-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="f3b77-122">La proprietà Name è "desktop".</span><span class="sxs-lookup"><span data-stu-id="f3b77-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f3b77-123">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="f3b77-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="f3b77-124">La proprietà **Role** è [**un \_ \_ client del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f3b77-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f3b77-125">**ottenere \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="f3b77-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f3b77-126">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="f3b77-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="f3b77-127">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="f3b77-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f3b77-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3b77-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b77-129">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f3b77-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





