---
title: Metodi ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Metodo PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333507"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="02615-104">ID2D1RenderTarget::P metodi ushAxisAlignedClip</span><span class="sxs-lookup"><span data-stu-id="02615-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="02615-105">Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.</span><span class="sxs-lookup"><span data-stu-id="02615-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="02615-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="02615-106">Overload list</span></span>



| <span data-ttu-id="02615-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="02615-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="02615-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02615-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="02615-109">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, \_ modalità antialias d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="02615-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="02615-110">Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.</span><span class="sxs-lookup"><span data-stu-id="02615-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="02615-111">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , d2d1 \_ antialias \_ mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="02615-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="02615-112">Specifica un rettangolo in cui tutte le operazioni di disegno successive vengono ritagliate.</span><span class="sxs-lookup"><span data-stu-id="02615-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="02615-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="02615-113">Remarks</span></span>

<span data-ttu-id="02615-114">Una coppia [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) può essere presente in un [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ma non può sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="02615-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="02615-115">La sequenza di **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** , ad esempio, è valida, ma la sequenza di **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** non è valida.</span><span class="sxs-lookup"><span data-stu-id="02615-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="02615-116">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="02615-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="02615-117">Per determinare se un'operazione di disegno (ad esempio **PushAxisAlignedClip**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="02615-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="02615-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="02615-118">Examples</span></span>

<span data-ttu-id="02615-119">Per un esempio, vedere la pagina relativa alla [clip con un rettangolo di ritaglio Axis-Aligned](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="02615-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02615-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02615-120">Requirements</span></span>



| <span data-ttu-id="02615-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="02615-121">Requirement</span></span> | <span data-ttu-id="02615-122">Valore</span><span class="sxs-lookup"><span data-stu-id="02615-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02615-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02615-123">Header</span></span><br/>  | <dl> <span data-ttu-id="02615-124"><dt>D2d1 \_ 1. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02615-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="02615-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="02615-125">Library</span></span><br/> | <dl> <span data-ttu-id="02615-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02615-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="02615-127">DLL</span><span class="sxs-lookup"><span data-stu-id="02615-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="02615-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02615-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="02615-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02615-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02615-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="02615-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="02615-131">�</span><span class="sxs-lookup"><span data-stu-id="02615-131">�</span></span>

<span data-ttu-id="02615-132">�</span><span class="sxs-lookup"><span data-stu-id="02615-132">�</span></span>
