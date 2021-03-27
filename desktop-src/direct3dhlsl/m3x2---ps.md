---
title: M3X2-PS
description: Moltiplica un vettore a 3 componenti per una matrice 3x2. | M3X2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982013"
---
# <a name="m3x2---ps"></a><span data-ttu-id="28e9a-104">M3X2-PS</span><span class="sxs-lookup"><span data-stu-id="28e9a-104">m3x2 - ps</span></span>

<span data-ttu-id="28e9a-105">Moltiplica un vettore a 3 componenti per una matrice 3x2.</span><span class="sxs-lookup"><span data-stu-id="28e9a-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e9a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28e9a-106">Syntax</span></span>



| <span data-ttu-id="28e9a-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="28e9a-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="28e9a-108">dove</span><span class="sxs-lookup"><span data-stu-id="28e9a-108">where</span></span>

-   <span data-ttu-id="28e9a-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28e9a-109">dst is the destination register.</span></span> <span data-ttu-id="28e9a-110">Il risultato è un vettore a 2 componenti.</span><span class="sxs-lookup"><span data-stu-id="28e9a-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="28e9a-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="28e9a-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="28e9a-112">src1 è un registro di origine che rappresenta una matrice 3x2, che corrisponde al primo di due registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="28e9a-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e9a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="28e9a-113">Remarks</span></span>



| <span data-ttu-id="28e9a-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="28e9a-114">Pixel shader versions</span></span> | <span data-ttu-id="28e9a-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="28e9a-115">1\_1</span></span> | <span data-ttu-id="28e9a-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="28e9a-116">1\_2</span></span> | <span data-ttu-id="28e9a-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="28e9a-117">1\_3</span></span> | <span data-ttu-id="28e9a-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="28e9a-118">1\_4</span></span> | <span data-ttu-id="28e9a-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28e9a-119">2\_0</span></span> | <span data-ttu-id="28e9a-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28e9a-120">2\_x</span></span> | <span data-ttu-id="28e9a-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28e9a-121">2\_sw</span></span> | <span data-ttu-id="28e9a-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28e9a-122">3\_0</span></span> | <span data-ttu-id="28e9a-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28e9a-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="28e9a-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="28e9a-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="28e9a-125">x</span><span class="sxs-lookup"><span data-stu-id="28e9a-125">x</span></span>    | <span data-ttu-id="28e9a-126">x</span><span class="sxs-lookup"><span data-stu-id="28e9a-126">x</span></span>    | <span data-ttu-id="28e9a-127">x</span><span class="sxs-lookup"><span data-stu-id="28e9a-127">x</span></span>     | <span data-ttu-id="28e9a-128">x</span><span class="sxs-lookup"><span data-stu-id="28e9a-128">x</span></span>    | <span data-ttu-id="28e9a-129">x</span><span class="sxs-lookup"><span data-stu-id="28e9a-129">x</span></span>     |



 

<span data-ttu-id="28e9a-130">La maschera XY è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28e9a-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="28e9a-131">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="28e9a-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="28e9a-132">Le equazioni seguenti illustrano il funzionamento dell'istruzione:</span><span class="sxs-lookup"><span data-stu-id="28e9a-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="28e9a-133">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="28e9a-133">The input vector is in register src0.</span></span> <span data-ttu-id="28e9a-134">La matrice di input 3x2 si trova in Register src1 e il successivo registro superiore nello stesso file di registro, come illustrato nella seguente espansione.</span><span class="sxs-lookup"><span data-stu-id="28e9a-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="28e9a-135">Viene generato un risultato 2D, lasciando inalterati gli altri elementi del registro di destinazione (dest. z e dest. w).</span><span class="sxs-lookup"><span data-stu-id="28e9a-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="28e9a-136">Questa operazione viene comunemente utilizzata per le trasformazioni 2D.</span><span class="sxs-lookup"><span data-stu-id="28e9a-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="28e9a-137">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="28e9a-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="28e9a-138">I modificatori swizzle e negazioni non sono validi per il registro src1.</span><span class="sxs-lookup"><span data-stu-id="28e9a-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="28e9a-139">Il registro DST e src0, o uno qualsiasi dei registri src1 + i, non può essere lo stesso.</span><span class="sxs-lookup"><span data-stu-id="28e9a-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28e9a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28e9a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28e9a-141">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="28e9a-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




