---
title: RWTexture3D
description: Una risorsa di lettura/scrittura. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- HLSL RWTexture3D
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352671"
---
# <a name="rwtexture3d"></a><span data-ttu-id="f5e67-105">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="f5e67-105">RWTexture3D</span></span>

<span data-ttu-id="f5e67-106">Una risorsa di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f5e67-106">A read/write resource.</span></span>



| <span data-ttu-id="f5e67-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="f5e67-107">Method</span></span>                                                        | <span data-ttu-id="f5e67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5e67-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="f5e67-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="f5e67-109">**GetDimensions**</span></span>](sm5-object-rwtexture3d-getdimensions.md) | <span data-ttu-id="f5e67-110">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5e67-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="f5e67-111">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="f5e67-111">**Load**</span></span>](rwtexture3d-load.md)                              | <span data-ttu-id="f5e67-112">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="f5e67-112">Reads texture data.</span></span>           |
| <span data-ttu-id="f5e67-113">[**Operatore\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="f5e67-113">[**Operator\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span></span>  | <span data-ttu-id="f5e67-114">Ottiene una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5e67-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="f5e67-115">È possibile anteporre gli oggetti **RWTexture3D** alla classe di archiviazione **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="f5e67-115">You can prefix **RWTexture3D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="f5e67-116">Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture.</span><span class="sxs-lookup"><span data-stu-id="f5e67-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="f5e67-117">Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="f5e67-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="f5e67-118">Un oggetto **RWTexture3D** richiede un tipo di elemento in un'istruzione di dichiarazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5e67-118">A **RWTexture3D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="f5e67-119">Ad esempio, la dichiarazione seguente è corretta:</span><span class="sxs-lookup"><span data-stu-id="f5e67-119">For example, the following declaration is correct:</span></span>


```
RWTexture3D<float> tex;
```



<span data-ttu-id="f5e67-120">Poiché un oggetto **RWTexture3D** è un oggetto di tipo UAV, le relative proprietà differiscono da un oggetto tipo di visualizzazione risorse shader (SRV), ad esempio un oggetto [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e67-120">Because a **RWTexture3D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture3D**](sm5-object-texture3d.md) object.</span></span> <span data-ttu-id="f5e67-121">Ad esempio, è possibile leggere e scrivere in un oggetto **RWTexture3D** , ma è possibile leggere solo da un oggetto **Texture3D** .</span><span class="sxs-lookup"><span data-stu-id="f5e67-121">For example, you can read from and write to a **RWTexture3D** object, but you can only read from a **Texture3D** object.</span></span>

<span data-ttu-id="f5e67-122">Un oggetto **RWTexture3D** non può usare i metodi di un oggetto [**Texture3D**](sm5-object-texture3d.md) , ad esempio [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f5e67-122">A **RWTexture3D** object cannot use methods from a [**Texture3D**](sm5-object-texture3d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="f5e67-123">Tuttavia, poiché è possibile creare più tipi di visualizzazione per la stessa risorsa, è possibile dichiarare più tipi di trama come una singola trama in più shader.</span><span class="sxs-lookup"><span data-stu-id="f5e67-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="f5e67-124">Ad esempio, è possibile dichiarare e usare un oggetto **RWTexture3D** come *Tex* in un compute shader e quindi dichiarare e usare un oggetto **Texture3D** come *Tex* in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f5e67-124">For example, you can declare and use a **RWTexture3D** object as *tex* in a compute shader and then declare and use a **Texture3D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="f5e67-125">Il Runtime impone determinati modelli di utilizzo quando si creano più tipi di visualizzazione nella stessa risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5e67-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="f5e67-126">Il runtime, ad esempio, non consente di avere un mapping UAV per una risorsa e un mapping SRV per la stessa risorsa attiva allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="f5e67-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="f5e67-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f5e67-127">Minimum Shader Model</span></span>

<span data-ttu-id="f5e67-128">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5e67-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="f5e67-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f5e67-129">Shader Model</span></span>                                                                | <span data-ttu-id="f5e67-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="f5e67-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f5e67-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="f5e67-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f5e67-132">sì</span><span class="sxs-lookup"><span data-stu-id="f5e67-132">yes</span></span>       |



 

<span data-ttu-id="f5e67-133">Questo oggetto è supportato per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5e67-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f5e67-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="f5e67-134">Vertex</span></span> | <span data-ttu-id="f5e67-135">Hull</span><span class="sxs-lookup"><span data-stu-id="f5e67-135">Hull</span></span> | <span data-ttu-id="f5e67-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="f5e67-136">Domain</span></span> | <span data-ttu-id="f5e67-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="f5e67-137">Geometry</span></span> | <span data-ttu-id="f5e67-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="f5e67-138">Pixel</span></span> | <span data-ttu-id="f5e67-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f5e67-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f5e67-140">x</span><span class="sxs-lookup"><span data-stu-id="f5e67-140">x</span></span>     | <span data-ttu-id="f5e67-141">x</span><span class="sxs-lookup"><span data-stu-id="f5e67-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f5e67-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5e67-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e67-143">Oggetti Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="f5e67-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




