---
title: Metodo IDWriteFontFallback MapCharacters
description: Determina un tipo di carattere appropriato da utilizzare per eseguire il rendering dell'intervallo iniziale del testo.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Scrittura diretta metodo MapCharacters
- Metodo MapCharacters scrittura diretta, interfaccia IDWriteFontFallback
- IDWriteFontFallback Interface Direct Write, metodo MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340833"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="feba8-106">Metodo IDWriteFontFallback:: MapCharacters</span><span class="sxs-lookup"><span data-stu-id="feba8-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="feba8-107">Determina un tipo di carattere appropriato da utilizzare per eseguire il rendering dell'intervallo iniziale del testo.</span><span class="sxs-lookup"><span data-stu-id="feba8-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="feba8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="feba8-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="feba8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="feba8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feba8-110">*source*</span><span class="sxs-lookup"><span data-stu-id="feba8-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-111">Tipo: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="feba8-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="feba8-112">L'implementazione di origine del testo include il testo e le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="feba8-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="feba8-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="feba8-114">Type: **UINT32**</span></span>

<span data-ttu-id="feba8-115">Posizione iniziale da analizzare.</span><span class="sxs-lookup"><span data-stu-id="feba8-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="feba8-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="feba8-117">Type: **UINT32**</span></span>

<span data-ttu-id="feba8-118">Lunghezza del testo da analizzare.</span><span class="sxs-lookup"><span data-stu-id="feba8-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-119">*baseFontCollection* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="feba8-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="feba8-120">Tipo: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="feba8-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="feba8-121">Raccolta dei tipi di carattere predefinita da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="feba8-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-122">_baseFamilyName \* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="feba8-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="feba8-123">Tipo: \**const \_ WCHAR \* t* _</span><span class="sxs-lookup"><span data-stu-id="feba8-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="feba8-124">Nome della famiglia del tipo di carattere di base.</span><span class="sxs-lookup"><span data-stu-id="feba8-124">Family name of the base font.</span></span> <span data-ttu-id="feba8-125">Se si passa null, non verrà eseguita alcuna corrispondenza per la famiglia.</span><span class="sxs-lookup"><span data-stu-id="feba8-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="feba8-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-127">Tipo: **[ **\_ \_ Spessore carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="feba8-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="feba8-128">Spessore desiderato.</span><span class="sxs-lookup"><span data-stu-id="feba8-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-129">*baseStyle*</span><span class="sxs-lookup"><span data-stu-id="feba8-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-130">Tipo: stile del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="feba8-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="feba8-131">Stile desiderato.</span><span class="sxs-lookup"><span data-stu-id="feba8-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-132">*baseStretch*</span><span class="sxs-lookup"><span data-stu-id="feba8-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="feba8-133">Tipo: estensione del tipo di **[ **\_ carattere \_ DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="feba8-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="feba8-134">Estensione desiderata.</span><span class="sxs-lookup"><span data-stu-id="feba8-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-135">*mappedLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="feba8-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feba8-136">Tipo: \**UInt32 \** _</span><span class="sxs-lookup"><span data-stu-id="feba8-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="feba8-137">Lunghezza del testo mappato al tipo di carattere mappato.</span><span class="sxs-lookup"><span data-stu-id="feba8-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="feba8-138">Sarà sempre minore o uguale alla lunghezza del testo e maggiore di zero (se la lunghezza del testo è diversa da zero), in modo che il chiamante anticipi almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="feba8-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="feba8-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="feba8-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feba8-140">Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="feba8-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="feba8-141">Il tipo di carattere da utilizzare per eseguire il rendering dei primi caratteri *mappedLength* del testo.</span><span class="sxs-lookup"><span data-stu-id="feba8-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="feba8-142">Se restituisce NULL, significa che nessun carattere può eseguire il rendering del testo e *mappedLength* è il numero di caratteri da ignorare (sottoposto a rendering con un glifo mancante).</span><span class="sxs-lookup"><span data-stu-id="feba8-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="feba8-143">*Ridimensiona* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="feba8-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feba8-144">Tipo: \**float \** _</span><span class="sxs-lookup"><span data-stu-id="feba8-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="feba8-145">Fattore di scala per moltiplicare le dimensioni em del tipo di carattere restituito da.</span><span class="sxs-lookup"><span data-stu-id="feba8-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feba8-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="feba8-146">Return value</span></span>

<span data-ttu-id="feba8-147">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="feba8-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="feba8-148">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="feba8-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="feba8-149">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="feba8-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="feba8-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="feba8-150">Requirements</span></span>



| <span data-ttu-id="feba8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="feba8-151">Requirement</span></span> | <span data-ttu-id="feba8-152">Valore</span><span class="sxs-lookup"><span data-stu-id="feba8-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feba8-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="feba8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="feba8-154">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="feba8-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="feba8-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="feba8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="feba8-156">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="feba8-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="feba8-157">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="feba8-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="feba8-158">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="feba8-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="feba8-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="feba8-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="feba8-160"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="feba8-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="feba8-161">DLL</span><span class="sxs-lookup"><span data-stu-id="feba8-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feba8-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feba8-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="feba8-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="feba8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feba8-164">**IDWriteFontFallback**</span><span class="sxs-lookup"><span data-stu-id="feba8-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

