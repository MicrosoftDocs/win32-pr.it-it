---
title: 'Funzione SampleBias:: SampleBias (S, float, float, int, float, uint) per Texture3D'
description: 'Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. | Funzione SampleBias:: SampleBias (S, float, float, int, float, uint) per Texture3D'
ms.assetid: 87B06414-F1A3-4BC8-B7DE-137B2156CFA7
keywords:
- Funzione SampleBias HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6155bbd4a3b21b86add57d13bc14a1185c76b73
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982670"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="b0192-105">Funzione SampleBias:: SampleBias (S, float, float, int, float, uint) per Texture3D</span><span class="sxs-lookup"><span data-stu-id="b0192-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="b0192-106">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="b0192-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="b0192-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0192-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0192-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0192-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b0192-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0192-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0192-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0192-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b0192-111">Type: **SamplerState**</span></span>

<span data-ttu-id="b0192-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b0192-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b0192-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="b0192-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b0192-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0192-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b0192-115">Type: **float**</span></span>

<span data-ttu-id="b0192-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="b0192-116">The texture coordinates.</span></span> <span data-ttu-id="b0192-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="b0192-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b0192-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b0192-118">Texture-Object Type</span></span>                    | <span data-ttu-id="b0192-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="b0192-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b0192-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b0192-120">Texture1D</span></span>                              | <span data-ttu-id="b0192-121">float</span><span class="sxs-lookup"><span data-stu-id="b0192-121">float</span></span>          |
| <span data-ttu-id="b0192-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b0192-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b0192-123">float2</span><span class="sxs-lookup"><span data-stu-id="b0192-123">float2</span></span>         |
| <span data-ttu-id="b0192-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b0192-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b0192-125">float3</span><span class="sxs-lookup"><span data-stu-id="b0192-125">float3</span></span>         |
| <span data-ttu-id="b0192-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b0192-126">TextureCubeArray</span></span>                       | <span data-ttu-id="b0192-127">float4</span><span class="sxs-lookup"><span data-stu-id="b0192-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b0192-128">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0192-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b0192-129">Type: **float**</span></span>

<span data-ttu-id="b0192-130">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="b0192-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b0192-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0192-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b0192-132">Type: **int**</span></span>

<span data-ttu-id="b0192-133">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="b0192-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b0192-134">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b0192-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="b0192-135">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="b0192-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b0192-136">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b0192-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b0192-137">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b0192-137">Texture-Object Type</span></span>           | <span data-ttu-id="b0192-138">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="b0192-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b0192-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b0192-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b0192-140">INT</span><span class="sxs-lookup"><span data-stu-id="b0192-140">int</span></span>            |
| <span data-ttu-id="b0192-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b0192-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b0192-142">int2</span><span class="sxs-lookup"><span data-stu-id="b0192-142">int2</span></span>           |
| <span data-ttu-id="b0192-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b0192-143">Texture3D</span></span>                     | <span data-ttu-id="b0192-144">int3</span><span class="sxs-lookup"><span data-stu-id="b0192-144">int3</span></span>           |
| <span data-ttu-id="b0192-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b0192-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b0192-146">non supportato</span><span class="sxs-lookup"><span data-stu-id="b0192-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b0192-147">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0192-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b0192-148">Type: **float**</span></span>

<span data-ttu-id="b0192-149">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="b0192-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b0192-150">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b0192-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b0192-151">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b0192-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0192-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b0192-152">Type: **uint**</span></span>

<span data-ttu-id="b0192-153">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0192-153">The status of the operation.</span></span> <span data-ttu-id="b0192-154">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b0192-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b0192-155">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b0192-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b0192-156">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="b0192-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0192-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0192-157">Return value</span></span>

<span data-ttu-id="b0192-158">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b0192-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b0192-159">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b0192-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b0192-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0192-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0192-161">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="b0192-161">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="b0192-162">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="b0192-162">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
