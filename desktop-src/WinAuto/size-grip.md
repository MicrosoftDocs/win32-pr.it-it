---
title: Grip dimensioni (riferimento all'elemento MSAA UI)
description: Il grip dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente a un utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714134"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="c53b0-103">Grip dimensioni (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="c53b0-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="c53b0-104">Il grip dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente a un utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="c53b0-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c53b0-105">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="c53b0-105">IAccessible Methods</span></span>

<span data-ttu-id="c53b0-106">Il grip dimensioni supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c53b0-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="c53b0-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c53b0-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c53b0-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="c53b0-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="c53b0-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="c53b0-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="c53b0-110">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="c53b0-110">IAccessible Properties</span></span>

<span data-ttu-id="c53b0-111">Il grip dimensioni supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="c53b0-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="c53b0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c53b0-112">Property</span></span>                                                                   | <span data-ttu-id="c53b0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c53b0-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c53b0-114">**ottenere \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="c53b0-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="c53b0-115">La proprietà **Description** è "può essere usata per ridimensionare la larghezza e l'altezza di una finestra".</span><span class="sxs-lookup"><span data-stu-id="c53b0-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="c53b0-116">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="c53b0-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="c53b0-117">La proprietà **Name** è "size box".</span><span class="sxs-lookup"><span data-stu-id="c53b0-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="c53b0-118">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="c53b0-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="c53b0-119">Finestra che contiene il riquadro delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c53b0-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="c53b0-120">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c53b0-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="c53b0-121">La proprietà **Role** è [**il \_ \_ grip del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c53b0-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="c53b0-122">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="c53b0-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="c53b0-123">Il valore della proprietà **state** è zero, che indica che l'oggetto è visibile oppure che il [**sistema di stato è \_ \_ invisibile**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c53b0-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c53b0-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c53b0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53b0-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="c53b0-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




