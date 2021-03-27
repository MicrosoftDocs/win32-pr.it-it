---
title: 'Funzione SampleBias:: SampleBias (S, float, float, int, float)'
description: 'Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. | Funzione SampleBias:: SampleBias (S, float, float, int, float)'
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
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
ms.openlocfilehash: 3af7ddaf3c015c2254761cce1d7cd30a2a68629b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995525"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="24764-105">Funzione SampleBias:: SampleBias (S, float, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="24764-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="24764-106">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="24764-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="24764-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24764-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="24764-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="24764-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24764-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24764-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24764-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="24764-110">Type: **SamplerState**</span></span>

<span data-ttu-id="24764-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="24764-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="24764-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="24764-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="24764-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24764-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24764-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="24764-114">Type: **float**</span></span>

<span data-ttu-id="24764-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="24764-115">The texture coordinates.</span></span> <span data-ttu-id="24764-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="24764-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="24764-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="24764-117">Texture-Object Type</span></span>                    | <span data-ttu-id="24764-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="24764-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="24764-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="24764-119">Texture1D</span></span>                              | <span data-ttu-id="24764-120">float</span><span class="sxs-lookup"><span data-stu-id="24764-120">float</span></span>          |
| <span data-ttu-id="24764-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="24764-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="24764-122">float2</span><span class="sxs-lookup"><span data-stu-id="24764-122">float2</span></span>         |
| <span data-ttu-id="24764-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="24764-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="24764-124">float3</span><span class="sxs-lookup"><span data-stu-id="24764-124">float3</span></span>         |
| <span data-ttu-id="24764-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="24764-125">TextureCubeArray</span></span>                       | <span data-ttu-id="24764-126">float4</span><span class="sxs-lookup"><span data-stu-id="24764-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="24764-127">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24764-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24764-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="24764-128">Type: **float**</span></span>

<span data-ttu-id="24764-129">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="24764-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="24764-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24764-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24764-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="24764-131">Type: **int**</span></span>

<span data-ttu-id="24764-132">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="24764-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="24764-133">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="24764-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="24764-134">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="24764-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="24764-135">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="24764-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="24764-136">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="24764-136">Texture-Object Type</span></span>           | <span data-ttu-id="24764-137">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="24764-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="24764-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="24764-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="24764-139">INT</span><span class="sxs-lookup"><span data-stu-id="24764-139">int</span></span>            |
| <span data-ttu-id="24764-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="24764-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="24764-141">int2</span><span class="sxs-lookup"><span data-stu-id="24764-141">int2</span></span>           |
| <span data-ttu-id="24764-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="24764-142">Texture3D</span></span>                     | <span data-ttu-id="24764-143">int3</span><span class="sxs-lookup"><span data-stu-id="24764-143">int3</span></span>           |
| <span data-ttu-id="24764-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="24764-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="24764-145">non supportato</span><span class="sxs-lookup"><span data-stu-id="24764-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="24764-146">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24764-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24764-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="24764-147">Type: **float**</span></span>

<span data-ttu-id="24764-148">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="24764-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="24764-149">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="24764-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24764-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24764-150">Return value</span></span>

<span data-ttu-id="24764-151">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="24764-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="24764-152">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="24764-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="24764-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24764-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24764-154">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="24764-154">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
