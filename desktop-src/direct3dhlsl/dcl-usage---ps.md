---
title: dcl_semantics (sm3 - ps asm)
description: Dichiarare l'associazione tra l'output del vertex shader e pixel shader input.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 178b31a386a7ae4aa266ac33ddbb1ee5c842f2d1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997168"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="4f685-103">semantica dcl \_ (sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="4f685-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="4f685-104">Dichiarare l'associazione tra l'output del vertex shader e pixel shader input.</span><span class="sxs-lookup"><span data-stu-id="4f685-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f685-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f685-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="4f685-106">dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="4f685-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="4f685-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="4f685-107">Where:</span></span>

-   <span data-ttu-id="4f685-108">\_semantica: identifica l'utilizzo dei dati previsto e può essere uno dei valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (senza il prefisso D3DDECLUSAGE). \_</span><span class="sxs-lookup"><span data-stu-id="4f685-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="4f685-109">Inoltre, è possibile aggiungere un indice integer alla semantica per distinguere i parametri che usano una semantica simile.</span><span class="sxs-lookup"><span data-stu-id="4f685-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="4f685-110">\[\_[Centroide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] è un modificatore di istruzione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4f685-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="4f685-111">È supportato nelle istruzioni di utilizzo dcl che dichiarano i registri \_ di input e nelle istruzioni di ricerca trame.</span><span class="sxs-lookup"><span data-stu-id="4f685-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="4f685-112">Il centroide viene aggiunto senza spazio.</span><span class="sxs-lookup"><span data-stu-id="4f685-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="4f685-113">dst: registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4f685-113">dst: destination register.</span></span> <span data-ttu-id="4f685-114">Vedere [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="4f685-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="4f685-115">write mask: lo stesso registro di output può essere dichiarato più volte, ogni volta con una maschera di scrittura univoca (in modo che sia possibile applicare una semantica diversa \_ ai singoli componenti).</span><span class="sxs-lookup"><span data-stu-id="4f685-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="4f685-116">Tuttavia, la stessa semantica non può essere usata più volte in una dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="4f685-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="4f685-117">Ciò significa che i vettori devono essere quattro componenti o meno e non possono attraversare i limiti del registro a quattro componenti (registri di output singoli).</span><span class="sxs-lookup"><span data-stu-id="4f685-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="4f685-118">Quando viene \_ usata la semantica psize, deve avere una maschera di scrittura completa perché è considerata scalare.</span><span class="sxs-lookup"><span data-stu-id="4f685-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="4f685-119">Quando viene usata la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti \_ devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="4f685-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f685-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f685-120">Remarks</span></span>



| <span data-ttu-id="4f685-121">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="4f685-121">Pixel shader versions</span></span> | <span data-ttu-id="4f685-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="4f685-122">1\_1</span></span> | <span data-ttu-id="4f685-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="4f685-123">1\_2</span></span> | <span data-ttu-id="4f685-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4f685-124">1\_3</span></span> | <span data-ttu-id="4f685-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="4f685-125">1\_4</span></span> | <span data-ttu-id="4f685-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f685-126">2\_0</span></span> | <span data-ttu-id="4f685-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4f685-127">2\_x</span></span> | <span data-ttu-id="4f685-128">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4f685-128">2\_sw</span></span> | <span data-ttu-id="4f685-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f685-129">3\_0</span></span> | <span data-ttu-id="4f685-130">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4f685-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4f685-131">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="4f685-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="4f685-132">x</span><span class="sxs-lookup"><span data-stu-id="4f685-132">x</span></span>    | <span data-ttu-id="4f685-133">x</span><span class="sxs-lookup"><span data-stu-id="4f685-133">x</span></span>     |



 

<span data-ttu-id="4f685-134">Tutte le istruzioni dcl \_ usage devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="4f685-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="4f685-135">Esempi di dichiarazione</span><span class="sxs-lookup"><span data-stu-id="4f685-135">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4f685-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f685-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f685-137">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="4f685-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="4f685-138">[Esempio di antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="4f685-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
