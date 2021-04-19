---
title: Metodi CreateLinearGradientBrush di ID2D1RenderTarget (D2d1. h)
description: Crea un oggetto ID2D1LinearGradientBrush per le aree di disegno con una sfumatura lineare.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Metodo CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326081"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a><span data-ttu-id="0c289-104">Metodi ID2D1RenderTarget:: CreateLinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="0c289-104">ID2D1RenderTarget::CreateLinearGradientBrush methods</span></span>

<span data-ttu-id="0c289-105">Crea un oggetto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) per le aree di disegno con una sfumatura lineare.</span><span class="sxs-lookup"><span data-stu-id="0c289-105">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) object for painting areas with a linear gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0c289-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="0c289-106">Overload list</span></span>



| <span data-ttu-id="0c289-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="0c289-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="0c289-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c289-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c289-109">[**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="0c289-109">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>                            | <span data-ttu-id="0c289-110">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base 1,0.</span><span class="sxs-lookup"><span data-stu-id="0c289-110">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="0c289-111">[**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_&, \_ proprietà del pennello d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="0c289-111">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>   | <span data-ttu-id="0c289-112">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate.</span><span class="sxs-lookup"><span data-stu-id="0c289-112">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="0c289-113">[**CreateLinearGradientBrush ( \_ proprietà del \_ pennello sfumatura lineare d2d1 \_ \_ \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="0c289-113">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span> | <span data-ttu-id="0c289-114">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate.</span><span class="sxs-lookup"><span data-stu-id="0c289-114">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="0c289-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="0c289-115">Examples</span></span>

<span data-ttu-id="0c289-116">Per un esempio che illustra come creare una raccolta di arresti sfumatura e usarla per definire una sfumatura lineare, vedere [How to create a linear gradient brush](how-to-create-a-linear-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="0c289-116">For an example showing how to create a gradient stop collection and use it to define a linear gradient, see [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c289-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c289-117">Requirements</span></span>



| <span data-ttu-id="0c289-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c289-118">Requirement</span></span> | <span data-ttu-id="0c289-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0c289-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0c289-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c289-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0c289-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c289-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c289-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c289-122">Library</span></span><br/> | <dl> <span data-ttu-id="0c289-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c289-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c289-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0c289-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c289-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c289-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c289-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c289-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c289-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="0c289-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="0c289-128">**CreateGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="0c289-128">**CreateGradientStopCollection**</span></span>](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[<span data-ttu-id="0c289-129">**ID2D1GradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="0c289-129">**ID2D1GradientStopCollection**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[<span data-ttu-id="0c289-130">**ID2D1LinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="0c289-130">**ID2D1LinearGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[<span data-ttu-id="0c289-131">**ID2D1RadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="0c289-131">**ID2D1RadialGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[<span data-ttu-id="0c289-132">Come creare un pennello sfumato lineare</span><span class="sxs-lookup"><span data-stu-id="0c289-132">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="0c289-133">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="0c289-133">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="0c289-134">�</span><span class="sxs-lookup"><span data-stu-id="0c289-134">�</span></span>

<span data-ttu-id="0c289-135">�</span><span class="sxs-lookup"><span data-stu-id="0c289-135">�</span></span>
