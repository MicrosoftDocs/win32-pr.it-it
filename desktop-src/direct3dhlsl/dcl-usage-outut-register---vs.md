---
title: output dcl_usage (SM1, SM2, SM3-vs ASM)
description: I vari tipi di registri di output sono stati compressi in dodici registri di output (due per colore, otto per trama, uno per la posizione e uno per la nebbia e la dimensione del punto).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993525"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="99598-103">\_output utilizzo DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="99598-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="99598-104">I vari tipi di registri di output sono stati compressi in dodici registri di output (due per colore, otto per trama, uno per la posizione e uno per la nebbia e la dimensione del punto).</span><span class="sxs-lookup"><span data-stu-id="99598-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="99598-105">Questi possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate di trama, colori, nebbia e così via.</span><span class="sxs-lookup"><span data-stu-id="99598-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="99598-106">I registri di output richiedono dichiarazioni che includono la semantica.</span><span class="sxs-lookup"><span data-stu-id="99598-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="99598-107">Ad esempio, i registri della posizione precedente e delle dimensioni dei punti vengono sostituiti dichiarando un registro di output con una posizione o una semantica delle dimensioni del punto.</span><span class="sxs-lookup"><span data-stu-id="99598-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="99598-108">Dei dodici registri di output, le dieci (non necessariamente o0 a O9) hanno quattro componenti (xyzw), un altro deve essere dichiarato come position (e deve includere anche tutti e quattro i componenti) e, facoltativamente, un altro può essere una dimensione scalare.</span><span class="sxs-lookup"><span data-stu-id="99598-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="99598-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99598-109">Syntax</span></span>

<span data-ttu-id="99598-110">La sintassi per la dichiarazione dei registri di output è simile a quella per il registro di input:</span><span class="sxs-lookup"><span data-stu-id="99598-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="99598-111">\_maschera di semantica DCL o \[ . Write \_\]</span><span class="sxs-lookup"><span data-stu-id="99598-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="99598-112">Dove:</span><span class="sxs-lookup"><span data-stu-id="99598-112">Where:</span></span>

-   <span data-ttu-id="99598-113">\_la semantica di DCL può utilizzare lo stesso set di semantica della dichiarazione di input.</span><span class="sxs-lookup"><span data-stu-id="99598-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="99598-114">I nomi semantici provengono da [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e sono associati a un indice, ad esempio POSITION3).</span><span class="sxs-lookup"><span data-stu-id="99598-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="99598-115">Quando non viene usato per l'elaborazione dei vertici, deve essere sempre presente un registro di output con la semantica positiont0.</span><span class="sxs-lookup"><span data-stu-id="99598-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="99598-116">La semantica positiont0 e la semantica pointsize0 sono le uniche che hanno un significato superiore a quello che consente semplicemente il collegamento da vertex a pixel shader.</span><span class="sxs-lookup"><span data-stu-id="99598-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="99598-117">Per gli shader con il controllo di flusso, si presuppone che l'output del case peggiore venga dichiarato.</span><span class="sxs-lookup"><span data-stu-id="99598-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="99598-118">Non esistono valori predefiniti se uno shader non genera effettivamente il risultato che dichiara, a causa del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="99598-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="99598-119">o è un registro di output.</span><span class="sxs-lookup"><span data-stu-id="99598-119">o is an output register.</span></span> <span data-ttu-id="99598-120">Vedere [ \_ registri di output](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="99598-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="99598-121">Write \_ mask indica lo stesso registro di output che può essere dichiarato più volte, in modo che sia possibile applicare una semantica diversa a singoli componenti, ogni volta con una maschera di scrittura univoca.</span><span class="sxs-lookup"><span data-stu-id="99598-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="99598-122">Tuttavia, la stessa semantica non può essere utilizzata più volte in una dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="99598-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="99598-123">Ciò significa che i vettori devono essere costituiti da quattro componenti o meno e non possono superare i limiti di registro a quattro componenti (registri singoli).</span><span class="sxs-lookup"><span data-stu-id="99598-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="99598-124">Quando si usa la semantica delle dimensioni del punto, deve avere una maschera di scrittura completa perché è considerata scalare.</span><span class="sxs-lookup"><span data-stu-id="99598-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="99598-125">Quando si usa la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="99598-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="99598-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="99598-126">Remarks</span></span>



| <span data-ttu-id="99598-127">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="99598-127">Vertex shader versions</span></span> | <span data-ttu-id="99598-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99598-128">3\_0</span></span> | <span data-ttu-id="99598-129">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="99598-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="99598-130">utilizzo di DCL \_</span><span class="sxs-lookup"><span data-stu-id="99598-130">dcl\_usage</span></span>             | <span data-ttu-id="99598-131">x</span><span class="sxs-lookup"><span data-stu-id="99598-131">x</span></span>    | <span data-ttu-id="99598-132">x</span><span class="sxs-lookup"><span data-stu-id="99598-132">x</span></span>     |



 

<span data-ttu-id="99598-133">Tutte le istruzioni di [ \_ utilizzo di DCL](dcl-usage-input-register---vs.md) devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="99598-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="99598-134">Esempi di dichiarazione</span><span class="sxs-lookup"><span data-stu-id="99598-134">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="99598-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99598-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99598-136">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="99598-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 