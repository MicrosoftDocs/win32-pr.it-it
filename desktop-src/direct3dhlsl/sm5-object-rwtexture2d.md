---
title: RWTexture2D
description: Una risorsa di lettura/scrittura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352971"
---
# <a name="rwtexture2d"></a><span data-ttu-id="a40ca-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="a40ca-105">RWTexture2D</span></span>

<span data-ttu-id="a40ca-106">Una risorsa di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a40ca-106">A read/write resource.</span></span>



| <span data-ttu-id="a40ca-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="a40ca-107">Method</span></span>                                                        | <span data-ttu-id="a40ca-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40ca-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="a40ca-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="a40ca-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="a40ca-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a40ca-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="a40ca-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="a40ca-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="a40ca-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="a40ca-112">Reads texture data.</span></span>           |
| <span data-ttu-id="a40ca-113">[**Operatore\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="a40ca-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="a40ca-114">Ottiene una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a40ca-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="a40ca-115">È possibile anteporre gli oggetti RWTexture2D alla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="a40ca-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="a40ca-116">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="a40ca-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="a40ca-117">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica solo una visualizzazione di accesso non ordinato (UAV) nel gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="a40ca-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="a40ca-118">Un oggetto RWTexture2D richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a40ca-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="a40ca-119">Ad esempio, la dichiarazione seguente non è corretta:</span><span class="sxs-lookup"><span data-stu-id="a40ca-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="a40ca-120">La dichiarazione seguente è corretta:</span><span class="sxs-lookup"><span data-stu-id="a40ca-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="a40ca-121">Poiché un oggetto RWTexture2D è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto tipo di visualizzazione risorse shader (SRV), ad esempio un oggetto [Texture2D](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="a40ca-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="a40ca-122">Ad esempio, è possibile leggere e scrivere in un oggetto RWTexture2D, ma è possibile leggere solo da un oggetto Texture2D.</span><span class="sxs-lookup"><span data-stu-id="a40ca-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="a40ca-123">Un oggetto RWTexture2D non può usare i metodi di un oggetto [Texture2D](sm5-object-texture2d.md) , ad esempio [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a40ca-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="a40ca-124">Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come una singola trama in più shader.</span><span class="sxs-lookup"><span data-stu-id="a40ca-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="a40ca-125">Ad esempio, i frammenti di codice seguenti illustrano come dichiarare e usare un oggetto RWTexture2D come *Tex* in un compute shader e quindi dichiarare e usare un oggetto Texture2D come *tex* in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="a40ca-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="a40ca-126">Il Runtime impone determinati modelli di utilizzo quando si creano più tipi di visualizzazione nella stessa risorsa.</span><span class="sxs-lookup"><span data-stu-id="a40ca-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="a40ca-127">Il runtime, ad esempio, non consente di avere un mapping UAV per una risorsa e un mapping SRV per la stessa risorsa attiva allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="a40ca-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="a40ca-128">Il codice seguente è per compute shader:</span><span class="sxs-lookup"><span data-stu-id="a40ca-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="a40ca-129">Il codice seguente è per il pixel shader:</span><span class="sxs-lookup"><span data-stu-id="a40ca-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a40ca-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a40ca-130">Minimum Shader Model</span></span>

<span data-ttu-id="a40ca-131">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a40ca-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="a40ca-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a40ca-132">Shader Model</span></span>                                                                | <span data-ttu-id="a40ca-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="a40ca-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a40ca-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="a40ca-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a40ca-135">sì</span><span class="sxs-lookup"><span data-stu-id="a40ca-135">yes</span></span>       |



 

<span data-ttu-id="a40ca-136">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a40ca-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a40ca-137">Vertice</span><span class="sxs-lookup"><span data-stu-id="a40ca-137">Vertex</span></span> | <span data-ttu-id="a40ca-138">Hull</span><span class="sxs-lookup"><span data-stu-id="a40ca-138">Hull</span></span> | <span data-ttu-id="a40ca-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="a40ca-139">Domain</span></span> | <span data-ttu-id="a40ca-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="a40ca-140">Geometry</span></span> | <span data-ttu-id="a40ca-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="a40ca-141">Pixel</span></span> | <span data-ttu-id="a40ca-142">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a40ca-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a40ca-143">x</span><span class="sxs-lookup"><span data-stu-id="a40ca-143">x</span></span>     | <span data-ttu-id="a40ca-144">x</span><span class="sxs-lookup"><span data-stu-id="a40ca-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a40ca-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a40ca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40ca-146">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a40ca-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




