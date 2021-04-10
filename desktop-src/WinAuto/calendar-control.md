---
title: Controllo Calendar (riferimento all'elemento MSAA UI)
description: I controlli calendario consentono a un utente di selezionare una data da un'interfaccia familiare in modo semplice e intuitivo.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855781"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="c0fef-103">Controllo Calendar (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="c0fef-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="c0fef-104">In questo argomento vengono descritti gli oggetti **controllo calendario** per gli scopi del riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="c0fef-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="c0fef-105">La creazione di oggetti **controllo calendario** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="c0fef-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="c0fef-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="c0fef-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="c0fef-107">I controlli calendario consentono a un utente di selezionare una data da un'interfaccia familiare in modo semplice e intuitivo.</span><span class="sxs-lookup"><span data-stu-id="c0fef-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="c0fef-108">Il nome della classe della finestra per un controllo calendario mensile è la \_ classe MONTHCAL, definita come "SysMonthCal32" in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="c0fef-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="c0fef-109">Le informazioni contenute in questo argomento si applicano al controllo calendario mensile nella versione 5 di COMmctrl. h.</span><span class="sxs-lookup"><span data-stu-id="c0fef-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c0fef-110">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="c0fef-110">IAccessible Methods</span></span>

<span data-ttu-id="c0fef-111">I controlli Calendar supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c0fef-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="c0fef-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c0fef-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c0fef-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="c0fef-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="c0fef-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="c0fef-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="c0fef-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="c0fef-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="c0fef-116">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="c0fef-116">IAccessible Properties</span></span>

<span data-ttu-id="c0fef-117">I controlli Calendar supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0fef-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="c0fef-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0fef-118">Property</span></span>                                                                 | <span data-ttu-id="c0fef-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0fef-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0fef-120">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="c0fef-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="c0fef-121">La proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="c0fef-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c0fef-122">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="c0fef-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="c0fef-123">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="c0fef-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="c0fef-124">La proprietà **Name** è ottenuta dal controllo testo statico che etichetta il controllo Calendar.</span><span class="sxs-lookup"><span data-stu-id="c0fef-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="c0fef-125">Quando si creano i controlli, gli sviluppatori di server devono garantire che un controllo testo statico preceda immediatamente il controllo che etichetta all'interno dell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="c0fef-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="c0fef-126">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="c0fef-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="c0fef-127">La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="c0fef-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="c0fef-128">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c0fef-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="c0fef-129">La proprietà **Role** è [**un \_ \_ client del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c0fef-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c0fef-130">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="c0fef-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="c0fef-131">La proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: lo stato del sistema dello stato [**\_ \_ Invisible**](object-state-constants.md) sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="c0fef-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c0fef-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0fef-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0fef-133">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="c0fef-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





