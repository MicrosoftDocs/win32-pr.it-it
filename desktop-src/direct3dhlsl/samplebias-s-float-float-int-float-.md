---
title: 'Funzione SampleBias:: SampleBias (S, float, float, int, float) per Texture2D'
description: 'La funzione SampleBias:: SampleBias (S, float, float, int, float) esegue il campionamento di un Texture2D, dopo aver applicato il valore di distorsione al livello mipmap.'
ms.assetid: 4E4A1188-DE45-4A43-B54D-4CA2E66707E3
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
ms.openlocfilehash: a34e6f2eb8211c0e4983d2d6a67f650d34c5dacf
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334323"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="07ba7-104">Funzione SampleBias:: SampleBias (S, float, float, int, float) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="07ba7-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="07ba7-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md), dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) campione su.</span><span class="sxs-lookup"><span data-stu-id="07ba7-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ba7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07ba7-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="07ba7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="07ba7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07ba7-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07ba7-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ba7-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="07ba7-109">Type: **SamplerState**</span></span>

<span data-ttu-id="07ba7-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="07ba7-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="07ba7-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="07ba7-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="07ba7-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07ba7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ba7-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="07ba7-113">Type: **float**</span></span>

<span data-ttu-id="07ba7-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="07ba7-114">The texture coordinates.</span></span> <span data-ttu-id="07ba7-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="07ba7-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="07ba7-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07ba7-116">Texture-Object Type</span></span>                    | <span data-ttu-id="07ba7-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="07ba7-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="07ba7-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="07ba7-118">Texture1D</span></span>                              | <span data-ttu-id="07ba7-119">float</span><span class="sxs-lookup"><span data-stu-id="07ba7-119">float</span></span>          |
| <span data-ttu-id="07ba7-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="07ba7-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="07ba7-121">float2</span><span class="sxs-lookup"><span data-stu-id="07ba7-121">float2</span></span>         |
| <span data-ttu-id="07ba7-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="07ba7-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="07ba7-123">float3</span><span class="sxs-lookup"><span data-stu-id="07ba7-123">float3</span></span>         |
| <span data-ttu-id="07ba7-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="07ba7-124">TextureCubeArray</span></span>                       | <span data-ttu-id="07ba7-125">float4</span><span class="sxs-lookup"><span data-stu-id="07ba7-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="07ba7-126">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07ba7-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ba7-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="07ba7-127">Type: **float**</span></span>

<span data-ttu-id="07ba7-128">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="07ba7-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="07ba7-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07ba7-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ba7-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="07ba7-130">Type: **int**</span></span>

<span data-ttu-id="07ba7-131">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="07ba7-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="07ba7-132">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="07ba7-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="07ba7-133">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="07ba7-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="07ba7-134">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="07ba7-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="07ba7-135">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07ba7-135">Texture-Object Type</span></span>           | <span data-ttu-id="07ba7-136">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="07ba7-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="07ba7-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="07ba7-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="07ba7-138">INT</span><span class="sxs-lookup"><span data-stu-id="07ba7-138">int</span></span>            |
| <span data-ttu-id="07ba7-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="07ba7-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="07ba7-140">int2</span><span class="sxs-lookup"><span data-stu-id="07ba7-140">int2</span></span>           |
| <span data-ttu-id="07ba7-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="07ba7-141">Texture3D</span></span>                     | <span data-ttu-id="07ba7-142">int3</span><span class="sxs-lookup"><span data-stu-id="07ba7-142">int3</span></span>           |
| <span data-ttu-id="07ba7-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="07ba7-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="07ba7-144">non supportato</span><span class="sxs-lookup"><span data-stu-id="07ba7-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="07ba7-145">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07ba7-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ba7-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="07ba7-146">Type: **float**</span></span>

<span data-ttu-id="07ba7-147">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="07ba7-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="07ba7-148">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="07ba7-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07ba7-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07ba7-149">Return value</span></span>

<span data-ttu-id="07ba7-150">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="07ba7-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="07ba7-151">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="07ba7-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="07ba7-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07ba7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ba7-153">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="07ba7-153">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
