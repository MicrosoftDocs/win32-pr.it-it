---
title: SampleCmp (oggetto trama di DirectX HLSL)
description: Esegue il campionamento di una trama e confronta un singolo componente con il valore di confronto specificato.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104993653"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="a4676-103">SampleCmp (oggetto trama di DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4676-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="a4676-104">Esegue il campionamento di una trama e confronta un singolo componente con il valore di confronto specificato.</span><span class="sxs-lookup"><span data-stu-id="a4676-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4676-105">float Object. SampleCmp (</span><span class="sxs-lookup"><span data-stu-id="a4676-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="a4676-106">SamplerComparisonState S,</span><span class="sxs-lookup"><span data-stu-id="a4676-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="a4676-107">Percorso float,</span><span class="sxs-lookup"><span data-stu-id="a4676-107">float Location,</span></span><br />
<span data-ttu-id="a4676-108">float CompareValue,</span><span class="sxs-lookup"><span data-stu-id="a4676-108">float CompareValue,</span></span><br />
<span data-ttu-id="a4676-109">[offset int]</span><span class="sxs-lookup"><span data-stu-id="a4676-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="a4676-110">);</span><span class="sxs-lookup"><span data-stu-id="a4676-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="a4676-111">Il confronto è un confronto a componente singolo tra il primo componente archiviato nella trama e il valore di confronto passato nel metodo.</span><span class="sxs-lookup"><span data-stu-id="a4676-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="a4676-112">Questo metodo può essere richiamato solo da un pixel shader; non è supportato in un vertex o in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="a4676-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4676-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4676-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4676-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="a4676-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="a4676-115">Qualsiasi tipo [di oggetto trama](dx-graphics-hlsl-to-type.md) (ad eccezione di Texture2DMS, Texture2DMSArray o Texture3D).</span><span class="sxs-lookup"><span data-stu-id="a4676-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="a4676-116"><span id="S"></span><span id="s"></span>*S*</span><span class="sxs-lookup"><span data-stu-id="a4676-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="a4676-117">\[in \] uno stato di confronto del campionatore, ovvero lo stato del campionatore più uno stato di confronto (una funzione di confronto e un filtro di confronto).</span><span class="sxs-lookup"><span data-stu-id="a4676-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="a4676-118">Per informazioni dettagliate e un esempio, vedere il [tipo di campionatore](dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="a4676-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="a4676-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Percorso*</span><span class="sxs-lookup"><span data-stu-id="a4676-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="a4676-120">\[nelle \] coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="a4676-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="a4676-121">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="a4676-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="a4676-122">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a4676-122">Texture-Object Type</span></span>          | <span data-ttu-id="a4676-123">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="a4676-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="a4676-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a4676-124">Texture1D</span></span>                    | <span data-ttu-id="a4676-125">float</span><span class="sxs-lookup"><span data-stu-id="a4676-125">float</span></span>          |
| <span data-ttu-id="a4676-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a4676-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="a4676-127">float2</span><span class="sxs-lookup"><span data-stu-id="a4676-127">float2</span></span>         |
| <span data-ttu-id="a4676-128">Texture2DArray ¹, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a4676-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="a4676-129">float3</span><span class="sxs-lookup"><span data-stu-id="a4676-129">float3</span></span>         |
| <span data-ttu-id="a4676-130">TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="a4676-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="a4676-131">float4</span><span class="sxs-lookup"><span data-stu-id="a4676-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="a4676-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span><span class="sxs-lookup"><span data-stu-id="a4676-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="a4676-133">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="a4676-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a4676-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span><span class="sxs-lookup"><span data-stu-id="a4676-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="a4676-135">\[in \] un offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="a4676-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a4676-136">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="a4676-136">The texture offsets need to be static.</span></span> <span data-ttu-id="a4676-137">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="a4676-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a4676-138">Per altre informazioni, vedere [applicazione degli offset delle coordinate di trama](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a4676-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="a4676-139">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a4676-139">Texture-Object Type</span></span>            | <span data-ttu-id="a4676-140">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="a4676-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="a4676-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a4676-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="a4676-142">INT</span><span class="sxs-lookup"><span data-stu-id="a4676-142">int</span></span>            |
| <span data-ttu-id="a4676-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="a4676-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="a4676-144">int2</span><span class="sxs-lookup"><span data-stu-id="a4676-144">int2</span></span>           |
| <span data-ttu-id="a4676-145">TextureCube, TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="a4676-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="a4676-146">Non supportato</span><span class="sxs-lookup"><span data-stu-id="a4676-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4676-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4676-147">Return Value</span></span>

<span data-ttu-id="a4676-148">Restituisce un valore a virgola mobile nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a4676-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="a4676-149">Per ogni Texel recuperato (in base alla configurazione campionatore della modalità filtro), **SampleCmp** esegue un confronto del valore z (terzo componente di input) dallo shader rispetto al valore Texel (1 se il confronto passa; in caso contrario 0).</span><span class="sxs-lookup"><span data-stu-id="a4676-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="a4676-150">**SampleCmp** combina quindi i risultati 0 e 1 per ogni Texel insieme al normale filtro della trama (non una media) e restituisce il \[ valore 0.. 1 risultante \] allo shader.</span><span class="sxs-lookup"><span data-stu-id="a4676-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4676-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4676-151">Remarks</span></span>

<span data-ttu-id="a4676-152">Il filtro di confronto fornisce un'operazione di filtro di base che risulta utile per l'applicazione di filtri con profondità più stretta.</span><span class="sxs-lookup"><span data-stu-id="a4676-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="a4676-153">Quando si usa questo metodo su una risorsa a virgola mobile (invece di un formato normalizzato o senza segno), il valore di confronto non viene automaticamente premuto tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4676-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="a4676-154">Pertanto, può essere necessario un morsetto manuale del valore di confronto per le tecniche di ombreggiatura comuni.</span><span class="sxs-lookup"><span data-stu-id="a4676-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="a4676-155">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="a4676-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="a4676-156">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a4676-156">Minimum Shader Model</span></span>

<span data-ttu-id="a4676-157">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a4676-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="a4676-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4676-158">vs\_4\_0</span></span> | <span data-ttu-id="a4676-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="a4676-159">vs\_4\_1²</span></span> | <span data-ttu-id="a4676-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4676-160">ps\_4\_0</span></span> | <span data-ttu-id="a4676-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="a4676-161">ps\_4\_1²</span></span> | <span data-ttu-id="a4676-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4676-162">gs\_4\_0</span></span> | <span data-ttu-id="a4676-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="a4676-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="a4676-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="a4676-164">x¹</span></span>       | <span data-ttu-id="a4676-165">x</span><span class="sxs-lookup"><span data-stu-id="a4676-165">x</span></span>         |          |           |

1.  <span data-ttu-id="a4676-166">Texture2DArray e TextureCubeArray sono disponibili nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a4676-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="a4676-167">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a4676-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="a4676-168">**SampleCmp** è disponibile anche in PS 4 \_ 0 \_ level \_ 9 \_ 1 e 4 \_ 0 \_ level \_ 9 \_ 3 quando si usano le tecniche descritte in implementazione di [buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="a4676-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4676-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4676-169">Related topics</span></span>

[<span data-ttu-id="a4676-170">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="a4676-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
