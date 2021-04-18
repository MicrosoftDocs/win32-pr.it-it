---
title: Metodo IDWriteTextLayout GetOverhangMetrics
description: Restituisce i blocchi (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi i glifi di testo e gli oggetti inline.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Scrittura diretta metodo GetOverhangMetrics
- Metodo GetOverhangMetrics scrittura diretta, interfaccia IDWriteTextLayout
- IDWriteTextLayout Interface Direct Write, metodo GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328148"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="bfca8-106">Metodo IDWriteTextLayout:: GetOverhangMetrics</span><span class="sxs-lookup"><span data-stu-id="bfca8-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="bfca8-107">Restituisce i blocchi (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi i glifi di testo e gli oggetti inline.</span><span class="sxs-lookup"><span data-stu-id="bfca8-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfca8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfca8-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bfca8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfca8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfca8-110">*blocchi* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bfca8-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfca8-111">Tipo: **[ **\_ \_ metrica di sporgenza DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="bfca8-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="bfca8-112">Overshoot degli extent visibili (in DIP) all'esterno del layout.</span><span class="sxs-lookup"><span data-stu-id="bfca8-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfca8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfca8-113">Return value</span></span>

<span data-ttu-id="bfca8-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfca8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bfca8-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bfca8-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bfca8-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bfca8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfca8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfca8-117">Remarks</span></span>

<span data-ttu-id="bfca8-118">Le sottolineature e strikethroughs non contribuiscono alla determinazione black box, perché vengono effettivamente disegnate dal renderer, che può essere disegnate in qualsiasi varietà di stili.</span><span class="sxs-lookup"><span data-stu-id="bfca8-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfca8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfca8-119">Requirements</span></span>



| <span data-ttu-id="bfca8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfca8-120">Requirement</span></span> | <span data-ttu-id="bfca8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca8-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfca8-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="bfca8-122">Library</span></span><br/> | <dl> <span data-ttu-id="bfca8-123"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfca8-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="bfca8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bfca8-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bfca8-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfca8-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfca8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfca8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfca8-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="bfca8-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="bfca8-128">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="bfca8-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

