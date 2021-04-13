---
title: Metodi di trasformazione IDCompositionVisual (Dcomp. h)
description: Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 2D utilizzata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 3 per 2 o un oggetto Transform.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341163"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="22c0c-106">Metodi IDCompositionVisual:: setransform</span><span class="sxs-lookup"><span data-stu-id="22c0c-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="22c0c-107">Imposta la proprietà Transform di questo oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="22c0c-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="22c0c-108">La proprietà Transform specifica una trasformazione 2D utilizzata per modificare il sistema di coordinate di questo oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="22c0c-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="22c0c-109">La proprietà può specificare una matrice di trasformazione 3 per 2 o un oggetto Transform.</span><span class="sxs-lookup"><span data-stu-id="22c0c-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="22c0c-110">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="22c0c-110">Overload list</span></span>



| <span data-ttu-id="22c0c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="22c0c-111">Method</span></span>                                                                                                    | <span data-ttu-id="22c0c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22c0c-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="22c0c-113">[**Setransform (D2D \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="22c0c-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="22c0c-114">Imposta la proprietà Transform sulla matrice di trasformazione specificata.</span><span class="sxs-lookup"><span data-stu-id="22c0c-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="22c0c-115">[**Setransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="22c0c-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="22c0c-116">Imposta la proprietà Transform sull'oggetto Transformation specificato.</span><span class="sxs-lookup"><span data-stu-id="22c0c-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="22c0c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22c0c-117">Requirements</span></span>



| <span data-ttu-id="22c0c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c0c-118">Requirement</span></span> | <span data-ttu-id="22c0c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="22c0c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22c0c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22c0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="22c0c-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="22c0c-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="22c0c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22c0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="22c0c-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="22c0c-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22c0c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22c0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c0c-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c0c-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22c0c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="22c0c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="22c0c-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22c0c-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="22c0c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="22c0c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c0c-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c0c-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c0c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22c0c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c0c-131">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="22c0c-132">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="22c0c-133">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="22c0c-134">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="22c0c-135">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="22c0c-136">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="22c0c-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="22c0c-137">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="22c0c-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="22c0c-138">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="22c0c-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="22c0c-139">**IDCompositionVisual:: seoffsety**</span><span class="sxs-lookup"><span data-stu-id="22c0c-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="22c0c-140">�</span><span class="sxs-lookup"><span data-stu-id="22c0c-140">�</span></span>

<span data-ttu-id="22c0c-141">�</span><span class="sxs-lookup"><span data-stu-id="22c0c-141">�</span></span>
