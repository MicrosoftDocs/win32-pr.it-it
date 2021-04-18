---
title: Metodi di trasformazione IDCompositionVisual3 (Dcomp. h)
description: Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 3D utilizzata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto Transform.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Metodi di trasformazione DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301722"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="571cf-106">Metodi IDCompositionVisual3:: setransform</span><span class="sxs-lookup"><span data-stu-id="571cf-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="571cf-107">Imposta la proprietà Transform di questo oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="571cf-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="571cf-108">La proprietà Transform specifica una trasformazione 3D utilizzata per modificare il sistema di coordinate di questo oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="571cf-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="571cf-109">La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto Transform.</span><span class="sxs-lookup"><span data-stu-id="571cf-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="571cf-110">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="571cf-110">Overload list</span></span>



| <span data-ttu-id="571cf-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="571cf-111">Method</span></span>                                                                                  | <span data-ttu-id="571cf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571cf-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="571cf-113">[**Setransform (D2D \_ Matrix \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="571cf-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="571cf-114">Imposta la proprietà Transform sulla matrice di trasformazione specificata.</span><span class="sxs-lookup"><span data-stu-id="571cf-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="571cf-115">[**Setransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="571cf-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="571cf-116">Imposta la proprietà Transform sull'oggetto Transformation specificato.</span><span class="sxs-lookup"><span data-stu-id="571cf-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="571cf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="571cf-117">Requirements</span></span>



| <span data-ttu-id="571cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="571cf-118">Requirement</span></span> | <span data-ttu-id="571cf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="571cf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="571cf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="571cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="571cf-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="571cf-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="571cf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="571cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="571cf-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="571cf-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="571cf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="571cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="571cf-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="571cf-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="571cf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="571cf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="571cf-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="571cf-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="571cf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="571cf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="571cf-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="571cf-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="571cf-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="571cf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="571cf-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="571cf-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="571cf-132">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="571cf-133">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="571cf-134">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="571cf-135">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="571cf-136">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="571cf-137">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="571cf-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="571cf-138">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="571cf-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="571cf-139">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="571cf-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="571cf-140">**IDCompositionVisual:: seoffsety**</span><span class="sxs-lookup"><span data-stu-id="571cf-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="571cf-141">�</span><span class="sxs-lookup"><span data-stu-id="571cf-141">�</span></span>

<span data-ttu-id="571cf-142">�</span><span class="sxs-lookup"><span data-stu-id="571cf-142">�</span></span>
