---
title: Controllo barra di stato (riferimento all'elemento MSAA UI)
description: Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332231"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="e1e91-103">Controllo barra di stato (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="e1e91-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="e1e91-104">Questo argomento descrive gli oggetti **controllo barra di stato** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="e1e91-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="e1e91-105">La creazione di oggetti **controllo barra di stato** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="e1e91-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="e1e91-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="e1e91-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="e1e91-107">Le barre di stato visualizzano le informazioni sullo stato in una finestra orizzontale nella parte inferiore di una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e1e91-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="e1e91-108">Le barre di stato sono spesso divise in parti, denominate riquadri e ogni riquadro Visualizza informazioni sullo stato diverse.</span><span class="sxs-lookup"><span data-stu-id="e1e91-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="e1e91-109">Inoltre, le barre di stato possono contenere oggetti di tipi diversi, inclusi pulsanti e barre di stato.</span><span class="sxs-lookup"><span data-stu-id="e1e91-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="e1e91-110">Il nome della classe della finestra per un controllo barra di stato è STATUSCLASSNAME, definito come "msctls \_ statusbar32" in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="e1e91-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="e1e91-111">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="e1e91-111">IAccessible Methods</span></span>

<span data-ttu-id="e1e91-112">Le barre di stato supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="e1e91-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="e1e91-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="e1e91-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="e1e91-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="e1e91-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="e1e91-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="e1e91-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="e1e91-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="e1e91-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="e1e91-117">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="e1e91-117">IAccessible Properties</span></span>

<span data-ttu-id="e1e91-118">Le barre di stato supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1e91-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="e1e91-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1e91-119">Property</span></span>                                                                 | <span data-ttu-id="e1e91-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1e91-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1e91-121">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="e1e91-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="e1e91-122">La proprietà **childCount** è il numero di riquadri nella barra di stato.</span><span class="sxs-lookup"><span data-stu-id="e1e91-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e1e91-123">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="e1e91-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="e1e91-124">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="e1e91-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="e1e91-125">L'oggetto barra di stato non dispone di una proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="e1e91-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="e1e91-126">La proprietà **Name** di ogni riquadro nella barra di stato corrisponde al testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e1e91-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="e1e91-127">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="e1e91-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="e1e91-128">La proprietà **Parent** dell'oggetto barra di stato è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="e1e91-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="e1e91-129">La proprietà **Parent** dei riquadri della barra di stato è l'oggetto della barra di stato.</span><span class="sxs-lookup"><span data-stu-id="e1e91-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="e1e91-130">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="e1e91-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="e1e91-131">La proprietà **Role** per l'oggetto barra di stato stesso è il [**sistema del ruolo \_ \_ StatusBar**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e1e91-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="e1e91-132">Il testo visualizzato in una barra di stato [**ha \_ \_ STATICTEXT del sistema ruolo**](object-roles.md) come proprietà del **ruolo** .</span><span class="sxs-lookup"><span data-stu-id="e1e91-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="e1e91-133">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="e1e91-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="e1e91-134">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="e1e91-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="e1e91-135">Note</span><span class="sxs-lookup"><span data-stu-id="e1e91-135">Notes</span></span>

<span data-ttu-id="e1e91-136">Poiché i tasti di scelta rapida non sono supportati per i controlli barra di stato o le aree di testo nelle barre di stato, [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e1e91-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1e91-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1e91-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e91-138">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="e1e91-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





