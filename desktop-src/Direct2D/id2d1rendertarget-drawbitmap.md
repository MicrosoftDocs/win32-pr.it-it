---
title: Metodi DrawBitmap di ID2D1RenderTarget
description: Disegna l'oggetto ID2D1Bitmap specificato.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Metodo DrawBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326073"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a><span data-ttu-id="3bc67-104">ID2D1RenderTarget::D Metodi rawBitmap</span><span class="sxs-lookup"><span data-stu-id="3bc67-104">ID2D1RenderTarget::DrawBitmap methods</span></span>

<span data-ttu-id="3bc67-105">Disegna l'oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)specificato.</span><span class="sxs-lookup"><span data-stu-id="3bc67-105">Draws the specified [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

### <a name="overload-list"></a><span data-ttu-id="3bc67-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="3bc67-106">Overload list</span></span>



| <span data-ttu-id="3bc67-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="3bc67-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="3bc67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bc67-108">Description</span></span>                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc67-109">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="3bc67-109">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span></span>   | <span data-ttu-id="3bc67-110">Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3bc67-110">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="3bc67-111">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="3bc67-111">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span>  | <span data-ttu-id="3bc67-112">Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3bc67-112">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="3bc67-113">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ Rect \_ f \* , float, d2d1 \_ bitmap \_ Interpolation \_ mode, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="3bc67-113">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F\*,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span> | <span data-ttu-id="3bc67-114">Disegna la bitmap specificata dopo averla ridimensionata fino alla dimensione del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3bc67-114">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="3bc67-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bc67-115">Remarks</span></span>

<span data-ttu-id="3bc67-116">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3bc67-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="3bc67-117">Per determinare se un'operazione di disegno (ad esempio **DrawBitmap**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="3bc67-117">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="3bc67-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="3bc67-118">Examples</span></span>

<span data-ttu-id="3bc67-119">Per un esempio, vedere [come creare una bitmap](how-to-draw-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="3bc67-119">For an example, see [How to Draw a Bitmap](how-to-draw-a-bitmap.md).</span></span> <span data-ttu-id="3bc67-120">Per un esempio che illustra come caricare una bitmap da una risorsa o da un file, vedere [come caricare una bitmap](how-to-load-a-bitmap-from-a-resource.md) da una risorsa e [come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="3bc67-120">For an example showing how to load a bitmap from a resource or a file, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md) and [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bc67-121">Requirements</span></span>



| <span data-ttu-id="3bc67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc67-122">Requirement</span></span> | <span data-ttu-id="3bc67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3bc67-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc67-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3bc67-124">Library</span></span><br/> | <dl> <span data-ttu-id="3bc67-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bc67-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bc67-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc67-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3bc67-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc67-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc67-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bc67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc67-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="3bc67-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="3bc67-130">Come creare una bitmap</span><span class="sxs-lookup"><span data-stu-id="3bc67-130">How to Draw a Bitmap</span></span>](how-to-draw-a-bitmap.md)
</dt> <dt>

[<span data-ttu-id="3bc67-131">Come caricare una bitmap da una risorsa</span><span class="sxs-lookup"><span data-stu-id="3bc67-131">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[<span data-ttu-id="3bc67-132">Come caricare una bitmap da un file</span><span class="sxs-lookup"><span data-stu-id="3bc67-132">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

