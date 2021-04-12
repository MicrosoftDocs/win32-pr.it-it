---
title: Metodo IDWriteFactory2 CreateGlyphRunAnalysis
description: Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Scrittura diretta metodo CreateGlyphRunAnalysis
- Metodo CreateGlyphRunAnalysis scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400758"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="56830-106">Metodo IDWriteFactory2:: CreateGlyphRunAnalysis</span><span class="sxs-lookup"><span data-stu-id="56830-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="56830-107">Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="56830-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="56830-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56830-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="56830-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="56830-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56830-110">*GlyphRun* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56830-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56830-111">Tipo: \**const [**DWrite \_ glifo \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _</span><span class="sxs-lookup"><span data-stu-id="56830-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="56830-112">Struttura che specifica le proprietà dell'esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="56830-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="56830-113">_transform \* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="56830-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56830-114">Tipo: \**const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="56830-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="56830-115">Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni.</span><span class="sxs-lookup"><span data-stu-id="56830-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="56830-116">Questa trasformazione viene applicata dopo il ridimensionamento specificato da emSize e pixelsPerDip.</span><span class="sxs-lookup"><span data-stu-id="56830-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="56830-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="56830-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-118">Tipo: **\_ \_ modalità di rendering DWrite**</span><span class="sxs-lookup"><span data-stu-id="56830-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="56830-119">Specifica la modalità di rendering, che deve essere una delle modalità di rendering raster (ovvero non predefinita e non struttura).</span><span class="sxs-lookup"><span data-stu-id="56830-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="56830-120">*measuringMode*</span><span class="sxs-lookup"><span data-stu-id="56830-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-121">Tipo: **[ **\_ \_ modalità di misurazione DWrite**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="56830-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="56830-122">Specifica il metodo per misurare i glifi.</span><span class="sxs-lookup"><span data-stu-id="56830-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="56830-123">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="56830-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-124">Tipo: **[ **DWrite \_ Grid \_ Fit \_ mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="56830-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="56830-125">Come grigliare le strutture di glifi.</span><span class="sxs-lookup"><span data-stu-id="56830-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="56830-126">Deve essere non predefinito.</span><span class="sxs-lookup"><span data-stu-id="56830-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="56830-127">*antialiasMode*</span><span class="sxs-lookup"><span data-stu-id="56830-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-128">Tipo: **[ **DWrite \_ Text \_ antialias \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="56830-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="56830-129">Specifica la modalità antialias.</span><span class="sxs-lookup"><span data-stu-id="56830-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="56830-130">*baselineOriginX*</span><span class="sxs-lookup"><span data-stu-id="56830-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="56830-131">Type: **FLOAT**</span></span>

<span data-ttu-id="56830-132">Posizione orizzontale dell'origine della linea di base, in DIP.</span><span class="sxs-lookup"><span data-stu-id="56830-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="56830-133">*baselineOriginY*</span><span class="sxs-lookup"><span data-stu-id="56830-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="56830-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="56830-134">Type: **FLOAT**</span></span>

<span data-ttu-id="56830-135">Posizione verticale dell'origine della linea di base, in DIP.</span><span class="sxs-lookup"><span data-stu-id="56830-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="56830-136">*glyphRunAnalysis* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="56830-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56830-137">Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="56830-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="56830-138">Riceve un puntatore all'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="56830-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56830-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56830-139">Return value</span></span>

<span data-ttu-id="56830-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="56830-140">Type: **HRESULT**</span></span>

<span data-ttu-id="56830-141">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56830-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56830-142">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56830-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56830-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56830-143">Requirements</span></span>



| <span data-ttu-id="56830-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="56830-144">Requirement</span></span> | <span data-ttu-id="56830-145">Valore</span><span class="sxs-lookup"><span data-stu-id="56830-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56830-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56830-146">Minimum supported client</span></span><br/> | <span data-ttu-id="56830-147">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="56830-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="56830-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56830-148">Minimum supported server</span></span><br/> | <span data-ttu-id="56830-149">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="56830-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="56830-150">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56830-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="56830-151">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="56830-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="56830-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="56830-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="56830-153"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56830-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="56830-154">DLL</span><span class="sxs-lookup"><span data-stu-id="56830-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56830-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56830-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56830-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56830-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56830-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="56830-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

