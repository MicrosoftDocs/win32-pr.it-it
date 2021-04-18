---
title: Metodi FillOpacityMask di ID2D1RenderTarget
description: Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e utilizza tale pennello per disegnare un'area della destinazione di rendering.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Metodo FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325083"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="75f56-104">Metodi ID2D1RenderTarget:: FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="75f56-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="75f56-105">Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e utilizza tale pennello per disegnare un'area della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="75f56-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="75f56-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="75f56-106">Overload list</span></span>



| <span data-ttu-id="75f56-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="75f56-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="75f56-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75f56-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f56-109">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ Opacity \_ mask \_ CONTENT, D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="75f56-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="75f56-110">Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e utilizza tale pennello per disegnare un'area della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="75f56-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="75f56-111">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ Opacity \_ mask \_ Content, D2D \_ Rect \_ f \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="75f56-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="75f56-112">Applica la maschera di opacità descritta dalla bitmap specificata a un pennello e utilizza tale pennello per disegnare un'area della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="75f56-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="75f56-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="75f56-113">Remarks</span></span>

<span data-ttu-id="75f56-114">Per il corretto funzionamento di questo metodo, è necessario che la destinazione di rendering usi la modalità di anti-aliasing con [**\_ \_ \_ alias in modalità antialias di d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) .</span><span class="sxs-lookup"><span data-stu-id="75f56-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="75f56-115">È possibile impostare la modalità di anti-aliasing chiamando il metodo [**ID2D1RenderTarget:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .</span><span class="sxs-lookup"><span data-stu-id="75f56-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="75f56-116">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="75f56-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="75f56-117">Per determinare se un'operazione di disegno (ad esempio **FillOpacityMask**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="75f56-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f56-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75f56-118">Requirements</span></span>



| <span data-ttu-id="75f56-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f56-119">Requirement</span></span> | <span data-ttu-id="75f56-120">Valore</span><span class="sxs-lookup"><span data-stu-id="75f56-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="75f56-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="75f56-121">Library</span></span><br/> | <dl> <span data-ttu-id="75f56-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75f56-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="75f56-123">DLL</span><span class="sxs-lookup"><span data-stu-id="75f56-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="75f56-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75f56-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f56-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75f56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f56-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="75f56-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

