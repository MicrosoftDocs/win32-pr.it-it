---
title: Metodi di IDCompositionVisual (Dcomp. h)
description: Imposta la proprietà di ritaglio di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Metodi di seclip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743410"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="a2119-104">Metodi IDCompositionVisual:: seclip</span><span class="sxs-lookup"><span data-stu-id="a2119-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="a2119-105">Imposta la proprietà di ritaglio di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato.</span><span class="sxs-lookup"><span data-stu-id="a2119-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="a2119-106">La proprietà clip limita il rendering della sottostruttura ad albero visuale che è radicata in questo oggetto visivo in un'area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="a2119-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a2119-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="a2119-107">Overload list</span></span>



| <span data-ttu-id="a2119-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="a2119-108">Method</span></span>                                                                                | <span data-ttu-id="a2119-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2119-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="a2119-110">[**Seclip (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="a2119-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="a2119-111">Imposta la proprietà clip sull'area rettangolare specificata.</span><span class="sxs-lookup"><span data-stu-id="a2119-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="a2119-112">[**Seclip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="a2119-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="a2119-113">Imposta la proprietà di ritaglio sull'oggetto clip specificato.</span><span class="sxs-lookup"><span data-stu-id="a2119-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="a2119-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2119-114">Requirements</span></span>



| <span data-ttu-id="a2119-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2119-115">Requirement</span></span> | <span data-ttu-id="a2119-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a2119-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2119-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2119-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2119-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2119-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2119-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2119-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2119-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2119-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2119-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2119-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2119-122"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2119-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2119-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2119-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2119-124"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2119-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2119-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a2119-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2119-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2119-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2119-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2119-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2119-128">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="a2119-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="a2119-129">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="a2119-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="a2119-130">�</span><span class="sxs-lookup"><span data-stu-id="a2119-130">�</span></span>

<span data-ttu-id="a2119-131">�</span><span class="sxs-lookup"><span data-stu-id="a2119-131">�</span></span>
