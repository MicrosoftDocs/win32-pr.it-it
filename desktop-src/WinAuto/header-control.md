---
title: Controllo Header (riferimento all'elemento MSAA UI)
description: Un controllo intestazione Visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni. Quando si seleziona la visualizzazione dettagli, Esplora risorse utilizza un controllo intestazione.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331439"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="3e014-104">Controllo Header (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="3e014-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="3e014-105">In questo argomento vengono descritti gli oggetti **controllo intestazione** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="3e014-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="3e014-106">La procedura per la creazione di oggetti **controllo intestazione** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="3e014-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="3e014-107">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="3e014-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="3e014-108">Un controllo intestazione Visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni.</span><span class="sxs-lookup"><span data-stu-id="3e014-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="3e014-109">Quando si seleziona la visualizzazione dettagli, Esplora risorse utilizza un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="3e014-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="3e014-110">Il nome della classe di finestra per un controllo intestazione è WC \_ header, definito come "SysHeader32" in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="3e014-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="3e014-111">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="3e014-111">IAccessible Methods</span></span>

<span data-ttu-id="3e014-112">Un controllo header supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="3e014-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="3e014-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3e014-113">Method</span></span>                                                                    | <span data-ttu-id="3e014-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e014-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="3e014-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="3e014-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="3e014-116">Questo metodo esegue l'azione predefinita facendo clic sull'intestazione.</span><span class="sxs-lookup"><span data-stu-id="3e014-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="3e014-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="3e014-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="3e014-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="3e014-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="3e014-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="3e014-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="3e014-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="3e014-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="3e014-121">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="3e014-121">IAccessible Properties</span></span>

<span data-ttu-id="3e014-122">Un controllo header supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e014-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="3e014-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e014-123">Property</span></span>                                                                       | <span data-ttu-id="3e014-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e014-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e014-125">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="3e014-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="3e014-126">La proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="3e014-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="3e014-127">**ottenere \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="3e014-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="3e014-128">La proprietà **DefaultAction** è "click".</span><span class="sxs-lookup"><span data-stu-id="3e014-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="3e014-129">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="3e014-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="3e014-130">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="3e014-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="3e014-131">La proprietà **Name** corrisponde al nome dell'intestazione di colonna.</span><span class="sxs-lookup"><span data-stu-id="3e014-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="3e014-132">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="3e014-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="3e014-133">La proprietà **Parent** è una finestra ( [**\_ \_ elenco del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="3e014-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="3e014-134">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="3e014-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="3e014-135">La proprietà **Role** è [**Role \_ System \_ COLUMNHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3e014-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="3e014-136">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="3e014-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="3e014-137">Il valore della proprietà **state** è sempre [**state \_ System \_ ReadOnly**](object-state-constants.md) e può includere anche il [**sistema di stato \_ \_ invisibile**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3e014-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3e014-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e014-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e014-139">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3e014-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




