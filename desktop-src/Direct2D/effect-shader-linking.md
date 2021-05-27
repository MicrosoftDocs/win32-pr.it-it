---
title: Collegamento degli shader degli effetti
description: Direct2D usa un'ottimizzazione denominata collegamento effect shader che combina più passaggi di rendering del grafico degli effetti in un singolo passaggio.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549236"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="3b8b1-103">Collegamento degli shader degli effetti</span><span class="sxs-lookup"><span data-stu-id="3b8b1-103">Effect Shader Linking</span></span>

<span data-ttu-id="3b8b1-104">Direct2D usa un'ottimizzazione denominata collegamento effect shader che combina più passaggi di rendering del grafico degli effetti in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="3b8b1-105">Panoramica del collegamento degli shader degli effetti</span><span class="sxs-lookup"><span data-stu-id="3b8b1-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="3b8b1-106">Uso del collegamento degli shader degli effetti</span><span class="sxs-lookup"><span data-stu-id="3b8b1-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="3b8b1-107">Creazione di un effetto personalizzato compatibile con il collegamento di shader</span><span class="sxs-lookup"><span data-stu-id="3b8b1-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="3b8b1-108">Esempio di shader con effetto compatibile con il collegamento</span><span class="sxs-lookup"><span data-stu-id="3b8b1-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="3b8b1-109">Compilazione di un linking compatible-shader</span><span class="sxs-lookup"><span data-stu-id="3b8b1-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="3b8b1-110">Passaggio 1: Compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="3b8b1-111">Passaggio 2: Compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="3b8b1-112">Esportare le specifiche della funzione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="3b8b1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b8b1-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="3b8b1-114">Panoramica del collegamento degli shader degli effetti</span><span class="sxs-lookup"><span data-stu-id="3b8b1-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="3b8b1-115">Le ottimizzazioni di collegamento degli effetti shader si basano sul collegamento dello shader HLSL, una funzionalità Direct3D 11.2 che consente di generare pixel e vertex shader in fase di esecuzione collegando funzioni shader precompilato.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="3b8b1-116">Le figure seguenti illustrano il concetto di collegamento degli shader degli effetti in un grafico degli effetti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="3b8b1-117">La prima figura mostra un tipico grafico degli effetti Direct2D con quattro trasformazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="3b8b1-118">Senza il collegamento dello shader, ogni trasformazione utilizza un passaggio di rendering e richiede una superficie intermedia. in totale, questo grafo richiede 4 passaggi e 3 intermedi.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>

![Grafico di trasformazione senza collegamento shader: 4 passaggi e 3 intermedi.](images/shader-transform-graph.png)

<span data-ttu-id="3b8b1-120">La seconda figura mostra lo stesso grafico degli effetti in cui ogni trasformazione di rendering è stata sostituita con una versione di funzione collegabile.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="3b8b1-121">Direct2D è in grado di collegare l'intero grafo ed eseguirlo in un unico passaggio senza richiedere alcun elemento intermedio.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="3b8b1-122">Ciò può fornire una riduzione significativa del tempo di esecuzione della GPU e una riduzione del consumo di memoria GPU di picco.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>

![Grafico di trasformazione con collegamento shader: 1 passaggio, 0 intermedi.](images/shader-linking-graph.png)



 

