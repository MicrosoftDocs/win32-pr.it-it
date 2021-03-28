---
title: Gather (oggetto trama DirectX HLSL)
description: Ottiene i quattro campioni (solo per il componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104976927"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="d9f37-103">Gather (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9f37-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="d9f37-104">Ottiene i quattro campioni (solo per il componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.</span><span class="sxs-lookup"><span data-stu-id="d9f37-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f37-105">&lt;Tipo &gt; di modello 4 Object. Gather (campionatore \_ stato S, float2 \| 3 \| 4 posizione \[ , offset int2 \] );</span><span class="sxs-lookup"><span data-stu-id="d9f37-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d9f37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9f37-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9f37-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9f37-107">Item</span></span></th>
<th><span data-ttu-id="d9f37-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9f37-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9f37-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="d9f37-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="d9f37-110">Sono supportati i tipi <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> seguenti: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="d9f37-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9f37-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="d9f37-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="d9f37-112">in <a href="dx-graphics-hlsl-sampler.md">Stato del campionatore</a>.</span><span class="sxs-lookup"><span data-stu-id="d9f37-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="d9f37-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="d9f37-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9f37-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Percorso</em></span><span class="sxs-lookup"><span data-stu-id="d9f37-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="d9f37-115">in Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="d9f37-115">[in] The texture coordinates.</span></span> <span data-ttu-id="d9f37-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d9f37-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9f37-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d9f37-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d9f37-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d9f37-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9f37-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d9f37-119">Texture2D</span></span></td>
<td><span data-ttu-id="d9f37-120">float2</span><span class="sxs-lookup"><span data-stu-id="d9f37-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9f37-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d9f37-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="d9f37-122">float3</span><span class="sxs-lookup"><span data-stu-id="d9f37-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9f37-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d9f37-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d9f37-124">float4</span><span class="sxs-lookup"><span data-stu-id="d9f37-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9f37-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="d9f37-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="d9f37-126">in Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="d9f37-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d9f37-127">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="d9f37-127">The texture offsets need to be static.</span></span> <span data-ttu-id="d9f37-128">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d9f37-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d9f37-129">Per altre informazioni, vedere <a href="dx-graphics-hlsl-to-sample.md">applicazione degli offset delle coordinate di trama</a>.</span><span class="sxs-lookup"><span data-stu-id="d9f37-129">For more info, see <a href="dx-graphics-hlsl-to-sample.md">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9f37-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d9f37-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d9f37-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d9f37-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9f37-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d9f37-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="d9f37-133">int2</span><span class="sxs-lookup"><span data-stu-id="d9f37-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9f37-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d9f37-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d9f37-135">non supportato</span><span class="sxs-lookup"><span data-stu-id="d9f37-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="d9f37-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9f37-136">Return Value</span></span>

<span data-ttu-id="d9f37-137">Vettore a quattro componenti, con quattro componenti di dati rossi, il cui tipo corrisponde al tipo di modello della trama.</span><span class="sxs-lookup"><span data-stu-id="d9f37-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d9f37-138">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d9f37-138">Minimum Shader Model</span></span>

<span data-ttu-id="d9f37-139">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9f37-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d9f37-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9f37-140">vs\_4\_0</span></span> | <span data-ttu-id="d9f37-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d9f37-141">vs\_4\_1</span></span>  | <span data-ttu-id="d9f37-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9f37-142">ps\_4\_0</span></span> | <span data-ttu-id="d9f37-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d9f37-143">ps\_4\_1</span></span>  | <span data-ttu-id="d9f37-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9f37-144">gs\_4\_0</span></span> | <span data-ttu-id="d9f37-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d9f37-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="d9f37-146">x</span><span class="sxs-lookup"><span data-stu-id="d9f37-146">x</span></span>         |          | <span data-ttu-id="d9f37-147">x</span><span class="sxs-lookup"><span data-stu-id="d9f37-147">x</span></span>         |          | <span data-ttu-id="d9f37-148">x</span><span class="sxs-lookup"><span data-stu-id="d9f37-148">x</span></span>         |



 

1.  <span data-ttu-id="d9f37-149">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d9f37-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="d9f37-150">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d9f37-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="d9f37-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="d9f37-151">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d9f37-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9f37-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9f37-153">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="d9f37-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





