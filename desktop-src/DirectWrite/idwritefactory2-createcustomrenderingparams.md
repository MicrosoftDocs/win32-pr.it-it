---
title: Metodo IDWriteFactory2 CreateCustomRenderingParams
description: Crea un oggetto parametri di rendering con le proprietà specificate.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Scrittura diretta metodo CreateCustomRenderingParams
- Metodo CreateCustomRenderingParams scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400759"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="e0c8e-106">Metodo IDWriteFactory2:: CreateCustomRenderingParams</span><span class="sxs-lookup"><span data-stu-id="e0c8e-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="e0c8e-107">Crea un oggetto parametri di rendering con le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c8e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0c8e-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e0c8e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0c8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c8e-110">*gamma*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-111">Type: **FLOAT**</span></span>

<span data-ttu-id="e0c8e-112">Valore gamma usato per la correzione gamma, che deve essere maggiore di zero e non può essere superiore a 256.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-113">*enhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-114">Type: **FLOAT**</span></span>

<span data-ttu-id="e0c8e-115">Quantità di miglioramento del contrasto, zero o superiore.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-116">*grayscaleEnhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-117">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-117">Type: **FLOAT**</span></span>

<span data-ttu-id="e0c8e-118">Quantità di miglioramento del contrasto, zero o superiore.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-119">*clearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-120">Type: **FLOAT**</span></span>

<span data-ttu-id="e0c8e-121">Grado di livello ClearType, da 0,0 f (senza ClearType) a 1,0 f (ClearType completo).</span><span class="sxs-lookup"><span data-stu-id="e0c8e-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-122">*pixelGeometry*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-123">Tipo: **[ **DWrite \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="e0c8e-124">Geometria di un pixel del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-125">*renderingMode*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-126">Tipo: **[ **\_ \_ modalità di rendering DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="e0c8e-127">Metodo di rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-127">Method of rendering glyphs.</span></span> <span data-ttu-id="e0c8e-128">Nella maggior parte dei casi, è consigliabile \_ \_ usare la modalità di rendering DWrite \_ per impostazione predefinita per usare automaticamente una modalità appropriata.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-129">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="e0c8e-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c8e-130">Tipo: **[ **DWrite \_ Grid \_ Fit \_ mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="e0c8e-131">Come grigliare i delineamenti dell'icona adatta.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="e0c8e-132">Nella maggior parte dei casi, deve essere DWRITE \_ Grid \_ Fit \_ default per scegliere automaticamente una modalità appropriata.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="e0c8e-133">*renderingParams* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e0c8e-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0c8e-134">Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0c8e-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="e0c8e-135">Include l'oggetto parametri di rendering appena creato oppure NULL in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c8e-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0c8e-136">Return value</span></span>

<span data-ttu-id="e0c8e-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-137">Type: **HRESULT**</span></span>

<span data-ttu-id="e0c8e-138">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e0c8e-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0c8e-139">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0c8e-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c8e-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0c8e-140">Requirements</span></span>



| <span data-ttu-id="e0c8e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0c8e-141">Requirement</span></span> | <span data-ttu-id="e0c8e-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e0c8e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c8e-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0c8e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c8e-144">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e0c8e-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="e0c8e-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0c8e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c8e-146">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e0c8e-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e0c8e-147">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0c8e-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e0c8e-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="e0c8e-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="e0c8e-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0c8e-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0c8e-150"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0c8e-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e0c8e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e0c8e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0c8e-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0c8e-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0c8e-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0c8e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c8e-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="e0c8e-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