<span data-ttu-id="3b8b1-124">Il collegamento degli effetti shader funziona su singole trasformazioni all'interno di un effetto; Ciò significa che anche un grafo con un singolo effetto può trarre vantaggio dal collegamento dello shader se tale effetto ha più trasformazioni valide.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="3b8b1-125">Uso del collegamento degli shader degli effetti</span><span class="sxs-lookup"><span data-stu-id="3b8b1-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="3b8b1-126">Se si sta creando un'applicazione Direct2D che usa gli effetti, non è necessario eseguire alcun'operazione per sfruttare i vantaggi del collegamento degli shader degli effetti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="3b8b1-127">Direct2D analizza automaticamente il grafico degli effetti per determinare il modo più ottimale per collegare ogni trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="3b8b1-128">Gli autori di effetti sono responsabili dell'implementazione del loro effetto in modo che supporti il collegamento degli shader degli effetti; Per altre informazioni, vedere la sezione [Creazione di un](#authoring-a-shader-linking-compatible-custom-effect) effetto personalizzato compatibile con il collegamento di uno shader di seguito.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="3b8b1-129">Tutti gli effetti predefiniti supportano il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="3b8b1-130">Direct2D collega solo trasformazioni di rendering adiacenti in situazioni in cui è utile.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="3b8b1-131">Tiene conto di più fattori quando si determina se collegare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="3b8b1-132">Ad esempio, il collegamento dello shader non viene eseguito se una delle trasformazioni usa vertex o compute shader, perché è possibile collegare solo pixel shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="3b8b1-133">Inoltre, se un effetto non è stato creato per essere compatibile con il collegamento dello shader, le trasformazioni circostanti non verranno collegate ad esso.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="3b8b1-134">Nel caso in cui esista un tale rischio di collegamento, Direct2D non collega alcuna trasformazione adiacente al pericolo, ma tenta comunque di collegare il resto del grafico.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>

![grafico di trasformazione con un pericolo di collegamento: 2 passaggi, 1 intermedio.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="3b8b1-136">Creazione di un effetto personalizzato compatibile con il collegamento di shader</span><span class="sxs-lookup"><span data-stu-id="3b8b1-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="3b8b1-137">Se si crea un effetto Direct2D personalizzato, è necessario assicurarsi che le relative trasformazioni supportino il collegamento degli shader degli effetti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="3b8b1-138">Ciò richiede alcune modifiche secondarie rispetto alla modalità di implementazione degli effetti personalizzati precedenti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="3b8b1-139">Se una trasformazione all'interno dell'effetto personalizzato non supporta il collegamento dello shader, Direct2D non la collega alle trasformazioni adiacenti nel grafico degli effetti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="3b8b1-140">L'autore di un effetto personalizzato deve essere a conoscenza di diversi concetti e requisiti chiave:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="3b8b1-141">**Nessuna modifica alle implementazioni dell'interfaccia effettive**</span><span class="sxs-lookup"><span data-stu-id="3b8b1-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="3b8b1-142">Non è necessario modificare il codice che implementa le varie interfacce di effetto, ad esempio [ID2D1DrawTransform.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="3b8b1-143">**Fornire sia una versione completa che una versione della funzione di esportazione degli shader**</span><span class="sxs-lookup"><span data-stu-id="3b8b1-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="3b8b1-144">È necessario fornire una versione della funzione di esportazione degli shader dell'effetto collegabili da Direct2D.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="3b8b1-145">È anche necessario continuare a fornire lo shader originale completo. Ciò è dovuto al fatto che Direct2D seleziona in fase di esecuzione la versione corretta dello shader a seconda che il collegamento dello shader sia applicato a un particolare collegamento nel grafico.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="3b8b1-146">Se una trasformazione fornisce solo il BLOB pixel shader completo (tramite [ID2D1EffectContext::LoadPixelShader),](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)non verrà collegato alle trasformazioni adiacenti.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="3b8b1-147">**Funzioni helper**</span><span class="sxs-lookup"><span data-stu-id="3b8b1-147">**Helper functions**</span></span>

    <span data-ttu-id="3b8b1-148">Direct2D fornisce macro [e funzioni helper HLSL](hlsl-helpers.md) che generano automaticamente le versioni delle funzioni complete ed esportate di uno shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="3b8b1-149">Questi helper sono disponibili in d2d1effecthelpers.hlsli.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="3b8b1-150">Inoltre, il compilatore HLSL (FXC) consente di inserire lo shader della funzione di esportazione in un campo privato nello shader completo.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="3b8b1-151">In questo modo, è necessario creare uno shader una sola volta e passare entrambe le versioni a Direct2D contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="3b8b1-152">Sia d2d1effecthelpers.hlsli che il compilatore FXC sono inclusi come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="3b8b1-153">Le funzioni helper:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-153">The helper functions:</span></span>

  - [<span data-ttu-id="3b8b1-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="3b8b1-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="3b8b1-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="3b8b1-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="3b8b1-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="3b8b1-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="3b8b1-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="3b8b1-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="3b8b1-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="3b8b1-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="3b8b1-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="3b8b1-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="3b8b1-160">VOCE D2D \_ \_ PS</span><span class="sxs-lookup"><span data-stu-id="3b8b1-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="3b8b1-161">È anche possibile creare manualmente due versioni di ogni shader e compilarle due volte, purché siano soddisfatte le specifiche descritte di seguito in [Esportare](#export-function-specifications) le specifiche della funzione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="3b8b1-162">**Solo pixel shader**</span><span class="sxs-lookup"><span data-stu-id="3b8b1-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="3b8b1-163">Direct2D non supporta il collegamento di calcolo o vertex shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="3b8b1-164">Tuttavia, se l'effetto usa sia un vertice che pixel shader, l'output del pixel shader può comunque essere collegato.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="3b8b1-165">**Campionamento semplice e complesso**</span><span class="sxs-lookup"><span data-stu-id="3b8b1-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="3b8b1-166">Il collegamento della funzione shader funziona connettendo l'output di pixel shader passaggio all'input di un passaggio pixel shader successivo.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="3b8b1-167">Ciò è possibile solo quando l'pixel shader richiede un solo valore di input per eseguire il calcolo. questo valore deriva in genere dal campionamento di una trama di input in corrispondenza della coordinata di trama emessa dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="3b8b1-168">Tale pixel shader si dice che eseere un campionamento semplice.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-168">Such a pixel shader is said to perform simple sampling.</span></span>

    ![La conversione in scala di grigi è un esempio di campionamento semplice.](images/simple-sampling.png)

    <span data-ttu-id="3b8b1-171">Alcuni pixel shader, ad esempio una sfocatura gaussiana, calcolano l'output da più campioni di input anziché da un singolo campione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="3b8b1-172">Tale pixel shader si dice che eseere un campionamento complesso.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    ![La sfocatura gaussiana è un esempio di campionamento complesso.](images/complex-sampling.png)

    
    <span data-ttu-id="3b8b1-175">Solo le funzioni shader con input semplici possono avere l'input fornito da un'altra funzione shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="3b8b1-176">Le funzioni shader con input complessi devono essere fornite con una trama di input da campionare.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="3b8b1-177">Ciò significa che Direct2D non collega uno shader con input complessi al relativo predecessore.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="3b8b1-178">Quando si usano [gli helper HLSL Direct2D,](hlsl-helpers.md)è necessario indicare in HLSL se uno shader usa input complessi o semplici.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="3b8b1-179">Esempio di shader con effetto compatibile con il collegamento</span><span class="sxs-lookup"><span data-stu-id="3b8b1-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="3b8b1-180">Usando gli helper D2D, il frammento di codice seguente rappresenta un semplice shader con effetto compatibile con il collegamento:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

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

<span data-ttu-id="3b8b1-181">In questo breve esempio si noti che non viene dichiarato alcun parametro di funzione, che il numero di input e il tipo di ogni input vengono dichiarati prima della funzione di immissione, l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive del preprocessore devono essere definite prima dell'inserimento del file helper.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="3b8b1-182">Uno shader compatibile con il collegamento deve fornire sia una normale funzione a pixel shader che una funzione di esportazione shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="3b8b1-183">La macro [D2D \_ PS \_ ENTRY](d2d-ps-entry.md) consente di generare ognuno di questi elementi dallo stesso codice, se usato in combinazione con lo script di compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="3b8b1-184">Quando si compila uno shader completo, le macro vengono espanse nel codice seguente, che ha una firma di input compatibile con gli effetti D2D.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="3b8b1-185">Quando si compila una versione della funzione di esportazione dello stesso codice, viene generato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="3b8b1-186">Si noti che l'input della trama, normalmente recuperato tramite campionamento di texture2D, è stato sostituito con un input di funzione (input0).</span><span class="sxs-lookup"><span data-stu-id="3b8b1-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="3b8b1-187">Per una descrizione dettagliata completa delle operazioni da eseguire per scrivere un effetto [](custom-effects.md) compatibile con il collegamento, vedere l'esercitazione sugli effetti personalizzati e l'esempio di effetti immagine personalizzati [Direct2D.](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="3b8b1-188">Compilazione di uno shader compatibile con il collegamento</span><span class="sxs-lookup"><span data-stu-id="3b8b1-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="3b8b1-189">Per poter essere collegabile, pixel shader BLOB passato a D2D deve contenere sia la versione completa che la versione della funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="3b8b1-190">Questa operazione viene eseguita incorporando la funzione di esportazione compilata nell'area DATI \_ PRIVATI DEL BLOB D3D. \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b8b1-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="3b8b1-191">Quando gli shader vengono creati con le funzioni helper D2D, è necessario definire una destinazione di compilazione D2D in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="3b8b1-192">I tipi di destinazione di compilazione sono D2D \_ FULL \_ SHADER e D2D \_ FUNCTION.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="3b8b1-193">La compilazione di uno shader con effetto compatibile con il collegamento è un processo in due passaggi:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="3b8b1-194">Compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="3b8b1-195">Compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="3b8b1-196">Quando si compila un effetto usando Visual Studio, è necessario creare un file batch che esegue entrambi i comandi FXC ed eseguire questo file batch come istruzione di compilazione personalizzata che viene eseguita prima del passaggio di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="3b8b1-197">Passaggio 1: Compilare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="3b8b1-198">Per compilare la versione della funzione di esportazione dello shader, è necessario passare i flag seguenti a FXC.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="3b8b1-199">Flag</span><span class="sxs-lookup"><span data-stu-id="3b8b1-199">Flag</span></span>                            |    <span data-ttu-id="3b8b1-200">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-200">Description</span></span>                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8b1-201">/t <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="3b8b1-201">/T <ShaderModel></span></span>         | <span data-ttu-id="3b8b1-202">Impostare <ShaderModel> sul profilo di pixel shader appropriato, come definito in [Sintassi FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="3b8b1-203">Deve trattarsi di uno dei profili elencati in "Collegamento dello shader HLSL".</span><span class="sxs-lookup"><span data-stu-id="3b8b1-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="3b8b1-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="3b8b1-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="3b8b1-205">Impostare <MyShaderFile> sul nome del file HLSL.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="3b8b1-206">FUNZIONE /D \_ D2D</span><span class="sxs-lookup"><span data-stu-id="3b8b1-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="3b8b1-207">Questa definizione indica a FXC di compilare la versione della funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="3b8b1-208">/D D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="3b8b1-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="3b8b1-209">Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro [D2D \_ PS \_ ENTRY.](d2d-ps-entry.md)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="3b8b1-210">/Fl <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="3b8b1-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="3b8b1-211">Impostare <MyShaderfile> su in cui archiviare la versione della funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="3b8b1-212">Si noti che l'estensione .fxlib è solo per facilitare l'identificazione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="3b8b1-213">Passaggio 2: Compilare lo shader completo e incorporare la funzione di esportazione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="3b8b1-214">Per compilare la versione completa dello shader con la versione di esportazione incorporata, è necessario passare i flag seguenti a FXC.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="3b8b1-215">Flag</span><span class="sxs-lookup"><span data-stu-id="3b8b1-215">Flag</span></span>                                    |    <span data-ttu-id="3b8b1-216">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-216">Description</span></span>                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8b1-217">/t <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="3b8b1-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="3b8b1-218">Impostare <ShaderModel> sul profilo di pixel shader appropriato, come definito in [Sintassi FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="3b8b1-219">Deve essere il profilo pixel shader corrispondente al profilo di collegamento specificato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="3b8b1-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="3b8b1-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="3b8b1-221">Impostare <MyShaderFile> sul nome del file HLSL.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3b8b1-222">/D D D2D \_ FULL \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="3b8b1-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="3b8b1-223">Questa definizione indica a FXC di compilare la versione completa dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="3b8b1-224">/D D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="3b8b1-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="3b8b1-225">Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro D2D PS \_ \_ ENTRY().</span><span class="sxs-lookup"><span data-stu-id="3b8b1-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="3b8b1-226">/e <entry></span><span class="sxs-lookup"><span data-stu-id="3b8b1-226">/E <entry></span></span>                       | <span data-ttu-id="3b8b1-227">Impostare <entry> sul nome del punto di ingresso HLSL definito all'interno della macro D2D \_ PS \_ ENTRY().</span><span class="sxs-lookup"><span data-stu-id="3b8b1-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="3b8b1-228">/setprivate <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="3b8b1-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="3b8b1-229">Questo argomento indica a FXC di incorporare lo shader della funzione di esportazione generato nel passaggio 1 nell'area DATI PRIVATI \_ DEL BLOB D3D. \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b8b1-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="3b8b1-230">/Fo <MyShader> .cso</span><span class="sxs-lookup"><span data-stu-id="3b8b1-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="3b8b1-231">Impostare <MyShader> su dove si vuole archiviare lo shader compilato finale combinato.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="3b8b1-232">/Fh <MyShader> .h</span><span class="sxs-lookup"><span data-stu-id="3b8b1-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="3b8b1-233">Impostare <MyShader> su dove si vuole archiviare l'intestazione finale combinata.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a><span data-ttu-id="3b8b1-234">Esportare le specifiche della funzione</span><span class="sxs-lookup"><span data-stu-id="3b8b1-234">Export function specifications</span></span>

<span data-ttu-id="3b8b1-235">È possibile, anche se non consigliato, creare uno shader con effetto compatibile senza usare gli helper forniti da D2D.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="3b8b1-236">È necessario assicurarsi che sia lo shader completo che le firme di input della funzione di esportazione siano conformi alle specifiche D2D.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="3b8b1-237">Le specifiche per gli shader completi sono le stesse delle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="3b8b1-238">In breve, i pixel shader di input devono essere SV POSITION, SCENE POSITION e \_ \_ un TEXCOORD per ogni input dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="3b8b1-239">Per la funzione di esportazione, la funzione deve restituire un valore float4 e i relativi input devono essere di uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b8b1-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="3b8b1-240">Input semplice</span><span class="sxs-lookup"><span data-stu-id="3b8b1-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="3b8b1-241">Per gli input semplici, D2D inserirà una funzione Sample tra la trama di input e la funzione shader oppure l'input verrà fornito dall'output di un'altra funzione shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="3b8b1-242">Input complesso</span><span class="sxs-lookup"><span data-stu-id="3b8b1-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="3b8b1-243">Per gli input complessi, D2D passerà solo una coordinata di trama, come descritto Windows 8 documentazione.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="3b8b1-244">Percorso di output</span><span class="sxs-lookup"><span data-stu-id="3b8b1-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="3b8b1-245">È possibile definire \_ un solo input SCENE POSITION.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="3b8b1-246">Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può usare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="3b8b1-247">La semantica deve essere definita come sopra, perché D2D ispeziona la semantica per decidere come collegare le funzioni.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="3b8b1-248">Se un input di funzione non corrisponde a uno dei tipi precedenti, la funzione verrà rifiutata per il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b8b1-249">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b8b1-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8b1-250">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="3b8b1-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="3b8b1-251">Interfaccia ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="3b8b1-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="3b8b1-252">Interfaccia ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="3b8b1-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 