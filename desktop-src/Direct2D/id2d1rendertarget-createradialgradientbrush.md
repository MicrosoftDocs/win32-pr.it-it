---
title: Metodi CreateRadialGradientBrush di ID2D1RenderTarget (D2d1. h)
description: Crea un oggetto ID2D1RadialGradientBrush che può essere usato per disegnare aree con una sfumatura radiale.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Metodo CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326080"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a><span data-ttu-id="5c270-104">Metodi ID2D1RenderTarget:: CreateRadialGradientBrush</span><span class="sxs-lookup"><span data-stu-id="5c270-104">ID2D1RenderTarget::CreateRadialGradientBrush methods</span></span>

<span data-ttu-id="5c270-105">Crea un oggetto [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che può essere usato per disegnare aree con una sfumatura radiale.</span><span class="sxs-lookup"><span data-stu-id="5c270-105">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) object that can be used to paint areas with a radial gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="5c270-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="5c270-106">Overload list</span></span>



| <span data-ttu-id="5c270-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="5c270-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="5c270-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c270-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c270-109">[**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5c270-109">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>                            | <span data-ttu-id="5c270-110">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati, non ha alcuna trasformazione e ha un'opacità di base 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c270-110">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="5c270-111">[**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_&, \_ proprietà del pennello d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5c270-111">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>   | <span data-ttu-id="5c270-112">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate.</span><span class="sxs-lookup"><span data-stu-id="5c270-112">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="5c270-113">[**CreateRadialGradientBrush ( \_ proprietà del \_ pennello sfumatura radiale d2d1 \_ \_ \* , \_ proprietà del pennello d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5c270-113">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span> | <span data-ttu-id="5c270-114">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) che contiene i cursori sfumatura specificati e presenta la trasformazione e l'opacità di base specificate.</span><span class="sxs-lookup"><span data-stu-id="5c270-114">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="5c270-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c270-115">Examples</span></span>

<span data-ttu-id="5c270-116">Per un esempio, vedere [come creare un pennello sfumatura radiale](how-to-create-a-radial-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="5c270-116">For an example, see [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c270-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c270-117">Requirements</span></span>



| <span data-ttu-id="5c270-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c270-118">Requirement</span></span> | <span data-ttu-id="5c270-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5c270-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c270-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c270-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5c270-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c270-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c270-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c270-122">Library</span></span><br/> | <dl> <span data-ttu-id="5c270-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c270-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c270-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5c270-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c270-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c270-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c270-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c270-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c270-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5c270-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="5c270-128">Come creare un pennello sfumatura radiale</span><span class="sxs-lookup"><span data-stu-id="5c270-128">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="5c270-129">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="5c270-129">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="5c270-130">�</span><span class="sxs-lookup"><span data-stu-id="5c270-130">�</span></span>

<span data-ttu-id="5c270-131">�</span><span class="sxs-lookup"><span data-stu-id="5c270-131">�</span></span>
