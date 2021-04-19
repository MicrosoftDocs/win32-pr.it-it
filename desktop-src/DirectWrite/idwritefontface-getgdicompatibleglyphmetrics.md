---
title: Metodo IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Ottiene le metriche del glifo in unità di progettazione dei tipi di carattere con i valori restituiti compatibili con i prodotti GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Scrittura diretta metodo GetGdiCompatibleGlyphMetrics
- Metodo GetGdiCompatibleGlyphMetrics scrittura diretta, interfaccia IDWriteFontFace
- IDWriteFontFace interface Direct Write, metodo GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330034"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="be5bc-106">Metodo IDWriteFontFace:: GetGdiCompatibleGlyphMetrics</span><span class="sxs-lookup"><span data-stu-id="be5bc-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="be5bc-107">Ottiene le metriche del glifo in unità di progettazione dei tipi di carattere con i valori restituiti compatibili con i prodotti GDI.</span><span class="sxs-lookup"><span data-stu-id="be5bc-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be5bc-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="be5bc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="be5bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5bc-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="be5bc-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="be5bc-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="be5bc-111">Type: **FLOAT**</span></span>

<span data-ttu-id="be5bc-112">Dimensioni ogico del tipo di carattere in unità DIP.</span><span class="sxs-lookup"><span data-stu-id="be5bc-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="be5bc-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="be5bc-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="be5bc-114">Type: **FLOAT**</span></span>

<span data-ttu-id="be5bc-115">Il numero di pixel fisici per DIP.</span><span class="sxs-lookup"><span data-stu-id="be5bc-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-116">*trasformazione* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="be5bc-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be5bc-117">Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="be5bc-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="be5bc-118">Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni.</span><span class="sxs-lookup"><span data-stu-id="be5bc-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="be5bc-119">Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e da *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="be5bc-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-120">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="be5bc-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="be5bc-121">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="be5bc-121">Type: **BOOL**</span></span>

<span data-ttu-id="be5bc-122">Se è impostato su **false**, le metriche corrispondono a quelle del testo con aliasing GDI.</span><span class="sxs-lookup"><span data-stu-id="be5bc-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="be5bc-123">Quando è impostato su **true**, le metriche corrispondono a quelle del testo misurato da GDI usando un tipo di carattere creato con la **\_ \_ qualità naturale CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="be5bc-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-124">*GlyphIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be5bc-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be5bc-125">Tipo: **const \* UInt16**</span><span class="sxs-lookup"><span data-stu-id="be5bc-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="be5bc-126">Matrice di indici di glifi per i quali calcolare la metrica.</span><span class="sxs-lookup"><span data-stu-id="be5bc-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-127">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="be5bc-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="be5bc-128">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be5bc-128">Type: **UINT32**</span></span>

<span data-ttu-id="be5bc-129">Numero di elementi nella matrice *GlyphIndices* .</span><span class="sxs-lookup"><span data-stu-id="be5bc-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-130">*glyphMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be5bc-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be5bc-131">Tipo: **[ **\_ \_ metrica glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="be5bc-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="be5bc-132">Matrice di strutture [**della \_ \_ metrica del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) riempite da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="be5bc-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="be5bc-133">Le metriche si trovano in unità di progettazione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="be5bc-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="be5bc-134">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="be5bc-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="be5bc-135">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="be5bc-135">Type: **BOOL**</span></span>

<span data-ttu-id="be5bc-136">Valore BOOL che indica se il tipo di carattere viene utilizzato in un'esecuzione laterale.</span><span class="sxs-lookup"><span data-stu-id="be5bc-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="be5bc-137">Questo può influire sulle metriche del glifo se il tipo di carattere presenta una simulazione obliqua perché la simulazione obliqua laterale differisce dalla simulazione obliqua non laterale.</span><span class="sxs-lookup"><span data-stu-id="be5bc-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be5bc-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be5bc-138">Return value</span></span>

<span data-ttu-id="be5bc-139">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be5bc-139">Type: **HRESULT**</span></span>

<span data-ttu-id="be5bc-140">Codice di errore **HRESULT** standard.</span><span class="sxs-lookup"><span data-stu-id="be5bc-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="be5bc-141">Se uno degli indici del glifo di input è esterno all'intervallo di indice del glifo valido per il tipo di carattere corrente, verrà restituito **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="be5bc-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5bc-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be5bc-142">Requirements</span></span>



| <span data-ttu-id="be5bc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5bc-143">Requirement</span></span> | <span data-ttu-id="be5bc-144">Valore</span><span class="sxs-lookup"><span data-stu-id="be5bc-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be5bc-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="be5bc-145">Library</span></span><br/> | <dl> <span data-ttu-id="be5bc-146"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be5bc-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="be5bc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="be5bc-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="be5bc-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be5bc-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5bc-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be5bc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5bc-150">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="be5bc-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="be5bc-151">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="be5bc-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

