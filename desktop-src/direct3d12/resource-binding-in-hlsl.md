---
title: Associazione di risorse in HLSL
description: In questo argomento vengono descritte alcune funzionalità specifiche dell'utilizzo del modello shader HLSL (High Level Shader Language) 5,1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548854"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="45f81-103">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="45f81-103">Resource binding in HLSL</span></span>

<span data-ttu-id="45f81-104">In questo argomento vengono descritte alcune funzionalità specifiche dell'utilizzo del [modello shader](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="45f81-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="45f81-105">Tutti i componenti hardware Direct3D 12 supportano il modello di shader 5,1, pertanto il supporto per questo modello non dipende dal livello di funzionalità hardware.</span><span class="sxs-lookup"><span data-stu-id="45f81-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="45f81-106">Tipi di risorse e matrici</span><span class="sxs-lookup"><span data-stu-id="45f81-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="45f81-107">Matrici di descrittori e matrici di trama</span><span class="sxs-lookup"><span data-stu-id="45f81-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="45f81-108">Alias delle risorse</span><span class="sxs-lookup"><span data-stu-id="45f81-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="45f81-109">Divergenze e derivati</span><span class="sxs-lookup"><span data-stu-id="45f81-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="45f81-110">UAV in pixel shader</span><span class="sxs-lookup"><span data-stu-id="45f81-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="45f81-111">Buffer costanti</span><span class="sxs-lookup"><span data-stu-id="45f81-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="45f81-112">Modifiche bytecode in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="45f81-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="45f81-113">Dichiarazioni HLSL di esempio</span><span class="sxs-lookup"><span data-stu-id="45f81-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="45f81-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45f81-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="45f81-115">Tipi di risorse e matrici</span><span class="sxs-lookup"><span data-stu-id="45f81-115">Resource types and arrays</span></span>

