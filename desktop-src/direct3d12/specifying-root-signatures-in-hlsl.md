---
title: Specifica delle firme radice in HLSL
description: Specificare le firme radice nel modello di shader HLSL 5.1 è un'alternativa a specificarle nel codice C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492283"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="fe909-103">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="fe909-104">Specificare le firme radice nel modello di shader HLSL 5.1 è un'alternativa a specificarle nel codice C++.</span><span class="sxs-lookup"><span data-stu-id="fe909-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="fe909-105">Esempio di firma radice HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="fe909-106">Firma radice versione 1.0</span><span class="sxs-lookup"><span data-stu-id="fe909-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="fe909-107">Firma radice versione 1.1</span><span class="sxs-lookup"><span data-stu-id="fe909-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="fe909-108">Flag radice</span><span class="sxs-lookup"><span data-stu-id="fe909-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="fe909-109">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="fe909-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="fe909-110">Visibilità</span><span class="sxs-lookup"><span data-stu-id="fe909-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="fe909-111">CBV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="fe909-112">SRV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="fe909-113">UAV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="fe909-114">Tabella dei descrittori</span><span class="sxs-lookup"><span data-stu-id="fe909-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="fe909-115">Campionatore statico</span><span class="sxs-lookup"><span data-stu-id="fe909-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="fe909-116">Compilazione di una firma radice HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="fe909-117">Modifica delle firme radice con il compilatore FXC</span><span class="sxs-lookup"><span data-stu-id="fe909-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="fe909-118">Note</span><span class="sxs-lookup"><span data-stu-id="fe909-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="fe909-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe909-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="fe909-120">Esempio di firma radice HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="fe909-121">Una firma radice può essere specificata in HLSL come stringa.</span><span class="sxs-lookup"><span data-stu-id="fe909-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="fe909-122">La stringa contiene una raccolta di clausole delimitati da virgole che descrivono i componenti costitutivi della firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="fe909-123">La firma radice deve essere identica tra gli shader per qualsiasi oggetto di stato della pipeline (PSO).</span><span class="sxs-lookup"><span data-stu-id="fe909-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="fe909-124">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="fe909-125">Firma radice versione 1.0</span><span class="sxs-lookup"><span data-stu-id="fe909-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="fe909-126">Questa definizione darebbe la firma radice seguente, notando:</span><span class="sxs-lookup"><span data-stu-id="fe909-126">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="fe909-127">Uso dei parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe909-127">The use of default parameters.</span></span>
-   <span data-ttu-id="fe909-128">b0 e (b0, space=1) non sono in conflitto</span><span class="sxs-lookup"><span data-stu-id="fe909-128">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="fe909-129">u0 è visibile solo allo shader geometry</span><span class="sxs-lookup"><span data-stu-id="fe909-129">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="fe909-130">Gli alias u4 e u5 sono alias dello stesso descrittore in un heap</span><span class="sxs-lookup"><span data-stu-id="fe909-130">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![una firma radice specificata usando il linguaggio shader di alto livello](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a><span data-ttu-id="fe909-132">Firma radice versione 1.1</span><span class="sxs-lookup"><span data-stu-id="fe909-132">Root Signature Version 1.1</span></span>

<span data-ttu-id="fe909-133">[La versione 1.1 della firma radice](root-signature-version-1-1.md) abilita le ottimizzazioni dei driver per i descrittori e i dati della firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-133">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="fe909-134">Il linguaggio di firma radice HLSL corrisponde strettamente alle API di firma radice C++ e ha una potenza espressiva equivalente.</span><span class="sxs-lookup"><span data-stu-id="fe909-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="fe909-135">La firma radice viene specificata come sequenza di clausole, separate da virgola.</span><span class="sxs-lookup"><span data-stu-id="fe909-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="fe909-136">L'ordine delle clausole è importante, in quanto l'ordine di analisi determina la posizione dello slot nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="fe909-137">Ogni clausola accetta uno o più parametri denominati.</span><span class="sxs-lookup"><span data-stu-id="fe909-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="fe909-138">L'ordine dei parametri, tuttavia, non è importante.</span><span class="sxs-lookup"><span data-stu-id="fe909-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="fe909-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="fe909-139">RootFlags</span></span>

<span data-ttu-id="fe909-140">La *clausola RootFlags* facoltativa accetta 0 (il valore predefinito per indicare nessun flag) o uno o più valori di flag radice predefiniti, connessi tramite l'operatore OR ' \| '.</span><span class="sxs-lookup"><span data-stu-id="fe909-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="fe909-141">I valori dei flag radice consentiti sono definiti da [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="fe909-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="fe909-142">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="fe909-143">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="fe909-143">Root Constants</span></span>

<span data-ttu-id="fe909-144">La *clausola RootConstants* specifica le costanti radice nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="fe909-145">Due parametri obbligatori sono: *num32BitConstants* e *bReg* (il registro corrispondente a *BaseShaderRegister* nelle API C++) di *cbuffer*.</span><span class="sxs-lookup"><span data-stu-id="fe909-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="fe909-146">I parametri space (*RegisterSpace* nelle API C++) e visibility (*ShaderVisibility* in C++) sono facoltativi e i valori predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="fe909-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="fe909-147">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="fe909-148">Visibilità</span><span class="sxs-lookup"><span data-stu-id="fe909-148">Visibility</span></span>

<span data-ttu-id="fe909-149">Visibility è un parametro facoltativo che può avere uno dei valori di [**D3D12 \_ SHADER \_ VISIBILITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)</span><span class="sxs-lookup"><span data-stu-id="fe909-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="fe909-150">SHADER \_ VISIBILITY ALL trasmette gli argomenti radice a tutti gli \_ shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="fe909-151">In alcuni hardware questa operazione non ha alcun costo, ma su altri componenti hardware è necessario creare una fork dei dati in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="fe909-152">L'impostazione di una delle opzioni, ad esempio SHADER \_ VISIBILITY \_ VERTEX, limita l'argomento radice a una singola fase dello shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="fe909-153">L'impostazione degli argomenti radice nelle fasi di uno shader singolo consente di usare lo stesso nome di associazione in fasi diverse.</span><span class="sxs-lookup"><span data-stu-id="fe909-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="fe909-154">Ad esempio, un'associazione SRV di `t0,SHADER_VISIBILITY_VERTEX` e l'associazione SRV `t0,SHADER_VISIBILITY_PIXEL` di sarebbero valide.</span><span class="sxs-lookup"><span data-stu-id="fe909-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="fe909-155">Tuttavia, se l'impostazione di visibilità fosse per una `t0,SHADER_VISIBILITY_ALL` delle associazioni, la firma radice non sarebbe valida.</span><span class="sxs-lookup"><span data-stu-id="fe909-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="fe909-156">CBV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-156">Root-level CBV</span></span>

<span data-ttu-id="fe909-157">La `CBV` clausola (visualizzazione buffer costante) specifica una voce Reg di buffer b-register costante a livello radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="fe909-158">Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="fe909-159">SRV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-159">Root-level SRV</span></span>

<span data-ttu-id="fe909-160">La `SRV` clausola (visualizzazione delle risorse shader) specifica una voce reg T-register SRV a livello di radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="fe909-161">Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="fe909-162">UAV a livello di radice</span><span class="sxs-lookup"><span data-stu-id="fe909-162">Root-level UAV</span></span>

<span data-ttu-id="fe909-163">La `UAV` clausola (visualizzazione di accesso non ordinato) specifica una voce reg UAV u-register a livello di radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="fe909-164">Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="fe909-165">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="fe909-166">Tabella dei descrittori</span><span class="sxs-lookup"><span data-stu-id="fe909-166">Descriptor Table</span></span>

<span data-ttu-id="fe909-167">La clausola è di per sé un elenco di clausole della tabella dei descrittori delimitati da virgole, nonché un `DescriptorTable` parametro di visibilità facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fe909-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="fe909-168">Le *clausole DescriptorTable* includono CBV, SRV, UAV e Sampler.</span><span class="sxs-lookup"><span data-stu-id="fe909-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="fe909-169">Si noti che i parametri sono diversi da quelli delle clausole a livello di radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="fe909-170">La tabella del descrittore `CBV` ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="fe909-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="fe909-171">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="fe909-172">Il parametro *obbligatorio bReg* specifica il reg iniziale dell'intervallo cbuffer.</span><span class="sxs-lookup"><span data-stu-id="fe909-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="fe909-173">Il *parametro numDescriptors* specifica il numero di descrittori nell'intervallo cbuffer contiguo. il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="fe909-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="fe909-174">La voce dichiara un intervallo cbuffer ` [Reg, Reg + numDescriptors - 1]` , quando *numDescriptors* è un numero.</span><span class="sxs-lookup"><span data-stu-id="fe909-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="fe909-175">Se *numDescriptors* è uguale a "unbounded", l'intervallo è , il che significa che l'app deve assicurarsi che non faccia riferimento a un'area non `[Reg, UINT_MAX]` in limiti.</span><span class="sxs-lookup"><span data-stu-id="fe909-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="fe909-176">Il *campo offset* rappresenta il parametro *OffsetInDescriptorsFromTableStart* nelle API C++, ovvero l'offset (in descrittori) dall'inizio della tabella.</span><span class="sxs-lookup"><span data-stu-id="fe909-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="fe909-177">Se l'offset è impostato su DESCRIPTOR RANGE OFFSET APPEND (impostazione predefinita), significa che l'intervallo è \_ \_ direttamente successivo \_ all'intervallo precedente.</span><span class="sxs-lookup"><span data-stu-id="fe909-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="fe909-178">Tuttavia, l'immissione di offset specifici consente la sovrapposizione degli intervalli, consentendo l'alias del registro.</span><span class="sxs-lookup"><span data-stu-id="fe909-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="fe909-179">La tabella del descrittore `SRV` ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="fe909-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="fe909-180">È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per le visualizzazioni delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="fe909-181">La tabella del descrittore `UAV` ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="fe909-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="fe909-182">È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per le viste di accesso non ordinate.</span><span class="sxs-lookup"><span data-stu-id="fe909-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="fe909-183">La tabella dei descrittori `Sampler` ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="fe909-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="fe909-184">È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per i campionatori shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="fe909-185">Si noti che i campionatori non possono essere misti con altri tipi di descrittori nella stessa tabella dei descrittori(poiché si tratta di un heap descrittore separato).</span><span class="sxs-lookup"><span data-stu-id="fe909-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="fe909-186">Campionatore statico</span><span class="sxs-lookup"><span data-stu-id="fe909-186">Static Sampler</span></span>

<span data-ttu-id="fe909-187">Il campionatore statico rappresenta la [**struttura DESC D3D12 \_ STATIC \_ SAMPLER. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="fe909-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="fe909-188">Il parametro obbligatorio per *StaticSampler* è un reg scalare, sampler s-register. Altri parametri sono facoltativi con i valori predefiniti illustrati di seguito.</span><span class="sxs-lookup"><span data-stu-id="fe909-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="fe909-189">La maggior parte dei campi accetta un set di enumerazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="fe909-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="fe909-190">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="fe909-191">Le opzioni dei parametri sono molto simili alle chiamate API C++, ad eccezione di *borderColor*, che è limitato a un'enumerazione in HLSL.</span><span class="sxs-lookup"><span data-stu-id="fe909-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="fe909-192">Il campo del filtro può essere uno di [**D3D12 \_ FILTER.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)</span><span class="sxs-lookup"><span data-stu-id="fe909-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="fe909-193">I campi dell'indirizzo possono essere ognuno di [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="fe909-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="fe909-194">La funzione di confronto può essere una di [**D3D12 \_ COMPARISON \_ FUNC.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)</span><span class="sxs-lookup"><span data-stu-id="fe909-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="fe909-195">Il campo del colore del bordo può essere uno di [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="fe909-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="fe909-196">La visibilità può essere una [**di D3D12 \_ SHADER \_ VISIBILITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)</span><span class="sxs-lookup"><span data-stu-id="fe909-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="fe909-197">Compilazione di una firma radice HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="fe909-198">Esistono due meccanismi per compilare una firma radice HLSL.</span><span class="sxs-lookup"><span data-stu-id="fe909-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="fe909-199">In primo luogo, è possibile associare una stringa di firma radice a un particolare shader tramite l'attributo *RootSignature* (nell'esempio seguente, usando il punto di ingresso **MyRS1):**</span><span class="sxs-lookup"><span data-stu-id="fe909-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="fe909-200">Il compilatore creerà e verificherà il BLOB della firma radice per lo shader e lo incorpora insieme al codice byte dello shader nel BLOB shader.</span><span class="sxs-lookup"><span data-stu-id="fe909-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="fe909-201">Il compilatore supporta la sintassi della firma radice per il modello shader 5.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fe909-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="fe909-202">Se una firma radice è incorporata in uno shader del modello di shader 5.0 e tale shader viene inviato al runtime D3D11, a differenza di D3D12, la parte della firma radice verrà automaticamente ignorata da D3D11.</span><span class="sxs-lookup"><span data-stu-id="fe909-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="fe909-203">L'altro meccanismo è creare un BLOB di firma radice autonomo, ad esempio per riutilizzarlo con un set di shader di grandi dimensioni, risparmiando spazio.</span><span class="sxs-lookup"><span data-stu-id="fe909-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="fe909-204">[Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supporta i modelli di shader **rootsig \_ 1 \_ 0** e **rootsig \_ \_ 1 1.**</span><span class="sxs-lookup"><span data-stu-id="fe909-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="fe909-205">Il nome della stringa di definizione viene specificato tramite il consueto argomento /E.</span><span class="sxs-lookup"><span data-stu-id="fe909-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="fe909-206">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fe909-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="fe909-207">Si noti che la stringa di firma radice definita può essere passata anche nella riga di comando, ad esempio /D MyRS1="...".</span><span class="sxs-lookup"><span data-stu-id="fe909-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="fe909-208">Modifica delle firme radice con il compilatore FXC</span><span class="sxs-lookup"><span data-stu-id="fe909-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="fe909-209">Il compilatore FXC crea il byte-code dello shader dai file di origine HLSL.</span><span class="sxs-lookup"><span data-stu-id="fe909-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="fe909-210">Esistono molti parametri facoltativi per questo compilatore. Fare riferimento a [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="fe909-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="fe909-211">Per la gestione delle firme radice di HLSL, la tabella seguente fornisce alcuni esempi di uso di FXC.</span><span class="sxs-lookup"><span data-stu-id="fe909-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="fe909-212">Linea</span><span class="sxs-lookup"><span data-stu-id="fe909-212">Line</span></span> | <span data-ttu-id="fe909-213">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="fe909-213">Command line</span></span>                                                                 | <span data-ttu-id="fe909-214">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe909-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe909-215">1</span><span class="sxs-lookup"><span data-stu-id="fe909-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="fe909-216">Compila uno shader per la destinazione pixel shader 5.1, l'origine dello shader si trova nel file shaderWithRootSig.hlsl, che include una firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="fe909-217">La firma shader e radice vengono compilate come BLOB separati nel file binario rs1.fxo.</span><span class="sxs-lookup"><span data-stu-id="fe909-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="fe909-218">2</span><span class="sxs-lookup"><span data-stu-id="fe909-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="fe909-219">Estrae la firma radice dal file creato dalla riga 1, quindi il file rs1.rs.fxo contiene solo una firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="fe909-220">3</span><span class="sxs-lookup"><span data-stu-id="fe909-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="fe909-221">Rimuove la firma radice dal file creato dalla riga 1, in modo che il file rs1.stripped.fxo contenga uno shader senza firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="fe909-222">4</span><span class="sxs-lookup"><span data-stu-id="fe909-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="fe909-223">Combina uno shader e una firma radice in file separati in un file binario contenente entrambi i BLOB.</span><span class="sxs-lookup"><span data-stu-id="fe909-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="fe909-224">In questo esempio rs1.new.fx0 sarebbe identico a rs1.fx0 nella riga 1.</span><span class="sxs-lookup"><span data-stu-id="fe909-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="fe909-225">5</span><span class="sxs-lookup"><span data-stu-id="fe909-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="fe909-226">Crea un file binario di firma radice autonomo da un'origine che può contenere più di una semplice firma radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="fe909-227">Si noti la destinazione rootsig 1 0 e che RS1 è il nome della stringa della macro root \_ \_ signature (define) nel file \# HLSL.</span><span class="sxs-lookup"><span data-stu-id="fe909-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="fe909-228">La funzionalità disponibile tramite FXC è disponibile anche a livello di codice usando la [**funzione D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="fe909-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="fe909-229">Questa chiamata compila uno shader con una firma radice o una firma radice autonoma (impostando la destinazione rootsig \_ 1 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="fe909-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="fe909-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) e [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) possono estrarre e collegare firme radice a un BLOB esistente.</span><span class="sxs-lookup"><span data-stu-id="fe909-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span>  <span data-ttu-id="fe909-231">D3D BLOB ROOT SIGNATURE viene usato per specificare il tipo di parte \_ \_ BLOB della firma \_ radice.</span><span class="sxs-lookup"><span data-stu-id="fe909-231">D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="fe909-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) rimuove la firma radice (usando il flag D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE) dal BLOB.</span><span class="sxs-lookup"><span data-stu-id="fe909-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="fe909-233">Note</span><span class="sxs-lookup"><span data-stu-id="fe909-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="fe909-234">Mentre la compilazione offline degli shader è fortemente consigliata, se gli shader devono essere compilati in fase di esecuzione, fare riferimento alle osservazioni per [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="fe909-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="fe909-235">Gli asset HLSL esistenti non devono essere modificati per gestire le firme radice da usare con esse.</span><span class="sxs-lookup"><span data-stu-id="fe909-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fe909-236">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe909-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe909-237">Indicizzazione dinamica con HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="fe909-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="fe909-238">Funzionalità di HLSL Shader Model 5.1 per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fe909-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="fe909-239">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="fe909-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="fe909-240">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="fe909-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="fe909-241">Firme radice</span><span class="sxs-lookup"><span data-stu-id="fe909-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="fe909-242">Modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="fe909-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="fe909-243">Valore di riferimento dello stencil specificato dello shader</span><span class="sxs-lookup"><span data-stu-id="fe909-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="fe909-244">Caricamenti Unordered Access View tipi</span><span class="sxs-lookup"><span data-stu-id="fe909-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
