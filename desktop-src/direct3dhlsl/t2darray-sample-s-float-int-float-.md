---
title: 'Funzione Texture2DArray:: Sample (S, float, int, float)'
description: 'Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione Texture2DArray:: Sample (S, float, int, float)'
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
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
ms.openlocfilehash: 8d85e4d7e5662d76c011b1c5684f3fd36e4191ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234692"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a><span data-ttu-id="ae0b5-105">Funzione Texture2DArray:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="ae0b5-105">Texture2DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="ae0b5-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae0b5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae0b5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="ae0b5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae0b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae0b5-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae0b5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae0b5-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ae0b5-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ae0b5-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ae0b5-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae0b5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae0b5-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-113">The texture coordinates.</span></span> <span data-ttu-id="ae0b5-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ae0b5-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ae0b5-115">Texture-Object Type</span></span>                    | <span data-ttu-id="ae0b5-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ae0b5-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ae0b5-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ae0b5-117">Texture1D</span></span>                              | <span data-ttu-id="ae0b5-118">float</span><span class="sxs-lookup"><span data-stu-id="ae0b5-118">float</span></span>          |
| <span data-ttu-id="ae0b5-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ae0b5-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ae0b5-120">float2</span><span class="sxs-lookup"><span data-stu-id="ae0b5-120">float2</span></span>         |
| <span data-ttu-id="ae0b5-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ae0b5-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ae0b5-122">float3</span><span class="sxs-lookup"><span data-stu-id="ae0b5-122">float3</span></span>         |
| <span data-ttu-id="ae0b5-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ae0b5-123">TextureCubeArray</span></span>                       | <span data-ttu-id="ae0b5-124">float4</span><span class="sxs-lookup"><span data-stu-id="ae0b5-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ae0b5-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae0b5-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae0b5-126">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ae0b5-127">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ae0b5-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ae0b5-129">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ae0b5-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ae0b5-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ae0b5-130">Texture-Object Type</span></span>           | <span data-ttu-id="ae0b5-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ae0b5-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ae0b5-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ae0b5-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ae0b5-133">INT</span><span class="sxs-lookup"><span data-stu-id="ae0b5-133">int</span></span>            |
| <span data-ttu-id="ae0b5-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ae0b5-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ae0b5-135">int2</span><span class="sxs-lookup"><span data-stu-id="ae0b5-135">int2</span></span>           |
| <span data-ttu-id="ae0b5-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ae0b5-136">Texture3D</span></span>                     | <span data-ttu-id="ae0b5-137">int3</span><span class="sxs-lookup"><span data-stu-id="ae0b5-137">int3</span></span>           |
| <span data-ttu-id="ae0b5-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ae0b5-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ae0b5-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="ae0b5-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ae0b5-140">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae0b5-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae0b5-141">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ae0b5-142">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ae0b5-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae0b5-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae0b5-143">Return value</span></span>

<span data-ttu-id="ae0b5-144">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ae0b5-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae0b5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae0b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae0b5-146">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="ae0b5-146">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
