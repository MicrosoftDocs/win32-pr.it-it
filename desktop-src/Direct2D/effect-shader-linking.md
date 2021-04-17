---
title: Collegamento Effect shader
description: Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351751"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="4873c-103">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="4873c-103">Effect Shader Linking</span></span>

<span data-ttu-id="4873c-104">Direct2D usa un'ottimizzazione denominata Effect shader linking che combina il rendering del grafico a più effetti passa in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="4873c-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="4873c-105">Panoramica del collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="4873c-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="4873c-106">Uso del collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="4873c-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="4873c-107">Creazione di un effetto personalizzato compatibile con il collegamento dello shader</span><span class="sxs-lookup"><span data-stu-id="4873c-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="4873c-108">Esempio di effetto di collegamento compatibile con lo shader</span><span class="sxs-lookup"><span data-stu-id="4873c-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="4873c-109">Compilazione di un compatibile con il collegamento-shader</span><span class="sxs-lookup"><span data-stu-id="4873c-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="4873c-110">Passaggio 1: compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="4873c-111">Passaggio 2: compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="4873c-112">Esporta specifiche delle funzioni</span><span class="sxs-lookup"><span data-stu-id="4873c-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="4873c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4873c-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="4873c-114">Panoramica del collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="4873c-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="4873c-115">Le ottimizzazioni di collegamento di Effect shader si basano sul collegamento a HLSL shader, una funzionalità Direct3D 11,2 che consente la generazione di pixel e vertex shader in fase di esecuzione tramite il collegamento di funzioni shader pre-compilate.</span><span class="sxs-lookup"><span data-stu-id="4873c-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="4873c-116">Le figure seguenti illustrano il concetto di effetto dello shader sul collegamento in un grafico effetto.</span><span class="sxs-lookup"><span data-stu-id="4873c-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="4873c-117">La prima figura mostra un grafo di effetto Direct2D tipico con quattro trasformazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="4873c-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="4873c-118">Senza il collegamento dello shader, ogni trasformazione utilizza un passaggio di rendering e richiede una superficie intermedia; in totale, questo grafico richiede 4 passaggi e 3 intermedi.</span><span class="sxs-lookup"><span data-stu-id="4873c-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![trasforma il grafico senza collegamento dello shader: 4 passaggi e 3 intermedi.](images/shader-transform-graph.png) |



 

<span data-ttu-id="4873c-120">La seconda figura mostra lo stesso grafico di effetto in cui ogni trasformazione di rendering è stata sostituita con una versione di funzione collegabile.</span><span class="sxs-lookup"><span data-stu-id="4873c-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="4873c-121">Direct2D è in grado di collegare l'intero grafico ed eseguirlo in un unico passaggio senza richiedere alcun intermedio.</span><span class="sxs-lookup"><span data-stu-id="4873c-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="4873c-122">Ciò può comportare una riduzione significativa del tempo di esecuzione della GPU e della riduzione del consumo di memoria GPU massimo.</span><span class="sxs-lookup"><span data-stu-id="4873c-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![trasforma grafico con collegamento shader: 1 passaggio, 0 intermedi.](images/shader-linking-graph.png) |



 