<span data-ttu-id="45f81-116">La sintassi delle risorse del modello shader 5 (SM 5.0) usa la `register` parola chiave per inoltrare informazioni importanti sulla risorsa al compilatore HLSL.</span><span class="sxs-lookup"><span data-stu-id="45f81-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="45f81-117">Nell'istruzione seguente, ad esempio, viene dichiarata una matrice di quattro trame associata a slot T3, T4, T5 e T6.</span><span class="sxs-lookup"><span data-stu-id="45f81-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="45f81-118">T3 è l'unico slot di registro presente nell'istruzione, che è semplicemente il primo nella matrice di quattro.</span><span class="sxs-lookup"><span data-stu-id="45f81-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="45f81-119">La sintassi delle risorse del modello di shader 5,1 (SM 5.1) in HLSL è basata sulla sintassi esistente per le risorse di registro, per semplificare il porting.</span><span class="sxs-lookup"><span data-stu-id="45f81-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="45f81-120">Le risorse Direct3D 12 in HLSL sono associate a registri virtuali all'interno di spazi di registro logici:</span><span class="sxs-lookup"><span data-stu-id="45f81-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="45f81-121">t: per le visualizzazioni delle risorse dello shader (SRV)</span><span class="sxs-lookup"><span data-stu-id="45f81-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="45f81-122">s – per i sampler</span><span class="sxs-lookup"><span data-stu-id="45f81-122">s – for samplers</span></span>
-   <span data-ttu-id="45f81-123">u: per le visualizzazioni di accesso non ordinato (UAV)</span><span class="sxs-lookup"><span data-stu-id="45f81-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="45f81-124">b: per le visualizzazioni dei buffer costanti (CBV)</span><span class="sxs-lookup"><span data-stu-id="45f81-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="45f81-125">La firma radice che fa riferimento allo shader deve essere compatibile con gli slot di registro dichiarati.</span><span class="sxs-lookup"><span data-stu-id="45f81-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="45f81-126">Ad esempio, la parte seguente di una firma radice è compatibile con l'uso di slot di trama da T3 a T6, perché descrive una tabella di descrittori con slot T0 tramite T98.</span><span class="sxs-lookup"><span data-stu-id="45f81-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="45f81-127">Una dichiarazione di risorsa può essere un valore scalare, una matrice 1D o una matrice multidimensionale:</span><span class="sxs-lookup"><span data-stu-id="45f81-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="45f81-128">SM 5.1 USA gli stessi tipi di risorse e tipi di elemento di SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="45f81-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="45f81-129">I limiti delle dichiarazioni di SM 5.1 sono più flessibili e vincolati solo dai limiti di runtime o hardware.</span><span class="sxs-lookup"><span data-stu-id="45f81-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="45f81-130">La `space` parola chiave specifica a quale spazio del registro logico è associato la variabile dichiarata.</span><span class="sxs-lookup"><span data-stu-id="45f81-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="45f81-131">Se la `space` parola chiave viene omessa, l'indice dello spazio predefinito pari a 0 viene assegnato in modo implicito all'intervallo (pertanto l' `tex2` intervallo sopra riportato si trova in `space0` ).</span><span class="sxs-lookup"><span data-stu-id="45f81-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="45f81-132">`register(t3,  space0)` non sarà mai in conflitto con `register(t3,  space1)` , né con alcuna matrice in un altro spazio che potrebbe includere T3.</span><span class="sxs-lookup"><span data-stu-id="45f81-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="45f81-133">Una risorsa di matrice può avere una dimensione senza limiti, che viene dichiarata specificando la prima dimensione da vuota o 0:</span><span class="sxs-lookup"><span data-stu-id="45f81-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="45f81-134">La tabella descrittore corrispondente potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="45f81-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="45f81-135">Una matrice senza limiti in HLSL non corrisponde a un set di numeri fissi con `numDescriptors` nella tabella descrittore e le dimensioni fisse in HLSL corrispondono a una dichiarazione non associata nella tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="45f81-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="45f81-136">Sono consentite matrici multidimensionali, incluse le dimensioni non associate.</span><span class="sxs-lookup"><span data-stu-id="45f81-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="45f81-137">Queste matrici multidimensionali sono bidimensionali nello spazio del registro.</span><span class="sxs-lookup"><span data-stu-id="45f81-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="45f81-138">L'aliasing degli intervalli di risorse non è consentito.</span><span class="sxs-lookup"><span data-stu-id="45f81-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="45f81-139">In altre parole, per ogni tipo di risorsa (t, s, u, b), gli intervalli di registro dichiarati non devono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="45f81-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="45f81-140">Che include anche gli intervalli non associati.</span><span class="sxs-lookup"><span data-stu-id="45f81-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="45f81-141">Gli intervalli dichiarati in diversi spazi di registro non si sovrappongono.</span><span class="sxs-lookup"><span data-stu-id="45f81-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="45f81-142">Si noti che l'unbounded `tex2` (sopra) risiede in `space0` , mentre unbounded `tex3` risiede in, in `space1` modo che non si sovrappongano.</span><span class="sxs-lookup"><span data-stu-id="45f81-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="45f81-143">L'accesso alle risorse dichiarate come matrici è semplice quanto l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="45f81-144">Esiste una restrizione predefinita importante per l'uso degli indici ( `myMaterialID` e `samplerID` nel codice precedente), in quanto non è consentito variare in un' [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="45f81-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="45f81-145">Anche la modifica dell'indice in base alle istanze viene conteggiata come variabile.</span><span class="sxs-lookup"><span data-stu-id="45f81-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="45f81-146">Se è necessario modificare l'indice, specificare il `NonUniformResourceIndex` qualificatore sull'indice, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="45f81-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="45f81-147">In alcuni componenti hardware l'uso di questo qualificatore genera codice aggiuntivo per applicare la correttezza (inclusi tutti i thread) ma con un minor costo in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="45f81-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="45f81-148">Se un indice viene modificato senza questo qualificatore e all'interno di un'operazione di estrazione/invio, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="45f81-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="45f81-149">Matrici di descrittori e matrici di trama</span><span class="sxs-lookup"><span data-stu-id="45f81-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="45f81-150">Le matrici di trame sono disponibili da DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="45f81-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="45f81-151">Le matrici di trama richiedono un descrittore, tuttavia tutte le sezioni di matrici devono condividere lo stesso formato, larghezza, altezza e numero di MIP.</span><span class="sxs-lookup"><span data-stu-id="45f81-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="45f81-152">Inoltre, la matrice deve occupare un intervallo contiguo nello spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="45f81-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="45f81-153">Il codice seguente illustra un esempio di accesso a una matrice di trame da uno shader.</span><span class="sxs-lookup"><span data-stu-id="45f81-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="45f81-154">In una matrice di trame, l'indice può variare liberamente, senza alcuna necessità di qualificatori, ad esempio `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="45f81-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="45f81-155">La matrice di descrittori equivalente sarà:</span><span class="sxs-lookup"><span data-stu-id="45f81-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="45f81-156">Si noti che l'uso imbarazzante di un valore float per l'indice della matrice viene sostituito con `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="45f81-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="45f81-157">Inoltre, le matrici di descrittori offrono maggiore flessibilità con le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="45f81-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="45f81-158">Il tipo, `Texture2D` è questo esempio, non può variare, ma il formato, la larghezza, l'altezza e il conteggio MIP possono variare a seconda di ogni descrittore.</span><span class="sxs-lookup"><span data-stu-id="45f81-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="45f81-159">È legittimo avere una matrice di descrittori di matrici di trame:</span><span class="sxs-lookup"><span data-stu-id="45f81-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="45f81-160">Non è lecito dichiarare una matrice di strutture, ogni struttura contenente descrittori, ad esempio il codice seguente non è supportata.</span><span class="sxs-lookup"><span data-stu-id="45f81-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="45f81-161">Questa operazione avrebbe consentito il layout della memoria **abcabcabc...**, ma è una limitazione del linguaggio e non è supportata.</span><span class="sxs-lookup"><span data-stu-id="45f81-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="45f81-162">Un metodo supportato per eseguire questa operazione è il seguente, anche se il layout della memoria in questo caso è **AAA... BBB... CCC...**</span><span class="sxs-lookup"><span data-stu-id="45f81-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="45f81-163">Per ottenere il layout di **abcabcabc...** Memory, utilizzare una tabella descrittore senza utilizzare la `myStruct` struttura.</span><span class="sxs-lookup"><span data-stu-id="45f81-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="45f81-164">Alias delle risorse</span><span class="sxs-lookup"><span data-stu-id="45f81-164">Resource aliasing</span></span>

<span data-ttu-id="45f81-165">Gli intervalli di risorse specificati negli shader HLSL sono intervalli logici.</span><span class="sxs-lookup"><span data-stu-id="45f81-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="45f81-166">Sono associate a intervalli di heap concreti in fase di esecuzione tramite il meccanismo di firma radice.</span><span class="sxs-lookup"><span data-stu-id="45f81-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="45f81-167">In genere, un intervallo logico viene mappato a un intervallo di heap che non si sovrappone ad altri intervalli di heap.</span><span class="sxs-lookup"><span data-stu-id="45f81-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="45f81-168">Tuttavia, il meccanismo di firma radice rende possibile l'alias (sovrapposizione) degli intervalli di heap dei tipi compatibili.</span><span class="sxs-lookup"><span data-stu-id="45f81-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="45f81-169">È ad esempio `tex2` possibile `tex3` eseguire il mapping degli intervalli di e dall'esempio precedente allo stesso intervallo di heap (o sovrapposto), che ha l'effetto di eseguire l'aliasing delle trame nel programma HLSL.</span><span class="sxs-lookup"><span data-stu-id="45f81-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="45f81-170">Se si desidera questo tipo di alias, lo shader deve essere compilato con \_ \_ l'opzione alias delle risorse di D3D10 shader \_ \_ , impostata tramite l'opzione *alias/res \_ May \_* per lo [strumento compilatore di effetti](/windows/desktop/direct3dtools/fxc) (FXC).</span><span class="sxs-lookup"><span data-stu-id="45f81-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="45f81-171">L'opzione fa sì che il compilatore produca codice corretto impedendo determinate ottimizzazioni di carico/archivio nel presupposto che le risorse possano essere alias.</span><span class="sxs-lookup"><span data-stu-id="45f81-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="45f81-172">Divergenze e derivati</span><span class="sxs-lookup"><span data-stu-id="45f81-172">Divergence and derivatives</span></span>

<span data-ttu-id="45f81-173">SM 5.1 non impone limitazioni per l'indice delle risorse. ovvero, ` tex2[idx].Sample(…)` -l'indice IDX può essere una costante letterale, una costante cbuffer o un valore interpolato.</span><span class="sxs-lookup"><span data-stu-id="45f81-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="45f81-174">Sebbene il modello di programmazione fornisca una grande flessibilità, è necessario tenere presenti i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="45f81-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="45f81-175">Se l'indice è diverso da un quad, le quantità derivate e derivate calcolate dall'hardware, ad esempio LOD, potrebbero non essere definite.</span><span class="sxs-lookup"><span data-stu-id="45f81-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="45f81-176">Il compilatore HLSL esegue il massimo sforzo per emettere un avviso in questo caso, ma non impedisce la compilazione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="45f81-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="45f81-177">Questo comportamento è simile all'elaborazione di derivati in un flusso di controllo divergente.</span><span class="sxs-lookup"><span data-stu-id="45f81-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="45f81-178">Se l'indice di risorsa è divergente, le prestazioni vengono diminuite rispetto al caso di un indice uniforme, perché l'hardware deve eseguire operazioni su diverse risorse.</span><span class="sxs-lookup"><span data-stu-id="45f81-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="45f81-179">Gli indici di risorse che possono essere divergenti devono essere contrassegnati con la `NonUniformResourceIndex` funzione nel codice HLSL.</span><span class="sxs-lookup"><span data-stu-id="45f81-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="45f81-180">In caso contrario, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="45f81-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="45f81-181">UAV in pixel shader</span><span class="sxs-lookup"><span data-stu-id="45f81-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="45f81-182">SM 5.1 non impone vincoli sugli intervalli di UAV nei pixel shader come nel caso di SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="45f81-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="45f81-183">Buffer costanti</span><span class="sxs-lookup"><span data-stu-id="45f81-183">Constant Buffers</span></span>

<span data-ttu-id="45f81-184">La sintassi di SM 5.1 Constant buffers (cbuffer) è cambiata da SM 5.0 per consentire agli sviluppatori di indicizzare i buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="45f81-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="45f81-185">Per abilitare i buffer di costanti indicizzabili, in SM 5.1 è stato introdotto il `ConstantBuffer` costrutto "template":</span><span class="sxs-lookup"><span data-stu-id="45f81-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="45f81-186">Il codice precedente dichiara la variabile del buffer costante `myCB1` di tipo `Foo` e dimensione 6 e una variabile di buffer costante scalare `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="45f81-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="45f81-187">È ora possibile indicizzare una variabile di buffer costante nello shader come segue:</span><span class="sxs-lookup"><span data-stu-id="45f81-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="45f81-188">I campi ' a' è b ' non diventano variabili globali, bensì devono essere considerati come campi.</span><span class="sxs-lookup"><span data-stu-id="45f81-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="45f81-189">Per compatibilità con le versioni precedenti, SM 5.1 supporta il vecchio concetto di cbuffer per cBuffers scalare.</span><span class="sxs-lookup"><span data-stu-id="45f81-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="45f81-190">L'istruzione seguente rende le variabili globali di sola lettura ' a' è b ' come in SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="45f81-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="45f81-191">Non è tuttavia possibile indicizzare un cbuffer di questo tipo obsoleto.</span><span class="sxs-lookup"><span data-stu-id="45f81-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="45f81-192">Attualmente, il compilatore shader supporta il `ConstantBuffer` modello solo per le strutture definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="45f81-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="45f81-193">Per motivi di compatibilità, il compilatore HLSL può assegnare automaticamente i registri delle risorse per gli intervalli dichiarati in `space0` .</span><span class="sxs-lookup"><span data-stu-id="45f81-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="45f81-194">Se ' Space ' viene omesso nella clausola Register, viene usato il valore predefinito `space0` .</span><span class="sxs-lookup"><span data-stu-id="45f81-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="45f81-195">Il compilatore usa l'euristica per il primo foro per assegnare i registri.</span><span class="sxs-lookup"><span data-stu-id="45f81-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="45f81-196">L'assegnazione può essere recuperata tramite l'API di reflection, che è stata estesa per aggiungere il campo *spazio* per lo spazio, mentre il campo *BindPoint* indica il limite inferiore dell'intervallo di registro delle risorse.</span><span class="sxs-lookup"><span data-stu-id="45f81-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="45f81-197">Modifiche bytecode in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="45f81-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="45f81-198">SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="45f81-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="45f81-199">La sintassi prevede la dichiarazione di una "variabile" del registro, in modo analogo al modo in cui viene eseguita per i registri di memoria condivisa del gruppo:</span><span class="sxs-lookup"><span data-stu-id="45f81-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="45f81-200">Questa operazione verrà disassemblata in:</span><span class="sxs-lookup"><span data-stu-id="45f81-200">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="45f81-201">Ogni intervallo di risorse shader dispone ora di un ID (un nome) univoco per il bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="45f81-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="45f81-202">Ad esempio, Tex1 (T10) texture array diventa ' T'1' nel bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="45f81-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="45f81-203">L'assegnazione di ID univoci a ogni intervallo di risorse consente due elementi:</span><span class="sxs-lookup"><span data-stu-id="45f81-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="45f81-204">Identificare in modo univoco l'intervallo di risorse (vedere \_ la pagina relativa \_ all'indicizzazione della risorsa DCL Texture2D) in un'istruzione (vedere l'istruzione di esempio).</span><span class="sxs-lookup"><span data-stu-id="45f81-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="45f81-205">Associazione di un set di attributi alla dichiarazione, ad esempio il tipo di elemento, le dimensioni stride, la modalità operativa raster e così via.</span><span class="sxs-lookup"><span data-stu-id="45f81-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="45f81-206">Si noti che l'ID dell'intervallo non è correlato alla dichiarazione di limite inferiore HLSL.</span><span class="sxs-lookup"><span data-stu-id="45f81-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="45f81-207">L'ordine delle associazioni di risorse di Reflection (elenco all'inizio) e le istruzioni per la dichiarazione dello shader (DCL \_ \* ) sono le stesse per facilitare l'identificazione della corrispondenza tra le variabili HLSL e gli ID bytecode.</span><span class="sxs-lookup"><span data-stu-id="45f81-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="45f81-208">Ogni istruzione di dichiarazione in SM 5.1 utilizza un operando 3D per definire: ID intervallo, limiti inferiori e superiori.</span><span class="sxs-lookup"><span data-stu-id="45f81-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="45f81-209">Viene emesso un token aggiuntivo per specificare lo spazio del registro.</span><span class="sxs-lookup"><span data-stu-id="45f81-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="45f81-210">È possibile che vengano generati anche altri token per fornire proprietà aggiuntive dell'intervallo, ad esempio cbuffer o l'istruzione di dichiarazione del buffer strutturato genera la dimensione di cbuffer o della struttura.</span><span class="sxs-lookup"><span data-stu-id="45f81-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="45f81-211">I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat. h e **D3D10ShaderBinary:: CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="45f81-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="45f81-212">Le istruzioni di SM 5.1 non emetteranno Informazioni aggiuntive sull'operando delle risorse come parte dell'istruzione (ad esempio, SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="45f81-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="45f81-213">Queste informazioni sono ora incluse nelle istruzioni di dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="45f81-214">In SM 5.0, le istruzioni per l'indicizzazione delle risorse gli attributi delle risorse devono essere descritte in token opcode estesi, perché l'indicizzazione ha offuscato l'associazione alla dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="45f81-215">In SM 5.1 ogni ID (ad esempio,' t 1') viene associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni necessarie sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="45f81-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="45f81-216">Pertanto, i token opcode estesi usati sulle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.</span><span class="sxs-lookup"><span data-stu-id="45f81-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="45f81-217">Nelle istruzioni di non dichiarazione, un operando di risorsa per Samplers, SRVs e UAV è un operando 2D.</span><span class="sxs-lookup"><span data-stu-id="45f81-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="45f81-218">Il primo indice è una costante letterale che specifica l'ID intervallo.</span><span class="sxs-lookup"><span data-stu-id="45f81-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="45f81-219">Il secondo indice rappresenta il valore linearizzato dell'indice.</span><span class="sxs-lookup"><span data-stu-id="45f81-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="45f81-220">Il valore viene calcolato in relazione all'inizio dello spazio di registro corrispondente (non relativo all'inizio dell'intervallo logico) per una migliore correlazione con la firma radice e per ridurre il carico del compilatore del driver per la modifica dell'indice.</span><span class="sxs-lookup"><span data-stu-id="45f81-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="45f81-221">Un operando di risorsa per CBVs è un operando 3D, che contiene l'ID letterale dell'intervallo, l'indice del buffer costante e l'offset nell'istanza specifica del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="45f81-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="45f81-222">Dichiarazioni HLSL di esempio</span><span class="sxs-lookup"><span data-stu-id="45f81-222">Example HLSL Declarations</span></span>

<span data-ttu-id="45f81-223">I programmi HLSL non devono conoscere alcuna firma radice.</span><span class="sxs-lookup"><span data-stu-id="45f81-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="45f81-224">Possono assegnare associazioni allo spazio di binding "Register" virtuale, t \# per SRVs, u \# per UAV, b \# per CBVs, s per i \# Samplers, oppure affidarsi al compilatore per selezionare le assegnazioni (ed eseguire query sui mapping risultanti utilizzando la reflection dello shader in seguito).</span><span class="sxs-lookup"><span data-stu-id="45f81-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="45f81-225">La firma radice esegue il mapping delle tabelle descrittore, dei descrittori radice e delle costanti radice allo spazio di registro virtuale.</span><span class="sxs-lookup"><span data-stu-id="45f81-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="45f81-226">Di seguito sono riportate alcune dichiarazioni di esempio che possono essere disponibili in HLSL shader.</span><span class="sxs-lookup"><span data-stu-id="45f81-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="45f81-227">Si noti che non sono presenti riferimenti a firme radice o tabelle descrittori.</span><span class="sxs-lookup"><span data-stu-id="45f81-227">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="45f81-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45f81-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f81-229">Indicizzazione dinamica con HLSL 5,1</span><span class="sxs-lookup"><span data-stu-id="45f81-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="45f81-230">Effect-strumento compilatore</span><span class="sxs-lookup"><span data-stu-id="45f81-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="45f81-231">Funzionalità del modello HLSL shader 5,1 per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="45f81-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="45f81-232">Visualizzazioni ordinate del rasterizzatore</span><span class="sxs-lookup"><span data-stu-id="45f81-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="45f81-233">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="45f81-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="45f81-234">Firme radice</span><span class="sxs-lookup"><span data-stu-id="45f81-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="45f81-235">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="45f81-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="45f81-236">Valore di riferimento dello stencil specificato dello shader</span><span class="sxs-lookup"><span data-stu-id="45f81-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="45f81-237">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="45f81-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 