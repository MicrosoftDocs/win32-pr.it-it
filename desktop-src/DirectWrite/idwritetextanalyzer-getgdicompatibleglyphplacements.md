---
title: Metodo IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Posizionare l'output dei glifi dal metodo GetGlyphs in base alle regole di rendering del tipo di carattere e del sistema di scrittura.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Scrittura diretta metodo GetGdiCompatibleGlyphPlacements
- Metodo GetGdiCompatibleGlyphPlacements scrittura diretta, interfaccia IDWriteTextAnalyzer
- IDWriteTextAnalyzer Interface Direct Write, metodo GetGdiCompatibleGlyphPlacements
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325292"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="8b5fc-106">Metodo IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements</span><span class="sxs-lookup"><span data-stu-id="8b5fc-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="8b5fc-107">Posizionare l'output dei glifi dal metodo [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) in base alle regole di rendering del tipo di carattere e del sistema di scrittura.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5fc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b5fc-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8b5fc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b5fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5fc-110">*textString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-111">Tipo: **const \* WCHAR**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="8b5fc-112">Matrice di caratteri contenente la stringa originale da cui provengono i glifi.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-113">*ClusterMap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-114">Tipo: **const \* UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="8b5fc-115">Puntatore al mapping da intervalli di caratteri a intervalli di glifi.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="8b5fc-116">Questa operazione viene restituita da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="8b5fc-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-117">*textProps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-118">Tipo: **[ **DWrite \_ shaping \_ \_ Proprietà testo**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="8b5fc-119">Puntatore a una matrice di strutture che contiene le proprietà di shaping per ogni carattere.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="8b5fc-120">Questa struttura viene restituita da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="8b5fc-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-122">Type: **UINT32**</span></span>

<span data-ttu-id="8b5fc-123">Lunghezza del testo di *textString*.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-124">*GlyphIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-125">Tipo: **const \* UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="8b5fc-126">Matrice di indici di glifi restituiti da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="8b5fc-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-127">*glyphProps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-128">Tipo: **const [**DWrite \_ shaping \_ Glyph \_ Properties**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="8b5fc-129">Puntatore a una matrice di strutture che contengono le proprietà di shaping per ogni glifo restituito da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="8b5fc-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-130">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-131">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-131">Type: **UINT32**</span></span>

<span data-ttu-id="8b5fc-132">Numero di glifi restituiti da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="8b5fc-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-133">*fontFace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-134">Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="8b5fc-135">Puntatore al tipo di carattere che rappresenta l'origine dei glifi di output.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-136">*fontEmSize*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-137">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-137">Type: **FLOAT**</span></span>

<span data-ttu-id="8b5fc-138">Dimensioni logiche del carattere in DIP.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-140">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-140">Type: **FLOAT**</span></span>

<span data-ttu-id="8b5fc-141">Il numero di pixel fisici per DIP.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-142">*trasformazione* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-143">Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="8b5fc-144">Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="8b5fc-145">Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e da *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="8b5fc-146">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-147">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-147">Type: **BOOL**</span></span>

<span data-ttu-id="8b5fc-148">Se è impostato su **false**, le metriche corrispondono a quelle del testo con aliasing GDI.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="8b5fc-149">Quando è impostato su **true**, le metriche corrispondono a quelle del testo misurato da GDI usando un tipo di carattere creato con la **\_ \_ qualità naturale CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-150">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-151">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-151">Type: **BOOL**</span></span>

<span data-ttu-id="8b5fc-152">Flag booleano impostato su **true** se il testo deve essere disegnato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-153">*isRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-154">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-154">Type: **BOOL**</span></span>

<span data-ttu-id="8b5fc-155">Flag booleano impostato su **true** per il testo da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-156">*scriptAnalysis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-157">Tipo: **const [**DWrite \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="8b5fc-158">Puntatore a un risultato dell'analisi di script da una chiamata [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .</span><span class="sxs-lookup"><span data-stu-id="8b5fc-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-159">*localeName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-160">Tipo: **const \* WCHAR**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="8b5fc-161">Matrice di caratteri contenente le impostazioni locali da utilizzare per la selezione dei glifi.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="8b5fc-162">Ad esempio, lo stesso carattere può essere mappato a glifi diversi per ja-JP rispetto a ZH-CHS.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="8b5fc-163">Se è **null**, viene utilizzato il mapping predefinito basato sullo script.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-164">*funzionalità* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-165">Tipo: **\* \* const [**DWrite le \_ \_ funzionalità tipografiche**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="8b5fc-166">Matrice di puntatori ai set di funzionalità tipografiche da utilizzare in ogni intervallo di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-167">*featureRangeLengths* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-168">Tipo: **const \* UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="8b5fc-169">Lunghezza di ogni intervallo di funzioni, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="8b5fc-170">La somma di tutte le lunghezze deve essere uguale a *TextLength*.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-171">*featureRanges*</span><span class="sxs-lookup"><span data-stu-id="8b5fc-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5fc-172">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-172">Type: **UINT32**</span></span>

<span data-ttu-id="8b5fc-173">Numero di intervalli di funzioni.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-174">*glyphAdvances* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-175">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="8b5fc-176">Quando termina, questo metodo contiene la larghezza di avanzamento di ogni glifo.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="8b5fc-177">*GlyphOffsets* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b5fc-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5fc-178">Tipo: **[ **\_ \_ offset glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="8b5fc-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="8b5fc-179">Quando termina, questo metodo contiene l'offset dell'origine di ogni glifo.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5fc-180">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b5fc-180">Return value</span></span>

<span data-ttu-id="8b5fc-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-181">Type: **HRESULT**</span></span>

<span data-ttu-id="8b5fc-182">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8b5fc-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b5fc-183">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b5fc-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5fc-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b5fc-184">Requirements</span></span>



| <span data-ttu-id="8b5fc-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5fc-185">Requirement</span></span> | <span data-ttu-id="8b5fc-186">Valore</span><span class="sxs-lookup"><span data-stu-id="8b5fc-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5fc-187">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b5fc-187">Library</span></span><br/> | <dl> <span data-ttu-id="8b5fc-188"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b5fc-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b5fc-189">DLL</span><span class="sxs-lookup"><span data-stu-id="8b5fc-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b5fc-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b5fc-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5fc-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b5fc-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5fc-192">**IDWriteTextAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8b5fc-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

