---
title: 'Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, int, uint) per Texture2D'
description: Campiona un Texture2D solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto, quindi restituisce lo stato dell'operazione. Per Texture2D.
ms.assetid: AEFE424F-2C77-434C-B9C0-8173778CB108
keywords:
- Funzione SampleCmpLevelZero HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a28dddeb687093a76f4f8bc60c96777468abc9f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996420"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="41715-105">Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, int, uint) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="41715-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="41715-106">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md) solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="41715-106">Samples a [**Texture2D**](sm5-object-texture2d.md) on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="41715-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="41715-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="41715-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41715-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="41715-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="41715-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41715-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41715-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41715-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="41715-111">Type: **SamplerState**</span></span>

<span data-ttu-id="41715-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="41715-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="41715-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="41715-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="41715-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41715-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41715-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="41715-115">Type: **float**</span></span>

<span data-ttu-id="41715-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="41715-116">The texture coordinates.</span></span> <span data-ttu-id="41715-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="41715-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="41715-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="41715-118">Texture-Object Type</span></span>                    | <span data-ttu-id="41715-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="41715-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="41715-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="41715-120">Texture1D</span></span>                              | <span data-ttu-id="41715-121">float</span><span class="sxs-lookup"><span data-stu-id="41715-121">float</span></span>          |
| <span data-ttu-id="41715-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="41715-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="41715-123">float2</span><span class="sxs-lookup"><span data-stu-id="41715-123">float2</span></span>         |
| <span data-ttu-id="41715-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="41715-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="41715-125">float3</span><span class="sxs-lookup"><span data-stu-id="41715-125">float3</span></span>         |
| <span data-ttu-id="41715-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="41715-126">TextureCubeArray</span></span>                       | <span data-ttu-id="41715-127">float4</span><span class="sxs-lookup"><span data-stu-id="41715-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="41715-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41715-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41715-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="41715-129">Type: **float**</span></span>

<span data-ttu-id="41715-130">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="41715-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="41715-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41715-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41715-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="41715-132">Type: **int**</span></span>

<span data-ttu-id="41715-133">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="41715-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="41715-134">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="41715-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="41715-135">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="41715-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="41715-136">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="41715-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="41715-137">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="41715-137">Texture-Object Type</span></span>           | <span data-ttu-id="41715-138">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="41715-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="41715-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="41715-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="41715-140">INT</span><span class="sxs-lookup"><span data-stu-id="41715-140">int</span></span>            |
| <span data-ttu-id="41715-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="41715-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="41715-142">int2</span><span class="sxs-lookup"><span data-stu-id="41715-142">int2</span></span>           |
| <span data-ttu-id="41715-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="41715-143">Texture3D</span></span>                     | <span data-ttu-id="41715-144">int3</span><span class="sxs-lookup"><span data-stu-id="41715-144">int3</span></span>           |
| <span data-ttu-id="41715-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="41715-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="41715-146">non supportato</span><span class="sxs-lookup"><span data-stu-id="41715-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="41715-147">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="41715-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41715-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="41715-148">Type: **uint**</span></span>

<span data-ttu-id="41715-149">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="41715-149">The status of the operation.</span></span> <span data-ttu-id="41715-150">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="41715-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="41715-151">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="41715-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="41715-152">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="41715-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41715-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41715-153">Return value</span></span>

<span data-ttu-id="41715-154">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="41715-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="41715-155">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="41715-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="41715-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41715-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41715-157">Metodi SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="41715-157">SampleCmpLevelZero methods</span></span>](texture2d-samplecmplevelzero.md)
</dt> </dl>

 

 
