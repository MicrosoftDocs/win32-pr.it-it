---
title: Funzione Sample (S, float, int, float) (riferimento HLSL)
description: Esegue il campionamento di un Texture2D con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
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
ms.openlocfilehash: e5c151c3d93f5e2fe374f0f60fd06798cf1ce52a
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104118694"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a><span data-ttu-id="fe4dd-104">Funzione Sample (S, float, int, float) (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe4dd-104">Sample(S,float,int,float) function (HLSL reference)</span></span>

<span data-ttu-id="fe4dd-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md) con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

> [!Note]  
> <span data-ttu-id="fe4dd-106">Richiede il [modello di shader 5](d3d11-graphics-reference-sm5.md) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe4dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe4dd-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a><span data-ttu-id="fe4dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe4dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe4dd-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe4dd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe4dd-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fe4dd-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fe4dd-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fe4dd-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe4dd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe4dd-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-113">The texture coordinates.</span></span> <span data-ttu-id="fe4dd-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fe4dd-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fe4dd-115">Texture-Object Type</span></span>                    | <span data-ttu-id="fe4dd-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="fe4dd-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fe4dd-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fe4dd-117">Texture1D</span></span>                              | <span data-ttu-id="fe4dd-118">float</span><span class="sxs-lookup"><span data-stu-id="fe4dd-118">float</span></span>          |
| <span data-ttu-id="fe4dd-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fe4dd-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fe4dd-120">float2</span><span class="sxs-lookup"><span data-stu-id="fe4dd-120">float2</span></span>         |
| <span data-ttu-id="fe4dd-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fe4dd-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fe4dd-122">float3</span><span class="sxs-lookup"><span data-stu-id="fe4dd-122">float3</span></span>         |
| <span data-ttu-id="fe4dd-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fe4dd-123">TextureCubeArray</span></span>                       | <span data-ttu-id="fe4dd-124">float4</span><span class="sxs-lookup"><span data-stu-id="fe4dd-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fe4dd-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe4dd-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe4dd-126">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fe4dd-127">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-127">The texture offsets need to be static.</span></span> <span data-ttu-id="fe4dd-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fe4dd-129">Per altre informazioni, vedere [applicazione degli offset delle coordinate di trama](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fe4dd-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fe4dd-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fe4dd-130">Texture-Object Type</span></span>           | <span data-ttu-id="fe4dd-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="fe4dd-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fe4dd-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fe4dd-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fe4dd-133">INT</span><span class="sxs-lookup"><span data-stu-id="fe4dd-133">int</span></span>            |
| <span data-ttu-id="fe4dd-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fe4dd-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fe4dd-135">int2</span><span class="sxs-lookup"><span data-stu-id="fe4dd-135">int2</span></span>           |
| <span data-ttu-id="fe4dd-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fe4dd-136">Texture3D</span></span>                     | <span data-ttu-id="fe4dd-137">int3</span><span class="sxs-lookup"><span data-stu-id="fe4dd-137">int3</span></span>           |
| <span data-ttu-id="fe4dd-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fe4dd-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fe4dd-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="fe4dd-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fe4dd-140">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe4dd-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe4dd-141">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fe4dd-142">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe4dd-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe4dd-143">Return value</span></span>

<span data-ttu-id="fe4dd-144">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fe4dd-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe4dd-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe4dd-145">Remarks</span></span>

<span data-ttu-id="fe4dd-146">Il campionamento della trama usa la posizione di Texel per cercare un valore di Texel.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-146">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="fe4dd-147">Un offset può essere applicato alla posizione prima della ricerca.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-147">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="fe4dd-148">Lo stato del campionatore contiene le opzioni di campionamento e filtro.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-148">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="fe4dd-149">Questo metodo può essere richiamato all'interno di una pixel shader, ma non è supportato in un vertex shader o in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-149">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="fe4dd-150">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-150">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="fe4dd-151">Calcolo delle posizioni di Texel</span><span class="sxs-lookup"><span data-stu-id="fe4dd-151">Calculating Texel Positions</span></span>

<span data-ttu-id="fe4dd-152">Le coordinate di trama sono valori a virgola mobile che fanno riferimento a dati di trama, noti anche come spazio di trama normalizzato.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-152">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="fe4dd-153">Le modalità di wrapping degli indirizzi vengono applicate in questo ordine (coordinate di trama + offset + modalità a capo) per modificare le coordinate di trama al di fuori dell' \[ intervallo 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4dd-153">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="fe4dd-154">Per le matrici di trama, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-154">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="fe4dd-155">Questo indice viene considerato come valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-155">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="fe4dd-156">La conversione in un indice Integer viene eseguita nell'ordine seguente (float + round-to-more-even integer + Clamp nell'intervallo di matrici).</span><span class="sxs-lookup"><span data-stu-id="fe4dd-156">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="fe4dd-157">Applicazione degli offset delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="fe4dd-157">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="fe4dd-158">Il parametro offset modifica le coordinate di trama, nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-158">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="fe4dd-159">Anche se le coordinate di trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-159">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="fe4dd-160">Si noti inoltre che gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-160">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="fe4dd-161">Il formato di dati restituito è determinato dal formato di trama.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-161">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="fe4dd-162">Se, ad esempio, la risorsa di trama è stata definita con il formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB format, l'operazione di campionamento converte i Texel campionati da gamma 2,0 a 1,0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4dd-162">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="fe4dd-163">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="fe4dd-163">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe4dd-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe4dd-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4dd-165">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="fe4dd-165">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="fe4dd-166">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="fe4dd-166">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
