---
title: Organizzazione dello stato in un effetto (Direct3D 11)
description: Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993472"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="e0eb3-103">Organizzazione dello stato in un effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e0eb3-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="e0eb3-104">Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="e0eb3-105">Di seguito sono riportate le strutture:</span><span class="sxs-lookup"><span data-stu-id="e0eb3-105">Here are the structures:</span></span>



| <span data-ttu-id="e0eb3-106">Stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="e0eb3-106">Pipeline State</span></span> | <span data-ttu-id="e0eb3-107">Struttura</span><span class="sxs-lookup"><span data-stu-id="e0eb3-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0eb3-108">Rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="e0eb3-108">Rasterization</span></span>  | [<span data-ttu-id="e0eb3-109">**D3D11 \_ rasterizzatore \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e0eb3-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="e0eb3-110">Unione output</span><span class="sxs-lookup"><span data-stu-id="e0eb3-110">Output Merger</span></span>  | <span data-ttu-id="e0eb3-111">[**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) e [ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="e0eb3-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="e0eb3-112">Shader</span><span class="sxs-lookup"><span data-stu-id="e0eb3-112">Shaders</span></span>        | <span data-ttu-id="e0eb3-113">Vedere di seguito</span><span class="sxs-lookup"><span data-stu-id="e0eb3-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="e0eb3-114">Per le fasi dello shader, in cui il numero di modifiche di stato deve essere più controllato da un'applicazione, lo stato è stato diviso nello stato del buffer costante, nello stato del campionatore, nello stato delle risorse dello shader e nello stato di visualizzazione dell'accesso non ordinato (per pixel e compute shader).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="e0eb3-115">Questo consente a un'applicazione progettata in modo accurato di aggiornare solo lo stato che sta cambiando, migliorando le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="e0eb3-116">In che modo è possibile organizzare lo stato della pipeline in un effetto?</span><span class="sxs-lookup"><span data-stu-id="e0eb3-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="e0eb3-117">La risposta è, l'ordine non è rilevante.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="e0eb3-118">Le variabili globali non devono essere posizionate nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="e0eb3-119">Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, in quanto è consigliabile organizzare i dati allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="e0eb3-120">Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="e0eb3-121">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="e0eb3-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="e0eb3-122">Shader</span><span class="sxs-lookup"><span data-stu-id="e0eb3-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="e0eb3-123">Gruppi, tecniche e sessioni</span><span class="sxs-lookup"><span data-stu-id="e0eb3-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="e0eb3-124">Variabili globali</span><span class="sxs-lookup"><span data-stu-id="e0eb3-124">Global Variables</span></span>

<span data-ttu-id="e0eb3-125">Analogamente alle procedure standard di C, le variabili globali vengono dichiarate per prime nella parte superiore del file.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="e0eb3-126">Spesso si tratta di variabili che verranno inizializzate da un'applicazione e quindi utilizzate in un effetto.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="e0eb3-127">In alcuni casi vengono inizializzati e mai modificati, in altre volte vengono aggiornati tutti i frame.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="e0eb3-128">Analogamente alle regole di ambito della funzione C, le variabili di effetto dichiarate al di fuori dell'ambito delle funzioni di effetto sono visibili in tutto l'effetto; qualsiasi variabile dichiarata all'interno di una funzione Effect è visibile solo all'interno di tale funzione.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="e0eb3-129">Di seguito è riportato un esempio delle variabili dichiarate in BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="e0eb3-130">La sintassi per le variabili di effetto è più dettagliata nella [sintassi delle variabili di effetto (Direct3D 11)](d3d11-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="e0eb3-131">La sintassi per samples texture Samplers è più dettagliata in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="e0eb3-132">Shader</span><span class="sxs-lookup"><span data-stu-id="e0eb3-132">Shaders</span></span>

<span data-ttu-id="e0eb3-133">Gli shader sono programmi eseguibili di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-133">Shaders are small executable programs.</span></span> <span data-ttu-id="e0eb3-134">È possibile considerare gli shader come incapsulamento dello stato dello shader, perché il codice HLSL implementa la funzionalità shader.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="e0eb3-135">La pipeline grafica è costituita da un massimo di cinque tipi diversi di shader.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="e0eb3-136">Vertex shaders: opera sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="e0eb3-137">Un vertice in restituisce un vertice in uscita.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="e0eb3-138">Hull shaders-opera sui dati della patch.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="e0eb3-139">Fase del punto di controllo: una chiamata restituisce un punto di controllo; Per ogni fase di fork e join: una patch restituisce una certa quantità di dati costanti di patch.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="e0eb3-140">Domain shaders: opera sui dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="e0eb3-141">Una primitiva può restituire 0, 1 o molte primitive.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="e0eb3-142">Geometry shaders: operare sui dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="e0eb3-143">Una primitiva in può restituire 0, 1 o molte primitive.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="e0eb3-144">Pixel shader: operare sui dati in pixel.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="e0eb3-145">Un pixel in restituisce 1 pixel, a meno che il pixel non venga eliminato da un rendering.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="e0eb3-146">La pipeline compute shader usa uno shader:</span><span class="sxs-lookup"><span data-stu-id="e0eb3-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="e0eb3-147">Compute Shaders: operare su qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="e0eb3-148">L'output è indipendente dal numero di thread.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="e0eb3-149">Gli shader sono funzioni locali e seguono le regole della funzione di tipo C.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="e0eb3-150">Quando viene compilato un effetto, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="e0eb3-151">Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D11Effect.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="e0eb3-152">A questo punto l'effetto compilato è in un formato intermedio.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="e0eb3-153">Per ulteriori informazioni sugli shader compilati, è necessario utilizzare la reflection dello shader.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="e0eb3-154">Questo è essenzialmente come chiedere al runtime di decompilare gli shader e restituire informazioni sul codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="e0eb3-155">La sintassi per gli shader effetti è più dettagliata in [effetti sulla sintassi delle funzioni (Direct3D 11)](d3d11-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="e0eb3-156">Gruppi, tecniche e sessioni</span><span class="sxs-lookup"><span data-stu-id="e0eb3-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="e0eb3-157">Un gruppo è una raccolta di tecniche.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-157">A group is a collection of techniques.</span></span> <span data-ttu-id="e0eb3-158">Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="e0eb3-159">Ogni effetto superato (simile all'ambito di un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per eseguire il rendering della geometria.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="e0eb3-160">I gruppi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-160">Groups are optional.</span></span> <span data-ttu-id="e0eb3-161">È presente un singolo gruppo senza nome che comprende tutte le tecniche globali.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="e0eb3-162">Tutti gli altri gruppi devono essere denominati.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-162">All other groups must be named.</span></span>

<span data-ttu-id="e0eb3-163">Di seguito è riportato un esempio di una tecnica (che include un passaggio) da BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="e0eb3-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="e0eb3-164">La sintassi per gli shader effetti è più dettagliatamente in [effetti sintassi tecnica (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e0eb3-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0eb3-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0eb3-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0eb3-166">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e0eb3-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 