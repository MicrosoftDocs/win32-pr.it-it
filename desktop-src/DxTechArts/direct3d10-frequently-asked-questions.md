---
title: Domande frequenti su Direct3D 10
description: Questo articolo contiene alcune delle domande frequenti riguardanti Direct3D 10, dal punto di vista di uno sviluppatore che trasferisce un'applicazione esistente da Direct3D 9 (D3D9) a Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118007"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="53845-103">Domande frequenti su Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="53845-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="53845-104">Questo articolo contiene alcune delle domande frequenti riguardanti Direct3D 10, dal punto di vista di uno sviluppatore che trasferisce un'applicazione esistente da Direct3D 9 (D3D9) a Direct3D 10 (D3D10).</span><span class="sxs-lookup"><span data-stu-id="53845-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="53845-105">Buffer costanti</span><span class="sxs-lookup"><span data-stu-id="53845-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="53845-106">State</span><span class="sxs-lookup"><span data-stu-id="53845-106">State</span></span>](#state)
-   [<span data-ttu-id="53845-107">Formati</span><span class="sxs-lookup"><span data-stu-id="53845-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="53845-108">Collegamento shader</span><span class="sxs-lookup"><span data-stu-id="53845-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="53845-109">Chiamate di progetto</span><span class="sxs-lookup"><span data-stu-id="53845-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="53845-110">Risorse</span><span class="sxs-lookup"><span data-stu-id="53845-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="53845-111">Profondità come trama</span><span class="sxs-lookup"><span data-stu-id="53845-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="53845-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="53845-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="53845-113">Crashes</span><span class="sxs-lookup"><span data-stu-id="53845-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="53845-114">Rendering predicato</span><span class="sxs-lookup"><span data-stu-id="53845-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="53845-115">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="53845-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="53845-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="53845-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="53845-117">Buffer costanti</span><span class="sxs-lookup"><span data-stu-id="53845-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="53845-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Qual è il modo migliore per aggiornare i buffer costanti?</span><span class="sxs-lookup"><span data-stu-id="53845-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="53845-119">Il UpdateSubresource e la mappa con lo scarto dovrebbero avere una velocità pari alla stessa.</span><span class="sxs-lookup"><span data-stu-id="53845-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="53845-120">Scegliere una delle due, a seconda di quale copia la quantità minima di memoria.</span><span class="sxs-lookup"><span data-stu-id="53845-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="53845-121">Se i dati sono già archiviati in memoria in un blocco contiguo, usare UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="53845-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="53845-122">Se è necessario accumulare dati da altre posizioni, usare Map con scarto.</span><span class="sxs-lookup"><span data-stu-id="53845-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="53845-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Qual è il modo peggiore per organizzare i buffer costanti?</span><span class="sxs-lookup"><span data-stu-id="53845-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="53845-124">Le prestazioni peggiori vengono realizzate inserendo tutte le costanti per un particolare shader in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="53845-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="53845-125">Sebbene questo sia spesso il modo più semplice per eseguire il porting da D3D9 a D3D10, può comportare un danneggiamento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53845-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="53845-126">Si consideri ad esempio uno scenario in cui viene utilizzato il buffer costante seguente:</span><span class="sxs-lookup"><span data-stu-id="53845-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="53845-127">Il buffer è 6560 byte.</span><span class="sxs-lookup"><span data-stu-id="53845-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="53845-128">Si supponga che esista un'applicazione con 1000 oggetti di cui eseguire il rendering, 100 di cui sono presenti mesh con skin e 900 di cui sono mesh statiche.</span><span class="sxs-lookup"><span data-stu-id="53845-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="53845-129">Si supponga inoltre che l'applicazione utilizzi il mapping Shadow con una sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="53845-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="53845-130">Ciò significa che sono disponibili due sessioni, una per la mappa di profondità sottoposta a rendering dalla luce e l'altra per il passaggio di rendering successivo.</span><span class="sxs-lookup"><span data-stu-id="53845-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="53845-131">In questo modo vengono generate 2000 chiamate di progetto.</span><span class="sxs-lookup"><span data-stu-id="53845-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="53845-132">Sebbene ogni chiamata di progetto non debba aggiornare ogni parte del buffer costante, l'intero buffer costante viene comunque aggiornato e inviato alla scheda.</span><span class="sxs-lookup"><span data-stu-id="53845-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="53845-133">In questo modo si ottiene l'aggiornamento di 13 MB di dati ogni frame (2000 chiamate di chiamata volte a 6560 KB).</span><span class="sxs-lookup"><span data-stu-id="53845-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="53845-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Qual è il modo migliore per organizzare i buffer costanti?</span><span class="sxs-lookup"><span data-stu-id="53845-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="53845-135">Il modo migliore consiste nell'organizzare i buffer costanti in base alla frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="53845-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="53845-136">Le costanti aggiornate a frequenze simili devono trovarsi nello stesso buffer.</span><span class="sxs-lookup"><span data-stu-id="53845-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="53845-137">Si consideri, ad esempio, lo scenario presentato in "Qual è il modo peggiore per organizzare i buffer costanti?", ma con un layout costante migliore:</span><span class="sxs-lookup"><span data-stu-id="53845-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="53845-138">I buffer costanti vengono suddivisi in base alla frequenza di aggiornamento, ma questa è solo la metà della soluzione.</span><span class="sxs-lookup"><span data-stu-id="53845-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="53845-139">L'applicazione deve aggiornare correttamente i buffer costanti per sfruttare al meglio la suddivisione.</span><span class="sxs-lookup"><span data-stu-id="53845-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="53845-140">Si presuppone la stessa scena precedente: 900 mesh statiche, 100 mesh con skin, un passaggio di luce e un passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="53845-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="53845-141">Si presuppone inoltre che vengano archiviati alcuni buffer costanti per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="53845-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="53845-142">Ciò significa che ogni oggetto conterrà un VSPerSkinnedCB o un VSPerStaticCB, a seconda che sia o meno una skin o statica.</span><span class="sxs-lookup"><span data-stu-id="53845-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="53845-143">Questa operazione viene eseguita in modo da evitare il raddoppio della quantità di matrici inviate attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="53845-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="53845-144">Il frame viene suddiviso in tre fasi.</span><span class="sxs-lookup"><span data-stu-id="53845-144">We split the frame into three phases.</span></span> <span data-ttu-id="53845-145">La prima fase è l'inizio del frame e non prevede alcun rendering, ma solo aggiornamenti costanti.</span><span class="sxs-lookup"><span data-stu-id="53845-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="53845-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Inizio frame**</span><span class="sxs-lookup"><span data-stu-id="53845-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="53845-147">Aggiornare VSGlobalPerFrameCB per il tempo applicazione (4 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="53845-148">Aggiornamento 100 VSPerSkinnedCB per gli oggetti con skinning 100 (640000 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="53845-149">Aggiornare VSPerStaticCB per 900 oggetti statici (57600 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="53845-150">Il passaggio successivo è la mappa Shadow.</span><span class="sxs-lookup"><span data-stu-id="53845-150">Next is the shadow map pass.</span></span> <span data-ttu-id="53845-151">Si noti che l'unico buffer costante effettivamente aggiornato è VSPerPassCB.</span><span class="sxs-lookup"><span data-stu-id="53845-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="53845-152">Tutti gli altri buffer costanti sono stati aggiornati durante il passaggio di inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="53845-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="53845-153">Sebbene sia ancora necessario associare questi buffer costanti, la quantità di informazioni passate alla scheda video è minima, perché i buffer sono già stati aggiornati.</span><span class="sxs-lookup"><span data-stu-id="53845-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="53845-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passaggio ombreggiatura**</span><span class="sxs-lookup"><span data-stu-id="53845-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="53845-155">Aggiornare VSPerPassCB (72 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="53845-156">Estrai mesh con skin 100 (100 associazioni, nessun aggiornamento)</span><span class="sxs-lookup"><span data-stu-id="53845-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="53845-157">Estrai 900 mesh statiche (100 associazioni, nessun aggiornamento)</span><span class="sxs-lookup"><span data-stu-id="53845-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="53845-158">Analogamente, il passaggio di rendering in diretta deve solo aggiornare i dati per materiale, perché non è stato archiviato per mesh.</span><span class="sxs-lookup"><span data-stu-id="53845-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="53845-159">Se si presuppone che nella scena siano in uso materiali 500:</span><span class="sxs-lookup"><span data-stu-id="53845-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="53845-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Passo successivo**</span><span class="sxs-lookup"><span data-stu-id="53845-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="53845-161">Aggiornare VSPerPassCB (72 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="53845-162">Aggiornamento 500 VSPerMaterialCBs (10000 byte)</span><span class="sxs-lookup"><span data-stu-id="53845-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="53845-163">Ciò comporta un totale di soli 707 KB.</span><span class="sxs-lookup"><span data-stu-id="53845-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="53845-164">Sebbene si tratta di uno scenario molto semplice, viene illustrato il grado di riduzione del sovraccarico di aggiornamenti costanti mediante l'ordinamento delle costanti in base alla frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="53845-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="53845-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Cosa accade se non si dispone di spazio sufficiente per archiviare i singoli buffer costanti per le mesh, il materiale e così via?</span><span class="sxs-lookup"><span data-stu-id="53845-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-166">È sempre possibile usare un sistema a più livelli di buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="53845-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="53845-167">Creare buffer costanti a dimensione variabile (16 byte, 32 byte, 64 byte e così via) fino alle dimensioni massime del buffer costante necessarie.</span><span class="sxs-lookup"><span data-stu-id="53845-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="53845-168">Quando è il momento di associare un buffer costante a uno shader, selezionare il buffer costante più piccolo che può conservare i dati necessari per lo shader.</span><span class="sxs-lookup"><span data-stu-id="53845-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="53845-169">Sebbene questo approccio sia leggermente meno efficiente, si tratta di un passaggio intermedio valido.</span><span class="sxs-lookup"><span data-stu-id="53845-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="53845-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Si condividono buffer costanti tra diversi shader.</span><span class="sxs-lookup"><span data-stu-id="53845-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="53845-171">Uno shader può usare tutte le costanti, ma un altro può usare alcune delle costanti.</span><span class="sxs-lookup"><span data-stu-id="53845-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="53845-172">Qual è il modo migliore per aggiornarli?</span><span class="sxs-lookup"><span data-stu-id="53845-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-173">Un approccio consiste nel suddividere ulteriormente il buffer costante.</span><span class="sxs-lookup"><span data-stu-id="53845-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="53845-174">Tuttavia, viene visualizzato un punto in cui sono associati troppi buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="53845-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="53845-175">In questo caso, spostare le costanti che potrebbero essere inutilizzate da diversi shader alla fine del buffer costante.</span><span class="sxs-lookup"><span data-stu-id="53845-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="53845-176">Quando si recuperano i dati della variabile dallo shader, usare il \_ flag D3D10 SVF \_ used dalla \_ variabile D3D10 shader \_ \_ DESC per determinare se la variabile viene usata.</span><span class="sxs-lookup"><span data-stu-id="53845-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="53845-177">Inserendo le variabili inutilizzate alla fine del buffer costante, è possibile associare un buffer più piccolo allo shader che non usa queste variabili, risparmiando così il costo dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="53845-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="53845-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Quanto è possibile migliorare la frequenza dei fotogrammi se si caricano solo le ossa dei miei caratteri una volta per ogni fotogramma anziché una volta per passaggio/estrazione?</span><span class="sxs-lookup"><span data-stu-id="53845-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-179">È possibile migliorare la frequenza dei fotogrammi tra l'8% e il 50% a seconda della quantità di dati ridondanti.</span><span class="sxs-lookup"><span data-stu-id="53845-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="53845-180">Nel peggiore dei casi, le prestazioni non verranno ridotte.</span><span class="sxs-lookup"><span data-stu-id="53845-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="53845-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Quanti buffer costanti è necessario associare contemporaneamente?</span><span class="sxs-lookup"><span data-stu-id="53845-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-182">Associare il numero minimo di buffer costanti necessari per ottenere tutti i dati nello shader.</span><span class="sxs-lookup"><span data-stu-id="53845-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="53845-183">In uno scenario realistico, cinque è il numero consigliato di buffer costanti da usare.</span><span class="sxs-lookup"><span data-stu-id="53845-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="53845-184">Anche la condivisione di buffer costanti tra gli shader (associazione dello stesso CB a VS e PS) può migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53845-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="53845-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>È previsto un costo per l'associazione di buffer costanti senza utilizzarli?</span><span class="sxs-lookup"><span data-stu-id="53845-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-186">Sì, se non si intende usare effettivamente il buffer, non chiamare VSSetConsantBuffer o PSSetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="53845-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="53845-187">Questo overhead dell'API aggiuntivo può essere aggiunto nel corso di più chiamate di estrazione.</span><span class="sxs-lookup"><span data-stu-id="53845-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="53845-188">State</span><span class="sxs-lookup"><span data-stu-id="53845-188">State</span></span>

<dl> <dt>

<span data-ttu-id="53845-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Qual è il modo migliore per gestire lo stato in D3D10?</span><span class="sxs-lookup"><span data-stu-id="53845-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-190">La soluzione migliore consiste nel comprendere tutti gli Stati di prima e creare gli oggetti di stato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="53845-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="53845-191">Ciò significa che in fase di rendering, l'associazione di stato è l'unica operazione che deve essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="53845-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="53845-192">D3D10 filtra anche i duplicati.</span><span class="sxs-lookup"><span data-stu-id="53845-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="53845-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Il gioco è stato caricato dinamicamente o contiene contenuto generato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="53845-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="53845-194">Non è possibile caricare tutti gli oggetti di stato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="53845-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="53845-195">Cosa devo fare?</span><span class="sxs-lookup"><span data-stu-id="53845-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-196">Qui sono disponibili due soluzioni.</span><span class="sxs-lookup"><span data-stu-id="53845-196">There are two solutions here.</span></span> <span data-ttu-id="53845-197">Il primo consiste nel creare solo oggetti di stato in tempo reale e consentire a D3D10 di filtrare i duplicati.</span><span class="sxs-lookup"><span data-stu-id="53845-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="53845-198">Questa operazione, tuttavia, non è consigliata per scenari con molte modifiche all'oggetto di stato per frame.</span><span class="sxs-lookup"><span data-stu-id="53845-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="53845-199">Una soluzione migliore consiste nell'eseguire l'hashing degli oggetti di stato e creare un oggetto stato solo se non è possibile trovare un oggetto che soddisfa i requisiti nella tabella hash.</span><span class="sxs-lookup"><span data-stu-id="53845-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="53845-200">Il motivo per cui si usa una tabella hash personalizzata è che un'applicazione può selezionare un hash rapido in base allo scenario di utilizzo specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="53845-201">Se, ad esempio, un'applicazione modifica solo rendertargetwritemask in BlendState e mantiene tutti gli altri valori uguali, l'applicazione può generare un hash da rendertargetwritemask anziché l'intera struttura.</span><span class="sxs-lookup"><span data-stu-id="53845-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="53845-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Lo stato di AlphaTest è Gone.</span><span class="sxs-lookup"><span data-stu-id="53845-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="53845-203">Dove è andato?</span><span class="sxs-lookup"><span data-stu-id="53845-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-204">AlphaTest dovrebbe ora essere prestazioni nello shader.</span><span class="sxs-lookup"><span data-stu-id="53845-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="53845-205">Vedere l'esempio FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="53845-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="53845-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Cosa è successo ai piani di ritaglio utente?</span><span class="sxs-lookup"><span data-stu-id="53845-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-207">I piani di ritaglio utente sono stati spostati nello shader.</span><span class="sxs-lookup"><span data-stu-id="53845-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="53845-208">Esistono due modi per gestire questo problema.</span><span class="sxs-lookup"><span data-stu-id="53845-208">There are two ways to handle this.</span></span> <span data-ttu-id="53845-209">Il primo consiste nell'output SV \_ Clipdistance dal vertex shader o dalla geometria shader.</span><span class="sxs-lookup"><span data-stu-id="53845-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="53845-210">L'altra opzione consiste nell'usare lo scarto nell'pixel shader in base a un valore passato dal vertex shader o dal geometry shader.</span><span class="sxs-lookup"><span data-stu-id="53845-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="53845-211">Sperimentare entrambi per vedere quale è più veloce per uno scenario specifico.</span><span class="sxs-lookup"><span data-stu-id="53845-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="53845-212">Se si usa SV \_ CLIPDISTANCE, l'hardware può usare una routine di ritaglio basata sulla geometria che può causare un rallentamento delle chiamate di tracciato con binding di geometria.</span><span class="sxs-lookup"><span data-stu-id="53845-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="53845-213">Allo stesso modo, l'uso di discard sposta il lavoro al pixel shader, che può causare un'esecuzione più lenta delle chiamate di disegni con associazione a pixel.</span><span class="sxs-lookup"><span data-stu-id="53845-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="53845-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>I cancellamenti non rispettano le impostazioni dello stato, ad esempio le impostazioni del recto della forbice nello stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="53845-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-215">Le cancellazioni sono state separate dallo stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="53845-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="53845-216">Per ottenere un comportamento di tipo D3D9, emulare i cancellamenti disegnando un quad a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="53845-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="53845-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Ho impostato di nuovo gli Stati su predefinito per provare a diagnosticare un errore di rendering.</span><span class="sxs-lookup"><span data-stu-id="53845-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="53845-218">Ora la schermata mostra semplicemente il nero, anche se so che sto disegnando oggetti sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="53845-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-219">Quando si imposta stato di nuovo su valori predefiniti (NULL), assicurarsi che SampleMask nella chiamata a OMSetBlendState non sia mai zero.</span><span class="sxs-lookup"><span data-stu-id="53845-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="53845-220">Se SampleMask è impostato su zero, tutti gli esempi vengono logicamente e con zero.</span><span class="sxs-lookup"><span data-stu-id="53845-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="53845-221">In questo scenario nessun campione supererà il test di Blend.</span><span class="sxs-lookup"><span data-stu-id="53845-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="53845-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Dove si è D3DSAMP lo \_ stato SRGBTEXTURE?</span><span class="sxs-lookup"><span data-stu-id="53845-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-223">SRGB è stato rimosso come parte dello stato del campionatore ed è ora associato al formato di trama.</span><span class="sxs-lookup"><span data-stu-id="53845-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="53845-224">Il binding di una trama SRGB comporterà lo stesso campionamento che si otterrebbe se è stato specificato D3DSAMP \_ SRGBTEXTURE in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="53845-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="53845-225">Formati</span><span class="sxs-lookup"><span data-stu-id="53845-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="53845-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Quale formato D3D9 corrisponde al formato D3D10?</span><span class="sxs-lookup"><span data-stu-id="53845-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-227">Per informazioni, vedere [considerazioni su Direct3D 9 in Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="53845-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="53845-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Che cosa è successo ai formati di trama A8R8G8B8?</span><span class="sxs-lookup"><span data-stu-id="53845-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-229">Sono stati deprecati in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="53845-230">È possibile ricreare le trame come R8G8B8A8 oppure swizzle durante il caricamento oppure è possibile swizzle nello shader.</span><span class="sxs-lookup"><span data-stu-id="53845-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="53845-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Ricerca per categorie usare le trame pallettizzati?</span><span class="sxs-lookup"><span data-stu-id="53845-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-232">Posizionare la tavolozza dei colori in una trama o in un buffer costante e associarla alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="53845-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="53845-233">Nella pixel shader eseguire una ricerca indiretta usando l'indice nella trama pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="53845-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="53845-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quali sono i nuovi formati SRGB?</span><span class="sxs-lookup"><span data-stu-id="53845-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-235">SRGB è stato rimosso come parte dello stato del campionatore ed è ora associato al formato di trama.</span><span class="sxs-lookup"><span data-stu-id="53845-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="53845-236">Il binding di una trama SRGB comporterà lo stesso campionamento che si otterrebbe se è stato specificato D3DSAMP \_ SRGBTEXTURE in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="53845-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="53845-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Dove sono andate le ventole del triangolo?</span><span class="sxs-lookup"><span data-stu-id="53845-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-238">Le ventole del triangolo sono state deprecate in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="53845-239">Le ventole del triangolo dovranno essere convertite nella pipeline del contenuto o in caso di caricamento.</span><span class="sxs-lookup"><span data-stu-id="53845-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="53845-240">Collegamento shader</span><span class="sxs-lookup"><span data-stu-id="53845-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="53845-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Gli shader Direct3D 9 vengono compilati correttamente nel modello di Shader 4,0, ma quando vengono associati alla pipeline, si ottengono errori di collegamento visualizzati nell'output di debug con il runtime di debug.</span><span class="sxs-lookup"><span data-stu-id="53845-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-242">Il collegamento dello shader è molto più restrittivo in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="53845-243">Gli elementi in una fase successiva devono essere letti nell'ordine in cui sono restituiti dalla fase precedente.</span><span class="sxs-lookup"><span data-stu-id="53845-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="53845-244">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="53845-244">For example:</span></span>

<span data-ttu-id="53845-245">Un vertex shader restituisce:</span><span class="sxs-lookup"><span data-stu-id="53845-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="53845-246">Pixel shader letture:</span><span class="sxs-lookup"><span data-stu-id="53845-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="53845-247">Sebbene la posizione non sia necessaria nell'pixel shader, questo genera un errore di collegamento, perché la posizione viene restituita dal vertex shader, ma non letta dall'pixel shader.</span><span class="sxs-lookup"><span data-stu-id="53845-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="53845-248">La versione più corretta avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="53845-248">The more correct version would look like this:</span></span>

<span data-ttu-id="53845-249">Un vertex shader restituisce:</span><span class="sxs-lookup"><span data-stu-id="53845-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="53845-250">Pixel shader letture:</span><span class="sxs-lookup"><span data-stu-id="53845-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="53845-251">In questo caso, il vertex shader sta inserendo le stesse informazioni, ma ora il pixel shader legge elementi nell'output dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="53845-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="53845-252">Poiché il pixel shader non legge nulla dopo Tex, non è necessario preoccuparsi del fatto che Visual Studio consentirà di ottenere altre informazioni rispetto a quelle eseguite da PS.</span><span class="sxs-lookup"><span data-stu-id="53845-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="53845-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Per creare un layout di input è necessario disporre di una firma shader, ma caricare le mesh e creare i layout prima di creare shader.</span><span class="sxs-lookup"><span data-stu-id="53845-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="53845-254">Cosa devo fare?</span><span class="sxs-lookup"><span data-stu-id="53845-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-255">Una soluzione consiste nel modificare l'ordine e caricare gli shader prima di caricare mesh.</span><span class="sxs-lookup"><span data-stu-id="53845-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="53845-256">Tuttavia, questa operazione è molto più semplice di quanto detto.</span><span class="sxs-lookup"><span data-stu-id="53845-256">However, this is much easier said than done.</span></span> <span data-ttu-id="53845-257">È sempre possibile creare il layout di input su richiesta quando necessario per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="53845-258">È necessario che sia presente una versione della firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="53845-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="53845-259">È necessario creare un hash basato sullo shader e sul layout del buffer e creare solo il layout di input se non esiste già un valore che corrisponde a.</span><span class="sxs-lookup"><span data-stu-id="53845-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="53845-260">Chiamate di progetto</span><span class="sxs-lookup"><span data-stu-id="53845-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="53845-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Qual è il limite per le chiamate di progetto che D3D10 può raggiungere 60 Hz?</span><span class="sxs-lookup"><span data-stu-id="53845-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="53845-262">30 Hz?</span><span class="sxs-lookup"><span data-stu-id="53845-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-263">Direct3D 9 ha avuto una limitazione per il numero di chiamate di progetto a causa del costo della CPU per ogni chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="53845-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="53845-264">In Direct3D 10, il costo di ogni chiamata di estrazione è stato ridotto.</span><span class="sxs-lookup"><span data-stu-id="53845-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="53845-265">Tuttavia, non esiste più una correlazione definita tra le chiamate di estrazione e la frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="53845-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="53845-266">Poiché le chiamate di estrazione spesso richiedono molte chiamate di supporto (aggiornamenti costanti del buffer, binding di trama, impostazione dello stato e così via), l'effetto della frequenza dei fotogrammi dell'API è ora più dipendente dall'utilizzo complessivo delle API anziché semplicemente da un numero elevato di chiamate.</span><span class="sxs-lookup"><span data-stu-id="53845-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="53845-267">Risorse</span><span class="sxs-lookup"><span data-stu-id="53845-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="53845-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Quale tipo di utilizzo delle risorse è consigliabile utilizzare per le operazioni?</span><span class="sxs-lookup"><span data-stu-id="53845-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-269">Usare il foglio informativo seguente:</span><span class="sxs-lookup"><span data-stu-id="53845-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="53845-270">La CPU aggiorna la risorsa più di una volta per fotogramma: utilizzo di D3D10 \_ \_ dinamico</span><span class="sxs-lookup"><span data-stu-id="53845-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="53845-271">La CPU aggiorna la risorsa meno di una volta per frame: D3D10 \_ Usage \_ default</span><span class="sxs-lookup"><span data-stu-id="53845-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="53845-272">La CPU non aggiorna la risorsa: l'utilizzo di D3D10 non è \_ \_ modificabile</span><span class="sxs-lookup"><span data-stu-id="53845-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="53845-273">La CPU deve leggere la risorsa: \_ gestione temporanea dell'utilizzo di D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="53845-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="53845-274">Poiché i buffer costanti sono sempre destinati a essere aggiornati di frequente, non sono conformi al "Cheat-Sheet".</span><span class="sxs-lookup"><span data-stu-id="53845-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="53845-275">Per i tipi di risorse da usare per i buffer costanti, vedere la sezione [buffer costanti](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="53845-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="53845-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Cosa è successo a DrawPrimitiveUP e DrawIndexedPrimitiveUP?</span><span class="sxs-lookup"><span data-stu-id="53845-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-277">Sono andati a D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-277">They are gone in D3D10.</span></span> <span data-ttu-id="53845-278">Per la geometria dinamica usare un buffer dinamico di utilizzo D3D10 di grandi dimensioni \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="53845-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="53845-279">All'inizio del frame, eseguirne il mapping con D3D10 \_ Map \_ Write \_ Ignora.</span><span class="sxs-lookup"><span data-stu-id="53845-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="53845-280">Per ogni chiamata di disegno successiva, avanzare il puntatore di scrittura oltre la posizione dei vertici disegnati in precedenza ed eseguire il mapping del buffer con D3D10 \_ Map \_ Write no overwrite \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="53845-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="53845-281">Se si avvicina la fine del buffer prima della fine del frame, eseguire il wrapping del puntatore di scrittura intorno all'inizio ed eseguire il mapping con lo \_ scarto di scrittura della mappa D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="53845-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="53845-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>È possibile scrivere indici a 16 bit e indici a 32 bit nello stesso buffer di geometria dinamica?</span><span class="sxs-lookup"><span data-stu-id="53845-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-283">Sì, è possibile, ma ciò può comportare una riduzione delle prestazioni su determinati componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="53845-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="53845-284">È più sicuro creare buffer distinti per i dati di indice dinamici a 16 bit e i dati dell'indice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="53845-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="53845-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Ricerca per categorie leggere i dati dalla GPU alla CPU?</span><span class="sxs-lookup"><span data-stu-id="53845-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-286">È necessario utilizzare una risorsa di staging.</span><span class="sxs-lookup"><span data-stu-id="53845-286">You must use a staging resource.</span></span> <span data-ttu-id="53845-287">Copiare i dati dalla risorsa GPU alla risorsa di gestione temporanea usando CopyResource.</span><span class="sxs-lookup"><span data-stu-id="53845-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="53845-288">Eseguire il mapping della risorsa di gestione temporanea per leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="53845-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="53845-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>L'applicazione dipende dalla funzionalità StretchRect.</span><span class="sxs-lookup"><span data-stu-id="53845-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-290">Poiché si trattava essenzialmente di un wrapper per la funzionalità Direct3D di base, è stato rimosso dall'API.</span><span class="sxs-lookup"><span data-stu-id="53845-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="53845-291">Alcune delle funzionalità di StretchRect sono state spostate in D3DX10LoadTextureFromTexture.</span><span class="sxs-lookup"><span data-stu-id="53845-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="53845-292">Per le conversioni di formato e la copia di trame, D3DX10LoadTextureFromTexture potrebbe eseguire il processo.</span><span class="sxs-lookup"><span data-stu-id="53845-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="53845-293">Tuttavia, le operazioni, ad esempio la conversione da una dimensione a un'altra, possono richiedere un'operazione di rendering per la trama nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="53845-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Non ci sono offset o dimensioni nelle chiamate di mappa per le risorse.</span><span class="sxs-lookup"><span data-stu-id="53845-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="53845-295">Queste erano presenti in caso di chiamate di blocco su Direct3D 9; perché sono cambiate?</span><span class="sxs-lookup"><span data-stu-id="53845-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-296">Gli offset e le dimensioni delle chiamate di blocco in Direct3D 9 erano fondamentalmente disordine dell'API e spesso ignorati dal driver.</span><span class="sxs-lookup"><span data-stu-id="53845-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="53845-297">Gli offset devono essere calcolati in alternativa dall'applicazione dal puntatore restituito nella chiamata della mappa.</span><span class="sxs-lookup"><span data-stu-id="53845-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="53845-298">Profondità come trama</span><span class="sxs-lookup"><span data-stu-id="53845-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="53845-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Che è più veloce?</span><span class="sxs-lookup"><span data-stu-id="53845-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="53845-300">Se si usa la profondità come trama o si scrive la profondità in alfa e la si legge?</span><span class="sxs-lookup"><span data-stu-id="53845-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-301">Si tratta di un'applicazione e di un hardware specifico.</span><span class="sxs-lookup"><span data-stu-id="53845-301">This is application and hardware specific.</span></span> <span data-ttu-id="53845-302">Usare quello che consente di risparmiare la larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="53845-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="53845-303">Se si usano già più destinazioni di rendering e si ha un canale aggiuntivo, la scrittura della profondità dallo shader può essere una soluzione migliore.</span><span class="sxs-lookup"><span data-stu-id="53845-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="53845-304">Inoltre, la scrittura di profondità in alfa o un'altra destinazione di rendering consente di scrivere valori di profondità lineare che potrebbero velocizzare i calcoli che devono accedere al buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="53845-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="53845-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>È possibile fare in modo che una trama venga associata come input e associata come trama di stencil profondità purché si disabilitano le scritture di profondità?</span><span class="sxs-lookup"><span data-stu-id="53845-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-306">Non in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="53845-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="53845-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="53845-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>È possibile risolvere una trama MSAA depth-stencil?</span><span class="sxs-lookup"><span data-stu-id="53845-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-309">Non in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-309">Not in D3D10.</span></span> <span data-ttu-id="53845-310">È tuttavia possibile campionare singoli campioni dalla trama MSAA.</span><span class="sxs-lookup"><span data-stu-id="53845-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="53845-311">Per informazioni dettagliate, vedere la sezione [HLSL](#hlsl) .</span><span class="sxs-lookup"><span data-stu-id="53845-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="53845-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Perché l'applicazione si arresta in modo anomalo non appena si Abilita MSAA?</span><span class="sxs-lookup"><span data-stu-id="53845-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-313">Assicurarsi di abilitare un numero di campioni MSAA e un numero di qualità che vengono effettivamente enumerati dal driver.</span><span class="sxs-lookup"><span data-stu-id="53845-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="53845-314">Crashes</span><span class="sxs-lookup"><span data-stu-id="53845-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="53845-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>L'applicazione si arresta in modo anomalo in D3D10 o nel driver e non so perché.</span><span class="sxs-lookup"><span data-stu-id="53845-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-316">Il primo passaggio consiste nell'abilitare il runtime di debug (il flag di [**debug di D3D10 \_ Create \_ Device \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) è stato passato in [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="53845-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="53845-317">Questa operazione esporrà gli errori più comuni come output di debug.</span><span class="sxs-lookup"><span data-stu-id="53845-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="53845-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX si arresta in modo anomalo quando si tenta di utilizzare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-319">Il primo passaggio consiste nell'abilitare il runtime di debug (il flag di [**debug di D3D10 \_ Create \_ Device \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) è stato passato in [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="53845-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="53845-320">La probabilità di arresto anomalo di PIX è molto più elevata se l'output di debug non è pulito.</span><span class="sxs-lookup"><span data-stu-id="53845-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="53845-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Il gioco esaurisce lo spazio degli indirizzi virtuali in vista a 32 bit in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="53845-322">Non sono presenti problemi in D3D9.</span><span class="sxs-lookup"><span data-stu-id="53845-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-323">Si sono verificati alcuni problemi con D3D10 e lo spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="53845-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="53845-324">Questo problema è stato risolto in [KB940105](https://support.microsoft.com/kb/940105).</span><span class="sxs-lookup"><span data-stu-id="53845-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="53845-325">Se il problema persiste, assicurarsi che non si stiano creando più risorse che possono essere mappate (bloccate) in D3D10 di quelle create in D3D9.</span><span class="sxs-lookup"><span data-stu-id="53845-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="53845-326">Si pensi anche al porting a 64 bit, perché questo diventerà più diffuso in futuro.</span><span class="sxs-lookup"><span data-stu-id="53845-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="53845-327">Rendering predicato</span><span class="sxs-lookup"><span data-stu-id="53845-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="53845-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Ho usato il rendering predicato (in base ai risultati delle query di occlusione).</span><span class="sxs-lookup"><span data-stu-id="53845-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="53845-329">Perché l'app ha ancora la stessa velocità?</span><span class="sxs-lookup"><span data-stu-id="53845-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-330">Prima di tutto, assicurarsi che il rendering che si desidera ignorare sia in realtà il collo di bottiglia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="53845-331">Se non si tratta di un collo di bottiglia, il rendering non consentirà la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="53845-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="53845-332">In secondo luogo, assicurarsi che sia passato tempo sufficiente tra il problema della query e il rendering che si desidera predicare.</span><span class="sxs-lookup"><span data-stu-id="53845-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="53845-333">Se la query non è stata completata nel momento in cui la chiamata di rendering raggiunge la GPU, il rendering si verificherà comunque.</span><span class="sxs-lookup"><span data-stu-id="53845-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="53845-334">In terzo luogo, predicazione Ignora solo determinate chiamate.</span><span class="sxs-lookup"><span data-stu-id="53845-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="53845-335">Le chiamate ignorate sono di estrazione, cancellazione, copia, aggiornamento, ResolveSubresource e GenerateMips.</span><span class="sxs-lookup"><span data-stu-id="53845-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="53845-336">L'impostazione dello stato, le chiamate di installazione, mapping e creazione di IA non rispettano predicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="53845-337">Se è presente una grande quantità di impostazioni di stato che consentono di predicare la chiamata di progetto, questi stati verranno comunque impostati.</span><span class="sxs-lookup"><span data-stu-id="53845-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="53845-338">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="53845-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="53845-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Devo usare geometry shader per conteggiarla suddividerla My (inserire qui)?</span><span class="sxs-lookup"><span data-stu-id="53845-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-340">No.</span><span class="sxs-lookup"><span data-stu-id="53845-340">No.</span></span> <span data-ttu-id="53845-341">Il geometry shader non deve essere usato per lo schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="53845-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="53845-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>È possibile usare geometry shader per creare la geometria?</span><span class="sxs-lookup"><span data-stu-id="53845-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-343">Sì, in scenari molto limitati.</span><span class="sxs-lookup"><span data-stu-id="53845-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="53845-344">Il geometry shader nelle parti D3D10 (2008) correnti non è equipaggiato per gestire una quantità eccessiva di espansione.</span><span class="sxs-lookup"><span data-stu-id="53845-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="53845-345">Questo potrebbe cambiare in futuro.</span><span class="sxs-lookup"><span data-stu-id="53845-345">This may change in the future.</span></span> <span data-ttu-id="53845-346">I fornitori di schede video possono avere un percorso speciale da una a quattro espansioni a causa dell'hardware punto-sprite esistente.</span><span class="sxs-lookup"><span data-stu-id="53845-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="53845-347">Qualsiasi altra espansione dovrebbe essere molto limitata.</span><span class="sxs-lookup"><span data-stu-id="53845-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="53845-348">Gli esempi di ParticlesGS e PipesGS raggiungono frequenze di frame elevate solo eseguendo un'espansione limitata.</span><span class="sxs-lookup"><span data-stu-id="53845-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="53845-349">Vengono espansi solo pochi punti per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="53845-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="53845-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Per cosa si deve usare geometry shader?</span><span class="sxs-lookup"><span data-stu-id="53845-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-351">Qualsiasi elemento che richiede operazioni su un'intera primitiva, ad esempio il rilevamento della siluetta, le coordinate baricentrica e così via.</span><span class="sxs-lookup"><span data-stu-id="53845-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="53845-352">Usarlo anche per selezionare la sezione di una matrice di destinazione di rendering a cui inviare le primitive.</span><span class="sxs-lookup"><span data-stu-id="53845-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="53845-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>È possibile generare una quantità variabile di geometria dalla geometria shader?</span><span class="sxs-lookup"><span data-stu-id="53845-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-354">Sì, ma ciò può causare problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53845-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="53845-355">Eseguire l'esempio di output di 1 punto per una chiamata e di 4 punti per un altro.</span><span class="sxs-lookup"><span data-stu-id="53845-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="53845-356">Quando si adattano alle linee guida di espansione, è possibile che i thread geometry shader vengano eseguiti in modo seriale.</span><span class="sxs-lookup"><span data-stu-id="53845-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="53845-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>In che modo D3D10 sa come generare indici adiacenza per la mesh?</span><span class="sxs-lookup"><span data-stu-id="53845-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="53845-358">In alternativa, perché D3D10 non esegue correttamente il rendering quando si specifica che geometry shader necessita di informazioni adiacenza.</span><span class="sxs-lookup"><span data-stu-id="53845-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-359">Le informazioni adiacenza non vengono create da D3D10, ma dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53845-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="53845-360">Gli indici adiacenza vengono generati dall'applicazione e devono contenere sei indici per primitiva; tra i sei, gli indici numerati dispari sono i vertici adiacenti dei bordi.</span><span class="sxs-lookup"><span data-stu-id="53845-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="53845-361">ID3DX10Mesh:: GenerateAdjacencyAndPointsReps può essere usato per generare questi dati.</span><span class="sxs-lookup"><span data-stu-id="53845-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="53845-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="53845-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="53845-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Le istruzioni Integer e bit per bit sono lente?</span><span class="sxs-lookup"><span data-stu-id="53845-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-364">Possono essere.</span><span class="sxs-lookup"><span data-stu-id="53845-364">They can be.</span></span> <span data-ttu-id="53845-365">Diverse schede D3D10 possono essere in grado di emettere solo operazioni integer su un subset delle unità ALU disponibili.</span><span class="sxs-lookup"><span data-stu-id="53845-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="53845-366">Questo dipende molto dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="53845-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="53845-367">Vedere il singolo fornitore di hardware per indicazioni su come risolvere le operazioni integer su tale hardware specifico.</span><span class="sxs-lookup"><span data-stu-id="53845-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="53845-368">Inoltre, prestare molta attenzione ai cast tra i tipi.</span><span class="sxs-lookup"><span data-stu-id="53845-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="53845-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Che cosa è successo a VPOS?</span><span class="sxs-lookup"><span data-stu-id="53845-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-370">Se si dichiara un input per il pixel shader come \_ posizione SV, si otterrà lo stesso comportamento della dichiarazione come vPOS.</span><span class="sxs-lookup"><span data-stu-id="53845-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="53845-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Ricerca per categorie campione di una trama MSAA?</span><span class="sxs-lookup"><span data-stu-id="53845-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-372">Nello shader dichiarare la trama come Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="53845-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="53845-373">È quindi possibile recuperare singoli esempi utilizzando i metodi di esempio all'esterno dell'oggetto Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="53845-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="53845-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Ricerca per categorie indicare se viene effettivamente utilizzata una variabile shader in un buffer costante?</span><span class="sxs-lookup"><span data-stu-id="53845-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-375">Esaminare lo struct D3D10 della \_ variabile shader \_ reflection \_ per la variabile.</span><span class="sxs-lookup"><span data-stu-id="53845-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="53845-376">per uFlags deve essere \_ impostato il flag D3D10 SVF \_ used.</span><span class="sxs-lookup"><span data-stu-id="53845-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="53845-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Ricerca per categorie indicare se una variabile shader in un buffer costante sta effettivamente utilizzando FX10?</span><span class="sxs-lookup"><span data-stu-id="53845-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-378">Attualmente non è possibile usare FX10.</span><span class="sxs-lookup"><span data-stu-id="53845-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="53845-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Non ho alcun controllo sui buffer costanti creati da FX10.</span><span class="sxs-lookup"><span data-stu-id="53845-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="53845-380">Come vengono creati e aggiornati?</span><span class="sxs-lookup"><span data-stu-id="53845-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-381">Tutti i buffer costanti gestiti da FX10 vengono creati come \_ risorse predefinite di utilizzo di D3D10 \_ e vengono aggiornati con UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="53845-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="53845-382">Poiché FX10 mantiene un archivio di backup di tutti i dati costanti, UpdateSubresource è l'approccio migliore per aggiornarli.</span><span class="sxs-lookup"><span data-stu-id="53845-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="53845-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Ricerca per categorie emulare la pipeline della funzione fissa usando gli shader?</span><span class="sxs-lookup"><span data-stu-id="53845-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-384">Vedere l'esempio FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="53845-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="53845-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>È consigliabile usare gli \[ hint del compilatore New unroll \] , \[ loop \] , \[ Branch \] e così via?</span><span class="sxs-lookup"><span data-stu-id="53845-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-386">Generalmente, no.</span><span class="sxs-lookup"><span data-stu-id="53845-386">In general, no.</span></span> <span data-ttu-id="53845-387">Il compilatore tenterà spesso entrambe le modalità e sceglierà quella più veloce.</span><span class="sxs-lookup"><span data-stu-id="53845-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="53845-388">In alcuni casi, potrebbe essere necessario utilizzare l'operazione di \[ disrolling \] , ad esempio quando un recupero di trama all'interno di un ciclo deve accedere a una sfumatura.</span><span class="sxs-lookup"><span data-stu-id="53845-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="53845-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>La precisione parziale fa qualsiasi differenza in D3D10?</span><span class="sxs-lookup"><span data-stu-id="53845-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="53845-390">Posso specificare la precisione parziale nel HLSL di D3D9, ma non in D3D10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="53845-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="53845-391">Tutte le operazioni di D3D10 vengono specificate per l'esecuzione in corrispondenza della precisione a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="53845-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="53845-392">Pertanto, la precisione parziale non deve apportare alcuna differenza in D3D10.</span><span class="sxs-lookup"><span data-stu-id="53845-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="53845-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9 è possibile eseguire il filtro delle ombreggiature HW PCF associando un buffer di profondità come trama e usando le normali istruzioni HLSL tex2D.</span><span class="sxs-lookup"><span data-stu-id="53845-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="53845-394">Ricerca per categorie eseguire questa operazione in D3D10?</span><span class="sxs-lookup"><span data-stu-id="53845-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-395">È necessario usare uno stato del campionatore di confronto e usare le istruzioni SampleCmp.</span><span class="sxs-lookup"><span data-stu-id="53845-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="53845-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>In che modo questa parola chiave register funziona in D3D10?</span><span class="sxs-lookup"><span data-stu-id="53845-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-397">La parola chiave register in D3D10 si applica ora a quale slot a cui è associata una determinata risorsa.</span><span class="sxs-lookup"><span data-stu-id="53845-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="53845-398">In questo caso, la risorsa può essere un buffer (costante o altro), una trama o un campionatore.</span><span class="sxs-lookup"><span data-stu-id="53845-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="53845-399">Per i buffer costanti, usare la sintassi: Register (bN), dove N è lo slot di input (0-15)</span><span class="sxs-lookup"><span data-stu-id="53845-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="53845-400">Per le trame, usare la sintassi: Register (tN), dove N è lo slot di input (0-127)</span><span class="sxs-lookup"><span data-stu-id="53845-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="53845-401">Per i sampler, usare la sintassi: Register (sN), dove N è lo slot di input (0-127)</span><span class="sxs-lookup"><span data-stu-id="53845-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="53845-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Ricerca per categorie inserire una variabile all'interno di un buffer costante se Register viene usato solo per specificare dove associare l'intero buffer?</span><span class="sxs-lookup"><span data-stu-id="53845-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="53845-403">Usare la parola chiave packoffset.</span><span class="sxs-lookup"><span data-stu-id="53845-403">Use the packoffset keyword.</span></span> <span data-ttu-id="53845-404">L'argomento di packoffset è nel formato c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="53845-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="53845-405">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="53845-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="53845-406">In questo buffer costante, IWaste2Floats viene inserito al terzo valore float (12 byte) nel buffer costante.</span><span class="sxs-lookup"><span data-stu-id="53845-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="53845-407">IWasteMore viene inserito in corrispondenza del tredicesimo float4 o 52 float nel buffer costante.</span><span class="sxs-lookup"><span data-stu-id="53845-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 