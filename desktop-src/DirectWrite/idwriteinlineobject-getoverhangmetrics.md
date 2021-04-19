---
title: Metodo IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline. Nel caso di una bitmap semplice, senza riempimento e senza sporgenza, tutti i blocchi verranno semplicemente azzerati.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Scrittura diretta metodo GetOverhangMetrics
- Metodo GetOverhangMetrics scrittura diretta, interfaccia IDWriteInlineObject
- IDWriteInlineObject interface Direct Write, metodo GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330162"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="dd246-107">Metodo IDWriteInlineObject:: GetOverhangMetrics</span><span class="sxs-lookup"><span data-stu-id="dd246-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="dd246-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline.</span><span class="sxs-lookup"><span data-stu-id="dd246-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="dd246-109">Nel caso di una bitmap semplice, senza riempimento e senza sporgenza, tutti i blocchi verranno semplicemente azzerati.</span><span class="sxs-lookup"><span data-stu-id="dd246-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="dd246-110">I blocchi devono essere restituiti rispetto alle dimensioni segnalate dell'oggetto (vedere le [**\_ \_ \_ metriche dell'oggetto inline DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) e non devono essere regolate dalla baseline.</span><span class="sxs-lookup"><span data-stu-id="dd246-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd246-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd246-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="dd246-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd246-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd246-113">*blocchi* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd246-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd246-114">Tipo: **[ **\_ \_ metrica di sporgenza DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="dd246-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="dd246-115">Overshoot degli extent visibili (in DIP) all'esterno dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd246-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd246-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd246-116">Return value</span></span>

<span data-ttu-id="dd246-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd246-117">Type: **HRESULT**</span></span>

<span data-ttu-id="dd246-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd246-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd246-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd246-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd246-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd246-120">Requirements</span></span>



| <span data-ttu-id="dd246-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd246-121">Requirement</span></span> | <span data-ttu-id="dd246-122">Valore</span><span class="sxs-lookup"><span data-stu-id="dd246-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd246-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd246-123">Library</span></span><br/> | <dl> <span data-ttu-id="dd246-124"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd246-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd246-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd246-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd246-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd246-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd246-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd246-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd246-128">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="dd246-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="dd246-129">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="dd246-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

