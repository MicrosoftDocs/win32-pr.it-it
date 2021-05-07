---
title: Gather (oggetto trama DirectX HLSL)
description: Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f333c204b77d6e0c64119e16f31e170fec1d0f6c
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644103"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="809e5-103">Gather (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="809e5-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="809e5-104">Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.</span><span class="sxs-lookup"><span data-stu-id="809e5-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="809e5-105">&lt;Tipo di &gt; modello 4 Object.Gather( sampler \_ state S, float2 \| 3 \| 4 \[ Location, int2 Offset \] );</span><span class="sxs-lookup"><span data-stu-id="809e5-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="809e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="809e5-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="809e5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="809e5-107">Item</span></span></th>
<th><span data-ttu-id="809e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="809e5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="809e5-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="809e5-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="809e5-110">Sono supportati <a href="dx-graphics-hlsl-to-type.md">i tipi di</a> oggetto trama seguenti: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="809e5-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="809e5-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="809e5-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="809e5-112">[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a></span><span class="sxs-lookup"><span data-stu-id="809e5-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="809e5-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="809e5-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="809e5-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em></span><span class="sxs-lookup"><span data-stu-id="809e5-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="809e5-115">[in] Coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="809e5-115">[in] The texture coordinates.</span></span> <span data-ttu-id="809e5-116">Il tipo di argomento dipende dal tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="809e5-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="809e5-117">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="809e5-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="809e5-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="809e5-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="809e5-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="809e5-119">Texture2D</span></span></td>
<td><span data-ttu-id="809e5-120">float2</span><span class="sxs-lookup"><span data-stu-id="809e5-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="809e5-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="809e5-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="809e5-122">float3</span><span class="sxs-lookup"><span data-stu-id="809e5-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="809e5-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="809e5-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="809e5-124">float4</span><span class="sxs-lookup"><span data-stu-id="809e5-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="809e5-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></span><span class="sxs-lookup"><span data-stu-id="809e5-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="809e5-126">[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="809e5-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="809e5-127">Il tipo di argomento dipende dal tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="809e5-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="809e5-128">Per gli shader con destinazione Shader Model 5.0 e successive, i 6 bit meno significativi di ogni valore di offset vengono rispettati come valore con segno, producendo l'intervallo [-32..31].</span><span class="sxs-lookup"><span data-stu-id="809e5-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="809e5-129">Per gli shader del modello di shader precedenti, gli offset devono essere numeri interi immediati compresi tra -8 e 7.</span><span class="sxs-lookup"><span data-stu-id="809e5-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="809e5-130">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="809e5-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="809e5-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="809e5-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="809e5-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="809e5-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="809e5-133">int2</span><span class="sxs-lookup"><span data-stu-id="809e5-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="809e5-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="809e5-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="809e5-135">non supportato</span><span class="sxs-lookup"><span data-stu-id="809e5-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="809e5-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="809e5-136">Return Value</span></span>

<span data-ttu-id="809e5-137">Vettore a quattro componenti, con quattro componenti di dati rossi, il cui tipo è uguale al tipo di modello della trama.</span><span class="sxs-lookup"><span data-stu-id="809e5-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="809e5-138">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="809e5-138">Minimum Shader Model</span></span>

<span data-ttu-id="809e5-139">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="809e5-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="809e5-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="809e5-140">vs\_4\_0</span></span> | <span data-ttu-id="809e5-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="809e5-141">vs\_4\_1</span></span>  | <span data-ttu-id="809e5-142">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="809e5-142">ps\_4\_0</span></span> | <span data-ttu-id="809e5-143">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="809e5-143">ps\_4\_1</span></span>  | <span data-ttu-id="809e5-144">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="809e5-144">gs\_4\_0</span></span> | <span data-ttu-id="809e5-145">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="809e5-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="809e5-146">x</span><span class="sxs-lookup"><span data-stu-id="809e5-146">x</span></span>         |          | <span data-ttu-id="809e5-147">x</span><span class="sxs-lookup"><span data-stu-id="809e5-147">x</span></span>         |          | <span data-ttu-id="809e5-148">x</span><span class="sxs-lookup"><span data-stu-id="809e5-148">x</span></span>         |



 

1.  <span data-ttu-id="809e5-149">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="809e5-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="809e5-150">Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="809e5-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="809e5-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="809e5-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="809e5-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="809e5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="809e5-153">Oggetto Texture</span><span class="sxs-lookup"><span data-stu-id="809e5-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





