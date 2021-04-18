---
title: Metodi FillEllipse di ID2D1RenderTarget (D2d1. h)
description: Disegna l'interno dell'ellisse specificata.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Metodo FillEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325084"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="be7fe-104">Metodi ID2D1RenderTarget:: FillEllipse</span><span class="sxs-lookup"><span data-stu-id="be7fe-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="be7fe-105">Disegna l'interno dell'ellisse specificata.</span><span class="sxs-lookup"><span data-stu-id="be7fe-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="be7fe-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="be7fe-106">Overload list</span></span>



| <span data-ttu-id="be7fe-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="be7fe-107">Method</span></span>                                                                                                             | <span data-ttu-id="be7fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be7fe-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="be7fe-109">[**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="be7fe-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="be7fe-110">Disegna l'interno dell'ellisse specificata.</span><span class="sxs-lookup"><span data-stu-id="be7fe-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="be7fe-111">[**FillEllipse ( \_ ellisse d2d1 \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="be7fe-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="be7fe-112">Disegna l'interno dell'ellisse specificata.</span><span class="sxs-lookup"><span data-stu-id="be7fe-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="be7fe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="be7fe-113">Remarks</span></span>

<span data-ttu-id="be7fe-114">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="be7fe-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="be7fe-115">Per determinare se un'operazione di disegno (ad esempio **FillEllipse**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="be7fe-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="be7fe-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="be7fe-116">Examples</span></span>

<span data-ttu-id="be7fe-117">Per un esempio, vedere [How to disegnare and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="be7fe-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be7fe-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be7fe-118">Requirements</span></span>



| <span data-ttu-id="be7fe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7fe-119">Requirement</span></span> | <span data-ttu-id="be7fe-120">Valore</span><span class="sxs-lookup"><span data-stu-id="be7fe-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be7fe-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be7fe-121">Header</span></span><br/>  | <dl> <span data-ttu-id="be7fe-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7fe-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="be7fe-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="be7fe-123">Library</span></span><br/> | <dl> <span data-ttu-id="be7fe-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be7fe-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="be7fe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be7fe-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="be7fe-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7fe-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7fe-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be7fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7fe-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="be7fe-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="be7fe-129">Come creare e riempire una forma di base</span><span class="sxs-lookup"><span data-stu-id="be7fe-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="be7fe-130">�</span><span class="sxs-lookup"><span data-stu-id="be7fe-130">�</span></span>

<span data-ttu-id="be7fe-131">�</span><span class="sxs-lookup"><span data-stu-id="be7fe-131">�</span></span>
