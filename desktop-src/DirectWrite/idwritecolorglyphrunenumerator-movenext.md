---
title: Metodo MoveNext IDWriteColorGlyphRunEnumerator
description: Passare al glifo successivo eseguito nell'enumeratore.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Scrittura diretta metodo MoveNext
- Metodo MoveNext scrittura diretta, interfaccia IDWriteColorGlyphRunEnumerator
- IDWriteColorGlyphRunEnumerator Interface Direct Write, metodo MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518112"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="1fb46-106">Metodo IDWriteColorGlyphRunEnumerator:: MoveNext</span><span class="sxs-lookup"><span data-stu-id="1fb46-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="1fb46-107">Passare al glifo successivo eseguito nell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1fb46-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fb46-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="1fb46-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fb46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb46-110">*haveRun* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1fb46-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb46-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="1fb46-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="1fb46-112">Restituisce _ *true*\* se è presente una successiva esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="1fb46-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb46-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fb46-113">Return value</span></span>

<span data-ttu-id="1fb46-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1fb46-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1fb46-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1fb46-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1fb46-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1fb46-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb46-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fb46-117">Requirements</span></span>



| <span data-ttu-id="1fb46-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb46-118">Requirement</span></span> | <span data-ttu-id="1fb46-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1fb46-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb46-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fb46-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb46-121">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1fb46-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1fb46-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fb46-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb46-123">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1fb46-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="1fb46-124">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fb46-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="1fb46-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="1fb46-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="1fb46-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fb46-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fb46-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb46-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1fb46-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb46-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb46-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb46-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fb46-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fb46-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb46-131">**IDWriteColorGlyphRunEnumerator**</span><span class="sxs-lookup"><span data-stu-id="1fb46-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





