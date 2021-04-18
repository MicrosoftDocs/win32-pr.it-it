---
title: 'Funzione della funzione SampleBias:: SampleBias (S, float, float, int, float) per Texture1D'
description: "La funzione SampleBias:: SampleBias (S, float, float, int, float) esegue il campionamento di una trama dopo l'applicazione del valore di distorsione al livello mipmap."
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
ms.openlocfilehash: 1f7c6979d9781964d6bdd89914602c1946ce481c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334378"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="f129b-104">Funzione SampleBias:: SampleBias (S, float, float, int, float) per Texture1D</span><span class="sxs-lookup"><span data-stu-id="f129b-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="f129b-105">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="f129b-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f129b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f129b-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="f129b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f129b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f129b-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f129b-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f129b-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f129b-109">Type: **SamplerState**</span></span>

<span data-ttu-id="f129b-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f129b-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f129b-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="f129b-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f129b-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f129b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f129b-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f129b-113">Type: **float**</span></span>

<span data-ttu-id="f129b-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f129b-114">The texture coordinates.</span></span> <span data-ttu-id="f129b-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f129b-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f129b-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f129b-116">Texture-Object Type</span></span>                    | <span data-ttu-id="f129b-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f129b-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f129b-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f129b-118">Texture1D</span></span>                              | <span data-ttu-id="f129b-119">float</span><span class="sxs-lookup"><span data-stu-id="f129b-119">float</span></span>          |
| <span data-ttu-id="f129b-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f129b-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f129b-121">float2</span><span class="sxs-lookup"><span data-stu-id="f129b-121">float2</span></span>         |
| <span data-ttu-id="f129b-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f129b-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f129b-123">float3</span><span class="sxs-lookup"><span data-stu-id="f129b-123">float3</span></span>         |
| <span data-ttu-id="f129b-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f129b-124">TextureCubeArray</span></span>                       | <span data-ttu-id="f129b-125">float4</span><span class="sxs-lookup"><span data-stu-id="f129b-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f129b-126">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f129b-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f129b-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f129b-127">Type: **float**</span></span>

<span data-ttu-id="f129b-128">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="f129b-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f129b-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f129b-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f129b-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f129b-130">Type: **int**</span></span>

<span data-ttu-id="f129b-131">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="f129b-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f129b-132">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f129b-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f129b-133">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f129b-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f129b-134">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f129b-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f129b-135">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f129b-135">Texture-Object Type</span></span>           | <span data-ttu-id="f129b-136">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f129b-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f129b-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f129b-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f129b-138">INT</span><span class="sxs-lookup"><span data-stu-id="f129b-138">int</span></span>            |
| <span data-ttu-id="f129b-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f129b-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f129b-140">int2</span><span class="sxs-lookup"><span data-stu-id="f129b-140">int2</span></span>           |
| <span data-ttu-id="f129b-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f129b-141">Texture3D</span></span>                     | <span data-ttu-id="f129b-142">int3</span><span class="sxs-lookup"><span data-stu-id="f129b-142">int3</span></span>           |
| <span data-ttu-id="f129b-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f129b-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f129b-144">non supportato</span><span class="sxs-lookup"><span data-stu-id="f129b-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f129b-145">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f129b-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f129b-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f129b-146">Type: **float**</span></span>

<span data-ttu-id="f129b-147">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="f129b-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f129b-148">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f129b-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f129b-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f129b-149">Return value</span></span>

<span data-ttu-id="f129b-150">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f129b-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f129b-151">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f129b-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f129b-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f129b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f129b-153">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="f129b-153">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
