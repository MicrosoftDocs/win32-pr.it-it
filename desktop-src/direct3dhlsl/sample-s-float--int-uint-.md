---
title: Funzione Sample (S, float, int, float, uint) (riferimento HLSL)
description: Esegue il campionamento di un Texture2D con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "103735218"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a><span data-ttu-id="483ed-104">Funzione Sample (S, float, int, float, uint) (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="483ed-104">Sample(S,float,int,float,uint) function (HLSL reference)</span></span>

<span data-ttu-id="483ed-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md) con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="483ed-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="483ed-106">Richiede il [modello di shader 5](d3d11-graphics-reference-sm5.md) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="483ed-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="483ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="483ed-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="483ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="483ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="483ed-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="483ed-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="483ed-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="483ed-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="483ed-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="483ed-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="483ed-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="483ed-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="483ed-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="483ed-113">The texture coordinates.</span></span> <span data-ttu-id="483ed-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="483ed-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="483ed-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="483ed-115">Texture-Object Type</span></span>                    | <span data-ttu-id="483ed-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="483ed-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="483ed-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="483ed-117">Texture1D</span></span>                              | <span data-ttu-id="483ed-118">float</span><span class="sxs-lookup"><span data-stu-id="483ed-118">float</span></span>          |
| <span data-ttu-id="483ed-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="483ed-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="483ed-120">float2</span><span class="sxs-lookup"><span data-stu-id="483ed-120">float2</span></span>         |
| <span data-ttu-id="483ed-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="483ed-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="483ed-122">float3</span><span class="sxs-lookup"><span data-stu-id="483ed-122">float3</span></span>         |
| <span data-ttu-id="483ed-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="483ed-123">TextureCubeArray</span></span>                       | <span data-ttu-id="483ed-124">float4</span><span class="sxs-lookup"><span data-stu-id="483ed-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="483ed-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="483ed-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="483ed-126">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="483ed-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="483ed-127">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="483ed-127">The texture offsets need to be static.</span></span> <span data-ttu-id="483ed-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="483ed-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="483ed-129">Per altre informazioni, vedere [applicazione degli offset delle coordinate di trama](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="483ed-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="483ed-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="483ed-130">Texture-Object Type</span></span>           | <span data-ttu-id="483ed-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="483ed-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="483ed-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="483ed-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="483ed-133">INT</span><span class="sxs-lookup"><span data-stu-id="483ed-133">int</span></span>            |
| <span data-ttu-id="483ed-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="483ed-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="483ed-135">int2</span><span class="sxs-lookup"><span data-stu-id="483ed-135">int2</span></span>           |
| <span data-ttu-id="483ed-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="483ed-136">Texture3D</span></span>                     | <span data-ttu-id="483ed-137">int3</span><span class="sxs-lookup"><span data-stu-id="483ed-137">int3</span></span>           |
| <span data-ttu-id="483ed-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="483ed-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="483ed-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="483ed-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="483ed-140">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="483ed-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="483ed-141">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="483ed-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="483ed-142">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="483ed-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="483ed-143">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="483ed-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="483ed-144">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="483ed-144">The status of the operation.</span></span> <span data-ttu-id="483ed-145">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="483ed-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="483ed-146">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="483ed-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="483ed-147">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="483ed-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="483ed-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="483ed-148">Return value</span></span>

<span data-ttu-id="483ed-149">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="483ed-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="483ed-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="483ed-150">Remarks</span></span>

<span data-ttu-id="483ed-151">Il campionamento della trama usa la posizione di Texel per cercare un valore di Texel.</span><span class="sxs-lookup"><span data-stu-id="483ed-151">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="483ed-152">Un offset può essere applicato alla posizione prima della ricerca.</span><span class="sxs-lookup"><span data-stu-id="483ed-152">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="483ed-153">Lo stato del campionatore contiene le opzioni di campionamento e filtro.</span><span class="sxs-lookup"><span data-stu-id="483ed-153">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="483ed-154">Questo metodo può essere richiamato all'interno di una pixel shader, ma non è supportato in un vertex shader o in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="483ed-154">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="483ed-155">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="483ed-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="483ed-156">Calcolo delle posizioni di Texel</span><span class="sxs-lookup"><span data-stu-id="483ed-156">Calculating Texel Positions</span></span>

<span data-ttu-id="483ed-157">Le coordinate di trama sono valori a virgola mobile che fanno riferimento a dati di trama, noti anche come spazio di trama normalizzato.</span><span class="sxs-lookup"><span data-stu-id="483ed-157">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="483ed-158">Le modalità di wrapping degli indirizzi vengono applicate in questo ordine (coordinate di trama + offset + modalità a capo) per modificare le coordinate di trama al di fuori dell' \[ intervallo 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="483ed-158">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="483ed-159">Per le matrici di trama, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="483ed-159">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="483ed-160">Questo indice viene considerato come valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard.</span><span class="sxs-lookup"><span data-stu-id="483ed-160">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="483ed-161">La conversione in un indice Integer viene eseguita nell'ordine seguente (float + round-to-more-even integer + Clamp nell'intervallo di matrici).</span><span class="sxs-lookup"><span data-stu-id="483ed-161">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="483ed-162">Applicazione degli offset delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="483ed-162">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="483ed-163">Il parametro offset modifica le coordinate di trama, nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="483ed-163">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="483ed-164">Anche se le coordinate di trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero.</span><span class="sxs-lookup"><span data-stu-id="483ed-164">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="483ed-165">Si noti inoltre che gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="483ed-165">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="483ed-166">Il formato di dati restituito è determinato dal formato di trama.</span><span class="sxs-lookup"><span data-stu-id="483ed-166">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="483ed-167">Se, ad esempio, la risorsa di trama è stata definita con il formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB format, l'operazione di campionamento converte i Texel campionati da gamma 2,0 a 1,0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="483ed-167">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="see-also"></a><span data-ttu-id="483ed-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="483ed-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="483ed-169">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="483ed-169">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="483ed-170">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="483ed-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
