---
title: 'Funzione Texture2DArray:: Sample (S, float, int, float, uint)'
description: "Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione. | Funzione Texture2DArray:: Sample (S, float, int, float, uint)"
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
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
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981194"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="44d35-105">Funzione Texture2DArray:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="44d35-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="44d35-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="44d35-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d35-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44d35-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="44d35-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="44d35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d35-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d35-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d35-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="44d35-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="44d35-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="44d35-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="44d35-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d35-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d35-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="44d35-113">The texture coordinates.</span></span> <span data-ttu-id="44d35-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="44d35-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="44d35-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="44d35-115">Texture-Object Type</span></span>                    | <span data-ttu-id="44d35-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="44d35-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="44d35-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="44d35-117">Texture1D</span></span>                              | <span data-ttu-id="44d35-118">float</span><span class="sxs-lookup"><span data-stu-id="44d35-118">float</span></span>          |
| <span data-ttu-id="44d35-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="44d35-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="44d35-120">float2</span><span class="sxs-lookup"><span data-stu-id="44d35-120">float2</span></span>         |
| <span data-ttu-id="44d35-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="44d35-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="44d35-122">float3</span><span class="sxs-lookup"><span data-stu-id="44d35-122">float3</span></span>         |
| <span data-ttu-id="44d35-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="44d35-123">TextureCubeArray</span></span>                       | <span data-ttu-id="44d35-124">float4</span><span class="sxs-lookup"><span data-stu-id="44d35-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="44d35-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d35-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d35-126">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="44d35-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="44d35-127">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="44d35-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="44d35-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="44d35-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="44d35-129">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="44d35-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="44d35-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="44d35-130">Texture-Object Type</span></span>           | <span data-ttu-id="44d35-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="44d35-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="44d35-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="44d35-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="44d35-133">INT</span><span class="sxs-lookup"><span data-stu-id="44d35-133">int</span></span>            |
| <span data-ttu-id="44d35-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="44d35-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="44d35-135">int2</span><span class="sxs-lookup"><span data-stu-id="44d35-135">int2</span></span>           |
| <span data-ttu-id="44d35-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="44d35-136">Texture3D</span></span>                     | <span data-ttu-id="44d35-137">int3</span><span class="sxs-lookup"><span data-stu-id="44d35-137">int3</span></span>           |
| <span data-ttu-id="44d35-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="44d35-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="44d35-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="44d35-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="44d35-140">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d35-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d35-141">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="44d35-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="44d35-142">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="44d35-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="44d35-143">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="44d35-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44d35-144">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="44d35-144">The status of the operation.</span></span> <span data-ttu-id="44d35-145">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="44d35-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="44d35-146">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="44d35-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="44d35-147">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="44d35-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d35-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44d35-148">Return value</span></span>

<span data-ttu-id="44d35-149">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="44d35-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="44d35-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44d35-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d35-151">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="44d35-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
