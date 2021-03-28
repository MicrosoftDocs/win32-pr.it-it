---
title: 'Funzione Texture1DArray:: Sample (S, float, int, float)'
description: 'Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione Texture1DArray:: Sample (S, float, int, float)'
ms.assetid: 3A965EEE-FCA3-4DD8-87D2-56679DFF5D3A
keywords:
- Funzione di esempio HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16d0a651d70aa618b9791fb760c51dfa05945752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995661"
---
# <a name="texture1darraysamplesfloatintfloat-function"></a><span data-ttu-id="74fb6-105">Funzione Texture1DArray:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="74fb6-105">Texture1DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="74fb6-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="74fb6-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="74fb6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74fb6-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="74fb6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74fb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74fb6-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74fb6-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74fb6-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="74fb6-110">Type: **SamplerState**</span></span>

<span data-ttu-id="74fb6-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="74fb6-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="74fb6-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="74fb6-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="74fb6-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74fb6-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74fb6-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74fb6-114">Type: **float**</span></span>

<span data-ttu-id="74fb6-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="74fb6-115">The texture coordinates.</span></span> <span data-ttu-id="74fb6-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="74fb6-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="74fb6-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74fb6-117">Texture-Object Type</span></span>                    | <span data-ttu-id="74fb6-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="74fb6-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="74fb6-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="74fb6-119">Texture1D</span></span>                              | <span data-ttu-id="74fb6-120">float</span><span class="sxs-lookup"><span data-stu-id="74fb6-120">float</span></span>          |
| <span data-ttu-id="74fb6-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="74fb6-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="74fb6-122">float2</span><span class="sxs-lookup"><span data-stu-id="74fb6-122">float2</span></span>         |
| <span data-ttu-id="74fb6-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="74fb6-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="74fb6-124">float3</span><span class="sxs-lookup"><span data-stu-id="74fb6-124">float3</span></span>         |
| <span data-ttu-id="74fb6-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74fb6-125">TextureCubeArray</span></span>                       | <span data-ttu-id="74fb6-126">float4</span><span class="sxs-lookup"><span data-stu-id="74fb6-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="74fb6-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74fb6-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74fb6-128">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="74fb6-128">Type: **int**</span></span>

<span data-ttu-id="74fb6-129">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="74fb6-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="74fb6-130">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="74fb6-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="74fb6-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="74fb6-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="74fb6-132">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="74fb6-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="74fb6-133">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74fb6-133">Texture-Object Type</span></span>           | <span data-ttu-id="74fb6-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="74fb6-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="74fb6-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="74fb6-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="74fb6-136">INT</span><span class="sxs-lookup"><span data-stu-id="74fb6-136">int</span></span>            |
| <span data-ttu-id="74fb6-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="74fb6-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="74fb6-138">int2</span><span class="sxs-lookup"><span data-stu-id="74fb6-138">int2</span></span>           |
| <span data-ttu-id="74fb6-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="74fb6-139">Texture3D</span></span>                     | <span data-ttu-id="74fb6-140">int3</span><span class="sxs-lookup"><span data-stu-id="74fb6-140">int3</span></span>           |
| <span data-ttu-id="74fb6-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74fb6-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="74fb6-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="74fb6-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="74fb6-143">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74fb6-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74fb6-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74fb6-144">Type: **float**</span></span>

<span data-ttu-id="74fb6-145">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="74fb6-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="74fb6-146">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="74fb6-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74fb6-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74fb6-147">Return value</span></span>

<span data-ttu-id="74fb6-148">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="74fb6-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="74fb6-149">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="74fb6-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="74fb6-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74fb6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74fb6-151">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="74fb6-151">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
