---
title: Configurazione della funzionalità di fusione
description: Le operazioni di fusione vengono eseguite ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering. Se è abilitato il campionamento multiplo, il blending viene eseguito in ogni multicampione; in caso contrario, la fusione viene eseguita su ogni pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993392"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="00f14-104">Configurazione della funzionalità di fusione</span><span class="sxs-lookup"><span data-stu-id="00f14-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="00f14-105">Le operazioni di fusione vengono eseguite ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="00f14-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="00f14-106">Se è abilitato il campionamento multiplo, il blending viene eseguito in ogni multicampione; in caso contrario, la fusione viene eseguita su ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="00f14-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="00f14-107">Creare lo stato di Blend</span><span class="sxs-lookup"><span data-stu-id="00f14-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="00f14-108">Associa lo stato di Blend</span><span class="sxs-lookup"><span data-stu-id="00f14-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="00f14-109">Argomenti di blending avanzati</span><span class="sxs-lookup"><span data-stu-id="00f14-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="00f14-110">Da Alpha a code coverage</span><span class="sxs-lookup"><span data-stu-id="00f14-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="00f14-111">Fusione di output di pixel shader</span><span class="sxs-lookup"><span data-stu-id="00f14-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="00f14-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00f14-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="00f14-113">Creare lo stato di Blend</span><span class="sxs-lookup"><span data-stu-id="00f14-113">Create the Blend State</span></span>

<span data-ttu-id="00f14-114">Lo stato di Blend è una raccolta di stati usati per controllare la fusione.</span><span class="sxs-lookup"><span data-stu-id="00f14-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="00f14-115">Questi stati (definiti in [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) vengono usati per creare l'oggetto di stato Blend chiamando [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span><span class="sxs-lookup"><span data-stu-id="00f14-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="00f14-116">Ad esempio, di seguito è riportato un esempio molto semplice di creazione dello stato di Blend che disabilita la fusione alfa e non usa la maschera dei pixel per componente.</span><span class="sxs-lookup"><span data-stu-id="00f14-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="00f14-117">Questo esempio è simile all' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="00f14-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="00f14-118">Associa lo stato di Blend</span><span class="sxs-lookup"><span data-stu-id="00f14-118">Bind the Blend State</span></span>

