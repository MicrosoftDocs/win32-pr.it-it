---
title: Controllo ToolTip (riferimento all'elemento MSAA UI)
description: Un controllo ToolTip Visualizza una piccola finestra popup contenente una riga di testo che descrive lo scopo di uno strumento, rappresentato come oggetto grafico, in un'applicazione.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856161"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="2c651-103">Controllo ToolTip (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="2c651-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="2c651-104">Questo argomento descrive gli oggetti **controllo della descrizione comando** per scopi di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="2c651-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="2c651-105">La creazione di oggetti **controllo ToolTip** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="2c651-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="2c651-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="2c651-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="2c651-107">Un controllo ToolTip Visualizza una piccola finestra popup contenente una riga di testo che descrive lo scopo di uno strumento, rappresentato come oggetto grafico, in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2c651-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="2c651-108">Il nome della classe della finestra per una descrizione comando è la classe TOOLTIPs \_ , definita come "tooltips \_ Class" in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="2c651-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="2c651-109">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="2c651-109">IAccessible Methods</span></span>

<span data-ttu-id="2c651-110">Un controllo ToolTip supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="2c651-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="2c651-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2c651-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2c651-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="2c651-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="2c651-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2c651-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2c651-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="2c651-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="2c651-115">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="2c651-115">IAccessible Properties</span></span>

<span data-ttu-id="2c651-116">Un controllo ToolTip supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c651-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="2c651-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c651-117">Property</span></span>                                                                 | <span data-ttu-id="2c651-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c651-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c651-119">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="2c651-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="2c651-120">La proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="2c651-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2c651-121">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="2c651-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2c651-122">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2c651-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="2c651-123">La proprietà **Name** è il testo contenuto nel controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="2c651-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="2c651-124">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="2c651-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="2c651-125">La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="2c651-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="2c651-126">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="2c651-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="2c651-127">La proprietà **Role** è [**la \_ \_ Descrizione comando del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2c651-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="2c651-128">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="2c651-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="2c651-129">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="2c651-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2c651-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c651-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c651-131">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="2c651-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





