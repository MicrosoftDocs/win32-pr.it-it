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
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129708"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="5e873-103">semantica dcl \_ (sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="5e873-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="5e873-104">Dichiarare l'associazione tra l'output del vertex shader e pixel shader input.</span><span class="sxs-lookup"><span data-stu-id="5e873-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e873-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e873-105">Syntax</span></span>

<span data-ttu-id="5e873-106">dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="5e873-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span>



 

<span data-ttu-id="5e873-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="5e873-107">Where:</span></span>

-   <span data-ttu-id="5e873-108">\_semantica: identifica l'utilizzo dei dati previsto e può essere uno dei valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (senza il prefisso D3DDECLUSAGE). \_</span><span class="sxs-lookup"><span data-stu-id="5e873-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="5e873-109">Inoltre, è possibile aggiungere un indice integer alla semantica per distinguere i parametri che usano una semantica simile.</span><span class="sxs-lookup"><span data-stu-id="5e873-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="5e873-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] è un modificatore di istruzione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5e873-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="5e873-111">È supportato nelle istruzioni di utilizzo dcl che dichiarano i registri \_ di input e nelle istruzioni di ricerca trame.</span><span class="sxs-lookup"><span data-stu-id="5e873-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="5e873-112">Il centroide viene aggiunto senza spazio.</span><span class="sxs-lookup"><span data-stu-id="5e873-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="5e873-113">dst: registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5e873-113">dst: destination register.</span></span> <span data-ttu-id="5e873-114">Vedere [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="5e873-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="5e873-115">write mask: lo stesso registro di output può essere dichiarato più volte, ogni volta con una maschera di scrittura univoca (in modo che sia possibile applicare una semantica diversa \_ ai singoli componenti).</span><span class="sxs-lookup"><span data-stu-id="5e873-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="5e873-116">Tuttavia, la stessa semantica non può essere usata più volte in una dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="5e873-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="5e873-117">Ciò significa che i vettori devono essere quattro componenti o meno e non possono attraversare i limiti del registro a quattro componenti (registri di output singoli).</span><span class="sxs-lookup"><span data-stu-id="5e873-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="5e873-118">Quando viene \_ usata la semantica psize, deve avere una maschera di scrittura completa perché è considerata scalare.</span><span class="sxs-lookup"><span data-stu-id="5e873-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="5e873-119">Quando viene usata la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti \_ devono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="5e873-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e873-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e873-120">Remarks</span></span>



| <span data-ttu-id="5e873-121">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="5e873-121">Pixel shader versions</span></span> | <span data-ttu-id="5e873-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="5e873-122">1\_1</span></span> | <span data-ttu-id="5e873-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="5e873-123">1\_2</span></span> | <span data-ttu-id="5e873-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5e873-124">1\_3</span></span> | <span data-ttu-id="5e873-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="5e873-125">1\_4</span></span> | <span data-ttu-id="5e873-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e873-126">2\_0</span></span> | <span data-ttu-id="5e873-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5e873-127">2\_x</span></span> | <span data-ttu-id="5e873-128">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5e873-128">2\_sw</span></span> | <span data-ttu-id="5e873-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e873-129">3\_0</span></span> | <span data-ttu-id="5e873-130">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5e873-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5e873-131">Utilizzo di \_ dcl</span><span class="sxs-lookup"><span data-stu-id="5e873-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="5e873-132">x</span><span class="sxs-lookup"><span data-stu-id="5e873-132">x</span></span>    | <span data-ttu-id="5e873-133">x</span><span class="sxs-lookup"><span data-stu-id="5e873-133">x</span></span>     |



 

<span data-ttu-id="5e873-134">Tutte le istruzioni di \_ utilizzo dcl devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="5e873-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="5e873-135">Esempi di dichiarazione</span><span class="sxs-lookup"><span data-stu-id="5e873-135">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5e873-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e873-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e873-137">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="5e873-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="5e873-138">[Esempio di antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5e873-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
