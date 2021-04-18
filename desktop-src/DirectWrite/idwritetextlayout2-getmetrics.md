---
title: Metodo GetMetrics IDWriteTextLayout2
description: Recupera la metrica complessiva per la stringa formattata.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Scrittura diretta metodo GetMetrics
- Metodo GetMetrics scrittura diretta, interfaccia IDWriteTextLayout2
- IDWriteTextLayout2 Interface Direct Write, metodo GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301930"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="2e11a-106">Metodo IDWriteTextLayout2:: GetMetrics</span><span class="sxs-lookup"><span data-stu-id="2e11a-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="2e11a-107">Recupera la metrica complessiva per la stringa formattata.</span><span class="sxs-lookup"><span data-stu-id="2e11a-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e11a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e11a-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2e11a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e11a-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="2e11a-110">*textMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e11a-111">Tipo: \**[**DWrite \_ testo \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="2e11a-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="2e11a-112">Quando termina, questo metodo contiene le distanze misurate del testo e il contenuto associato dopo la formattazione.</span><span class="sxs-lookup"><span data-stu-id="2e11a-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e11a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e11a-113">Return value</span></span>

<span data-ttu-id="2e11a-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2e11a-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2e11a-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e11a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e11a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e11a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e11a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e11a-117">Requirements</span></span>



| <span data-ttu-id="2e11a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e11a-118">Requirement</span></span> | <span data-ttu-id="2e11a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2e11a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e11a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e11a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e11a-121">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="2e11a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e11a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e11a-123">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2e11a-124">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e11a-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2e11a-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="2e11a-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2e11a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e11a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e11a-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e11a-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2e11a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2e11a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e11a-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e11a-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e11a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e11a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e11a-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="2e11a-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





