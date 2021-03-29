---
title: 'Funzione SampleLevel:: SampleLevel (S, float, float, int, uint) per Texture2D'
description: Esegue il campionamento di un Texture2D sul livello mipmap specificato e restituisce lo stato dell'operazione.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
keywords:
- Funzione SampleLevel HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996409"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="3cc39-104">Funzione SampleLevel:: SampleLevel (S, float, float, int, uint) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="3cc39-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="3cc39-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md) sul livello mipmap specificato e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3cc39-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc39-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cc39-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3cc39-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cc39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc39-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cc39-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc39-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3cc39-109">Type: **SamplerState**</span></span>

<span data-ttu-id="3cc39-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3cc39-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3cc39-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="3cc39-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3cc39-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cc39-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc39-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3cc39-113">Type: **float**</span></span>

<span data-ttu-id="3cc39-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3cc39-114">The texture coordinates.</span></span> <span data-ttu-id="3cc39-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3cc39-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3cc39-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3cc39-116">Texture-Object Type</span></span>                    | <span data-ttu-id="3cc39-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3cc39-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3cc39-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3cc39-118">Texture1D</span></span>                              | <span data-ttu-id="3cc39-119">float</span><span class="sxs-lookup"><span data-stu-id="3cc39-119">float</span></span>          |
| <span data-ttu-id="3cc39-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3cc39-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3cc39-121">float2</span><span class="sxs-lookup"><span data-stu-id="3cc39-121">float2</span></span>         |
| <span data-ttu-id="3cc39-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3cc39-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3cc39-123">float3</span><span class="sxs-lookup"><span data-stu-id="3cc39-123">float3</span></span>         |
| <span data-ttu-id="3cc39-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cc39-124">TextureCubeArray</span></span>                       | <span data-ttu-id="3cc39-125">float4</span><span class="sxs-lookup"><span data-stu-id="3cc39-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3cc39-126">*LOD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cc39-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc39-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3cc39-127">Type: **float**</span></span>

<span data-ttu-id="3cc39-128">\[in \] un numero che specifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="3cc39-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="3cc39-129">Se il valore è ≤ 0, viene usato il livello mipmap 0 (mapping più grande).</span><span class="sxs-lookup"><span data-stu-id="3cc39-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="3cc39-130">Il valore frazionario (se fornito) viene usato per interpolare tra due livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="3cc39-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="3cc39-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cc39-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc39-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3cc39-132">Type: **int**</span></span>

<span data-ttu-id="3cc39-133">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="3cc39-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3cc39-134">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="3cc39-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3cc39-135">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3cc39-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3cc39-136">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3cc39-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3cc39-137">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3cc39-137">Texture-Object Type</span></span>           | <span data-ttu-id="3cc39-138">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3cc39-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3cc39-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3cc39-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3cc39-140">INT</span><span class="sxs-lookup"><span data-stu-id="3cc39-140">int</span></span>            |
| <span data-ttu-id="3cc39-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3cc39-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3cc39-142">int2</span><span class="sxs-lookup"><span data-stu-id="3cc39-142">int2</span></span>           |
| <span data-ttu-id="3cc39-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3cc39-143">Texture3D</span></span>                     | <span data-ttu-id="3cc39-144">int3</span><span class="sxs-lookup"><span data-stu-id="3cc39-144">int3</span></span>           |
| <span data-ttu-id="3cc39-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cc39-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3cc39-146">non supportato</span><span class="sxs-lookup"><span data-stu-id="3cc39-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3cc39-147">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3cc39-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc39-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cc39-148">Type: **uint**</span></span>

<span data-ttu-id="3cc39-149">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3cc39-149">The status of the operation.</span></span> <span data-ttu-id="3cc39-150">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3cc39-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3cc39-151">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3cc39-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3cc39-152">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="3cc39-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc39-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cc39-153">Return value</span></span>

<span data-ttu-id="3cc39-154">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3cc39-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3cc39-155">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3cc39-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3cc39-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cc39-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc39-157">Metodi SampleLevel</span><span class="sxs-lookup"><span data-stu-id="3cc39-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
