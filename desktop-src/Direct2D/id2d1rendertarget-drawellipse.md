---
title: Metodi DrawEllipse di ID2D1RenderTarget (D2d1. h)
description: Disegna il contorno di un'ellisse con le dimensioni e il tratto specificati.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Metodo DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326072"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="4213c-104">ID2D1RenderTarget::D Metodi rawEllipse</span><span class="sxs-lookup"><span data-stu-id="4213c-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="4213c-105">Disegna il contorno di un'ellisse con le dimensioni e il tratto specificati.</span><span class="sxs-lookup"><span data-stu-id="4213c-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4213c-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="4213c-106">Overload list</span></span>



| <span data-ttu-id="4213c-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="4213c-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="4213c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4213c-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4213c-109">[**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="4213c-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="4213c-110">Disegna il contorno dell'ellisse specificata utilizzando lo stile del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="4213c-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="4213c-111">[**DrawEllipse (D2D1 \_ ellisse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="4213c-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="4213c-112">Disegna il contorno dell'ellisse specificata utilizzando lo stile del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="4213c-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="4213c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4213c-113">Remarks</span></span>

<span data-ttu-id="4213c-114">Se ha esito negativo, il metodo **DrawEllipse** non restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4213c-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="4213c-115">Per determinare se un'operazione di disegno (ad esempio **DrawEllipse**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="4213c-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="4213c-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4213c-116">Examples</span></span>

<span data-ttu-id="4213c-117">Per un esempio, vedere [How to disegnare and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="4213c-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4213c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4213c-118">Requirements</span></span>



| <span data-ttu-id="4213c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4213c-119">Requirement</span></span> | <span data-ttu-id="4213c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4213c-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4213c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4213c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4213c-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="4213c-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="4213c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="4213c-123">Library</span></span><br/> | <dl> <span data-ttu-id="4213c-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4213c-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="4213c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4213c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4213c-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4213c-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4213c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4213c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4213c-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="4213c-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="4213c-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="4213c-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="4213c-130">�</span><span class="sxs-lookup"><span data-stu-id="4213c-130">�</span></span>

<span data-ttu-id="4213c-131">�</span><span class="sxs-lookup"><span data-stu-id="4213c-131">�</span></span>
