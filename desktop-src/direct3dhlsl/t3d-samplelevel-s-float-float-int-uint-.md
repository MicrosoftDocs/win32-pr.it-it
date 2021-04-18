---
title: 'Funzione SampleLevel:: SampleLevel (S, float, float, int, uint) per Texture3D'
description: "Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione. Per Texture3D. | Funzione SampleLevel:: SampleLevel (S, float, float, int, uint)"
ms.assetid: D79247AC-A922-49C7-BAC6-807C31F279B1
keywords:
- Funzione SampleLevel HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ae92245b6a8b6cff89805a73dd724e5aeac43a9
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982811"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture3d"></a><span data-ttu-id="7e38c-106">Funzione SampleLevel:: SampleLevel (S, float, float, int, uint) per Texture3D</span><span class="sxs-lookup"><span data-stu-id="7e38c-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture3D</span></span>

<span data-ttu-id="7e38c-107">Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7e38c-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e38c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e38c-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7e38c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e38c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e38c-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e38c-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e38c-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="7e38c-111">Type: **SamplerState**</span></span>

<span data-ttu-id="7e38c-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7e38c-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="7e38c-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="7e38c-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="7e38c-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e38c-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e38c-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7e38c-115">Type: **float**</span></span>

<span data-ttu-id="7e38c-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7e38c-116">The texture coordinates.</span></span> <span data-ttu-id="7e38c-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="7e38c-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="7e38c-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7e38c-118">Texture-Object Type</span></span>                    | <span data-ttu-id="7e38c-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="7e38c-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="7e38c-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7e38c-120">Texture1D</span></span>                              | <span data-ttu-id="7e38c-121">float</span><span class="sxs-lookup"><span data-stu-id="7e38c-121">float</span></span>          |
| <span data-ttu-id="7e38c-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7e38c-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="7e38c-123">float2</span><span class="sxs-lookup"><span data-stu-id="7e38c-123">float2</span></span>         |
| <span data-ttu-id="7e38c-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="7e38c-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="7e38c-125">float3</span><span class="sxs-lookup"><span data-stu-id="7e38c-125">float3</span></span>         |
| <span data-ttu-id="7e38c-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7e38c-126">TextureCubeArray</span></span>                       | <span data-ttu-id="7e38c-127">float4</span><span class="sxs-lookup"><span data-stu-id="7e38c-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="7e38c-128">*LOD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e38c-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e38c-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7e38c-129">Type: **float**</span></span>

<span data-ttu-id="7e38c-130">\[in \] un numero che specifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="7e38c-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="7e38c-131">Se il valore è ≤ 0, viene usato il livello mipmap 0 (mapping più grande).</span><span class="sxs-lookup"><span data-stu-id="7e38c-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="7e38c-132">Il valore frazionario (se fornito) viene usato per interpolare tra due livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="7e38c-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="7e38c-133">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e38c-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e38c-134">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7e38c-134">Type: **int**</span></span>

<span data-ttu-id="7e38c-135">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="7e38c-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="7e38c-136">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="7e38c-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="7e38c-137">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="7e38c-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="7e38c-138">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="7e38c-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="7e38c-139">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7e38c-139">Texture-Object Type</span></span>           | <span data-ttu-id="7e38c-140">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="7e38c-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="7e38c-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7e38c-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="7e38c-142">INT</span><span class="sxs-lookup"><span data-stu-id="7e38c-142">int</span></span>            |
| <span data-ttu-id="7e38c-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7e38c-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="7e38c-144">int2</span><span class="sxs-lookup"><span data-stu-id="7e38c-144">int2</span></span>           |
| <span data-ttu-id="7e38c-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7e38c-145">Texture3D</span></span>                     | <span data-ttu-id="7e38c-146">int3</span><span class="sxs-lookup"><span data-stu-id="7e38c-146">int3</span></span>           |
| <span data-ttu-id="7e38c-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7e38c-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="7e38c-148">non supportato</span><span class="sxs-lookup"><span data-stu-id="7e38c-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="7e38c-149">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7e38c-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e38c-150">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7e38c-150">Type: **uint**</span></span>

<span data-ttu-id="7e38c-151">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7e38c-151">The status of the operation.</span></span> <span data-ttu-id="7e38c-152">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7e38c-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7e38c-153">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7e38c-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7e38c-154">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="7e38c-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e38c-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e38c-155">Return value</span></span>

<span data-ttu-id="7e38c-156">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="7e38c-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="7e38c-157">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="7e38c-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="7e38c-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e38c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e38c-159">Metodi SampleLevel</span><span class="sxs-lookup"><span data-stu-id="7e38c-159">SampleLevel methods</span></span>](texture3d-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="7e38c-160">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="7e38c-160">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
