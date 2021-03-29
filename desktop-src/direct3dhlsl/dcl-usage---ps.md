---
title: dcl_semantics (SM3-PS ASM)
description: Dichiarare l'associazione tra l'output del vertex shader e l'input pixel shader.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118067"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="61ebc-103">\_semantica di DCL (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="61ebc-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="61ebc-104">Dichiarare l'associazione tra l'output del vertex shader e l'input pixel shader.</span><span class="sxs-lookup"><span data-stu-id="61ebc-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ebc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61ebc-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="61ebc-106">\_maschera di semantica di DCL \[ \_ \] \[ . \_\]</span><span class="sxs-lookup"><span data-stu-id="61ebc-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="61ebc-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="61ebc-107">Where:</span></span>

-   <span data-ttu-id="61ebc-108">\_semantica: identifica l'utilizzo previsto dei dati e può essere uno qualsiasi dei valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (senza il \_ prefisso D3DDECLUSAGE).</span><span class="sxs-lookup"><span data-stu-id="61ebc-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="61ebc-109">Inoltre, un indice Integer può essere aggiunto alla semantica per distinguere i parametri che usano una semantica simile.</span><span class="sxs-lookup"><span data-stu-id="61ebc-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="61ebc-110">\[\_[](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) Centro \] modificatore di istruzione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61ebc-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="61ebc-111">È supportato nelle istruzioni di utilizzo di DCL \_ che dichiarano i registri di input e le istruzioni per la ricerca di trame.</span><span class="sxs-lookup"><span data-stu-id="61ebc-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="61ebc-112">Il baricentro viene aggiunto senza spazio.</span><span class="sxs-lookup"><span data-stu-id="61ebc-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="61ebc-113">DST: Registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="61ebc-113">dst: destination register.</span></span> <span data-ttu-id="61ebc-114">Vedere [ \_ registri PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="61ebc-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="61ebc-115">\_maschera di scrittura: lo stesso registro di output può essere dichiarato più volte, ogni volta con una maschera di scrittura univoca (pertanto è possibile applicare una semantica diversa ai singoli componenti).</span><span class="sxs-lookup"><span data-stu-id="61ebc-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="61ebc-116">Tuttavia, la stessa semantica non può essere utilizzata più volte in una dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="61ebc-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="61ebc-117">Ciò significa che i vettori devono essere costituiti da quattro componenti o meno e non possono superare i limiti di registro a quattro componenti (singoli registri di output).</span><span class="sxs-lookup"><span data-stu-id="61ebc-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="61ebc-118">Quando si \_ Usa la semantica psize, deve avere una maschera di scrittura completa perché è considerata scalare.</span><span class="sxs-lookup"><span data-stu-id="61ebc-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="61ebc-119">Quando \_ si usa la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="61ebc-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="61ebc-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="61ebc-120">Remarks</span></span>



| <span data-ttu-id="61ebc-121">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="61ebc-121">Pixel shader versions</span></span> | <span data-ttu-id="61ebc-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="61ebc-122">1\_1</span></span> | <span data-ttu-id="61ebc-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="61ebc-123">1\_2</span></span> | <span data-ttu-id="61ebc-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="61ebc-124">1\_3</span></span> | <span data-ttu-id="61ebc-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="61ebc-125">1\_4</span></span> | <span data-ttu-id="61ebc-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="61ebc-126">2\_0</span></span> | <span data-ttu-id="61ebc-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="61ebc-127">2\_x</span></span> | <span data-ttu-id="61ebc-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61ebc-128">2\_sw</span></span> | <span data-ttu-id="61ebc-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="61ebc-129">3\_0</span></span> | <span data-ttu-id="61ebc-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61ebc-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="61ebc-131">utilizzo di DCL \_</span><span class="sxs-lookup"><span data-stu-id="61ebc-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="61ebc-132">x</span><span class="sxs-lookup"><span data-stu-id="61ebc-132">x</span></span>    | <span data-ttu-id="61ebc-133">x</span><span class="sxs-lookup"><span data-stu-id="61ebc-133">x</span></span>     |



 

<span data-ttu-id="61ebc-134">Tutte le \_ istruzioni di utilizzo di DCL devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="61ebc-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="61ebc-135">Esempi di dichiarazione</span><span class="sxs-lookup"><span data-stu-id="61ebc-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="61ebc-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61ebc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ebc-137">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="61ebc-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="61ebc-138">[Esempio antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="61ebc-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 