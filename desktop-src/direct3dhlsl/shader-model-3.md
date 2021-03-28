---
title: Shader Model 3 (riferimento HLSL)
description: I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399208"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="30c29-103">Shader Model 3 (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="30c29-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="30c29-104">I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="30c29-105">Se si stanno implementando shader in hardware, non è possibile usare vs \_ 3 \_ 0 o PS \_ 3 \_ 0 con altre versioni di shader e non è possibile usare uno shader con la pipeline della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="30c29-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="30c29-106">Queste modifiche consentono di semplificare i driver e il Runtime.</span><span class="sxs-lookup"><span data-stu-id="30c29-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="30c29-107">L'unica eccezione è che gli shader solo software e \_ 3 \_ 0 possono essere utilizzati con qualsiasi versione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="30c29-108">Inoltre, se si utilizza uno shader solo software e \_ 3 \_ 0 con una versione precedente di pixel shader, il vertex shader può utilizzare solo la semantica di output compatibile con i codici FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="30c29-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="30c29-109">La semantica utilizzata per gli output di vertex shader deve essere utilizzata su input pixel shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="30c29-110">La semantica viene usata per eseguire il mapping degli output del vertex shader agli input pixel shader, in modo analogo al modo in cui viene eseguito il mapping della dichiarazione del vertice ai registri di input del vertex shader e ai modelli shader precedenti.</span><span class="sxs-lookup"><span data-stu-id="30c29-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="30c29-111">Vedere semantica di corrispondenza sugli shader vs 3,0 e PS 3,0.</span><span class="sxs-lookup"><span data-stu-id="30c29-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="30c29-112">Sono stati aggiunti stati di rendering della modalità a capo aggiuntivo per coprire la possibilità di ulteriori coordinate di trama in questo nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="30c29-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="30c29-113">Gli attributi con D3DDECLUSAGE \_ TEXCOORD e l'indice di utilizzo da 0 a 15 vengono interpolati in modalità a capo quando viene impostato il [**ritorno a \_ capo \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="30c29-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="30c29-114">Funzionalità di Vertex Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="30c29-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="30c29-115">Funzionalità del pixel shader modello 3</span><span class="sxs-lookup"><span data-stu-id="30c29-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="30c29-116">Semantica di corrispondenza in Visual Studio \_ 3 \_ 0 e PS \_ 3 \_ 0 Shader</span><span class="sxs-lookup"><span data-stu-id="30c29-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="30c29-117">Modifiche della modalità nebbia, profondità e ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="30c29-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="30c29-118">Conversioni a virgola mobile e Integer</span><span class="sxs-lookup"><span data-stu-id="30c29-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="30c29-119">Specifica della precisione completa o parziale</span><span class="sxs-lookup"><span data-stu-id="30c29-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="30c29-120">Vertex e pixel shader software</span><span class="sxs-lookup"><span data-stu-id="30c29-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="30c29-121">Funzionalità di Vertex Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="30c29-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="30c29-122">I tipi di registro di output vertex shader sono stati compressi in dodici registri (vedere [log di output](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="30c29-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="30c29-123">Ogni registro utilizzato deve essere dichiarato utilizzando l'istruzione [DCL](dcl-usage---ps.md) e una semantica (ad esempio, DCL \_ Color0 o0. xyzw).</span><span class="sxs-lookup"><span data-stu-id="30c29-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="30c29-124">Il \_ modello di vertex shader 3 0 (vs \_ 3 \_ 0) si espande sulle funzionalità di vs \_ 2 \_ 0 con un'indicizzazione dei registri più potente, un set di registri di output semplificati, la possibilità di campionare una trama in un vertex shader e la possibilità di controllare la velocità con cui vengono inizializzati gli input dello shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="30c29-125">Indicizzare qualsiasi registro</span><span class="sxs-lookup"><span data-stu-id="30c29-125">Index Any Register</span></span>

<span data-ttu-id="30c29-126">Tutti i registri (registri di [input](dx9-graphics-reference-asm-vs-registers-input.md) e di [output](dx9-graphics-reference-asm-vs-registers-output.md)) possono essere indicizzati tramite il registro del [contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) . solo i registri costanti possono essere indicizzati nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="30c29-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="30c29-127">Prima di indicizzarle, è necessario dichiarare i registri di input e di output.</span><span class="sxs-lookup"><span data-stu-id="30c29-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="30c29-128">Tuttavia, non è possibile indicizzare alcun registro di output dichiarato con una semantica di posizione o dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="30c29-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="30c29-129">Infatti, se si usa l'indicizzazione, la semantica position e psize deve essere dichiarata rispettivamente nei registri o0 e O1.</span><span class="sxs-lookup"><span data-stu-id="30c29-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="30c29-130">È consentito solo indicizzare un intervallo continuo di registri; ovvero non è possibile indicizzare tra i registri che non sono stati dichiarati.</span><span class="sxs-lookup"><span data-stu-id="30c29-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="30c29-131">Sebbene questa restrizione possa risultare scomoda, consente di eseguire l'ottimizzazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="30c29-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="30c29-132">Il tentativo di eseguire l'indicizzazione tra registri non contigui produrrà risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="30c29-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="30c29-133">La convalida dello shader non impone questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="30c29-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="30c29-134">Semplificare i registri di output</span><span class="sxs-lookup"><span data-stu-id="30c29-134">Simplify Output Registers</span></span>

<span data-ttu-id="30c29-135">Tutti i vari tipi di registri di output sono stati compressi in dodici registri di output: 1 per posizione, 2 per colore, 8 per trama e 1 per nebbia o dimensione punto.</span><span class="sxs-lookup"><span data-stu-id="30c29-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="30c29-136">Questi registri eseguiranno l'interpolazione di tutti i dati che contengono per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="30c29-137">Le dichiarazioni di registro di output sono obbligatorie e la semantica viene assegnata a ogni registro.</span><span class="sxs-lookup"><span data-stu-id="30c29-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="30c29-138">I registri possono essere suddivisi come segue:</span><span class="sxs-lookup"><span data-stu-id="30c29-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="30c29-139">Almeno un registro deve essere dichiarato come una posizione a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="30c29-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="30c29-140">Si tratta dell'unico registro vertex shader obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="30c29-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="30c29-141">I primi dieci registri utilizzati da uno shader possono usare un massimo di quattro componenti (xyzw).</span><span class="sxs-lookup"><span data-stu-id="30c29-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="30c29-142">Il registro ultimo (o dodicesimo) può contenere solo un valore scalare, ad esempio la dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="30c29-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="30c29-143">Per un elenco dei registri, vedere [Registers-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="30c29-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="30c29-144">Esempio di trama in un vertex shader</span><span class="sxs-lookup"><span data-stu-id="30c29-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="30c29-145">Vertex Shader 3 \_ 0 supporta la ricerca di trame nel vertex shader usando [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="30c29-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="30c29-146">Funzionalità del pixel shader modello 3</span><span class="sxs-lookup"><span data-stu-id="30c29-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="30c29-147">I registri colori e trama pixel shader sono stati compressi in dieci registri di input (vedere [tipi di registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="30c29-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="30c29-148">Il registro visi è un registro scalare a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="30c29-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="30c29-149">Solo il segno di questo registro è valido.</span><span class="sxs-lookup"><span data-stu-id="30c29-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="30c29-150">Se il segno è negativo, la primitiva è una faccia posteriore.</span><span class="sxs-lookup"><span data-stu-id="30c29-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="30c29-151">Questa operazione può essere utilizzata all'interno di un pixel shader per ottenere l'illuminazione a due lati, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="30c29-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="30c29-152">Il registro di posizione fa riferimento ai pixel correnti (x, y).</span><span class="sxs-lookup"><span data-stu-id="30c29-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="30c29-153">I registri costanti dello shader possono essere impostati utilizzando:</span><span class="sxs-lookup"><span data-stu-id="30c29-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="30c29-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="30c29-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="30c29-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="30c29-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="30c29-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="30c29-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="30c29-157">Semantica di corrispondenza in Visual Studio \_ 3 \_ 0 e PS \_ 3 \_ 0 Shader</span><span class="sxs-lookup"><span data-stu-id="30c29-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="30c29-158">Esistono alcune restrizioni sull'utilizzo semantico con vs \_ 3 \_ 0 e PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30c29-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="30c29-159">In generale, è necessario prestare attenzione quando si usa una semantica per un input dello shader che corrisponde a una semantica usata in un output dello shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="30c29-160">Ad esempio, questo pixel shader comprime più nomi in un unico registro:</span><span class="sxs-lookup"><span data-stu-id="30c29-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="30c29-161">Ogni registro presenta una semantica diversa.</span><span class="sxs-lookup"><span data-stu-id="30c29-161">Each register has a different semantic.</span></span> <span data-ttu-id="30c29-162">Si noti che è anche possibile denominare V0. x e V0. YZ con una semantica diversa (multipla) a causa dell'uso della maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="30c29-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="30c29-163">Data la pixel shader, \_ non è possibile associare il seguente shader a Visual Studio 3 \_ 0:</span><span class="sxs-lookup"><span data-stu-id="30c29-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="30c29-164">Questi due shader sono in conflitto con l'uso della semantica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1** .</span><span class="sxs-lookup"><span data-stu-id="30c29-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="30c29-165">Riscrivere il vertex shader come questo per evitare la collisione semantica:</span><span class="sxs-lookup"><span data-stu-id="30c29-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="30c29-166">Analogamente, non è possibile usare un nome semantico dichiarato in registri di input diversi nel pixel shader (V0 e V1 nel pixel shader) in un unico registro di output in questo vertex shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="30c29-167">Questo vertex shader, ad esempio, non può essere associato al pixel shader perché D3DDECLUSAGE \_ TEXCOORD1 viene usato per i registri di input pixel shader (V0, V1) e il registro di output di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="30c29-168">D'altra parte, questo vertex shader non può essere associato al pixel shader perché la maschera di output per un parametro con una semantica specificata non fornisce i dati richiesti dall'pixel shader:</span><span class="sxs-lookup"><span data-stu-id="30c29-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="30c29-169">Questo vertex shader non fornisce un output con uno dei nomi semantici richiesti dall'pixel shader, quindi l'associazione dello shader non è valida:</span><span class="sxs-lookup"><span data-stu-id="30c29-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="30c29-170">Modifiche della modalità nebbia, profondità e ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="30c29-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="30c29-171">Quando D3DRS \_ MODOOMBRA è impostato per l'ombreggiatura flat durante la rasterizzazione e la rasterizzazione dei triangolari, gli attributi con \_ colore D3DDECLUSAGE vengono interpolati come ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="30c29-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="30c29-172">Se uno o più componenti di un registro sono dichiarati con una semantica di colore, ma a altri componenti dello stesso registro viene assegnata una semantica diversa, l'interpolazione dell'ombreggiatura piatta (lineare rispetto a quella Flat) non sarà definita nei componenti di tale registro senza una semantica di colore.</span><span class="sxs-lookup"><span data-stu-id="30c29-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="30c29-173">Se si desidera il rendering di nebbia, gli \_ shader vs 3 \_ 0 e PS \_ 3 \_ 0 devono implementare la nebbia.</span><span class="sxs-lookup"><span data-stu-id="30c29-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="30c29-174">Nessun calcolo di nebbia viene eseguito all'esterno degli shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="30c29-175">Non esiste alcun registro di nebbia in vs \_ 3 \_ 0 e la semantica aggiuntiva D3DDECLUSAGE \_ Fog (per il fattore di Blend di nebbia calcolato per vertice) e \_ la profondità D3DDECLUSAGE (per passare un valore di profondità al pixel shader per calcolare il fattore di Blend di nebbia) sono state aggiunte.</span><span class="sxs-lookup"><span data-stu-id="30c29-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="30c29-176">Lo stato della fase trama D3DTSS \_ TEXCOORDINDEX viene ignorato quando si usa pixel shader 3,0.</span><span class="sxs-lookup"><span data-stu-id="30c29-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="30c29-177">Per soddisfare queste modifiche sono stati aggiunti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="30c29-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="30c29-178">Conversioni a virgola mobile e Integer</span><span class="sxs-lookup"><span data-stu-id="30c29-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="30c29-179">La matematica a virgola mobile si verifica con precisione e intervalli diversi (a 16 bit, a 24 bit e a 32 bit) in parti diverse della pipeline.</span><span class="sxs-lookup"><span data-stu-id="30c29-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="30c29-180">Un valore maggiore dell'intervallo dinamico della pipeline che immette la pipeline (ad esempio, una mappa di trama float a 32 bit viene campionata in una pipeline float a 24 bit in PS \_ 2 \_ 0) crea un risultato non definito.</span><span class="sxs-lookup"><span data-stu-id="30c29-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="30c29-181">Per un comportamento prevedibile, è necessario bloccare tale valore all'intervallo dinamico massimo.</span><span class="sxs-lookup"><span data-stu-id="30c29-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="30c29-182">La conversione da un valore a virgola mobile a un numero intero si verifica in diversi punti, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="30c29-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="30c29-183">Quando si incontra un'istruzione [mova-vs](mova---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="30c29-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="30c29-184">Durante l'indirizzamento della trama.</span><span class="sxs-lookup"><span data-stu-id="30c29-184">During texture addressing.</span></span>
-   <span data-ttu-id="30c29-185">Quando si scrive in una destinazione di rendering non a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="30c29-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="30c29-186">Specifica della precisione completa o parziale</span><span class="sxs-lookup"><span data-stu-id="30c29-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="30c29-187">PS \_ 3 \_ 0 e PS \_ 2 \_ x offrono supporto per due livelli di precisione:</span><span class="sxs-lookup"><span data-stu-id="30c29-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="30c29-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30c29-188">ps\_3\_0</span></span> | <span data-ttu-id="30c29-189">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30c29-189">ps\_2\_0</span></span> | <span data-ttu-id="30c29-190">Precision</span><span class="sxs-lookup"><span data-stu-id="30c29-190">Precision</span></span>         | <span data-ttu-id="30c29-191">Valore</span><span class="sxs-lookup"><span data-stu-id="30c29-191">Value</span></span>                |
| <span data-ttu-id="30c29-192">x</span><span class="sxs-lookup"><span data-stu-id="30c29-192">x</span></span>        |          | <span data-ttu-id="30c29-193">Full</span><span class="sxs-lookup"><span data-stu-id="30c29-193">Full</span></span>              | <span data-ttu-id="30c29-194">FP32 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="30c29-194">fp32 or higher</span></span>       |
| <span data-ttu-id="30c29-195">x</span><span class="sxs-lookup"><span data-stu-id="30c29-195">x</span></span>        |          | <span data-ttu-id="30c29-196">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="30c29-196">Partial precision</span></span> | <span data-ttu-id="30c29-197">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="30c29-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="30c29-198">x</span><span class="sxs-lookup"><span data-stu-id="30c29-198">x</span></span>        | <span data-ttu-id="30c29-199">x</span><span class="sxs-lookup"><span data-stu-id="30c29-199">x</span></span>        | <span data-ttu-id="30c29-200">Full</span><span class="sxs-lookup"><span data-stu-id="30c29-200">Full</span></span>              | <span data-ttu-id="30c29-201">fp24 = s16e7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="30c29-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="30c29-202">x</span><span class="sxs-lookup"><span data-stu-id="30c29-202">x</span></span>        | <span data-ttu-id="30c29-203">x</span><span class="sxs-lookup"><span data-stu-id="30c29-203">x</span></span>        | <span data-ttu-id="30c29-204">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="30c29-204">Partial precision</span></span> | <span data-ttu-id="30c29-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="30c29-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="30c29-206">PS \_ 3 \_ 0 supporta una precisione maggiore di quella di PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30c29-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="30c29-207">Per impostazione predefinita, tutte le operazioni si verificano a livello di precisione totale.</span><span class="sxs-lookup"><span data-stu-id="30c29-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="30c29-208">La precisione parziale (vedere [modificatori del registro pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)) viene richiesta aggiungendo il \_ modificatore PP al codice dello shader (purché l'implementazione sottostante la supporti).</span><span class="sxs-lookup"><span data-stu-id="30c29-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="30c29-209">Le implementazioni sono sempre libere di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="30c29-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="30c29-210">Il \_ modificatore di PP può essere eseguito in due contesti:</span><span class="sxs-lookup"><span data-stu-id="30c29-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="30c29-211">In una dichiarazione di coordinata di trama per passare le coordinate di trama a precisione parziale al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="30c29-212">Questo può essere usato quando le coordinate di trama inoltrano i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.</span><span class="sxs-lookup"><span data-stu-id="30c29-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="30c29-213">Su qualsiasi istruzione per richiedere l'uso della precisione parziale, incluse le istruzioni per il caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="30c29-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="30c29-214">Ciò indica che l'implementazione è autorizzata a eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="30c29-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="30c29-215">In assenza di un modificatore esplicito, l'istruzione deve essere eseguita a precisione completa (indipendentemente dalla precisione degli operandi di input).</span><span class="sxs-lookup"><span data-stu-id="30c29-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="30c29-216">Un'applicazione può scegliere intenzionalmente di comportare la precisione per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="30c29-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="30c29-217">Esistono diversi tipi di dati di input dello shader che sono candidati naturali per l'elaborazione della precisione parziale:</span><span class="sxs-lookup"><span data-stu-id="30c29-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="30c29-218">Gli iteratori di colore sono rappresentati correttamente da valori con precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="30c29-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="30c29-219">I valori di trama dalla maggior parte dei formati possono essere rappresentati in modo accurato da valori a precisione parziale (i valori campionati da trame 32 in formato a virgola mobile sono un'eccezione ovvia).</span><span class="sxs-lookup"><span data-stu-id="30c29-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="30c29-220">Le costanti possono essere rappresentate dalla rappresentazione a precisione parziale, in base alle esigenze dello shader.</span><span class="sxs-lookup"><span data-stu-id="30c29-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="30c29-221">In tutti questi casi lo sviluppatore può scegliere di specificare la precisione parziale per elaborare i dati, sapendo che non viene persa la precisione dei dati di input.</span><span class="sxs-lookup"><span data-stu-id="30c29-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="30c29-222">In alcuni casi, è possibile che uno shader richieda che i passaggi interni di un calcolo vengano eseguiti con la massima precisione anche quando i valori di input e di output finale non hanno una precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="30c29-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="30c29-223">Vertex e pixel shader software</span><span class="sxs-lookup"><span data-stu-id="30c29-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="30c29-224">Le implementazioni del software (Runtime e riferimento per vertex shader e informazioni di riferimento per i pixel shader) della versione 2 \_ 0 Shader e versioni successive presentano una convalida attenuata.</span><span class="sxs-lookup"><span data-stu-id="30c29-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="30c29-225">Questa operazione è utile a scopo di debug e creazione di prototipi.</span><span class="sxs-lookup"><span data-stu-id="30c29-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="30c29-226">L'applicazione indica al runtime/assembler che necessita di una convalida attenuata usando il \_ flag SW nell'assembler (ad esempio, vs \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="30c29-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="30c29-227">Uno shader software non funzionerà con l'hardware.</span><span class="sxs-lookup"><span data-stu-id="30c29-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="30c29-228">vs \_ 2 \_ SW è un relax fino al limite massimo di vs \_ 2 \_ x; Analogamente, PS \_ 2 \_ SW è un rilassamento per i limiti massimi di PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="30c29-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="30c29-229">In particolare, le convalide seguenti sono rilassate:</span><span class="sxs-lookup"><span data-stu-id="30c29-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c29-230">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="30c29-230">Shader Model</span></span>                               | <span data-ttu-id="30c29-231">Risorsa</span><span class="sxs-lookup"><span data-stu-id="30c29-231">Resource</span></span>                             | <span data-ttu-id="30c29-232">Limite</span><span class="sxs-lookup"><span data-stu-id="30c29-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="30c29-233">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-234">Conteggi istruzioni</span><span class="sxs-lookup"><span data-stu-id="30c29-234">Instruction Counts</span></span>                   | <span data-ttu-id="30c29-235">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="30c29-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="30c29-236">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-237">Registri costanti float</span><span class="sxs-lookup"><span data-stu-id="30c29-237">Float Constant Registers</span></span>             | <span data-ttu-id="30c29-238">8192</span><span class="sxs-lookup"><span data-stu-id="30c29-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="30c29-239">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-240">Registri costanti Integer</span><span class="sxs-lookup"><span data-stu-id="30c29-240">Integer Constant Registers</span></span>           | <span data-ttu-id="30c29-241">2048</span><span class="sxs-lookup"><span data-stu-id="30c29-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="30c29-242">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-243">Registri costanti booleani</span><span class="sxs-lookup"><span data-stu-id="30c29-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="30c29-244">2048</span><span class="sxs-lookup"><span data-stu-id="30c29-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="30c29-245">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="30c29-246">Profondità lettura dipendente</span><span class="sxs-lookup"><span data-stu-id="30c29-246">Dependent-read depth</span></span>                 | <span data-ttu-id="30c29-247">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="30c29-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="30c29-248">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="30c29-249">istruzioni ed etichette per il controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="30c29-249">flow control instructions and labels</span></span> | <span data-ttu-id="30c29-250">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="30c29-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="30c29-251">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-252">Inizio/passaggio/conteggi ciclo</span><span class="sxs-lookup"><span data-stu-id="30c29-252">Loop start/step/counts</span></span>               | <span data-ttu-id="30c29-253">Le dimensioni del passaggio di iterazione e inizio iterazione per le istruzioni Rep e loop sono interi con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="30c29-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="30c29-254">Il numero può essere massimo di \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="30c29-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="30c29-255">vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="30c29-256">Limiti della porta</span><span class="sxs-lookup"><span data-stu-id="30c29-256">Port limits</span></span>                          | <span data-ttu-id="30c29-257">I limiti della porta per tutti i file di registro sono rilassati.</span><span class="sxs-lookup"><span data-stu-id="30c29-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="30c29-258">Visual Studio \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="30c29-259">Numero di interpolatori</span><span class="sxs-lookup"><span data-stu-id="30c29-259">Number of interpolators</span></span>              | <span data-ttu-id="30c29-260">16 registri di output in vs \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="30c29-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="30c29-261">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30c29-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="30c29-262">Numero di interpolatori</span><span class="sxs-lookup"><span data-stu-id="30c29-262">Number of interpolators</span></span>              | <span data-ttu-id="30c29-263">14 (16-2) registri di input per PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="30c29-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="30c29-264">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30c29-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c29-265">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30c29-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 