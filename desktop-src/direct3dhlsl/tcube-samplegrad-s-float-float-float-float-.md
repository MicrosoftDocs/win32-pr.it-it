---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, float) per TextureCube'
description: Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
keywords:
- Funzione SampleGrad HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531122"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="96b5f-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, float) per TextureCube</span><span class="sxs-lookup"><span data-stu-id="96b5f-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="96b5f-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="96b5f-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b5f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96b5f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="96b5f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96b5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b5f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96b5f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b5f-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="96b5f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="96b5f-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="96b5f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="96b5f-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="96b5f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="96b5f-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96b5f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b5f-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="96b5f-114">Type: **float**</span></span>

<span data-ttu-id="96b5f-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="96b5f-115">The texture coordinates.</span></span> <span data-ttu-id="96b5f-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="96b5f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="96b5f-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="96b5f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="96b5f-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="96b5f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="96b5f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="96b5f-119">Texture1D</span></span>                              | <span data-ttu-id="96b5f-120">float</span><span class="sxs-lookup"><span data-stu-id="96b5f-120">float</span></span>          |
| <span data-ttu-id="96b5f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="96b5f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="96b5f-122">float2</span><span class="sxs-lookup"><span data-stu-id="96b5f-122">float2</span></span>         |
| <span data-ttu-id="96b5f-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="96b5f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="96b5f-124">float3</span><span class="sxs-lookup"><span data-stu-id="96b5f-124">float3</span></span>         |
| <span data-ttu-id="96b5f-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="96b5f-126">float4</span><span class="sxs-lookup"><span data-stu-id="96b5f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="96b5f-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96b5f-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b5f-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="96b5f-128">Type: **float**</span></span>

<span data-ttu-id="96b5f-129">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="96b5f-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="96b5f-130">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="96b5f-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="96b5f-131">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="96b5f-131">Texture-Object Type</span></span>                      | <span data-ttu-id="96b5f-132">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="96b5f-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="96b5f-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="96b5f-134">float</span><span class="sxs-lookup"><span data-stu-id="96b5f-134">float</span></span>          |
| <span data-ttu-id="96b5f-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="96b5f-136">float2</span><span class="sxs-lookup"><span data-stu-id="96b5f-136">float2</span></span>         |
| <span data-ttu-id="96b5f-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="96b5f-138">float3</span><span class="sxs-lookup"><span data-stu-id="96b5f-138">float3</span></span>         |
| <span data-ttu-id="96b5f-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="96b5f-140">non supportato</span><span class="sxs-lookup"><span data-stu-id="96b5f-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="96b5f-141">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96b5f-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b5f-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="96b5f-142">Type: **float**</span></span>

<span data-ttu-id="96b5f-143">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="96b5f-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="96b5f-144">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="96b5f-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="96b5f-145">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="96b5f-145">Texture-Object Type</span></span>                      | <span data-ttu-id="96b5f-146">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="96b5f-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="96b5f-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="96b5f-148">float</span><span class="sxs-lookup"><span data-stu-id="96b5f-148">float</span></span>          |
| <span data-ttu-id="96b5f-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="96b5f-150">float2</span><span class="sxs-lookup"><span data-stu-id="96b5f-150">float2</span></span>         |
| <span data-ttu-id="96b5f-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="96b5f-152">float3</span><span class="sxs-lookup"><span data-stu-id="96b5f-152">float3</span></span>         |
| <span data-ttu-id="96b5f-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="96b5f-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="96b5f-154">non supportato</span><span class="sxs-lookup"><span data-stu-id="96b5f-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="96b5f-155">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96b5f-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b5f-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="96b5f-156">Type: **float**</span></span>

<span data-ttu-id="96b5f-157">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="96b5f-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="96b5f-158">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="96b5f-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b5f-159">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96b5f-159">Return value</span></span>

<span data-ttu-id="96b5f-160">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="96b5f-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="96b5f-161">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="96b5f-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="96b5f-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96b5f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b5f-163">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="96b5f-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="96b5f-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="96b5f-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
