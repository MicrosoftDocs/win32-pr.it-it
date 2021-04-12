---
title: Metodo IDWriteFontFallbackBuilder AddMapping
description: Accoda un singolo mapping all'elenco. Chiamare questa volta per ogni mapping aggiuntivo.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Scrittura diretta Metodo AddMapping
- Metodo AddMapping scrittura diretta, interfaccia IDWriteFontFallbackBuilder
- IDWriteFontFallbackBuilder Interface Direct Write, Metodo AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400755"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="c24da-107">Metodo IDWriteFontFallbackBuilder:: AddMapping</span><span class="sxs-lookup"><span data-stu-id="c24da-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="c24da-108">Accoda un singolo mapping all'elenco.</span><span class="sxs-lookup"><span data-stu-id="c24da-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="c24da-109">Chiamare questa volta per ogni mapping aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="c24da-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24da-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c24da-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="c24da-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c24da-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24da-112">*intervalli*</span><span class="sxs-lookup"><span data-stu-id="c24da-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="c24da-113">Tipo: \**[**DWrite \_ Unicode \_ Range**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _</span><span class="sxs-lookup"><span data-stu-id="c24da-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="c24da-114">Intervalli Unicode applicabili a questo mapping.</span><span class="sxs-lookup"><span data-stu-id="c24da-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="c24da-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="c24da-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c24da-116">Type: **UINT32**</span></span>

<span data-ttu-id="c24da-117">Numero di intervalli Unicode.</span><span class="sxs-lookup"><span data-stu-id="c24da-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-118">*targetFamilyNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c24da-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c24da-119">Tipo: **const \* \* WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c24da-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="c24da-120">Elenco delle stringhe del nome della famiglia di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c24da-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-121">*targetFamilyNamesCount*</span><span class="sxs-lookup"><span data-stu-id="c24da-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="c24da-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c24da-122">Type: **UINT32**</span></span>

<span data-ttu-id="c24da-123">Numero di nomi di famiglia di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c24da-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-124">*FontCollection* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c24da-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c24da-125">Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="c24da-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="c24da-126">Raccolta di tipi di carattere esplicita facoltativa per questo mapping.</span><span class="sxs-lookup"><span data-stu-id="c24da-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-127">*localeName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c24da-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c24da-128">Tipo: \**const \* WCHAR* _</span><span class="sxs-lookup"><span data-stu-id="c24da-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="c24da-129">Impostazioni locali del contesto.</span><span class="sxs-lookup"><span data-stu-id="c24da-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-130">_baseFamilyName \* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c24da-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c24da-131">Tipo: \**const \* WCHAR* _</span><span class="sxs-lookup"><span data-stu-id="c24da-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="c24da-132">Nome della famiglia di base in base al quale trovare la corrispondenza, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="c24da-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="c24da-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="c24da-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="c24da-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c24da-134">Type: **FLOAT**</span></span>

<span data-ttu-id="c24da-135">Fattore di scala per moltiplicare il tipo di carattere di destinazione risultato per.</span><span class="sxs-lookup"><span data-stu-id="c24da-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24da-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c24da-136">Return value</span></span>

<span data-ttu-id="c24da-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c24da-137">Type: **HRESULT**</span></span>

<span data-ttu-id="c24da-138">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c24da-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c24da-139">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c24da-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c24da-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c24da-140">Requirements</span></span>



| <span data-ttu-id="c24da-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c24da-141">Requirement</span></span> | <span data-ttu-id="c24da-142">Valore</span><span class="sxs-lookup"><span data-stu-id="c24da-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c24da-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c24da-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c24da-144">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c24da-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c24da-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c24da-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c24da-146">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c24da-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c24da-147">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c24da-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c24da-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c24da-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c24da-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="c24da-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="c24da-150"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c24da-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c24da-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c24da-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c24da-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c24da-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c24da-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c24da-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24da-154">**IDWriteFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="c24da-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

