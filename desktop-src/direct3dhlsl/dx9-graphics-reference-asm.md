---
title: Informazioni di riferimento su ASM shader
description: Gli shader guidano la pipeline grafica programmabile.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104976543"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="0a925-103">Informazioni di riferimento su ASM shader</span><span class="sxs-lookup"><span data-stu-id="0a925-103">Asm Shader Reference</span></span>

<span data-ttu-id="0a925-104">Gli shader guidano la pipeline grafica programmabile.</span><span class="sxs-lookup"><span data-stu-id="0a925-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="0a925-105">Riferimento vertex shader</span><span class="sxs-lookup"><span data-stu-id="0a925-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="0a925-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0a925-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="0a925-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a925-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="0a925-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0a925-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="0a925-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a925-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="0a925-110">[Differenze tra vertex shader](dx9-graphics-reference-asm-vs-differences.md) riepiloga le differenze tra le versioni di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0a925-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="0a925-111">Riferimento a pixel shader</span><span class="sxs-lookup"><span data-stu-id="0a925-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="0a925-112">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="0a925-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="0a925-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a925-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="0a925-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0a925-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="0a925-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a925-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="0a925-116">[Differenze pixel shader](dx9-graphics-reference-asm-ps-differences.md) riepiloga le differenze tra pixel shader versioni.</span><span class="sxs-lookup"><span data-stu-id="0a925-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="0a925-117">Riferimento al modello Shader 4 e 5</span><span class="sxs-lookup"><span data-stu-id="0a925-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="0a925-118">Le sezioni assembly [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) e [Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) sono descritte le istruzioni supportate dal modello Shader 4 e 5.</span><span class="sxs-lookup"><span data-stu-id="0a925-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="0a925-119">Comportamento dei registri costanti negli shader degli assembly</span><span class="sxs-lookup"><span data-stu-id="0a925-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="0a925-120">Esistono due modi per impostare i registri costanti in un assembly shader:</span><span class="sxs-lookup"><span data-stu-id="0a925-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="0a925-121">Dichiarare una costante dello shader nel codice assembly usando una delle istruzioni def \* .</span><span class="sxs-lookup"><span data-stu-id="0a925-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="0a925-122">Usare uno dei metodi dell' \* \* \* API set ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="0a925-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="0a925-123">Costanti shader Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="0a925-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="0a925-124">In Direct3D 9 la durata delle costanti definite in un dato shader è confinata solo all'esecuzione di tale shader (e non è sottoponibile a override).</span><span class="sxs-lookup"><span data-stu-id="0a925-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="0a925-125">Le costanti definite in Direct3D 9 non hanno effetti collaterali al di fuori dello shader.</span><span class="sxs-lookup"><span data-stu-id="0a925-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="0a925-126">Di seguito è riportato un esempio di utilizzo di Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="0a925-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="0a925-127">In Direct3D 9 la chiamata a Get \* \* \* ShaderConstant \* recupererà solo i valori costanti impostati tramite set \* \* \* ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="0a925-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="0a925-128">Costanti shader Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="0a925-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="0a925-129">Questo comportamento è diverso in Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="0a925-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="0a925-130">In Direct3D 8. x set \* \* \* ShaderConstant viene applicato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0a925-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="0a925-131">Si consideri lo scenario indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0a925-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="0a925-132">Il risultato indesiderato è che l'ordine in cui gli shader sono impostati potrebbe influire sul comportamento osservato dei singoli shader.</span><span class="sxs-lookup"><span data-stu-id="0a925-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="0a925-133">Requisiti del modello di driver shader</span><span class="sxs-lookup"><span data-stu-id="0a925-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="0a925-134">Le interfacce Direct3D 9 sono limitate ai driver DDI (Device Driver Interface) che sono a livello di DirectX 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0a925-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="0a925-135">Per controllare il livello di DDI, eseguire lo [strumento di diagnostica DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) ed esaminare il file di testo salvato.</span><span class="sxs-lookup"><span data-stu-id="0a925-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="0a925-136">Per riferimento, le interfacce Direct3D 8 funzionano solo su driver DDI con estensione DirectX 6 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0a925-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="0a925-137">Formato binario dello shader</span><span class="sxs-lookup"><span data-stu-id="0a925-137">Shader Binary Format</span></span>

<span data-ttu-id="0a925-138">Il layout bit per bit del flusso di istruzioni dello shader è definito in D3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="0a925-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="0a925-139">Se si desidera progettare il proprio compilatore shader o gli strumenti di costruzione e si desiderano ulteriori informazioni sul flusso di token shader, fare riferimento a Direct3D 9 Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="0a925-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="0a925-140">Linguaggio shader simile a C</span><span class="sxs-lookup"><span data-stu-id="0a925-140">C-like Shader Language</span></span>

<span data-ttu-id="0a925-141">Vedere informazioni di [riferimento su HLSL](dx-graphics-hlsl-reference.md) per sperimentare un linguaggio di shader simile a C.</span><span class="sxs-lookup"><span data-stu-id="0a925-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a925-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a925-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a925-143">Riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="0a925-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