<span data-ttu-id="00f14-119">Dopo aver creato l'oggetto di stato Blend, associare l'oggetto di stato Blend alla fase di Unione dell'output chiamando [**sul ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="00f14-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="00f14-120">Questa API accetta tre parametri: l'oggetto di stato Blend, un fattore di fusione a quattro componenti e una maschera di esempio.</span><span class="sxs-lookup"><span data-stu-id="00f14-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="00f14-121">È possibile passare un **valore null** per l'oggetto di stato Blend per specificare lo stato di Blend predefinito oppure passare un oggetto di stato Blend.</span><span class="sxs-lookup"><span data-stu-id="00f14-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="00f14-122">Se è stato creato l'oggetto di stato Blend con [**d3d11 \_ Blend \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) o [**d3d11 \_ Blend \_ inv \_ Blend \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), è possibile passare un fattore di fusione per modulare i valori per il pixel shader, la destinazione di rendering o entrambi.</span><span class="sxs-lookup"><span data-stu-id="00f14-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="00f14-123">Se non è stato creato l'oggetto di stato Blend con **d3d11 \_ Blend \_ Blend \_ Factor** o **d3d11 \_ Blend \_ inv \_ Blend \_**, è comunque possibile passare un fattore di Blend non null, ma la fase di fusione non usa il fattore di Blend. il runtime archivia il fattore di Blend ed è quindi possibile chiamare [**sul ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) per recuperare il fattore di Blend.</span><span class="sxs-lookup"><span data-stu-id="00f14-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="00f14-124">Se si passa **null**, il runtime USA o archivia un fattore di fusione uguale a {1, 1, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="00f14-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="00f14-125">La maschera di esempio è una maschera definita dall'utente che determina come campionare la destinazione di rendering esistente prima di aggiornarla.</span><span class="sxs-lookup"><span data-stu-id="00f14-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="00f14-126">La maschera di campionamento predefinita è 0xFFFFFFFF, che definisce il campionamento dei punti.</span><span class="sxs-lookup"><span data-stu-id="00f14-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="00f14-127">Nella maggior parte degli schemi di buffering, il pixel più vicino alla fotocamera è quello che viene disegnato.</span><span class="sxs-lookup"><span data-stu-id="00f14-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="00f14-128">Quando si [Configura lo stato depth stencil](d3d10-graphics-programming-guide-depth-stencil.md), il membro **DepthFunc** di [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) può essere qualsiasi funzione di [**\_ confronto d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="00f14-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="00f14-129">In genere, è preferibile che **DepthFunc** il **\_ confronto d3d11 \_ meno**, in modo che i pixel più vicini alla fotocamera sovrascrivano i pixel sottostanti.</span><span class="sxs-lookup"><span data-stu-id="00f14-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="00f14-130">Tuttavia, a seconda delle esigenze dell'applicazione, è possibile usare qualsiasi altra funzione di confronto per eseguire il test di profondità.</span><span class="sxs-lookup"><span data-stu-id="00f14-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="00f14-131">Argomenti di blending avanzati</span><span class="sxs-lookup"><span data-stu-id="00f14-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="00f14-132">Da Alpha a code coverage</span><span class="sxs-lookup"><span data-stu-id="00f14-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="00f14-133">Fusione di output di pixel shader</span><span class="sxs-lookup"><span data-stu-id="00f14-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="00f14-134">Da Alpha a code coverage</span><span class="sxs-lookup"><span data-stu-id="00f14-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="00f14-135">Alpha-to-coverage è una tecnica di campionamento multiplo particolarmente utile per situazioni come il fogliame denso in cui sono presenti diversi poligoni sovrapposti che usano la trasparenza alpha per definire i bordi all'interno della superficie.</span><span class="sxs-lookup"><span data-stu-id="00f14-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="00f14-136">È possibile usare il membro **AlphaToCoverageEnable** di [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) o [**d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) per indicare se il runtime converte il. un componente (alfa) del registro di output [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 dalla pixel shader a una maschera di code coverage n-Step (dato un n-Sample **renderTarget**).</span><span class="sxs-lookup"><span data-stu-id="00f14-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="00f14-137">Il runtime esegue un'operazione **e** di questa maschera con la tipica copertura di esempio per il pixel della primitiva (oltre alla maschera di esempio) per determinare gli esempi da aggiornare in tutti i **renderTarget** attivi.</span><span class="sxs-lookup"><span data-stu-id="00f14-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="00f14-138">Se il pixel shader restituisce [il \_ code coverage SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), il runtime Disabilita l'alfa per la copertura.</span><span class="sxs-lookup"><span data-stu-id="00f14-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="00f14-139">Durante il campionamento multiplo, il runtime condivide solo una copertura per tutti i **renderTarget**.</span><span class="sxs-lookup"><span data-stu-id="00f14-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="00f14-140">Il fatto che il runtime legga e converta. a [dalla \_ destinazione SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di output 0 al code coverage quando **AlphaToCoverageEnable** è true non modifica. un valore che passa a Blender in **renderTarget** 0 (se viene impostato un **renderTarget** ).</span><span class="sxs-lookup"><span data-stu-id="00f14-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="00f14-141">In generale, se si Abilita la funzionalità Alpha-to-coverage, non si influisce sul modo in cui tutti gli output dei colori dei pixel shader interagiscono con **renderTarget** tramite la [fase di Unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) , ad eccezione del fatto che il runtime esegue un'operazione **e** della maschera di code coverage con la maschera da Alpha a code coverage.</span><span class="sxs-lookup"><span data-stu-id="00f14-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="00f14-142">L'Alpha a code coverage funziona indipendentemente dal fatto che il Runtime sia in grado di fondere **renderTarget** o se si usa la fusione in **renderTarget**.</span><span class="sxs-lookup"><span data-stu-id="00f14-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="00f14-143">L'hardware grafico non specifica esattamente il modo in cui converte pixel shader [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) in una maschera di code coverage, ad eccezione del fatto che alfa di 0 (o meno) deve eseguire il mapping a nessuna copertura e Alpha di 1 (o superiore) deve eseguire il mapping alla copertura completa (prima che il runtime esegua un'operazione **and** con una copertura primitiva effettiva)</span><span class="sxs-lookup"><span data-stu-id="00f14-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="00f14-144">Poiché Alpha va da 0 a 1, il code coverage risultante dovrebbe in genere aumentare in modo monotono.</span><span class="sxs-lookup"><span data-stu-id="00f14-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="00f14-145">Tuttavia, l'hardware può eseguire la rethering dell'area per fornire una migliore quantizzazione dei valori alfa al costo della risoluzione spaziale e del rumore.</span><span class="sxs-lookup"><span data-stu-id="00f14-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="00f14-146">Un valore alfa di NaN (non un numero) comporta una maschera senza copertura (zero).</span><span class="sxs-lookup"><span data-stu-id="00f14-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="00f14-147">L'Alpha a code coverage viene usato tradizionalmente anche per la trasparenza dello schermo o per la definizione di sagome dettagliate per Sprite altrimenti opachi.</span><span class="sxs-lookup"><span data-stu-id="00f14-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="00f14-148">Fusione di output di pixel shader</span><span class="sxs-lookup"><span data-stu-id="00f14-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="00f14-149">Questa funzionalità consente all'Unione di output di usare contemporaneamente gli output pixel shader come origini di input in un'operazione di fusione con la singola destinazione di rendering nello slot 0.</span><span class="sxs-lookup"><span data-stu-id="00f14-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="00f14-150">Questo esempio accetta due risultati e li combina in un unico passaggio, fondendone uno nella destinazione con un moltiplicatore e l'altro con un valore di aggiunta:</span><span class="sxs-lookup"><span data-stu-id="00f14-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="00f14-151">Questo esempio Mostra come configurare il primo output pixel shader come colore di origine e il secondo output come fattore di Blend di componenti per colore.</span><span class="sxs-lookup"><span data-stu-id="00f14-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="00f14-152">Questo esempio illustra il modo in cui i fattori di Blend devono corrispondere allo shader swizzles:</span><span class="sxs-lookup"><span data-stu-id="00f14-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="00f14-153">Insieme, i fattori di Blend e il codice dello shader implicano che il pixel shader è necessario per restituire almeno o0. r e O1. a.</span><span class="sxs-lookup"><span data-stu-id="00f14-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="00f14-154">I componenti di output aggiuntivi possono essere restituiti dallo shader, ma verrebbero ignorati e un numero inferiore di componenti produrrebbe risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="00f14-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00f14-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00f14-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f14-156">Output-fase di Unione</span><span class="sxs-lookup"><span data-stu-id="00f14-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="00f14-157">Fasi della pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="00f14-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 