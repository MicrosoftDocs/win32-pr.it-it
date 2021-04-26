---
title: dcl_usage output (sm1, sm2, sm3 - vs asm)
description: I vari tipi di registri di output sono stati compressi in dodici registri di output (due per il colore, otto per la trama, uno per la posizione e uno per le dimensioni dei punti e dei punti).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999168"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="7d967-103">Output dcl \_ usage (sm1, sm2, sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="7d967-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="7d967-104">I vari tipi di registri di output sono stati compressi in dodici registri di output (due per il colore, otto per la trama, uno per la posizione e uno per le dimensioni dei punti e dei punti).</span><span class="sxs-lookup"><span data-stu-id="7d967-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="7d967-105">Possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate della trama, colori, tempo e così via.</span><span class="sxs-lookup"><span data-stu-id="7d967-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="7d967-106">I registri di output richiedono dichiarazioni che includono semantica.</span><span class="sxs-lookup"><span data-stu-id="7d967-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="7d967-107">Ad esempio, la posizione precedente e i registri delle dimensioni dei punti vengono sostituiti dichiarando un registro di output con una semantica di posizione o dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="7d967-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="7d967-108">Dei dodici registri di output, ogni dieci (non necessariamente o0 a o9) ha quattro componenti (xyzw), un altro deve essere dichiarato come position (e deve includere anche tutti e quattro i componenti) e, facoltativamente, uno può essere una dimensione in punti scalari.</span><span class="sxs-lookup"><span data-stu-id="7d967-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d967-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d967-109">Syntax</span></span>

<span data-ttu-id="7d967-110">La sintassi per la dichiarazione dei registri di output è simile alle dichiarazioni per il registro di input:</span><span class="sxs-lookup"><span data-stu-id="7d967-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="7d967-111">dcl \_ semantics o \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="7d967-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="7d967-112">Dove:</span><span class="sxs-lookup"><span data-stu-id="7d967-112">Where:</span></span>

-   <span data-ttu-id="7d967-113">La semantica dcl \_ può usare lo stesso set di semantica della dichiarazione di input.</span><span class="sxs-lookup"><span data-stu-id="7d967-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="7d967-114">I nomi semantici [**provengono da D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e sono associati a un indice, ad esempio position3).</span><span class="sxs-lookup"><span data-stu-id="7d967-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="7d967-115">Deve essere sempre presente un registro di output con la semantica positiont0 quando non viene usato per l'elaborazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="7d967-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="7d967-116">La semantica positiont0 e la semantica pointsize0 sono gli unici che hanno significato oltre a consentire semplicemente il collegamento da vertex shader a pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7d967-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="7d967-117">Per gli shader con controllo di flusso, si presuppone che l'output del caso peggiore sia dichiarato.</span><span class="sxs-lookup"><span data-stu-id="7d967-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="7d967-118">Non sono presenti impostazioni predefinite se uno shader non restituisce effettivamente l'output che dovrebbe (a causa del controllo di flusso).</span><span class="sxs-lookup"><span data-stu-id="7d967-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="7d967-119">o è un registro di output.</span><span class="sxs-lookup"><span data-stu-id="7d967-119">o is an output register.</span></span> <span data-ttu-id="7d967-120">Vedere [Registri \_ di output.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)</span><span class="sxs-lookup"><span data-stu-id="7d967-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="7d967-121">write mask indica lo stesso registro di output che può essere dichiarato più volte (in modo che sia possibile applicare una semantica diversa ai singoli componenti), ogni volta con \_ una maschera di scrittura univoca.</span><span class="sxs-lookup"><span data-stu-id="7d967-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="7d967-122">Tuttavia, la stessa semantica non può essere usata più volte in una dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="7d967-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="7d967-123">Ciò significa che i vettori devono essere quattro componenti o meno e non possono attraversare i limiti del registro a quattro componenti (singoli registri).</span><span class="sxs-lookup"><span data-stu-id="7d967-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="7d967-124">Quando viene usata la semantica delle dimensioni in punti, deve avere una maschera di scrittura completa perché è considerata scalare.</span><span class="sxs-lookup"><span data-stu-id="7d967-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="7d967-125">Quando viene usata la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="7d967-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d967-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d967-126">Remarks</span></span>



| <span data-ttu-id="7d967-127">Versioni di vertex shader</span><span class="sxs-lookup"><span data-stu-id="7d967-127">Vertex shader versions</span></span> | <span data-ttu-id="7d967-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d967-128">3\_0</span></span> | <span data-ttu-id="7d967-129">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="7d967-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="7d967-130">Utilizzo di \_ dcl</span><span class="sxs-lookup"><span data-stu-id="7d967-130">dcl\_usage</span></span>             | <span data-ttu-id="7d967-131">x</span><span class="sxs-lookup"><span data-stu-id="7d967-131">x</span></span>    | <span data-ttu-id="7d967-132">x</span><span class="sxs-lookup"><span data-stu-id="7d967-132">x</span></span>     |



 

<span data-ttu-id="7d967-133">Tutte [le istruzioni dcl \_ usage](dcl-usage-input-register---vs.md) devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7d967-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="7d967-134">Esempi di dichiarazione</span><span class="sxs-lookup"><span data-stu-id="7d967-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="7d967-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d967-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d967-136">Istruzioni per vertex shader</span><span class="sxs-lookup"><span data-stu-id="7d967-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
