---
title: Scrittura di shader HLSL in Direct3D 9
description: Scrittura di shader HLSL in Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335385"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="ea1e8-103">Scrittura di shader HLSL in Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="ea1e8-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="ea1e8-104">Nozioni di base su vertex shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="ea1e8-105">Nozioni di base sul pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="ea1e8-106">Stati della fase della trama e del campionatore</span><span class="sxs-lookup"><span data-stu-id="ea1e8-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="ea1e8-107">Input pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="ea1e8-108">Output pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="ea1e8-109">Input e variabili shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="ea1e8-110">Dichiarazione di variabili shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="ea1e8-111">Input uniform shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="ea1e8-112">Variazione di input e semantica di shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="ea1e8-113">Campionatori e oggetti Texture</span><span class="sxs-lookup"><span data-stu-id="ea1e8-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="ea1e8-114">Scrittura di funzioni</span><span class="sxs-lookup"><span data-stu-id="ea1e8-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="ea1e8-115">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="ea1e8-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="ea1e8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea1e8-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="ea1e8-117">Vertex-Shader di base</span><span class="sxs-lookup"><span data-stu-id="ea1e8-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="ea1e8-118">Quando è in funzione, un vertex shader programmabile sostituisce l'elaborazione dei vertici eseguita dalla pipeline grafica Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="ea1e8-119">Quando si usa un vertex shader, le informazioni sullo stato relative alle operazioni di trasformazione e illuminazione vengono ignorate dalla pipeline di funzioni fisse.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="ea1e8-120">Quando il vertex shader è disabilitato e viene restituita l'elaborazione di funzioni fisse, vengono applicate tutte le impostazioni dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="ea1e8-121">Prima dell'esecuzione del vertex shader, è necessario eseguire il tessellamento delle primitive di ordine elevato.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="ea1e8-122">Le implementazioni che eseguono la tessellazione della superficie dopo l'elaborazione dello shader devono eseguire questa operazione in modo non evidente per il codice dell'applicazione e dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="ea1e8-123">Come minimo, un vertex shader deve eseguire l'output della posizione del vertice nello spazio di ritaglio omogeneo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="ea1e8-124">Facoltativamente, il vertex shader può eseguire l'output delle coordinate della trama, del colore dei vertici, dell'illuminazione dei vertici, dei fattori del vertice e così via.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="ea1e8-125">Pixel-Shader di base</span><span class="sxs-lookup"><span data-stu-id="ea1e8-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="ea1e8-126">L'elaborazione dei pixel viene eseguita dai pixel shader su singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="ea1e8-127">I pixel shader funzionano insieme ai vertex shader; l'output di un vertex shader fornisce gli input per un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="ea1e8-128">Altre operazioni sui pixel (fusione della nebbia, operazioni di stencil e fusione della destinazione di rendering) si verificano dopo l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="ea1e8-129">Stati della fase di trama e del campionatore</span><span class="sxs-lookup"><span data-stu-id="ea1e8-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="ea1e8-130">Un pixel shader sostituisce completamente la funzionalità di fusione dei pixel specificata dal blender a più trame, incluse le operazioni definite in precedenza dagli stati della fase di trama.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="ea1e8-131">Le operazioni di campionamento e filtro trame controllate dagli stati della fase di trama standard per la minificazione, l'ingrandimento, il filtro mip e le modalità di indirizzamento del wrapping, possono essere inizializzate negli shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="ea1e8-132">L'applicazione è libera di modificare questi stati senza richiedere la rigenerazione dello shader attualmente associato.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="ea1e8-133">L'impostazione dello stato può essere resa ancora più semplice se gli shader sono progettati all'interno di un effetto.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="ea1e8-134">Input pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="ea1e8-135">Per pixel shader versioni ps 1 - ps 2 0, i colori diffusi e \_ \_ speculari vengono \_ saturati (con chiusura) nell'intervallo da 0 a 1 prima dell'uso da parte dello \_ shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="ea1e8-136">Si presuppone che i valori dei pixel shader siano corretti dal punto di vista, ma questo non è garantito (per tutto l'hardware).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="ea1e8-137">I colori campionati dalle coordinate della trama vengono iterati in modo corretto dal punto di vista e sono ancorati all'intervallo da 0 a 1 durante l'iterazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="ea1e8-138">Output pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="ea1e8-139">Per pixel shader versioni ps \_ \_ 1 1 - ps 1 4, il risultato generato dal pixel shader è il contenuto del \_ \_ registro r0.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="ea1e8-140">Tutto ciò che contiene al termine dell'elaborazione dello shader viene inviato alla fase della nebbia e al blender di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="ea1e8-141">Per pixel shader versioni ps 2 0 e successive, il colore di output viene generato da \_ \_ oC0 - oC4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="ea1e8-142">Input shader e variabili shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="ea1e8-143">Dichiarazione di variabili shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="ea1e8-144">Input uniform shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="ea1e8-145">Variazione di input e semantica di shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="ea1e8-146">Campionatori e oggetti Texture</span><span class="sxs-lookup"><span data-stu-id="ea1e8-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="ea1e8-147">Dichiarazione di variabili shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-147">Declaring Shader Variables</span></span>

<span data-ttu-id="ea1e8-148">La dichiarazione di variabile più semplice include un tipo e un nome di variabile, ad esempio questa dichiarazione a virgola mobile:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="ea1e8-149">È possibile inizializzare una variabile nella stessa istruzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="ea1e8-150">È possibile dichiarare una matrice di variabili.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="ea1e8-151">o dichiarato e inizializzato nella stessa istruzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="ea1e8-152">Di seguito sono illustrate alcune dichiarazioni che illustrano molte delle caratteristiche delle variabili HLSL (High-Level Shader Language):</span><span class="sxs-lookup"><span data-stu-id="ea1e8-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="ea1e8-153">Le dichiarazioni di dati possono usare qualsiasi tipo valido, tra cui:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="ea1e8-154">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="ea1e8-155">Tipo di vettore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="ea1e8-156">Tipo matrice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="ea1e8-157">Tipo shader (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="ea1e8-158">Tipo di campionatore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="ea1e8-159">Tipo definito dall'utente (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="ea1e8-160">Uno shader può avere variabili, argomenti e funzioni di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="ea1e8-161">Le variabili di primo livello vengono dichiarate all'esterno di tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="ea1e8-162">Gli argomenti di primo livello sono parametri di una funzione di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="ea1e8-163">Una funzione di primo livello è qualsiasi funzione chiamata dall'applicazione (a differenza di una funzione chiamata da un'altra funzione).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="ea1e8-164">Input uniform shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="ea1e8-165">I vertex shader e i pixel shader accettano due tipi di dati di input: variabili e uniformi.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="ea1e8-166">L'input variabile è dato da dati univoci per ogni esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="ea1e8-167">Per un vertex shader, i dati variabili (ad esempio posizione, normale e così via) provengono dai flussi dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="ea1e8-168">I dati uniformi ,ad esempio il colore del materiale, la trasformazione del mondo e così via, sono costanti per più esecuzioni di uno shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="ea1e8-169">Per gli utenti che hanno familiarità con i modelli di shader dell'assembly, i dati uniformi vengono specificati da registri costanti e dati variabili dai registri v e t.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="ea1e8-170">I dati uniformi possono essere specificati da due metodi.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="ea1e8-171">Il metodo più comune è dichiarare le variabili globali e usarle all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="ea1e8-172">Qualsiasi uso di variabili globali all'interno di uno shader comporta l'aggiunta di tale variabile all'elenco di variabili uniformi richieste dallo shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="ea1e8-173">Il secondo metodo è contrassegnare un parametro di input della funzione shader di primo livello come uniforme.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="ea1e8-174">Questo contrassegno specifica che la variabile specificata deve essere aggiunta all'elenco di variabili uniformi.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="ea1e8-175">Le variabili uniformi usate da uno shader vengono comunicate all'applicazione tramite la tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="ea1e8-176">La tabella delle costanti è il nome della tabella dei simboli che definisce il modo in cui le variabili uniformi usate da uno shader si adattano ai registri costanti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="ea1e8-177">I parametri uniformi della funzione vengono visualizzati nella tabella delle costanti preceduti da un segno di dollaro ($), a differenza delle variabili globali.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="ea1e8-178">Il simbolo del dollaro è necessario per evitare conflitti di nome tra input uniformi locali e variabili globali con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="ea1e8-179">La tabella delle costanti contiene le posizioni dei registri costanti di tutte le variabili uniformi usate dallo shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="ea1e8-180">La tabella include anche le informazioni sul tipo e il valore predefinito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="ea1e8-181">Variazione di input e semantica di shader</span><span class="sxs-lookup"><span data-stu-id="ea1e8-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="ea1e8-182">I parametri di input variabili (di una funzione shader di primo livello) devono essere contrassegnati con una parola chiave semantica o uniforme che indica che il valore è costante per l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="ea1e8-183">Se un input dello shader di primo livello non è contrassegnato con una parola chiave semantica o uniforme, la compilazione dello shader avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="ea1e8-184">La semantica di input è un nome usato per collegare l'input specificato a un output della parte precedente della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="ea1e8-185">Ad esempio, la semantica di input POSITION0 viene usata dai vertex shader per specificare dove devono essere collegati i dati di posizione dal vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="ea1e8-186">I pixel shader e i vertex shader hanno set diversi di semantica di input a causa delle diverse parti della pipeline grafica che si inserire in ogni unità shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="ea1e8-187">La semantica di input del vertex shader descrive le informazioni per vertice (ad esempio: posizione, normale, coordinate della trama, colore, tangente, binormale e così via) da caricare da un buffer dei vertici in un modulo che può essere utilizzato dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="ea1e8-188">La semantica di input esegue direttamente il mapping all'utilizzo della dichiarazione dei vertici e all'indice di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="ea1e8-189">La semantica di input del pixel shader descrive le informazioni fornite per pixel dall'unità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="ea1e8-190">I dati vengono generati interpolando tra gli output del vertex shader per ogni vertice della primitiva corrente.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="ea1e8-191">La semantica pixel shader input di base collega le informazioni sul colore di output e sulle coordinate della trama ai parametri di input.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="ea1e8-192">La semantica di input può essere assegnata all'input dello shader tramite due metodi:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="ea1e8-193">Aggiunta di due punti e del nome semantico alla dichiarazione del parametro.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="ea1e8-194">Definizione di una struttura di input con semantica di input assegnata a ogni membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="ea1e8-195">I vertex shader e i pixel shader forniscono dati di output alla fase successiva della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="ea1e8-196">La semantica di output viene usata per specificare il modo in cui i dati generati dallo shader devono essere collegati agli input della fase successiva.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="ea1e8-197">Ad esempio, la semantica di output per un vertex shader viene usata per collegare gli output degli interpolatori nel rasterizzatore per generare i dati di input per l'pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="ea1e8-198">Gli pixel shader output sono i valori forniti all'unità di fusione alfa per ognuna delle destinazioni di rendering o il valore di profondità scritto nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="ea1e8-199">La semantica di output del vertex shader viene usata per collegare lo shader sia al pixel shader che alla fase di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="ea1e8-200">Un vertex shader utilizzato dal rasterizzatore e non esposto al pixel shader deve generare almeno i dati di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="ea1e8-201">I vertex shader che generano dati di coordinate e colori della trama forniscono i dati a un pixel shader al termine dell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="ea1e8-202">La semantica di output del pixel shader associa i colori di output di un pixel shader alla destinazione di rendering corretta.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="ea1e8-203">Il pixel shader di output è collegato alla fase di alpha blend, che determina come vengono modificate le destinazioni di rendering di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="ea1e8-204">L pixel shader di profondità può essere usato per modificare i valori di profondità di destinazione nella posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="ea1e8-205">L'output di profondità e più destinazioni di rendering sono supportati solo con alcuni modelli di shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="ea1e8-206">La sintassi per la semantica di output è identica alla sintassi per specificare la semantica di input.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="ea1e8-207">La semantica può essere specificata direttamente nei parametri dichiarati come parametri "out" o assegnata durante la definizione di una struttura restituita come parametro "out" o come valore restituito di una funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="ea1e8-208">La semantica identifica la origine dei dati.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="ea1e8-209">La semantica è un identificatore facoltativo che identifica gli input e gli output dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="ea1e8-210">La semantica viene visualizzata in una delle tre posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="ea1e8-211">Dopo un membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-211">After a structure member.</span></span>
-   <span data-ttu-id="ea1e8-212">Dopo un argomento nell'elenco di argomenti di input di una funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="ea1e8-213">Dopo l'elenco di argomenti di input della funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-213">After the function's input argument list.</span></span>

<span data-ttu-id="ea1e8-214">Questo esempio usa una struttura per fornire uno o più input di vertex shader e un'altra struttura per fornire uno o più output di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="ea1e8-215">Ogni membro della struttura usa una semantica.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="ea1e8-216">La struttura di input identifica i dati del vertex buffer che fornirà gli input dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="ea1e8-217">Questo shader esegue il mapping dei dati degli elementi position, normal e blendweight del buffer dei vertici nei registri vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="ea1e8-218">Il tipo di dati di input non deve corrispondere esattamente al tipo di dati della dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="ea1e8-219">Se non corrisponde esattamente, i dati dei vertici verranno convertiti automaticamente nel tipo di dati HLSL quando vengono scritti nei registri shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="ea1e8-220">Ad esempio, se i dati normali fossero definiti come di tipo UINT dall'applicazione, verrebbero convertiti in float3 quando vengono letti dallo shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="ea1e8-221">Se i dati nel flusso dei vertici contengono meno componenti del tipo di dati shader corrispondente, i componenti mancanti verranno inizializzati su 0 (ad eccezione di w, che viene inizializzato su 1).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="ea1e8-222">La semantica di input è simile ai valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="ea1e8-223">La struttura di output identifica i parametri di output del vertex shader di posizione e colore.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="ea1e8-224">Questi output verranno usati dalla pipeline per la rasterizzazione del triangolo (nell'elaborazione primitiva).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="ea1e8-225">L'output contrassegnato come dati di posizione indica la posizione di un vertice nello spazio omogeneo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="ea1e8-226">Come minimo, un vertex shader deve generare dati di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="ea1e8-227">La posizione dello spazio dello schermo viene calcolata dopo il completamento del vertex shader dividendo la coordinata (x, y, z) per w.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="ea1e8-228">Nello spazio dello schermo , -1 e 1 sono i valori minimo e massimo x e y dei limiti del viewport, mentre z viene usato per il test z-buffer.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="ea1e8-229">La semantica di output è simile ai valori in [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="ea1e8-230">In generale, una struttura di output per un vertex shader può essere usata anche come struttura di input per un pixel shader, a condizione che il pixel shader non letta da alcuna variabile contrassegnata con la semantica di posizione, dimensione del punto o osa.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="ea1e8-231">Questa semantica è associata a valori scalari per vertice che non vengono usati da un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="ea1e8-232">Se questi valori sono necessari per il pixel shader, possono essere copiati in un'altra variabile di output che usa una pixel shader semantica.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="ea1e8-233">Le variabili globali vengono assegnate automaticamente ai registri dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="ea1e8-234">Le variabili globali sono chiamate anche parametri uniformi perché il contenuto della variabile è lo stesso per tutti i pixel elaborati ogni volta che viene chiamato lo shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="ea1e8-235">I registri sono contenuti nella tabella delle costanti, che può essere letta usando [**l'interfaccia ID3DXConstantTable.**](/windows/desktop/direct3d9/id3dxconstanttable)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="ea1e8-236">La semantica di input per i pixel shader esegue il mapping dei valori in registri hardware specifici per il trasporto tra vertex shader e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="ea1e8-237">Ogni tipo di registro ha proprietà specifiche.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-237">Each register type has specific properties.</span></span> <span data-ttu-id="ea1e8-238">Poiché attualmente esistono solo due semantiche per le coordinate di colore e trama, è comune che la maggior parte dei dati sia contrassegnata come coordinata di trama anche quando non lo è.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="ea1e8-239">Si noti che la struttura di output del vertex shader ha usato un input con dati di posizione, che non viene usato dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="ea1e8-240">HLSL consente dati di output validi di un vertex shader che non sono dati di input validi per un pixel shader, purché non vi sia riferimento nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="ea1e8-241">Gli argomenti di input possono anche essere matrici.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="ea1e8-242">La semantica viene incrementata automaticamente dal compilatore per ogni elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="ea1e8-243">Si consideri, ad esempio, la dichiarazione esplicita seguente:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="ea1e8-244">La dichiarazione esplicita specificata in precedenza equivale alla dichiarazione seguente che avrà una semantica incrementata automaticamente dal compilatore:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="ea1e8-245">Proprio come la semantica di input, la semantica di output identifica l'utilizzo dei pixel shader di output.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="ea1e8-246">Molti pixel shader scrivono in un solo colore di output.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="ea1e8-247">I pixel shader possono anche scrivere un valore di profondità in una o più destinazioni di rendering contemporaneamente (fino a quattro).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="ea1e8-248">Analogamente ai vertex shader, i pixel shader usano una struttura per restituire più di un output.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="ea1e8-249">Questo shader scrive 0 nei componenti di colore e nel componente di profondità.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="ea1e8-250">I colori di output del pixel shader devono essere di tipo float4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="ea1e8-251">Quando si scrivono più colori, tutti i colori di output devono essere utilizzati in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="ea1e8-252">In altre parole, [COLOR1 non può](dx-graphics-hlsl-semantics.md) essere un output a meno [che COLOR0](dx-graphics-hlsl-semantics.md) non sia già stato scritto.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="ea1e8-253">L'output della profondità del pixel shader deve essere di tipo float1.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="ea1e8-254">Campionatori e oggetti Texture</span><span class="sxs-lookup"><span data-stu-id="ea1e8-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="ea1e8-255">Un campionatore contiene lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-255">A sampler contains sampler state.</span></span> <span data-ttu-id="ea1e8-256">Lo stato del campionatore specifica la trama da campionare e controlla il filtro eseguito durante il campionamento.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="ea1e8-257">Per campionare una trama sono necessari tre elementi:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="ea1e8-258">Trama</span><span class="sxs-lookup"><span data-stu-id="ea1e8-258">A texture</span></span>
-   <span data-ttu-id="ea1e8-259">Un campionatore (con stato sampler)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="ea1e8-260">Istruzione di campionamento</span><span class="sxs-lookup"><span data-stu-id="ea1e8-260">A sampling instruction</span></span>

<span data-ttu-id="ea1e8-261">I campionatori possono essere inizializzati con trame e stato del campionatore, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="ea1e8-262">Ecco un esempio del codice per campionare una trama 2D:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="ea1e8-263">La trama viene dichiarata con una variabile di trama tex0.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="ea1e8-264">In questo esempio viene dichiarata una variabile sampler denominata s \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="ea1e8-265">Il campionatore contiene lo stato del campionatore all'interno delle parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="ea1e8-266">Include la trama che verrà campionata e, facoltativamente, lo stato del filtro, ovvero le modalità di ritorno a capo, le modalità di filtro e così via.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="ea1e8-267">Se lo stato del campionatore viene omesso, viene applicato uno stato del campionatore predefinito che specifica un filtro lineare e una modalità di ritorno a capo per le coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="ea1e8-268">La funzione sampler accetta una coordinata di trama a virgola mobile a due componenti e restituisce un colore a due componenti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="ea1e8-269">Viene rappresentato con il tipo restituito float2 e rappresenta i dati nei componenti rosso e verde.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="ea1e8-270">Sono definiti quattro tipi di campionatori (vedere Parole chiave [)](dx-graphics-hlsl-appendix.md)e le ricerche trame vengono eseguite dalle funzioni intrinseche: [**tex1D(s, t) (DirectX HLSL),**](dx-graphics-hlsl-tex1d.md) [**tex2D(s, t) (DirectX HLSL),**](dx-graphics-hlsl-tex2d.md) [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL).**](dx-graphics-hlsl-texcube.md)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="ea1e8-271">Ecco un esempio di campionamento 3D:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="ea1e8-272">Questa dichiarazione del campionatore usa lo stato del campionatore predefinito per le impostazioni del filtro e la modalità indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="ea1e8-273">Ecco l'esempio di campionamento del cubo corrispondente:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="ea1e8-274">Infine, ecco l'esempio di campionamento 1D:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="ea1e8-275">Poiché il runtime non supporta trame 1D, il compilatore userà una trama 2D con la consapevolezza che la coordinata y non è importante.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="ea1e8-276">Poiché [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) viene implementato come ricerca trame 2D, il compilatore è libero di scegliere il componente y in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="ea1e8-277">In alcuni rari scenari, il compilatore non può scegliere un componente y efficiente, nel qual caso verrà generato un avviso.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="ea1e8-278">Questo particolare esempio è inefficiente perché il compilatore deve spostare la coordinata di input in un altro registro (perché una ricerca 1D viene implementata come ricerca 2D e la coordinata di trama è dichiarata come float1).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="ea1e8-279">Se il codice viene riscritto usando un input float2 anziché float1, il compilatore può usare la coordinata di trama di input perché sa che y viene inizializzato su qualcosa.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="ea1e8-280">Tutte le ricerche trame possono essere aggiunte con "bias" o "proj", ovvero [**tex2Dbias (DirectX HLSL),**](dx-graphics-hlsl-tex2dbias.md) [**texCUBEproj (DirectX HLSL).**](dx-graphics-hlsl-texcubeproj.md)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="ea1e8-281">Con il suffisso "proj", la coordinata della trama viene divisa per il componente w.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="ea1e8-282">Con "bias", il livello mip viene spostato dal componente w.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="ea1e8-283">Pertanto, tutte le ricerche trame con un suffisso accettano sempre un input float4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="ea1e8-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) e [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorano rispettivamente i componenti yz e z.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="ea1e8-285">I campionatori possono essere usati anche nella matrice, anche se nessun back-end supporta attualmente l'accesso dinamico alle matrici dei campionatori.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="ea1e8-286">Pertanto, quanto segue è valido perché può essere risolto in fase di compilazione:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="ea1e8-287">Questo esempio, tuttavia, non è valido.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="ea1e8-288">L'accesso dinamico dei campionatori è utile principalmente per la scrittura di programmi con cicli letterali.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="ea1e8-289">Il codice seguente illustra l'accesso alla matrice sampler:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="ea1e8-290">L'uso del runtime di debug Microsoft Direct3D consente di rilevare le mancate corrispondenze tra il numero di componenti in una trama e un campionatore.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="ea1e8-291">Scrittura di funzioni</span><span class="sxs-lookup"><span data-stu-id="ea1e8-291">Writing Functions</span></span>

<span data-ttu-id="ea1e8-292">Le funzioni suddivideno le attività di grandi dimensioni in attività più piccole.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="ea1e8-293">Piccole attività sono più facili da eseguire il debug e possono essere riutilizzate, una volta dimostrate.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="ea1e8-294">Le funzioni possono essere usate per nascondere i dettagli di altre funzioni, in modo da semplificare l'esecuzione di un programma composto da funzioni.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="ea1e8-295">Le funzioni HLSL sono simili alle funzioni C in diversi modi: entrambe contengono una definizione e un corpo di funzione ed entrambi dichiarano tipi restituiti ed elenchi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="ea1e8-296">Analogamente alle funzioni C, la convalida HLSL esegue il controllo dei tipi per gli argomenti, i tipi di argomento e il valore restituito durante la compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="ea1e8-297">A differenza delle funzioni C, le funzioni del punto di ingresso HLSL usano la semantica per associare gli argomenti della funzione agli input e agli output dello shader (le funzioni HLSL chiamate internamente ignorano la semantica).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="ea1e8-298">In questo modo è più semplice associare i dati del buffer a uno shader e associare gli output dello shader agli input dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="ea1e8-299">Una funzione contiene una dichiarazione e un corpo e la dichiarazione deve precedere il corpo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="ea1e8-300">La dichiarazione di funzione include tutti gli elementi prima delle parentesi graffe:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="ea1e8-301">Una dichiarazione di funzione contiene:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-301">A function declaration contains:</span></span>

-   <span data-ttu-id="ea1e8-302">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="ea1e8-302">A return type</span></span>
-   <span data-ttu-id="ea1e8-303">Nome di una funzione</span><span class="sxs-lookup"><span data-stu-id="ea1e8-303">A function name</span></span>
-   <span data-ttu-id="ea1e8-304">Elenco di argomenti (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-304">An argument list (optional)</span></span>
-   <span data-ttu-id="ea1e8-305">Semantica di output (facoltativa)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="ea1e8-306">Annotazione (facoltativa)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-306">An annotation (optional)</span></span>

<span data-ttu-id="ea1e8-307">Il tipo restituito può essere uno qualsiasi dei tipi di dati di base HLSL, ad esempio float4:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="ea1e8-308">Il tipo restituito può essere una struttura già definita:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="ea1e8-309">Se la funzione non restituisce un valore, è possibile usare void come tipo restituito.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="ea1e8-310">Il tipo restituito viene sempre visualizzato per primo in una dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="ea1e8-311">Un elenco di argomenti dichiara gli argomenti di input per una funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="ea1e8-312">Può anche dichiarare i valori che verranno restituiti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="ea1e8-313">Alcuni argomenti sono sia argomenti di input che di output.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="ea1e8-314">Di seguito è riportato un esempio di shader che accetta quattro argomenti di input.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="ea1e8-315">Questa funzione restituisce un colore finale, che è una combinazione di un campione di trama e del colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="ea1e8-316">La funzione accetta quattro input.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-316">The function takes four inputs.</span></span> <span data-ttu-id="ea1e8-317">Due input hanno semantica: LightDir ha la semantica [TEXCOORD1](dx-graphics-hlsl-semantics.md) e texcrd ha la [semantica TEXCOORD0.](dx-graphics-hlsl-semantics.md)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="ea1e8-318">La semantica indica che i dati per queste variabili provengono dal vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="ea1e8-319">Anche se la variabile LightDir ha una semantica [TEXCOORD1,](dx-graphics-hlsl-semantics.md) è probabile che il parametro non sia una coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="ea1e8-320">Il tipo semantico TEXCOORDn viene spesso usato per fornire una semantica per un tipo non predefinito (non esiste una semantica di input vertex shader per una direzione di luce).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="ea1e8-321">Gli altri due input LightColor e samp sono etichettati con la [parola chiave uniform.](dx-graphics-hlsl-appendix.md)</span><span class="sxs-lookup"><span data-stu-id="ea1e8-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="ea1e8-322">Si tratta di costanti uniformi che non cambieranno tra le chiamate di disegno.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="ea1e8-323">I valori per questi parametri provengono da variabili globali dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="ea1e8-324">Gli argomenti possono essere etichettati come input con la parola chiave in e gli argomenti di output con la parola chiave out.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="ea1e8-325">Gli argomenti non possono essere passati per riferimento. Tuttavia, un argomento può essere sia un input che un output se viene dichiarato con la parola chiave inout.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="ea1e8-326">Gli argomenti passati a una funzione contrassegnati con la parola chiave inout vengono considerati copie dell'originale fino a quando la funzione non viene restituita e vengono copiati nuovamente.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="ea1e8-327">Di seguito è riportato un esempio di uso di inout:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="ea1e8-328">Questa funzione incrementa i valori in A e B e li restituisce.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="ea1e8-329">Il corpo della funzione è tutto il codice dopo la dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="ea1e8-330">Il corpo è costituito da istruzioni racchiuse tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="ea1e8-331">Il corpo della funzione implementa tutte le funzionalità usando variabili, valori letterali, espressioni e istruzioni.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="ea1e8-332">Il corpo dello shader esegue due operazioni: esegue una moltiplicazione di matrice e restituisce un risultato float4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="ea1e8-333">La moltiplicazione della matrice viene eseguita con la [**funzione mul (DirectX HLSL),**](dx-graphics-hlsl-mul.md) che esegue una moltiplicazione di matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="ea1e8-334">**mul (DirectX HLSL)** è detto funzione intrinseca perché è già incorporata nella libreria di funzioni HLSL.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="ea1e8-335">Le funzioni intrinseche verranno trattate in modo più dettagliato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="ea1e8-336">La moltiplicazione matrice combina un vettore di input Pos e una matrice composita WorldViewProj.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="ea1e8-337">Il risultato è la posizione dei dati trasformati nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="ea1e8-338">Si tratta dell'elaborazione minima di vertex shader che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="ea1e8-339">Se si usa la pipeline di funzioni fisse invece di un vertex shader, è possibile disegnare i dati dei vertici dopo aver effettuato questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="ea1e8-340">L'ultima istruzione nel corpo di una funzione è un'istruzione return.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="ea1e8-341">Analogamente a C, questa istruzione restituisce il controllo dalla funzione all'istruzione che ha chiamato la funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="ea1e8-342">I tipi restituiti di funzione possono essere qualsiasi tipo di dati semplice definito in HLSL, inclusi bool, int half, float e double.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="ea1e8-343">I tipi restituiti possono essere uno dei tipi di dati complessi, ad esempio vettori e matrici.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="ea1e8-344">I tipi HLSL che fanno riferimento a oggetti non possono essere usati come tipi restituiti.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="ea1e8-345">Sono inclusi pixelshader, vertexshader, texture e sampler.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="ea1e8-346">Di seguito è riportato un esempio di funzione che usa una struttura per un tipo restituito.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="ea1e8-347">Il tipo restituito float4 è stato sostituito con la struttura VS \_ OUTPUT, che ora contiene un singolo membro float4.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="ea1e8-348">Un'istruzione return segnala la fine di una funzione.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="ea1e8-349">Si tratta dell'istruzione return più semplice.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-349">This is the simplest return statement.</span></span> <span data-ttu-id="ea1e8-350">Restituisce il controllo dalla funzione al programma chiamante.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="ea1e8-351">Non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="ea1e8-352">Un'istruzione return può restituire uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-352">A return statement can return one or more values.</span></span> <span data-ttu-id="ea1e8-353">In questo esempio viene restituito un valore letterale:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="ea1e8-354">In questo esempio viene restituito il risultato scalare di un'espressione:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled;
```



<span data-ttu-id="ea1e8-355">Questo esempio restituisce un valore float4 costruito da una variabile locale e un valore letterale:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="ea1e8-356">Questo esempio restituisce un valore float4 costruito dal risultato restituito da una funzione intrinseca e alcuni valori letterali:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="ea1e8-357">Questo esempio restituisce una struttura che contiene uno o più membri:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="ea1e8-358">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="ea1e8-358">Flow Control</span></span>

<span data-ttu-id="ea1e8-359">La maggior parte dei vertici e pixel shader hardware è progettata per eseguire uno shader riga per riga, eseguendo ogni istruzione una sola volta.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="ea1e8-360">HLSL supporta il controllo di flusso, che include la diramazione statica, le istruzioni predicate, il ciclo statico, la diramazione dinamica e il ciclo dinamico.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="ea1e8-361">In precedenza, l'uso di un'istruzione if generava codice shader in linguaggio assembly che implementava sia il lato if che il lato else del flusso di codice.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="ea1e8-362">Di seguito è riportato un esempio di nel codice HLSL compilato per vs \_ 1 \_ 1:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="ea1e8-363">Di seguito è riportato il codice assembly risultante:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="ea1e8-364">Alcuni componenti hardware consentono il ciclo statico o dinamico, ma la maggior parte richiede l'esecuzione lineare.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="ea1e8-365">Nei modelli che non supportano il ciclo, è necessario annullare la registrazione di tutti i cicli.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="ea1e8-366">Un esempio è [l'esempio DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) che usa cicli non srotodati anche per shader ps \_ \_ 1 1.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="ea1e8-367">HLSL include ora il supporto per ognuno di questi tipi di controllo di flusso:</span><span class="sxs-lookup"><span data-stu-id="ea1e8-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="ea1e8-368">diramazione statica</span><span class="sxs-lookup"><span data-stu-id="ea1e8-368">static branching</span></span>
-   <span data-ttu-id="ea1e8-369">istruzioni predicate</span><span class="sxs-lookup"><span data-stu-id="ea1e8-369">predicated instructions</span></span>
-   <span data-ttu-id="ea1e8-370">ciclo statico</span><span class="sxs-lookup"><span data-stu-id="ea1e8-370">static looping</span></span>
-   <span data-ttu-id="ea1e8-371">diramazione dinamica</span><span class="sxs-lookup"><span data-stu-id="ea1e8-371">dynamic branching</span></span>
-   <span data-ttu-id="ea1e8-372">ciclo dinamico</span><span class="sxs-lookup"><span data-stu-id="ea1e8-372">dynamic looping</span></span>

<span data-ttu-id="ea1e8-373">La diramazione statica consente di attivare o disattivare i blocchi di codice shader in base a una costante shader booleana.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="ea1e8-374">Si tratta di un metodo pratico per abilitare o disabilitare i percorsi del codice in base al tipo di oggetto di cui è in corso il rendering.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="ea1e8-375">Tra le chiamate di disegno, è possibile decidere quali funzionalità si vuole supportare con lo shader corrente e quindi impostare i flag booleani necessari per ottenere tale comportamento.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="ea1e8-376">Tutte le istruzioni disabilitate da una costante booleana vengono ignorate durante l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="ea1e8-377">Il supporto di diramazione più familiare è la diramazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="ea1e8-378">Con la diramazione dinamica, la condizione di confronto si trova in una variabile, il che significa che il confronto viene eseguito per ogni vertice o ogni pixel in fase di esecuzione (a differenza del confronto che si verifica in fase di compilazione o tra due chiamate di disegno).</span><span class="sxs-lookup"><span data-stu-id="ea1e8-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="ea1e8-379">L'effetto sulle prestazioni è il costo del ramo più il costo delle istruzioni sul lato del ramo assunto.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="ea1e8-380">La diramazione dinamica viene implementata nel modello shader 3 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="ea1e8-381">L'ottimizzazione degli shader che funzionano con questi modelli è simile all'ottimizzazione del codice eseguito in una CPU.</span><span class="sxs-lookup"><span data-stu-id="ea1e8-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea1e8-382">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea1e8-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea1e8-383">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="ea1e8-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
