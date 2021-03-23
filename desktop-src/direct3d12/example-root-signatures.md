---
title: Firme radice di esempio
description: Nella sezione seguente vengono illustrate le firme radice che variano in complessità da vuote a completamente complete.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103407"
---
# <a name="example-root-signatures"></a><span data-ttu-id="7267f-103">Firme radice di esempio</span><span class="sxs-lookup"><span data-stu-id="7267f-103">Example Root Signatures</span></span>

<span data-ttu-id="7267f-104">Nella sezione seguente vengono illustrate le firme radice che variano in complessità da vuote a completamente complete.</span><span class="sxs-lookup"><span data-stu-id="7267f-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="7267f-105">Firma radice vuota</span><span class="sxs-lookup"><span data-stu-id="7267f-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="7267f-106">Una costante</span><span class="sxs-lookup"><span data-stu-id="7267f-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="7267f-107">Aggiunta di un Constant Buffer View radice</span><span class="sxs-lookup"><span data-stu-id="7267f-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="7267f-108">Binding di tabelle descrittori</span><span class="sxs-lookup"><span data-stu-id="7267f-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="7267f-109">Firma radice più complessa</span><span class="sxs-lookup"><span data-stu-id="7267f-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="7267f-110">Streaming di visualizzazioni delle risorse dello shader</span><span class="sxs-lookup"><span data-stu-id="7267f-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="7267f-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7267f-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="7267f-112">Firma radice vuota</span><span class="sxs-lookup"><span data-stu-id="7267f-112">An empty root signature</span></span>

![una firma radice vuota non contiene associazioni](images/root-tables-0.png)

<span data-ttu-id="7267f-114">È improbabile che una firma radice vuota sia utile, ma può essere usata in un passaggio di rendering semplice con l'uso solo dell'assembler di input e di vertex shader e pixel shader minimi che non accedono a nessun descrittore.</span><span class="sxs-lookup"><span data-stu-id="7267f-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="7267f-115">Sono disponibili anche la fase di Blend, la destinazione di rendering e le fasi di stencil Depth, anche con una firma radice vuota.</span><span class="sxs-lookup"><span data-stu-id="7267f-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="7267f-116">Una costante</span><span class="sxs-lookup"><span data-stu-id="7267f-116">One constant</span></span>

![una singola costante radice](images/root-tables-constant.png)

