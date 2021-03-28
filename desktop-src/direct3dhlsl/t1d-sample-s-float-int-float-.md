---
title: 'Funzione Texture1D:: Sample (S, float, int, float)'
description: 'Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione Texture1D:: Sample (S, float, int, float)'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
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
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058546"
---
# <a name="texture1dsamplesfloatintfloat-function"></a><span data-ttu-id="d629e-105">Funzione Texture1D:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="d629e-105">Texture1D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="d629e-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="d629e-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="d629e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d629e-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="d629e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d629e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d629e-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d629e-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d629e-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d629e-110">Type: **SamplerState**</span></span>

<span data-ttu-id="d629e-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d629e-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d629e-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="d629e-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d629e-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d629e-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d629e-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d629e-114">Type: **float**</span></span>

<span data-ttu-id="d629e-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="d629e-115">The texture coordinates.</span></span> <span data-ttu-id="d629e-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d629e-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d629e-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d629e-117">Texture-Object Type</span></span>                    | <span data-ttu-id="d629e-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d629e-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d629e-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d629e-119">Texture1D</span></span>                              | <span data-ttu-id="d629e-120">float</span><span class="sxs-lookup"><span data-stu-id="d629e-120">float</span></span>          |
| <span data-ttu-id="d629e-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d629e-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d629e-122">float2</span><span class="sxs-lookup"><span data-stu-id="d629e-122">float2</span></span>         |
| <span data-ttu-id="d629e-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d629e-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d629e-124">float3</span><span class="sxs-lookup"><span data-stu-id="d629e-124">float3</span></span>         |
| <span data-ttu-id="d629e-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d629e-125">TextureCubeArray</span></span>                       | <span data-ttu-id="d629e-126">float4</span><span class="sxs-lookup"><span data-stu-id="d629e-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d629e-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d629e-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d629e-128">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d629e-128">Type: **int**</span></span>

<span data-ttu-id="d629e-129">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="d629e-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d629e-130">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d629e-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d629e-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d629e-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d629e-132">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d629e-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d629e-133">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d629e-133">Texture-Object Type</span></span>           | <span data-ttu-id="d629e-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d629e-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d629e-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d629e-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d629e-136">INT</span><span class="sxs-lookup"><span data-stu-id="d629e-136">int</span></span>            |
| <span data-ttu-id="d629e-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d629e-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d629e-138">int2</span><span class="sxs-lookup"><span data-stu-id="d629e-138">int2</span></span>           |
| <span data-ttu-id="d629e-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d629e-139">Texture3D</span></span>                     | <span data-ttu-id="d629e-140">int3</span><span class="sxs-lookup"><span data-stu-id="d629e-140">int3</span></span>           |
| <span data-ttu-id="d629e-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d629e-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d629e-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="d629e-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d629e-143">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d629e-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d629e-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d629e-144">Type: **float**</span></span>

<span data-ttu-id="d629e-145">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="d629e-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d629e-146">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="d629e-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d629e-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d629e-147">Return value</span></span>

<span data-ttu-id="d629e-148">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d629e-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d629e-149">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d629e-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d629e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d629e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d629e-151">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="d629e-151">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
