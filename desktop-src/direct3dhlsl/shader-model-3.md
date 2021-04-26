---
title: Modello shader 3 (informazioni di riferimento su HLSL)
description: I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c277723628d5337e41e5fbf83baa9fda8af16adf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993868"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="2453b-103">Modello shader 3 (informazioni di riferimento su HLSL)</span><span class="sxs-lookup"><span data-stu-id="2453b-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="2453b-104">I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="2453b-105">Se si implementano shader nell'hardware, non è possibile usare vs \_ 3 0 o \_ ps \_ 3 0 con altre versioni dello shader e non è possibile usare alcun tipo di shader con la pipeline di funzioni \_ fisse.</span><span class="sxs-lookup"><span data-stu-id="2453b-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="2453b-106">Queste modifiche consentono di semplificare i driver e il runtime.</span><span class="sxs-lookup"><span data-stu-id="2453b-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="2453b-107">L'unica eccezione è che gli shader solo software e 3 0 possono essere usati con qualsiasi \_ \_ pixel shader versione.</span><span class="sxs-lookup"><span data-stu-id="2453b-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="2453b-108">Inoltre, se si usa uno shader solo software rispetto a 3 0 con una versione precedente di pixel shader, il vertex shader può usare solo la semantica di output compatibile con i codici \_ \_ FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="2453b-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="2453b-109">La semantica usata per gli output di vertex shader deve essere usata pixel shader input.</span><span class="sxs-lookup"><span data-stu-id="2453b-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="2453b-110">La semantica viene usata per eseguire il mapping degli output del vertex shader agli input pixel shader, analogamente al modo in cui viene eseguito il mapping della dichiarazione dei vertici ai registri di input del vertex shader e ai modelli shader precedenti.</span><span class="sxs-lookup"><span data-stu-id="2453b-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="2453b-111">Vedere Match Semantics on vs 3.0 and ps 3.0 Shaders (Semantica di corrispondenza in vs 3.0 e ps 3.0 Shader).</span><span class="sxs-lookup"><span data-stu-id="2453b-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="2453b-112">Sono stati aggiunti altri stati di rendering della modalità di ritorno a capo per coprire la possibilità di coordinate di trama aggiuntive in questo nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="2453b-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="2453b-113">Gli attributi con D3DDECLUSAGE TEXCOORD e l'indice di utilizzo da 0 a 15 vengono interpolati in modalità di ritorno a capo quando viene impostato il corrispondente \_ [**\_ WRAP \* D3DRS.**](/windows/desktop/direct3d9/d3drenderstatetype)</span><span class="sxs-lookup"><span data-stu-id="2453b-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="2453b-114">Funzionalità di Vertex Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="2453b-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="2453b-115">Funzionalità di Pixel Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="2453b-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="2453b-116">Semantica di corrispondenza per gli \_ shader 3 \_ 0 e ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2453b-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="2453b-117">Modifiche alla modalità nebbia, profondità e ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="2453b-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="2453b-118">Conversioni a virgola mobile e interi</span><span class="sxs-lookup"><span data-stu-id="2453b-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="2453b-119">Specifica della precisione completa o parziale</span><span class="sxs-lookup"><span data-stu-id="2453b-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="2453b-120">Vertici software e pixel shader</span><span class="sxs-lookup"><span data-stu-id="2453b-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="2453b-121">Funzionalità del modello vertex shader 3</span><span class="sxs-lookup"><span data-stu-id="2453b-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="2453b-122">I tipi di registro di output del vertex shader sono stati compressi in dodici registri (vedere [Registri di output).](dx9-graphics-reference-asm-vs-registers-output.md)</span><span class="sxs-lookup"><span data-stu-id="2453b-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="2453b-123">Ogni registro usato deve essere dichiarato usando l'istruzione [dcl](dcl-usage---ps.md) e una semantica ,ad esempio dcl \_ color0 o0.xyzw.</span><span class="sxs-lookup"><span data-stu-id="2453b-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="2453b-124">Il modello di vertex shader a \_ 3 0 (vs 3 0) si espande sulle funzionalità di vs 2 0 con un'indicizzazione dei registri più potente, un set di registri di output semplificati, la possibilità di campionare una trama in un vertex shader e la possibilità di controllare la frequenza con cui vengono inizializzati \_ \_ gli input dello \_ \_ shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="2453b-125">Indicizzare qualsiasi registro</span><span class="sxs-lookup"><span data-stu-id="2453b-125">Index Any Register</span></span>

