---
description: "Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:"
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organizzazione dello stato in effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126321"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="b8abd-103">Organizzazione dello stato in effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b8abd-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="b8abd-104">Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8abd-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="b8abd-105">Stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="b8abd-105">Pipeline State</span></span>  | <span data-ttu-id="b8abd-106">Struttura</span><span class="sxs-lookup"><span data-stu-id="b8abd-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8abd-107">Assembler input</span><span class="sxs-lookup"><span data-stu-id="b8abd-107">Input Assembler</span></span> | [<span data-ttu-id="b8abd-108">**D3D10 \_ \_ elemento input \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="b8abd-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="b8abd-109">Rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="b8abd-109">Rasterization</span></span>   | [<span data-ttu-id="b8abd-110">**D3D10 \_ rasterizzatore \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="b8abd-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="b8abd-111">Unione output</span><span class="sxs-lookup"><span data-stu-id="b8abd-111">Output Merger</span></span>   | <span data-ttu-id="b8abd-112">[**D3D10 \_ BLEND \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) e [ **D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="b8abd-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="b8abd-113">Per le fasi dello shader, in cui il numero di modifiche di stato deve essere più controllato da un'applicazione, lo stato è stato diviso nello stato del buffer costante, nello stato del campionatore e nello stato delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8abd-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="b8abd-114">Questo consente a un'applicazione progettata in modo accurato di aggiornare solo lo stato che sta cambiando, migliorando le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.</span><span class="sxs-lookup"><span data-stu-id="b8abd-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="b8abd-115">In che modo è possibile organizzare lo stato della pipeline in un effetto?</span><span class="sxs-lookup"><span data-stu-id="b8abd-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="b8abd-116">La risposta è, l'ordine non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="b8abd-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="b8abd-117">Le variabili globali non devono essere posizionate nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="b8abd-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="b8abd-118">Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, in quanto è consigliabile organizzare i dati allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="b8abd-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="b8abd-119">Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="b8abd-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="b8abd-120">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="b8abd-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="b8abd-121">Shader</span><span class="sxs-lookup"><span data-stu-id="b8abd-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="b8abd-122">Tecniche e sessioni</span><span class="sxs-lookup"><span data-stu-id="b8abd-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="b8abd-123">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="b8abd-123">Global Variables</span></span>

<span data-ttu-id="b8abd-124">Analogamente alle procedure standard di C, le variabili globali vengono dichiarate per prime nella parte superiore del file.</span><span class="sxs-lookup"><span data-stu-id="b8abd-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="b8abd-125">Spesso si tratta di variabili che verranno inizializzate da un'applicazione e quindi utilizzate in un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8abd-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="b8abd-126">In alcuni casi vengono inizializzati e mai modificati, in altre volte vengono aggiornati tutti i frame.</span><span class="sxs-lookup"><span data-stu-id="b8abd-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="b8abd-127">Analogamente alle regole di ambito della funzione C, le variabili di effetto dichiarate al di fuori dell'ambito delle funzioni di effetto sono visibili in tutto l'effetto; qualsiasi variabile dichiarata all'interno di una funzione Effect è visibile solo all'interno di tale funzione.</span><span class="sxs-lookup"><span data-stu-id="b8abd-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="b8abd-128">Di seguito è riportato un esempio delle variabili dichiarate in BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="b8abd-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="b8abd-129">La sintassi per le variabili di effetto è più dettagliata nella [sintassi delle variabili di effetto (Direct3D 10)](d3d10-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b8abd-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="b8abd-130">La sintassi per samples texture Samplers è più dettagliata in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b8abd-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="b8abd-131">Shader</span><span class="sxs-lookup"><span data-stu-id="b8abd-131">Shaders</span></span>

<span data-ttu-id="b8abd-132">Gli shader sono programmi eseguibili di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b8abd-132">Shaders are small executable programs.</span></span> <span data-ttu-id="b8abd-133">È possibile considerare gli shader come incapsulamento dello stato dello shader, perché il codice HLSL implementa la funzionalità shader.</span><span class="sxs-lookup"><span data-stu-id="b8abd-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="b8abd-134">La pipeline usa tre tipi diversi di shader.</span><span class="sxs-lookup"><span data-stu-id="b8abd-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="b8abd-135">Vertex shaders: opera sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="b8abd-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="b8abd-136">Un vertice in restituisce un vertice in uscita.</span><span class="sxs-lookup"><span data-stu-id="b8abd-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="b8abd-137">Geometry shaders: operare sui dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="b8abd-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="b8abd-138">Una primitiva in può restituire 0, 1 o molte primitive.</span><span class="sxs-lookup"><span data-stu-id="b8abd-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="b8abd-139">Pixel shader: operare sui dati in pixel.</span><span class="sxs-lookup"><span data-stu-id="b8abd-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="b8abd-140">Un pixel in restituisce 1 pixel, a meno che il pixel non venga eliminato da un rendering.</span><span class="sxs-lookup"><span data-stu-id="b8abd-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="b8abd-141">Gli shader sono funzioni locali e seguono le regole della funzione di tipo C.</span><span class="sxs-lookup"><span data-stu-id="b8abd-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="b8abd-142">Quando viene compilato un effetto, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente.</span><span class="sxs-lookup"><span data-stu-id="b8abd-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="b8abd-143">Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D10Effect.</span><span class="sxs-lookup"><span data-stu-id="b8abd-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="b8abd-144">A questo punto l'effetto compilato è in un formato intermedio.</span><span class="sxs-lookup"><span data-stu-id="b8abd-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="b8abd-145">Per ulteriori informazioni sugli shader compilati, è necessario utilizzare la reflection dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8abd-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="b8abd-146">Questo è essenzialmente come chiedere al runtime di decompilare gli shader e restituire informazioni sul codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8abd-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="b8abd-147">La sintassi per gli shader effetti è più dettagliata in [effetti sulla sintassi delle funzioni (Direct3D 10)](d3d10-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b8abd-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="b8abd-148">Tecniche e sessioni</span><span class="sxs-lookup"><span data-stu-id="b8abd-148">Techniques and Passes</span></span>

<span data-ttu-id="b8abd-149">Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio).</span><span class="sxs-lookup"><span data-stu-id="b8abd-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="b8abd-150">Ogni effetto superato (simile all'ambito di un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per eseguire il rendering della geometria.</span><span class="sxs-lookup"><span data-stu-id="b8abd-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="b8abd-151">Di seguito è riportato un esempio di una tecnica (che include un passaggio) da BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="b8abd-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="b8abd-152">La sintassi per gli shader effetti è più dettagliatamente in [effetti sintassi tecnica (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b8abd-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8abd-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8abd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8abd-154">Effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b8abd-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