<span data-ttu-id="4873c-124">Il collegamento Effect shader opera sulle singole trasformazioni all'interno di un effetto; Ciò significa che anche un grafo con un singolo effetto può trarre vantaggio dal collegamento dello shader se tale effetto dispone di più trasformazioni valide.</span><span class="sxs-lookup"><span data-stu-id="4873c-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="4873c-125">Uso del collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="4873c-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="4873c-126">Se si compila un'applicazione Direct2D che usa gli effetti, non è necessario eseguire alcuna operazione per sfruttare il collegamento Effect shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="4873c-127">Direct2D analizza automaticamente il grafico degli effetti per determinare il modo più ottimale per collegare ogni trasformazione.</span><span class="sxs-lookup"><span data-stu-id="4873c-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="4873c-128">Gli autori degli effetti sono responsabili dell'implementazione del loro effetto in modo da supportare il collegamento Effect shader; Per ulteriori informazioni, vedere la sezione [creazione di un effetto personalizzato compatibile con il collegamento shader](#authoring-a-shader-linking-compatible-custom-effect) di seguito.</span><span class="sxs-lookup"><span data-stu-id="4873c-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="4873c-129">Tutti gli effetti predefiniti supportano il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="4873c-130">Direct2D collegherà solo le trasformazioni di rendering adiacenti in situazioni in cui è utile.</span><span class="sxs-lookup"><span data-stu-id="4873c-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="4873c-131">Prende in considerazione diversi fattori quando si determina se collegare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="4873c-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="4873c-132">Ad esempio, il collegamento dello shader non viene eseguito se una delle trasformazioni USA vertex o Compute Shaders, in quanto è possibile collegare solo i pixel shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="4873c-133">Inoltre, se un effetto non è stato creato per essere compatibile con il collegamento dello shader, le trasformazioni circostanti non verranno collegate.</span><span class="sxs-lookup"><span data-stu-id="4873c-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="4873c-134">Nel caso in cui esista un rischio di collegamento di questo tipo, Direct2D non collegherà le trasformazioni adiacenti al rischio, ma tenterà comunque di collegare il resto del grafo.</span><span class="sxs-lookup"><span data-stu-id="4873c-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![trasforma il grafico con un rischio di collegamento: 2 passaggi, 1 intermedio.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="4873c-136">Creazione di un effetto personalizzato compatibile con il collegamento dello shader</span><span class="sxs-lookup"><span data-stu-id="4873c-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="4873c-137">Se si crea un effetto Direct2D personalizzato, è necessario assicurarsi che le trasformazioni supportino il collegamento Effect shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="4873c-138">Questa operazione richiede alcune modifiche minime rispetto al modo in cui sono stati implementati gli effetti personalizzati precedenti.</span><span class="sxs-lookup"><span data-stu-id="4873c-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="4873c-139">Se una trasformazione all'interno dell'effetto personalizzato non supporta il collegamento dello shader, Direct2D non lo collegherà con le trasformazioni adiacenti al grafico di effetto.</span><span class="sxs-lookup"><span data-stu-id="4873c-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="4873c-140">Come autore dell'effetto personalizzato, è necessario conoscere diversi concetti chiave e requisiti:</span><span class="sxs-lookup"><span data-stu-id="4873c-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="4873c-141">**Nessuna modifica alle implementazioni dell'interfaccia di effetto**</span><span class="sxs-lookup"><span data-stu-id="4873c-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="4873c-142">Non è necessario modificare il codice che implementa le varie interfacce di effetto, ad esempio [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span><span class="sxs-lookup"><span data-stu-id="4873c-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="4873c-143">**Fornire una versione completa ed Esporta della funzione shader**</span><span class="sxs-lookup"><span data-stu-id="4873c-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="4873c-144">È necessario fornire una versione della funzione Export degli shader dell'effetto che possono essere collegati da Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4873c-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="4873c-145">Inoltre, è necessario continuare a fornire lo shader originale completo; Questo perché Direct2D seleziona in fase di esecuzione la versione shader corretta, a seconda che il collegamento dello shader venga applicato a un particolare collegamento nel grafico.</span><span class="sxs-lookup"><span data-stu-id="4873c-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="4873c-146">Se una trasformazione fornisce solo il BLOB pixel shader completo (tramite [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), non verrà collegato a trasformazioni adiacenti.</span><span class="sxs-lookup"><span data-stu-id="4873c-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="4873c-147">**Funzioni helper**</span><span class="sxs-lookup"><span data-stu-id="4873c-147">**Helper functions**</span></span>

    <span data-ttu-id="4873c-148">Direct2D fornisce le funzioni e le macro [Helper HLSL](hlsl-helpers.md) che generano automaticamente le versioni della funzione complete ed export di uno shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="4873c-149">Questi helper si trovano in d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="4873c-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="4873c-150">Inoltre, il compilatore HLSL (FXC) consente di inserire la funzione di esportazione shader in un campo privato dello shader completo.</span><span class="sxs-lookup"><span data-stu-id="4873c-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="4873c-151">In questo modo, è sufficiente creare uno shader una sola volta e passare contemporaneamente entrambe le versioni a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4873c-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="4873c-152">D2d1effecthelpers. hlsli e il compilatore FXC sono inclusi come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4873c-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="4873c-153">Funzioni helper:</span><span class="sxs-lookup"><span data-stu-id="4873c-153">The helper functions:</span></span>

  - [<span data-ttu-id="4873c-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="4873c-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="4873c-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="4873c-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="4873c-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="4873c-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="4873c-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="4873c-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="4873c-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="4873c-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="4873c-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="4873c-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="4873c-160">\_Voce D2D PS \_</span><span class="sxs-lookup"><span data-stu-id="4873c-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="4873c-161">È anche possibile creare manualmente due versioni di ogni shader e compilarle due volte, purché vengano soddisfatte le specifiche descritte di seguito nelle [specifiche delle funzioni di esportazione](#export-function-specifications) .</span><span class="sxs-lookup"><span data-stu-id="4873c-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="4873c-162">**Solo pixel shader**</span><span class="sxs-lookup"><span data-stu-id="4873c-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="4873c-163">Direct2D non supporta il collegamento di COMPUTE o vertex shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="4873c-164">Tuttavia, se l'effetto USA sia un vertice che un pixel shader, l'output del pixel shader può ancora essere collegato.</span><span class="sxs-lookup"><span data-stu-id="4873c-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="4873c-165">**Campionamento semplice e complesso**</span><span class="sxs-lookup"><span data-stu-id="4873c-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="4873c-166">Il collegamento della funzione shader funziona connettendo l'output di uno pixel shader passare all'input di un passaggio di pixel shader successivo.</span><span class="sxs-lookup"><span data-stu-id="4873c-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="4873c-167">Questa operazione è possibile solo quando il pixel shader di consumo richiede solo un singolo valore di input per eseguire il calcolo. Questo valore, in genere, proviene dal campionamento di una trama di input in corrispondenza della coordinata di trama emessa dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="4873c-168">Questo pixel shader si afferma di eseguire un campionamento semplice.</span><span class="sxs-lookup"><span data-stu-id="4873c-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la conversione in scala di grigi è un esempio di campionamento semplice.](images/simple-sampling.png) |

    

     

    <span data-ttu-id="4873c-171">Alcuni pixel shader, ad esempio una sfocatura gaussiana, calcolano l'output da più campioni di input piuttosto che solo un singolo campione.</span><span class="sxs-lookup"><span data-stu-id="4873c-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="4873c-172">Questo pixel shader si afferma di eseguire un campionamento complesso.</span><span class="sxs-lookup"><span data-stu-id="4873c-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la sfocatura gaussiana è un esempio di campionamento complesso.](images/complex-sampling.png) |

    

     

    <span data-ttu-id="4873c-175">Solo le funzioni shader con input semplici possono avere un input fornito da un'altra funzione shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="4873c-176">Le funzioni shader con input complessi devono essere fornite con una trama di input da campionare.</span><span class="sxs-lookup"><span data-stu-id="4873c-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="4873c-177">Questo significa che Direct2D non collegherà uno shader con input complessi al suo predecessore.</span><span class="sxs-lookup"><span data-stu-id="4873c-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="4873c-178">Quando si usano gli [Helper HLSL Direct2D](hlsl-helpers.md), è necessario indicare in HLSL se uno shader usa input complessi o semplici.</span><span class="sxs-lookup"><span data-stu-id="4873c-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="4873c-179">Esempio di effetto di collegamento compatibile con lo shader</span><span class="sxs-lookup"><span data-stu-id="4873c-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="4873c-180">Utilizzando gli helper D2D, il frammento di codice seguente rappresenta un semplice shader Effect compatibile con collegamento:</span><span class="sxs-lookup"><span data-stu-id="4873c-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="4873c-181">In questo breve esempio si noti che non vengono dichiarati parametri di funzione, che il numero di input e il tipo di ogni input sono dichiarati prima della funzione entry, che l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive per il preprocessore devono essere definite prima che il file helper venga incluso.</span><span class="sxs-lookup"><span data-stu-id="4873c-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="4873c-182">Uno shader compatibile con il collegamento deve fornire sia un pixel shader a singolo passaggio normale che una funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="4873c-183">La macro di [ \_ \_ immissione D2D PS](d2d-ps-entry.md) consente la generazione di ognuno di questi dallo stesso codice, se usato insieme allo script di compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="4873c-184">Quando si compila uno shader completo, le macro vengono espanse nel codice seguente, che ha una firma di input compatibile con gli effetti D2D.</span><span class="sxs-lookup"><span data-stu-id="4873c-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="4873c-185">Quando si compila una versione della funzione Export dello stesso codice, viene generato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="4873c-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="4873c-186">Si noti che l'input di trama, generalmente recuperato tramite il campionamento di un Texture2D, è stato sostituito con un input di funzione (input0).</span><span class="sxs-lookup"><span data-stu-id="4873c-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="4873c-187">Per una descrizione completa, dettagliata delle operazioni da eseguire per scrivere un effetto compatibile con il collegamento, vedere l' [esercitazione sugli effetti personalizzati](custom-effects.md) e l' [esempio di effetti immagine personalizzati Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="4873c-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="4873c-188">Compilazione di un compatibile con il collegamento-shader</span><span class="sxs-lookup"><span data-stu-id="4873c-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="4873c-189">Per poter essere collegato, il BLOB pixel shader passato a D2D deve contenere sia la versione completa che la funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="4873c-190">Questa operazione viene eseguita incorporando la funzione di esportazione compilata \_ nell' \_ area dati privata del BLOB D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="4873c-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="4873c-191">Quando gli shader vengono creati con le funzioni di supporto D2D, è necessario definire una destinazione di compilazione D2D in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="4873c-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="4873c-192">I tipi di destinazione di compilazione sono D2D \_ full \_ shader e D2D \_ funzione.</span><span class="sxs-lookup"><span data-stu-id="4873c-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="4873c-193">La compilazione di un effetto shader compatibile con il collegamento è un processo in due passaggi:</span><span class="sxs-lookup"><span data-stu-id="4873c-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="4873c-194">Compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="4873c-195">Compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="4873c-196">Quando si compila un effetto usando Visual Studio, è necessario creare un file batch che esegua entrambi i comandi FXC ed eseguire questo file batch come un'istruzione di compilazione personalizzata che viene eseguita prima del passaggio di compilazione.</span><span class="sxs-lookup"><span data-stu-id="4873c-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="4873c-197">Passaggio 1: compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="4873c-198">Per compilare la versione della funzione di esportazione dello shader, è necessario passare i flag seguenti a FXC.</span><span class="sxs-lookup"><span data-stu-id="4873c-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4873c-199">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="4873c-199">**Flag**</span></span>                       | <span data-ttu-id="4873c-200">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4873c-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="4873c-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="4873c-201">/T <ShaderModel></span></span>         | <span data-ttu-id="4873c-202">Impostare sul <ShaderModel> profilo di pixel shader appropriato come definito nella [sintassi FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="4873c-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="4873c-203">Deve essere uno dei profili elencati in "HLSL shader linking".</span><span class="sxs-lookup"><span data-stu-id="4873c-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="4873c-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="4873c-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="4873c-205">Impostare sul <MyShaderFile> nome del file HLSL.</span><span class="sxs-lookup"><span data-stu-id="4873c-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="4873c-206">/D \_ funzione D2D</span><span class="sxs-lookup"><span data-stu-id="4873c-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="4873c-207">Questa definizione indica a FXC di compilare la versione della funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="4873c-208">/D D2D \_ voce =<entry></span><span class="sxs-lookup"><span data-stu-id="4873c-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="4873c-209">Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro [di \_ \_ immissione D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="4873c-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="4873c-210">/FL <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="4873c-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="4873c-211">Impostare <MyShaderfile> la posizione in cui si desidera archiviare la versione della funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="4873c-212">Si noti che l'estensione. fxlib è solo per semplificare l'identificazione.</span><span class="sxs-lookup"><span data-stu-id="4873c-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="4873c-213">Passaggio 2: compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="4873c-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="4873c-214">Per compilare la versione completa dello shader con la versione di esportazione incorporata, è necessario passare i flag seguenti a FXC.</span><span class="sxs-lookup"><span data-stu-id="4873c-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4873c-215">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="4873c-215">**Flag**</span></span>                               | <span data-ttu-id="4873c-216">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4873c-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4873c-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="4873c-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="4873c-218">Impostare sul <ShaderModel> profilo di pixel shader appropriato come definito nella [sintassi FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="4873c-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="4873c-219">Deve corrispondere al profilo pixel shader corrispondente al profilo di collegamento specificato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="4873c-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="4873c-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="4873c-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="4873c-221">Impostare sul <MyShaderFile> nome del file HLSL.</span><span class="sxs-lookup"><span data-stu-id="4873c-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="4873c-222">/D D2D \_ completo dello \_ shader</span><span class="sxs-lookup"><span data-stu-id="4873c-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="4873c-223">Questa definizione indica a FXC di compilare la versione completa dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="4873c-224">/D D2D \_ voce =<entry></span><span class="sxs-lookup"><span data-stu-id="4873c-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="4873c-225">Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ entry ().</span><span class="sxs-lookup"><span data-stu-id="4873c-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="4873c-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="4873c-226">/E <entry></span></span>                       | <span data-ttu-id="4873c-227">Impostare sul <entry> nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ entry ().</span><span class="sxs-lookup"><span data-stu-id="4873c-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="4873c-228">/SetPrivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="4873c-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="4873c-229">Questo argomento indica a FXC di incorporare la funzione di esportazione shader generata nel passaggio 1 nell' \_ \_ area dati privata del BLOB D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="4873c-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="4873c-230">/Fo <MyShader> . cso</span><span class="sxs-lookup"><span data-stu-id="4873c-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="4873c-231">Impostare <MyShader> la posizione in cui si desidera archiviare lo shader compilato combinato finale.</span><span class="sxs-lookup"><span data-stu-id="4873c-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="4873c-232">/FH <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="4873c-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="4873c-233">Impostare <MyShader> la posizione in cui si desidera archiviare l'intestazione combinata finale.</span><span class="sxs-lookup"><span data-stu-id="4873c-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="4873c-234">Esporta specifiche delle funzioni</span><span class="sxs-lookup"><span data-stu-id="4873c-234">Export function specifications</span></span>

<span data-ttu-id="4873c-235">È possibile, sebbene non consigliato, creare uno shader con effetto compatibile senza usare gli helper forniti da D2D.</span><span class="sxs-lookup"><span data-stu-id="4873c-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="4873c-236">È necessario prestare attenzione per assicurarsi che entrambe le firme di input complete dello shader e della funzione Export siano conformi alle specifiche D2D.</span><span class="sxs-lookup"><span data-stu-id="4873c-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="4873c-237">Le specifiche per gli shader completi sono le stesse delle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="4873c-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="4873c-238">In breve, i parametri di input pixel shader devono essere \_ posizione SV, posizione della scena \_ e un input TEXCOORD per effetto.</span><span class="sxs-lookup"><span data-stu-id="4873c-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="4873c-239">Per la funzione Export, la funzione deve restituire un float4 e i relativi input devono essere uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4873c-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="4873c-240">Input semplice</span><span class="sxs-lookup"><span data-stu-id="4873c-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="4873c-241">Per gli input semplici, D2D inserisce una funzione di esempio tra la trama di input e la funzione shader oppure l'input viene fornito dall'output di un'altra funzione shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="4873c-242">Input complesso</span><span class="sxs-lookup"><span data-stu-id="4873c-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="4873c-243">Per gli input complessi, D2D passa una coordinata di trama solo come descritto nella documentazione di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4873c-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="4873c-244">Percorso di output</span><span class="sxs-lookup"><span data-stu-id="4873c-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="4873c-245">\_È possibile definire solo un input di posizione della scena.</span><span class="sxs-lookup"><span data-stu-id="4873c-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="4873c-246">Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può utilizzare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4873c-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="4873c-247">La semantica deve essere definita come descritto in precedenza, poiché D2D controllerà la semantica per stabilire come collegare le funzioni.</span><span class="sxs-lookup"><span data-stu-id="4873c-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="4873c-248">Se un input di funzione non corrisponde a uno dei tipi precedenti, la funzione verrà rifiutata per il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="4873c-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4873c-249">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4873c-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4873c-250">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="4873c-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="4873c-251">Interfaccia ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="4873c-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="4873c-252">Interfaccia ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="4873c-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 