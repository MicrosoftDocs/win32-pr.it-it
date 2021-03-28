---
description: In questo argomento vengono elencati i metodi ExcludeClip della classe Graphics. Per un elenco completo dei metodi per la classe graphics, vedere Graphics.
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: Metodi Graphics. ExcludeClip (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996468"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="cf1c6-104">Metodi Graphics. ExcludeClip</span><span class="sxs-lookup"><span data-stu-id="cf1c6-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="cf1c6-105">In questo argomento vengono elencati i metodi ExcludeClip della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cf1c6-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="cf1c6-106">Per un elenco completo dei metodi per la classe **Graphics** , vedere [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="cf1c6-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="cf1c6-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="cf1c6-107">Overload list</span></span>



| <span data-ttu-id="cf1c6-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="cf1c6-108">Method</span></span>                                                                         | <span data-ttu-id="cf1c6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf1c6-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1c6-110">[**ExcludeClip (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="cf1c6-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="cf1c6-111">Il metodo [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) aggiorna l'area di ridimensionamento alla parte di se stessa che non interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="cf1c6-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="cf1c6-112">[**ExcludeClip (RectF&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf1c6-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="cf1c6-113">Il metodo [**Graphics:: ExcludeClip**](/previous-versions//ms535975(v=vs.85)) aggiorna l'area di ridimensionamento alla parte di se stessa che non interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="cf1c6-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="cf1c6-114">[**ExcludeClip (regione \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="cf1c6-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="cf1c6-115">Il metodo [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) aggiorna l'area di visualizzazione con la parte di se stessa che non si sovrappone all'area specificata.</span><span class="sxs-lookup"><span data-stu-id="cf1c6-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="cf1c6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf1c6-116">Requirements</span></span>



| <span data-ttu-id="cf1c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf1c6-117">Requirement</span></span> | <span data-ttu-id="cf1c6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cf1c6-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1c6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf1c6-119">Header</span></span><br/> | <dl> <span data-ttu-id="cf1c6-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf1c6-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