<span data-ttu-id="7267f-118">Lo slot di associazione API è il punto in cui l'argomento radice per questo parametro verrà associato in fase di record dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="7267f-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="7267f-119">Il numero degli slot di associazione API è implicito, in base all'ordine dei parametri nella firma radice (il primo è sempre zero).</span><span class="sxs-lookup"><span data-stu-id="7267f-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="7267f-120">Lo slot di binding HLSL è il punto in cui verrà visualizzato il parametro radice.</span><span class="sxs-lookup"><span data-stu-id="7267f-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="7267f-121">Il tipo ("uint" nell'esempio precedente) non è noto all'hardware ma è semplicemente un commento nell'immagine, l'hardware visualizzerà semplicemente il valore DWORD singolo come contenuto.</span><span class="sxs-lookup"><span data-stu-id="7267f-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="7267f-122">Per associare una costante in fase di record dell'elenco di comandi, viene usato un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="7267f-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="7267f-123">Aggiunta di un Constant Buffer View radice</span><span class="sxs-lookup"><span data-stu-id="7267f-123">Adding a root Constant Buffer View</span></span>

![aggiunge una visualizzazione del buffer costante alla firma radice](images/root-tables-cbv.png)

<span data-ttu-id="7267f-125">Questo esempio mostra due costanti radice e un Constant Buffer View radice (CBV) che costa due slot DWORD.</span><span class="sxs-lookup"><span data-stu-id="7267f-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="7267f-126">Per associare una visualizzazione del buffer costante, usare un comando simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="7267f-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="7267f-127">Si noti che il primo parametro (2) è lo slot visualizzato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7267f-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="7267f-128">In genere, una matrice di costanti verrà configurata e resa disponibile per gli shader a B0 come CBV.</span><span class="sxs-lookup"><span data-stu-id="7267f-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="7267f-129">Binding di tabelle descrittori</span><span class="sxs-lookup"><span data-stu-id="7267f-129">Binding descriptor tables</span></span>

![aggiunge le tabelle dei descrittori alla firma radice](images/root-tables-2.png)

<span data-ttu-id="7267f-131">In questo esempio viene illustrato l'utilizzo di due tabelle dei descrittori. uno che dichiara una tabella di cinque descrittori che saranno disponibili in fase di esecuzione in un \_ heap del \_ descrittore CBV SRV UAV e un altro che dichiara una tabella di due descrittori che verranno visualizzati in fase di esecuzione in un heap descrittore del campionatore.</span><span class="sxs-lookup"><span data-stu-id="7267f-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="7267f-132">Per associare le tabelle dei descrittori durante la registrazione di un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="7267f-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="7267f-133">Un'altra funzionalità della firma radice è la costante radice float4 che rappresenta quattro DWORD di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="7267f-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="7267f-134">Il comando che segue associa solo i due DWORD centrali dei quattro.</span><span class="sxs-lookup"><span data-stu-id="7267f-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="7267f-135">Firma radice più complessa</span><span class="sxs-lookup"><span data-stu-id="7267f-135">A more complex root signature</span></span>

![firma radice complessa con molti elementi](images/root-tables-3.png)

<span data-ttu-id="7267f-137">Questo esempio mostra una firma radice densa con la maggior parte dei tipi di voci.</span><span class="sxs-lookup"><span data-stu-id="7267f-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="7267f-138">Due delle tabelle dei descrittori (negli slot 3 e 6) includono matrici di dimensioni non vincolate.</span><span class="sxs-lookup"><span data-stu-id="7267f-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="7267f-139">Il fardello è che l'applicazione deve solo toccare descrittori validi in un heap.</span><span class="sxs-lookup"><span data-stu-id="7267f-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="7267f-140">Per le matrici non vincolate o di dimensioni molto grandi, è necessario il livello hardware 2 + del supporto per l'associazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="7267f-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="7267f-141">Sono disponibili due Samplers statici (associati senza richiedere slot di firma radice).</span><span class="sxs-lookup"><span data-stu-id="7267f-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="7267f-142">A slot 9, UAV U4 e UAV U5 vengono dichiarati con lo stesso offset della tabella descrittore.</span><span class="sxs-lookup"><span data-stu-id="7267f-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="7267f-143">Questo è l'uso di un descrittore con alias, un descrittore in memoria verrà visualizzato sia come U4 che come U5 negli shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="7267f-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="7267f-144">In questo caso lo shader deve essere compilato con l'opzione di \_ alias risorse dello shader D3D10 \_ \_ \_ o l' `/res_may_alias` opzione o in fxc.</span><span class="sxs-lookup"><span data-stu-id="7267f-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="7267f-145">I descrittori con alias consentono di associare un descrittore a più punti di binding, senza dover apportare alcuna modifica agli shader.</span><span class="sxs-lookup"><span data-stu-id="7267f-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="7267f-146">Streaming di visualizzazioni delle risorse dello shader</span><span class="sxs-lookup"><span data-stu-id="7267f-146">Streaming Shader Resource Views</span></span>

![flusso di viste delle risorse dello shader in questa firma radice](images/root-tables-4.png)

<span data-ttu-id="7267f-148">Questa firma radice illustra uno scenario in cui tutti SRVs vengono trasmessi in e da una matrice di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="7267f-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="7267f-149">In fase di esecuzione è possibile impostare una tabella dei descrittori una volta quando la firma radice è impostata.</span><span class="sxs-lookup"><span data-stu-id="7267f-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="7267f-150">Quindi, tutte le letture di trama vengono eseguite indicizzando la matrice tramite costanti alimentate tramite i primi argomenti radice.</span><span class="sxs-lookup"><span data-stu-id="7267f-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="7267f-151">È necessario solo un singolo heap del descrittore e viene aggiornato solo quando le trame vengono trasmesse in o da slot descrittore gratuiti.</span><span class="sxs-lookup"><span data-stu-id="7267f-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="7267f-152">Gli offset del descrittore nell'heap di grandi dimensioni sono identificati da shader che usano le costanti nelle visualizzazioni del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="7267f-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="7267f-153">Se, ad esempio, a uno shader viene assegnato un ID materiale, può indicizzare in una matrice di grandi dimensioni usando la costante per accedere al descrittore richiesto, che fa riferimento alla trama richiesta.</span><span class="sxs-lookup"><span data-stu-id="7267f-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="7267f-154">Questo scenario richiede hardware con associazione di risorse livello 2 +.</span><span class="sxs-lookup"><span data-stu-id="7267f-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7267f-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7267f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7267f-156">Livelli hardware di associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="7267f-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="7267f-157">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="7267f-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="7267f-158">Firme radice</span><span class="sxs-lookup"><span data-stu-id="7267f-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




