---
title: Load (oggetto trama DirectX HLSL)
description: Legge i dati di Texel senza filtro o campionamento.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104123318"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="4e578-103">Load (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e578-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="4e578-104">Legge i dati di Texel senza filtro o campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e578-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e578-105">RET Object. Load (</span><span class="sxs-lookup"><span data-stu-id="4e578-105">ret Object.Load(</span></span><dl> <span data-ttu-id="4e578-106">Percorso typeX,</span><span class="sxs-lookup"><span data-stu-id="4e578-106">typeX Location,</span></span><br />
<span data-ttu-id="4e578-107">[typeX SampleIndex,]</span><span class="sxs-lookup"><span data-stu-id="4e578-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="4e578-108">[offset typeX]</span><span class="sxs-lookup"><span data-stu-id="4e578-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="4e578-109">);</span><span class="sxs-lookup"><span data-stu-id="4e578-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e578-110">typeX indica che ci sono quattro tipi possibili: **int**, **int2**, **INT3** o **INT4**.</span><span class="sxs-lookup"><span data-stu-id="4e578-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="4e578-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e578-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e578-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="4e578-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="4e578-113">Un tipo di [oggetto trama](dx-graphics-hlsl-to-type.md) (ad eccezione di TextureCube o TextureCubeArray).</span><span class="sxs-lookup"><span data-stu-id="4e578-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="4e578-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Percorso*</span><span class="sxs-lookup"><span data-stu-id="4e578-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="4e578-115">\[nelle \] coordinate di trama; l'ultimo componente specifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="4e578-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="4e578-116">Questo metodo usa un sistema di coordinate basato su 0 e non un sistema UV 0,0-1.0.</span><span class="sxs-lookup"><span data-stu-id="4e578-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="4e578-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="4e578-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4e578-118">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="4e578-118">Object Type</span></span>                                  | <span data-ttu-id="4e578-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="4e578-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="4e578-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="4e578-120">Buffer</span></span>                                       | <span data-ttu-id="4e578-121">INT</span><span class="sxs-lookup"><span data-stu-id="4e578-121">int</span></span>            |
| <span data-ttu-id="4e578-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="4e578-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="4e578-123">int2</span><span class="sxs-lookup"><span data-stu-id="4e578-123">int2</span></span>           |
| <span data-ttu-id="4e578-124">Texture1DArray, trama 2D, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4e578-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="4e578-125">int3</span><span class="sxs-lookup"><span data-stu-id="4e578-125">int3</span></span>           |
| <span data-ttu-id="4e578-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="4e578-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="4e578-127">int4</span><span class="sxs-lookup"><span data-stu-id="4e578-127">int4</span></span>           |



 

<span data-ttu-id="4e578-128">Ad esempio, per accedere a una trama 2D, fornire le coordinate UV per i primi due componenti e un livello di mipmap per il terzo componente.</span><span class="sxs-lookup"><span data-stu-id="4e578-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="4e578-129">Quando una o più coordinate nella *posizione* superano le dimensioni del livello u, v o w mipmap della trama, **Load** restituisce zero in tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="4e578-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="4e578-130">Direct3D garantisce che restituisca zero per tutte le risorse a cui si accede fuori limite.</span><span class="sxs-lookup"><span data-stu-id="4e578-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="4e578-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="4e578-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4e578-132">\[in \] un indice di campionamento facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e578-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="4e578-133">Tipo di trama</span><span class="sxs-lookup"><span data-stu-id="4e578-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="4e578-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="4e578-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="4e578-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4e578-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4e578-136">non supportato</span><span class="sxs-lookup"><span data-stu-id="4e578-136">not supported</span></span>  |
| <span data-ttu-id="4e578-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="4e578-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="4e578-138">INT</span><span class="sxs-lookup"><span data-stu-id="4e578-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="4e578-139">*SampleIndex* è disponibile solo per le trame multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="4e578-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="4e578-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span><span class="sxs-lookup"><span data-stu-id="4e578-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="4e578-141">\[in \] un offset facoltativo applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e578-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="4e578-142">Il tipo di offset dipende dal tipo di oggetto trama e deve essere statico.</span><span class="sxs-lookup"><span data-stu-id="4e578-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="4e578-143">Tipo di trama</span><span class="sxs-lookup"><span data-stu-id="4e578-143">Texture Type</span></span>                                             | <span data-ttu-id="4e578-144">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="4e578-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="4e578-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4e578-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="4e578-146">INT</span><span class="sxs-lookup"><span data-stu-id="4e578-146">int</span></span>            |
| <span data-ttu-id="4e578-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4e578-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="4e578-148">int2</span><span class="sxs-lookup"><span data-stu-id="4e578-148">int2</span></span>           |
| <span data-ttu-id="4e578-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4e578-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="4e578-150">int3</span><span class="sxs-lookup"><span data-stu-id="4e578-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="4e578-151">Se si usa l' *offset* con trame multicampionamento, è necessario specificare anche *SampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="4e578-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e578-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e578-152">Return Value</span></span>

<span data-ttu-id="4e578-153">Il tipo restituito corrisponde al tipo nella dichiarazione dell' *oggetto* .</span><span class="sxs-lookup"><span data-stu-id="4e578-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="4e578-154">Ad esempio, un oggetto Texture2D dichiarato come "Texture2d <uint4> texture;" ha un valore restituito di tipo **uint4**.</span><span class="sxs-lookup"><span data-stu-id="4e578-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4e578-155">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4e578-155">Minimum Shader Model</span></span>

<span data-ttu-id="4e578-156">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e578-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e578-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e578-157">vs\_4\_0</span></span> | <span data-ttu-id="4e578-158">vs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="4e578-158">vs\_4\_1¹</span></span> | <span data-ttu-id="4e578-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e578-159">ps\_4\_0</span></span> | <span data-ttu-id="4e578-160">PS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="4e578-160">ps\_4\_1¹</span></span> | <span data-ttu-id="4e578-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e578-161">gs\_4\_0</span></span> | <span data-ttu-id="4e578-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="4e578-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="4e578-163">x</span><span class="sxs-lookup"><span data-stu-id="4e578-163">x</span></span>        | <span data-ttu-id="4e578-164">x</span><span class="sxs-lookup"><span data-stu-id="4e578-164">x</span></span>         | <span data-ttu-id="4e578-165">x</span><span class="sxs-lookup"><span data-stu-id="4e578-165">x</span></span>        | <span data-ttu-id="4e578-166">x</span><span class="sxs-lookup"><span data-stu-id="4e578-166">x</span></span>         | <span data-ttu-id="4e578-167">x</span><span class="sxs-lookup"><span data-stu-id="4e578-167">x</span></span>        | <span data-ttu-id="4e578-168">x</span><span class="sxs-lookup"><span data-stu-id="4e578-168">x</span></span>         |



 

-   <span data-ttu-id="4e578-169">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4e578-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="4e578-170">Esempio</span><span class="sxs-lookup"><span data-stu-id="4e578-170">Example</span></span>

<span data-ttu-id="4e578-171">Questo esempio di codice parziale viene dal file Paint. FX nell' [esempio AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4e578-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="4e578-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e578-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e578-173">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="4e578-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




