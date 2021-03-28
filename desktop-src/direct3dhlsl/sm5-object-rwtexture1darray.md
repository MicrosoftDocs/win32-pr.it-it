---
title: RWTexture1DArray
description: Una risorsa di lettura/scrittura. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- HLSL RWTexture1DArray
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969171"
---
# <a name="rwtexture1darray"></a><span data-ttu-id="d7a97-105">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="d7a97-105">RWTexture1DArray</span></span>

<span data-ttu-id="d7a97-106">Una risorsa di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d7a97-106">A read/write resource.</span></span>



| <span data-ttu-id="d7a97-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="d7a97-107">Method</span></span>                                                             | <span data-ttu-id="d7a97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7a97-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="d7a97-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="d7a97-109">**GetDimensions**</span></span>](sm5-object-rwtexture1darray-getdimensions.md) | <span data-ttu-id="d7a97-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7a97-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="d7a97-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="d7a97-111">**Load**</span></span>](rwtexture1darray-load.md)                              | <span data-ttu-id="d7a97-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="d7a97-112">Reads texture data.</span></span>           |
| <span data-ttu-id="d7a97-113">[**Operatore\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="d7a97-113">[**Operator\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span></span>  | <span data-ttu-id="d7a97-114">Ottiene una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7a97-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="d7a97-115">È possibile anteporre gli oggetti **RWTexture1DArray** alla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="d7a97-115">You can prefix **RWTexture1DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="d7a97-116">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="d7a97-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="d7a97-117">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="d7a97-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="d7a97-118">Un oggetto **RWTexture1DArray** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7a97-118">A **RWTexture1DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="d7a97-119">Ad esempio, la dichiarazione seguente è corretta:</span><span class="sxs-lookup"><span data-stu-id="d7a97-119">For example, the following declaration is correct:</span></span>


```
RWTexture1DArray<float> tex;
```



<span data-ttu-id="d7a97-120">Poiché un oggetto **RWTexture1DArray** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto tipo di visualizzazione risorse shader (SRV), ad esempio un oggetto [**Texture1DArray**](sm5-object-texture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a97-120">Because a **RWTexture1DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1DArray**](sm5-object-texture1darray.md) object.</span></span> <span data-ttu-id="d7a97-121">Ad esempio, è possibile leggere e scrivere in un oggetto **RWTexture1DArray** , ma è possibile leggere solo da un oggetto **Texture1DArray** .</span><span class="sxs-lookup"><span data-stu-id="d7a97-121">For example, you can read from and write to a **RWTexture1DArray** object, but you can only read from a **Texture1DArray** object.</span></span>

<span data-ttu-id="d7a97-122">Un oggetto **RWTexture1DArray** non può usare i metodi di un oggetto [**Texture1DArray**](sm5-object-texture1darray.md) , ad esempio [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d7a97-122">A **RWTexture1DArray** object cannot use methods from a [**Texture1DArray**](sm5-object-texture1darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="d7a97-123">Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come una singola trama in più shader.</span><span class="sxs-lookup"><span data-stu-id="d7a97-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="d7a97-124">Ad esempio, è possibile dichiarare e usare un oggetto **RWTexture1DArray** come *Tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture1DArray** come *Tex* in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d7a97-124">For example, you can declare and use a **RWTexture1DArray** object as *tex* in a compute shader and then declare and use a **Texture1DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="d7a97-125">Il Runtime impone determinati modelli di utilizzo quando si creano più tipi di visualizzazione nella stessa risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7a97-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="d7a97-126">Il runtime, ad esempio, non consente di avere un mapping UAV per una risorsa e un mapping SRV per la stessa risorsa attiva allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="d7a97-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7a97-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d7a97-127">Minimum Shader Model</span></span>

<span data-ttu-id="d7a97-128">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7a97-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d7a97-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d7a97-129">Shader Model</span></span>                                                                | <span data-ttu-id="d7a97-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="d7a97-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d7a97-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="d7a97-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d7a97-132">sì</span><span class="sxs-lookup"><span data-stu-id="d7a97-132">yes</span></span>       |



 

<span data-ttu-id="d7a97-133">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7a97-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d7a97-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="d7a97-134">Vertex</span></span> | <span data-ttu-id="d7a97-135">Hull</span><span class="sxs-lookup"><span data-stu-id="d7a97-135">Hull</span></span> | <span data-ttu-id="d7a97-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="d7a97-136">Domain</span></span> | <span data-ttu-id="d7a97-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="d7a97-137">Geometry</span></span> | <span data-ttu-id="d7a97-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="d7a97-138">Pixel</span></span> | <span data-ttu-id="d7a97-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d7a97-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d7a97-140">x</span><span class="sxs-lookup"><span data-stu-id="d7a97-140">x</span></span>     | <span data-ttu-id="d7a97-141">x</span><span class="sxs-lookup"><span data-stu-id="d7a97-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d7a97-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7a97-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a97-143">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="d7a97-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




