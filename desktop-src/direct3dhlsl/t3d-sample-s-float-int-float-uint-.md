---
title: 'Funzione Texture3D:: Sample (S, float, int, float, uint)'
description: "Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione. | Funzione Texture3D:: Sample (S, float, int, float, uint)"
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995341"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="2637b-105">Funzione Texture3D:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="2637b-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="2637b-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2637b-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2637b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2637b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2637b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2637b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2637b-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2637b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2637b-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2637b-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2637b-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="2637b-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2637b-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2637b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2637b-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2637b-113">The texture coordinates.</span></span> <span data-ttu-id="2637b-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2637b-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2637b-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2637b-115">Texture-Object Type</span></span>                    | <span data-ttu-id="2637b-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2637b-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2637b-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2637b-117">Texture1D</span></span>                              | <span data-ttu-id="2637b-118">float</span><span class="sxs-lookup"><span data-stu-id="2637b-118">float</span></span>          |
| <span data-ttu-id="2637b-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2637b-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2637b-120">float2</span><span class="sxs-lookup"><span data-stu-id="2637b-120">float2</span></span>         |
| <span data-ttu-id="2637b-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2637b-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2637b-122">float3</span><span class="sxs-lookup"><span data-stu-id="2637b-122">float3</span></span>         |
| <span data-ttu-id="2637b-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2637b-123">TextureCubeArray</span></span>                       | <span data-ttu-id="2637b-124">float4</span><span class="sxs-lookup"><span data-stu-id="2637b-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2637b-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2637b-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2637b-126">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2637b-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2637b-127">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2637b-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2637b-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2637b-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2637b-129">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2637b-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2637b-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2637b-130">Texture-Object Type</span></span>           | <span data-ttu-id="2637b-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2637b-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2637b-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2637b-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2637b-133">INT</span><span class="sxs-lookup"><span data-stu-id="2637b-133">int</span></span>            |
| <span data-ttu-id="2637b-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2637b-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2637b-135">int2</span><span class="sxs-lookup"><span data-stu-id="2637b-135">int2</span></span>           |
| <span data-ttu-id="2637b-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2637b-136">Texture3D</span></span>                     | <span data-ttu-id="2637b-137">int3</span><span class="sxs-lookup"><span data-stu-id="2637b-137">int3</span></span>           |
| <span data-ttu-id="2637b-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2637b-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2637b-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="2637b-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2637b-140">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2637b-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2637b-141">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="2637b-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2637b-142">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2637b-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="2637b-143">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2637b-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2637b-144">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2637b-144">The status of the operation.</span></span> <span data-ttu-id="2637b-145">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2637b-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2637b-146">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2637b-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2637b-147">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2637b-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2637b-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2637b-148">Return value</span></span>

<span data-ttu-id="2637b-149">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2637b-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2637b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2637b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2637b-151">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="2637b-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="2637b-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="2637b-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
