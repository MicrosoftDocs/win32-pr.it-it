---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, int, float, uint) per Texture2D'
description: Informazioni su come questa funzione esegue il campionamento di un Texture2D, usando un valore di confronto per rifiutare gli esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Restituisce lo stato dell'operazione.
ms.assetid: 039EA69B-DFE0-4351-963A-C0326FDEF844
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
ms.openlocfilehash: 4b4667594a4b4eeaf9e533338411b79810fee5eb
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982779"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="b70b2-105">Funzione SampleCmp:: SampleCmp (S, float, float, int, float, uint) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="b70b2-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="b70b2-106">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md), usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="b70b2-106">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="b70b2-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b70b2-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b70b2-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b70b2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b70b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70b2-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b70b2-111">Type: **SamplerState**</span></span>

<span data-ttu-id="b70b2-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b70b2-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b70b2-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="b70b2-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b70b2-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b70b2-115">Type: **float**</span></span>

<span data-ttu-id="b70b2-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="b70b2-116">The texture coordinates.</span></span> <span data-ttu-id="b70b2-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="b70b2-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b70b2-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b70b2-118">Texture-Object Type</span></span>                    | <span data-ttu-id="b70b2-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="b70b2-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b70b2-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b70b2-120">Texture1D</span></span>                              | <span data-ttu-id="b70b2-121">float</span><span class="sxs-lookup"><span data-stu-id="b70b2-121">float</span></span>          |
| <span data-ttu-id="b70b2-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b70b2-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b70b2-123">float2</span><span class="sxs-lookup"><span data-stu-id="b70b2-123">float2</span></span>         |
| <span data-ttu-id="b70b2-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b70b2-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b70b2-125">float3</span><span class="sxs-lookup"><span data-stu-id="b70b2-125">float3</span></span>         |
| <span data-ttu-id="b70b2-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b70b2-126">TextureCubeArray</span></span>                       | <span data-ttu-id="b70b2-127">float4</span><span class="sxs-lookup"><span data-stu-id="b70b2-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b70b2-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b70b2-129">Type: **float**</span></span>

<span data-ttu-id="b70b2-130">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b70b2-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="b70b2-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b70b2-132">Type: **int**</span></span>

<span data-ttu-id="b70b2-133">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="b70b2-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b70b2-134">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b70b2-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="b70b2-135">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="b70b2-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b70b2-136">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b70b2-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b70b2-137">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b70b2-137">Texture-Object Type</span></span>           | <span data-ttu-id="b70b2-138">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="b70b2-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b70b2-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b70b2-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b70b2-140">INT</span><span class="sxs-lookup"><span data-stu-id="b70b2-140">int</span></span>            |
| <span data-ttu-id="b70b2-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b70b2-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b70b2-142">int2</span><span class="sxs-lookup"><span data-stu-id="b70b2-142">int2</span></span>           |
| <span data-ttu-id="b70b2-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b70b2-143">Texture3D</span></span>                     | <span data-ttu-id="b70b2-144">int3</span><span class="sxs-lookup"><span data-stu-id="b70b2-144">int3</span></span>           |
| <span data-ttu-id="b70b2-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b70b2-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b70b2-146">non supportato</span><span class="sxs-lookup"><span data-stu-id="b70b2-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b70b2-147">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b70b2-148">Type: **float**</span></span>

<span data-ttu-id="b70b2-149">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="b70b2-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b70b2-150">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b70b2-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b70b2-151">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b70b2-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b70b2-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b70b2-152">Type: **uint**</span></span>

<span data-ttu-id="b70b2-153">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b70b2-153">The status of the operation.</span></span> <span data-ttu-id="b70b2-154">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b70b2-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b70b2-155">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b70b2-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b70b2-156">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="b70b2-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70b2-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b70b2-157">Return value</span></span>

<span data-ttu-id="b70b2-158">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b70b2-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b70b2-159">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b70b2-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b70b2-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b70b2-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70b2-161">Metodi SampleCmp</span><span class="sxs-lookup"><span data-stu-id="b70b2-161">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
