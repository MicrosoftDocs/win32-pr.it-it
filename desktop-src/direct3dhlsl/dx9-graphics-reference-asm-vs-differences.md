---
title: Differenze di vertex shader
description: Differenze di vertex shader
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046875"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="97cfd-103">Differenze di vertex shader</span><span class="sxs-lookup"><span data-stu-id="97cfd-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="97cfd-104">Slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="97cfd-104">Instruction Slots</span></span>

<span data-ttu-id="97cfd-105">Ogni versione supporta un numero diverso di slot di istruzioni massime.</span><span class="sxs-lookup"><span data-stu-id="97cfd-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="97cfd-106">Versione</span><span class="sxs-lookup"><span data-stu-id="97cfd-106">Version</span></span>  | <span data-ttu-id="97cfd-107">Numero massimo di slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="97cfd-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97cfd-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="97cfd-108">vs\_1\_1</span></span> | <span data-ttu-id="97cfd-109">128</span><span class="sxs-lookup"><span data-stu-id="97cfd-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="97cfd-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cfd-110">vs\_2\_0</span></span> | <span data-ttu-id="97cfd-111">256</span><span class="sxs-lookup"><span data-stu-id="97cfd-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="97cfd-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97cfd-112">vs\_2\_x</span></span> | <span data-ttu-id="97cfd-113">256</span><span class="sxs-lookup"><span data-stu-id="97cfd-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="97cfd-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cfd-114">vs\_3\_0</span></span> | <span data-ttu-id="97cfd-115">512 minimo e fino al numero di slot in D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="97cfd-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="97cfd-116">Vedere [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="97cfd-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="97cfd-117">Per informazioni sulle limitazioni degli shader software, vedere [software shaders](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="97cfd-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="97cfd-118">Limiti di nidificazione del controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="97cfd-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="97cfd-119">Vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="97cfd-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="97cfd-120">funzionalità di Visual Studio \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="97cfd-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="97cfd-121">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="97cfd-121">New instructions:</span></span>

<span data-ttu-id="97cfd-122">Vedere [le istruzioni-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="97cfd-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="97cfd-123">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="97cfd-123">New registers:</span></span>

<span data-ttu-id="97cfd-124">Vedere [Registers-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="97cfd-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="97cfd-125">Funzionalità di vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cfd-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="97cfd-126">Nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="97cfd-126">New features:</span></span>

-   <span data-ttu-id="97cfd-127">Controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="97cfd-127">Static flow control</span></span>
-   <span data-ttu-id="97cfd-128">Sono disponibili tutti e quattro i componenti del [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md) (a0).</span><span class="sxs-lookup"><span data-stu-id="97cfd-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="97cfd-129">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="97cfd-129">New instructions:</span></span>

-   <span data-ttu-id="97cfd-130">Istruzioni di installazione- [defb-vs](defb---vs.md), [defi-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="97cfd-131">Istruzioni aritmetiche- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [POW-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [SinCos-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="97cfd-132">Istruzioni per il controllo di flusso statico- [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [EndLoop-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [if bool-vs](if-bool---vs.md), [Label-vs](label---vs.md), [loop-vs](loop---vs.md), [Rep-vs](rep---vs.md), [ret-vs](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="97cfd-133">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="97cfd-133">New registers:</span></span>

-   <span data-ttu-id="97cfd-134">[Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="97cfd-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="97cfd-135">[Registro Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="97cfd-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="97cfd-136">[Registro contatore cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="97cfd-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="97cfd-137">Funzionalità di vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97cfd-137">vs\_2\_x Features</span></span>

<span data-ttu-id="97cfd-138">Nuove funzionalità (D3DCAPS9. VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="97cfd-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="97cfd-139">Controllo dinamico di flusso</span><span class="sxs-lookup"><span data-stu-id="97cfd-139">Dynamic flow control</span></span>
-   <span data-ttu-id="97cfd-140">Annidamento per istruzioni di controllo di flusso statiche e dinamiche</span><span class="sxs-lookup"><span data-stu-id="97cfd-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="97cfd-141">Il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) è aumentato</span><span class="sxs-lookup"><span data-stu-id="97cfd-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="97cfd-142">Predicazione</span><span class="sxs-lookup"><span data-stu-id="97cfd-142">Predication</span></span>

<span data-ttu-id="97cfd-143">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="97cfd-143">New Instructions:</span></span>

-   <span data-ttu-id="97cfd-144">Istruzioni per il controllo dinamico del flusso- [Break-vs](break---vs.md), [break \_ comp-vs](break-comp---vs.md), [Breakp-vs](breakp---vs.md), [callnz Predator-vs](callnz-pred---vs.md), [if \_ comp-vs](if-comp---vs.md), [if prede-vs](if-pred---vs.md), [setp \_ comp-vs](setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="97cfd-145">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="97cfd-145">New registers:</span></span>

-   <span data-ttu-id="97cfd-146">[Registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="97cfd-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="97cfd-147">Funzionalità di vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cfd-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="97cfd-148">Nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="97cfd-148">New features :</span></span>

-   <span data-ttu-id="97cfd-149">Ricerca trama</span><span class="sxs-lookup"><span data-stu-id="97cfd-149">Texture lookup</span></span>
-   <span data-ttu-id="97cfd-150">Registri di [output](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indicizzabili (o \# )</span><span class="sxs-lookup"><span data-stu-id="97cfd-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="97cfd-151">Il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) è aumentato a 32</span><span class="sxs-lookup"><span data-stu-id="97cfd-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="97cfd-152">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="97cfd-152">New instructions:</span></span>

-   <span data-ttu-id="97cfd-153">Istruzioni di installazione- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="97cfd-154">Istruzione di trama- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="97cfd-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="97cfd-155">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="97cfd-155">New registers:</span></span>

-   <span data-ttu-id="97cfd-156">[Campionatore (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) / \# i</span><span class="sxs-lookup"><span data-stu-id="97cfd-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="97cfd-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97cfd-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97cfd-158">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="97cfd-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 