<span data-ttu-id="2453b-126">Tutti i registri ( [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md) e Registri di [output](dx9-graphics-reference-asm-vs-registers-output.md)) possono essere indicizzati usando loop [counter register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo i registri costanti possono essere indicizzati nelle versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="2453b-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="2453b-127">È necessario dichiarare i registri di input e output prima di indicizzarli.</span><span class="sxs-lookup"><span data-stu-id="2453b-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="2453b-128">Tuttavia, non è possibile indicizzare alcun registro di output dichiarato con una semantica di posizione o dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="2453b-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="2453b-129">In realtà, se si usa l'indicizzazione, la semantica di posizione e psize deve essere dichiarata rispettivamente nei registri o0 e o1.</span><span class="sxs-lookup"><span data-stu-id="2453b-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="2453b-130">È consentito indicizzare solo un intervallo continuo di registri. ciò significa che non è possibile indicizzare i registri che non sono stati dichiarati.</span><span class="sxs-lookup"><span data-stu-id="2453b-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="2453b-131">Anche se questa restrizione può essere poco pratico, consente l'ottimizzazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2453b-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="2453b-132">Il tentativo di indicizzare i registri non contigui produrrà risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="2453b-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="2453b-133">La convalida dello shader non applica questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="2453b-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="2453b-134">Semplificare i registri di output</span><span class="sxs-lookup"><span data-stu-id="2453b-134">Simplify Output Registers</span></span>

<span data-ttu-id="2453b-135">Tutti i vari tipi di registri di output sono stati compressi in dodici registri di output: 1 per la posizione, 2 per il colore, 8 per la trama e 1 per le dimensioni del punto o del punto.</span><span class="sxs-lookup"><span data-stu-id="2453b-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="2453b-136">Questi registri interpoleranno tutti i dati che contengono per il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="2453b-137">Le dichiarazioni dei registri di output sono obbligatorie e la semantica viene assegnata a ogni registro.</span><span class="sxs-lookup"><span data-stu-id="2453b-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="2453b-138">I registri possono essere suddivisi come segue:</span><span class="sxs-lookup"><span data-stu-id="2453b-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="2453b-139">Almeno un registro deve essere dichiarato come registro di posizione a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="2453b-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="2453b-140">Questo è l'unico registro vertex shader necessario.</span><span class="sxs-lookup"><span data-stu-id="2453b-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="2453b-141">I primi dieci registri utilizzati da uno shader possono usare un massimo di quattro componenti (xyzw).</span><span class="sxs-lookup"><span data-stu-id="2453b-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="2453b-142">L'ultimo registro (o dodicesimo) può contenere solo un valore scalare (ad esempio dimensioni in punti).</span><span class="sxs-lookup"><span data-stu-id="2453b-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="2453b-143">Per un elenco dei registri, vedere [Registri - vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="2453b-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="2453b-144">Esempio di trama in un vertex shader</span><span class="sxs-lookup"><span data-stu-id="2453b-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="2453b-145">Vertex shader 3 0 supporta la ricerca di trame nel \_ vertex shader [usando texldl - rispetto a](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="2453b-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="2453b-146">Funzionalità di Pixel Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="2453b-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="2453b-147">I pixel shader colori e trame sono stati compressi in dieci registri di input (vedere [Tipi di registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="2453b-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="2453b-148">Il registro viso è un registro scalare a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2453b-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="2453b-149">Solo il segno di questo registro è valido.</span><span class="sxs-lookup"><span data-stu-id="2453b-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="2453b-150">Se il segno è negativo, la primitiva è un viso posteriore.</span><span class="sxs-lookup"><span data-stu-id="2453b-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="2453b-151">Può essere usato all'interno di un pixel shader per ottenere l'illuminazione a due lati, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="2453b-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="2453b-152">Il Registro posizioni fa riferimento ai pixel correnti (x,y).</span><span class="sxs-lookup"><span data-stu-id="2453b-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="2453b-153">I registri delle costanti shader possono essere impostati usando:</span><span class="sxs-lookup"><span data-stu-id="2453b-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="2453b-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="2453b-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="2453b-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="2453b-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="2453b-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="2453b-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="2453b-157">Semantica di corrispondenza per gli \_ shader 3 \_ 0 e ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2453b-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="2453b-158">Esistono alcune restrizioni sull'utilizzo semantico rispetto a \_ 3 \_ 0 e ps \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="2453b-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="2453b-159">In generale, è necessario prestare attenzione quando si usa una semantica per un input shader che corrisponde a una semantica usata in un output dello shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="2453b-160">Ad esempio, questo pixel shader più nomi in un unico registro:</span><span class="sxs-lookup"><span data-stu-id="2453b-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="2453b-161">Ogni registro ha una semantica diversa.</span><span class="sxs-lookup"><span data-stu-id="2453b-161">Each register has a different semantic.</span></span> <span data-ttu-id="2453b-162">Si noti che è anche possibile assegnare ai nomi v0.x e v0.yz una semantica diversa (multipla) a causa dell'uso della maschera di scrittura.</span><span class="sxs-lookup"><span data-stu-id="2453b-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="2453b-163">Dato il pixel shader, lo shader 3 0 seguente non \_ può essere associato ad \_ esso:</span><span class="sxs-lookup"><span data-stu-id="2453b-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="2453b-164">Questi due shader sono in conflitto con l'uso della semantica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1.**</span><span class="sxs-lookup"><span data-stu-id="2453b-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="2453b-165">Riscrivere il vertex shader in questo modo per evitare la collisione semantica:</span><span class="sxs-lookup"><span data-stu-id="2453b-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="2453b-166">Analogamente, un nome semantico dichiarato in registri di input diversi nel pixel shader (v0 e v1 nel pixel shader) non può essere usato in un singolo registro di output in questo vertex shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="2453b-167">Ad esempio, questo vertex shader non può essere associato al pixel shader perché D3DDECLUSAGE TEXCOORD1 viene usato sia per i registri di input pixel shader (v0, v1) che per il registro di output del \_ vertex shader o3.</span><span class="sxs-lookup"><span data-stu-id="2453b-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="2453b-168">D'altra parte, questo vertex shader non può essere associato al pixel shader perché la maschera di output per un parametro con una determinata semantica non fornisce i dati richiesti dal pixel shader:</span><span class="sxs-lookup"><span data-stu-id="2453b-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="2453b-169">Questo vertex shader non fornisce un output con uno dei nomi semantici richiesti dal pixel shader, quindi l'associazione di shader non è valida:</span><span class="sxs-lookup"><span data-stu-id="2453b-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


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



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="2453b-170">Modifiche alla modalità di ombreggiatura, profondità e profondità</span><span class="sxs-lookup"><span data-stu-id="2453b-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="2453b-171">Quando L'opzione D3DRS SHADEMODE è impostata per l'ombreggiatura piana durante la rasterizzazione del triangolo e del ritaglio, gli attributi con \_ COLORE D3DDECLUSAGE vengono interpolati come ombreggiati. \_</span><span class="sxs-lookup"><span data-stu-id="2453b-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="2453b-172">Se a qualsiasi componente di un registro viene dichiarata una semantica dei colori, ma ad altri componenti dello stesso registro viene data una semantica diversa, l'interpolazione di ombreggiatura piatta (lineare o flat) non sarà definita nei componenti del registro senza una semantica di colore.</span><span class="sxs-lookup"><span data-stu-id="2453b-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="2453b-173">Se si desidera eseguire il rendering del rendering, gli \_ shader 3 0 e \_ ps 3 0 devono \_ \_ implementare il modello a confronto.</span><span class="sxs-lookup"><span data-stu-id="2453b-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="2453b-174">Non viene eseguito alcun calcolo al di fuori degli shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="2453b-175">Non è presente alcun registro di nebbia in confronto a 3 0 e sono state aggiunte altre semantiche D3DDECLUSAGE FOG (per il fattore di blend della nebbia calcolato per vertice) e \_ \_ \_ D3DDECLUSAGE DEPTH (per passare un valore di profondità al pixel shader per calcolare il fattore di blend della \_ nebbia).</span><span class="sxs-lookup"><span data-stu-id="2453b-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="2453b-176">Lo stato della fase della trama D3DTSS TEXCOORDINDEX viene ignorato quando si usa \_ pixel shader 3.0.</span><span class="sxs-lookup"><span data-stu-id="2453b-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="2453b-177">Per supportare queste modifiche, sono stati aggiunti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2453b-177">The following values have been added to accommodate these changes:</span></span>


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



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="2453b-178">Conversioni a virgola mobile e interi</span><span class="sxs-lookup"><span data-stu-id="2453b-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="2453b-179">La matematica a virgola mobile avviene a precisione e intervalli diversi (16 bit, 24 bit e 32 bit) in parti diverse della pipeline.</span><span class="sxs-lookup"><span data-stu-id="2453b-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="2453b-180">Un valore maggiore dell'intervallo dinamico della pipeline che entra nella pipeline (ad esempio, una mappa di trama float a 32 bit viene campionata in una pipeline float a 24 bit in ps \_ 2 0) crea un risultato non \_ definito.</span><span class="sxs-lookup"><span data-stu-id="2453b-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="2453b-181">Per un comportamento prevedibile, è necessario impostare tale valore sul valore massimo dell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="2453b-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="2453b-182">La conversione da un valore a virgola mobile a un numero intero avviene in diverse posizioni, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2453b-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="2453b-183">Quando si incontra una [mova- o un'istruzione.](mova---vs.md)</span><span class="sxs-lookup"><span data-stu-id="2453b-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="2453b-184">Durante l'indirizzamento della trama.</span><span class="sxs-lookup"><span data-stu-id="2453b-184">During texture addressing.</span></span>
-   <span data-ttu-id="2453b-185">Quando si scrive in una destinazione di rendering non a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2453b-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="2453b-186">Specifica della precisione completa o parziale</span><span class="sxs-lookup"><span data-stu-id="2453b-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="2453b-187">Sia ps \_ 3 \_ 0 che ps 2 x forniscono il supporto \_ per due livelli di \_ precisione:</span><span class="sxs-lookup"><span data-stu-id="2453b-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="2453b-188">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2453b-188">ps\_3\_0</span></span> | <span data-ttu-id="2453b-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2453b-189">ps\_2\_0</span></span> | <span data-ttu-id="2453b-190">Precisione</span><span class="sxs-lookup"><span data-stu-id="2453b-190">Precision</span></span>         | <span data-ttu-id="2453b-191">Valore</span><span class="sxs-lookup"><span data-stu-id="2453b-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="2453b-192">x</span><span class="sxs-lookup"><span data-stu-id="2453b-192">x</span></span>        |          | <span data-ttu-id="2453b-193">Full</span><span class="sxs-lookup"><span data-stu-id="2453b-193">Full</span></span>              | <span data-ttu-id="2453b-194">fp32 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2453b-194">fp32 or higher</span></span>       |
| <span data-ttu-id="2453b-195">x</span><span class="sxs-lookup"><span data-stu-id="2453b-195">x</span></span>        |          | <span data-ttu-id="2453b-196">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="2453b-196">Partial precision</span></span> | <span data-ttu-id="2453b-197">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="2453b-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="2453b-198">x</span><span class="sxs-lookup"><span data-stu-id="2453b-198">x</span></span>        | <span data-ttu-id="2453b-199">x</span><span class="sxs-lookup"><span data-stu-id="2453b-199">x</span></span>        | <span data-ttu-id="2453b-200">Full</span><span class="sxs-lookup"><span data-stu-id="2453b-200">Full</span></span>              | <span data-ttu-id="2453b-201">fp24=s16e7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2453b-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="2453b-202">x</span><span class="sxs-lookup"><span data-stu-id="2453b-202">x</span></span>        | <span data-ttu-id="2453b-203">x</span><span class="sxs-lookup"><span data-stu-id="2453b-203">x</span></span>        | <span data-ttu-id="2453b-204">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="2453b-204">Partial precision</span></span> | <span data-ttu-id="2453b-205">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="2453b-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="2453b-206">ps \_ 3 \_ 0 supporta una precisione maggiore rispetto a ps \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="2453b-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="2453b-207">Per impostazione predefinita, tutte le operazioni vengono eseguite al livello di precisione completo.</span><span class="sxs-lookup"><span data-stu-id="2453b-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="2453b-208">La precisione parziale (vedere [Modificatori di registro](dx9-graphics-reference-asm-ps-registers-modifiers.md)pixel shader) viene richiesta aggiungendo il modificatore pp al codice dello shader (a condizione che l'implementazione \_ sottostante lo supporti).</span><span class="sxs-lookup"><span data-stu-id="2453b-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="2453b-209">Le implementazioni sono sempre liberi di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="2453b-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="2453b-210">Il \_ modificatore pp può verificarsi in due contesti:</span><span class="sxs-lookup"><span data-stu-id="2453b-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="2453b-211">In una dichiarazione di coordinate di trama per passare coordinate di trama a precisione parziale al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="2453b-212">Può essere usato quando la trama coordina l'inoltro dei dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.</span><span class="sxs-lookup"><span data-stu-id="2453b-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="2453b-213">In qualsiasi istruzione per richiedere l'uso di precisione parziale, incluse le istruzioni di caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="2453b-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="2453b-214">Ciò indica che l'implementazione può eseguire l'istruzione con precisione parziale e archiviare un risultato a precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="2453b-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="2453b-215">In assenza di un modificatore esplicito, l'istruzione deve essere eseguita con precisione completa (indipendentemente dalla precisione degli operandi di input).</span><span class="sxs-lookup"><span data-stu-id="2453b-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="2453b-216">Un'applicazione potrebbe scegliere deliberatamente di trovare un compromesso tra precisione e prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2453b-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="2453b-217">Esistono diversi tipi di dati di input shader che sono candidati naturali per l'elaborazione con precisione parziale:</span><span class="sxs-lookup"><span data-stu-id="2453b-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="2453b-218">Gli iteratori di colore sono ben rappresentati da valori a precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="2453b-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="2453b-219">I valori di trama della maggior parte dei formati possono essere rappresentati in modo accurato da valori a precisione parziale (i valori campionati da trame in formato a virgola mobile a 32 bit sono un'eccezione ovvia).</span><span class="sxs-lookup"><span data-stu-id="2453b-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="2453b-220">Le costanti possono essere rappresentate da una rappresentazione a precisione parziale in base alle esigenze dello shader.</span><span class="sxs-lookup"><span data-stu-id="2453b-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="2453b-221">In tutti questi casi lo sviluppatore può scegliere di specificare una precisione parziale per elaborare i dati, sapendo che non viene persa alcuna precisione dei dati di input.</span><span class="sxs-lookup"><span data-stu-id="2453b-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="2453b-222">In alcuni casi, uno shader può richiedere che i passaggi interni di un calcolo siano eseguiti con la massima precisione anche quando i valori di input e di output finale non hanno una precisione maggiore di parziale.</span><span class="sxs-lookup"><span data-stu-id="2453b-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="2453b-223">Vertici software e pixel shader</span><span class="sxs-lookup"><span data-stu-id="2453b-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="2453b-224">Le implementazioni software (run-time e riferimento per i vertex shader e informazioni di riferimento per i pixel shader) degli shader versione 2 0 e successive hanno una convalida \_ più disassociato.</span><span class="sxs-lookup"><span data-stu-id="2453b-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="2453b-225">Ciò è utile a scopo di debug e prototipazione.</span><span class="sxs-lookup"><span data-stu-id="2453b-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="2453b-226">L'applicazione indica al runtime/assembler che è necessario un po' della convalida con il \_ flag sw nell'assembler (ad esempio, vs \_ 2 \_ sw).</span><span class="sxs-lookup"><span data-stu-id="2453b-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="2453b-227">Uno shader software non funzionerà con l'hardware.</span><span class="sxs-lookup"><span data-stu-id="2453b-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="2453b-228">rispetto a 2 sw è un relax rispetto ai limiti massimi di vs \_ \_ \_ 2 \_ x; analogamente, ps 2 sw è un relax ai limiti massimi di \_ \_ ps \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="2453b-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="2453b-229">In particolare, le convalide seguenti sono di tipo relaxed:</span><span class="sxs-lookup"><span data-stu-id="2453b-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2453b-230">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2453b-230">Shader Model</span></span>                               | <span data-ttu-id="2453b-231">Risorsa</span><span class="sxs-lookup"><span data-stu-id="2453b-231">Resource</span></span>                             | <span data-ttu-id="2453b-232">Limite</span><span class="sxs-lookup"><span data-stu-id="2453b-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="2453b-233">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-234">Conteggi delle istruzioni</span><span class="sxs-lookup"><span data-stu-id="2453b-234">Instruction Counts</span></span>                   | <span data-ttu-id="2453b-235">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="2453b-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="2453b-236">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-237">Registri costanti float</span><span class="sxs-lookup"><span data-stu-id="2453b-237">Float Constant Registers</span></span>             | <span data-ttu-id="2453b-238">8192</span><span class="sxs-lookup"><span data-stu-id="2453b-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="2453b-239">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-240">Registri costanti Integer</span><span class="sxs-lookup"><span data-stu-id="2453b-240">Integer Constant Registers</span></span>           | <span data-ttu-id="2453b-241">2048</span><span class="sxs-lookup"><span data-stu-id="2453b-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="2453b-242">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-243">Registri costanti booleani</span><span class="sxs-lookup"><span data-stu-id="2453b-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="2453b-244">2048</span><span class="sxs-lookup"><span data-stu-id="2453b-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="2453b-245">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="2453b-246">Profondità di lettura dipendente</span><span class="sxs-lookup"><span data-stu-id="2453b-246">Dependent-read depth</span></span>                 | <span data-ttu-id="2453b-247">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="2453b-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="2453b-248">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="2453b-249">Istruzioni ed etichette per il controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="2453b-249">flow control instructions and labels</span></span> | <span data-ttu-id="2453b-250">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="2453b-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="2453b-251">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-252">Inizio ciclo/passaggio/conteggio</span><span class="sxs-lookup"><span data-stu-id="2453b-252">Loop start/step/counts</span></span>               | <span data-ttu-id="2453b-253">Le dimensioni dei passaggi di inizio e iterazione per le istruzioni rep e loop sono interi con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2453b-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="2453b-254">Il conteggio può essere fino a MAX \_ INT/64.</span><span class="sxs-lookup"><span data-stu-id="2453b-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="2453b-255">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="2453b-256">Limiti delle porte</span><span class="sxs-lookup"><span data-stu-id="2453b-256">Port limits</span></span>                          | <span data-ttu-id="2453b-257">I limiti delle porte per tutti i file di registro sono di tipo relaxed.</span><span class="sxs-lookup"><span data-stu-id="2453b-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="2453b-258">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="2453b-259">Numero di interpolatori</span><span class="sxs-lookup"><span data-stu-id="2453b-259">Number of interpolators</span></span>              | <span data-ttu-id="2453b-260">16 registri di output in vs \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="2453b-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="2453b-261">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2453b-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="2453b-262">Numero di interpolatori</span><span class="sxs-lookup"><span data-stu-id="2453b-262">Number of interpolators</span></span>              | <span data-ttu-id="2453b-263">14(16-2) registri di input per ps \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="2453b-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="2453b-264">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2453b-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2453b-265">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2453b-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
