---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture2DArray'
description: Informazioni su come questa funzione esegue il campionamento di una trama usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per Texture2DArray.
ms.assetid: 6455BF80-2A22-43BB-80A2-61FBEC66C348
keywords:
- Funzione SampleCmp HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0692166766b9f52a1b6b13719c2427438b59835f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762430"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="314bb-105">Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="314bb-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="314bb-106">Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="314bb-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="314bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="314bb-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="314bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="314bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314bb-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="314bb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bb-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="314bb-110">Type: **SamplerState**</span></span>

<span data-ttu-id="314bb-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="314bb-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="314bb-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="314bb-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="314bb-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="314bb-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bb-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bb-114">Type: **float**</span></span>

<span data-ttu-id="314bb-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="314bb-115">The texture coordinates.</span></span> <span data-ttu-id="314bb-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="314bb-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="314bb-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="314bb-117">Texture-Object Type</span></span>                    | <span data-ttu-id="314bb-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="314bb-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="314bb-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="314bb-119">Texture1D</span></span>                              | <span data-ttu-id="314bb-120">float</span><span class="sxs-lookup"><span data-stu-id="314bb-120">float</span></span>          |
| <span data-ttu-id="314bb-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="314bb-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="314bb-122">float2</span><span class="sxs-lookup"><span data-stu-id="314bb-122">float2</span></span>         |
| <span data-ttu-id="314bb-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="314bb-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="314bb-124">float3</span><span class="sxs-lookup"><span data-stu-id="314bb-124">float3</span></span>         |
| <span data-ttu-id="314bb-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="314bb-125">TextureCubeArray</span></span>                       | <span data-ttu-id="314bb-126">float4</span><span class="sxs-lookup"><span data-stu-id="314bb-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="314bb-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="314bb-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bb-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bb-128">Type: **float**</span></span>

<span data-ttu-id="314bb-129">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="314bb-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="314bb-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="314bb-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bb-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="314bb-131">Type: **int**</span></span>

<span data-ttu-id="314bb-132">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="314bb-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="314bb-133">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="314bb-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="314bb-134">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="314bb-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="314bb-135">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="314bb-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="314bb-136">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="314bb-136">Texture-Object Type</span></span>           | <span data-ttu-id="314bb-137">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="314bb-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="314bb-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="314bb-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="314bb-139">INT</span><span class="sxs-lookup"><span data-stu-id="314bb-139">int</span></span>            |
| <span data-ttu-id="314bb-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="314bb-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="314bb-141">int2</span><span class="sxs-lookup"><span data-stu-id="314bb-141">int2</span></span>           |
| <span data-ttu-id="314bb-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="314bb-142">Texture3D</span></span>                     | <span data-ttu-id="314bb-143">int3</span><span class="sxs-lookup"><span data-stu-id="314bb-143">int3</span></span>           |
| <span data-ttu-id="314bb-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="314bb-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="314bb-145">non supportato</span><span class="sxs-lookup"><span data-stu-id="314bb-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="314bb-146">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="314bb-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bb-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bb-147">Type: **float**</span></span>

<span data-ttu-id="314bb-148">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="314bb-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="314bb-149">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="314bb-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314bb-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="314bb-150">Return value</span></span>

<span data-ttu-id="314bb-151">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="314bb-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="314bb-152">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="314bb-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="314bb-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="314bb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314bb-154">Metodi SampleCmp</span><span class="sxs-lookup"><span data-stu-id="314bb-154">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> </dl>

 

 
