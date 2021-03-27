---
title: M3X2-vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x2. | M3X2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234697"
---
# <a name="m3x2---vs"></a><span data-ttu-id="38f57-104">M3X2-vs</span><span class="sxs-lookup"><span data-stu-id="38f57-104">m3x2 - vs</span></span>

<span data-ttu-id="38f57-105">Moltiplica un vettore a 3 componenti per una matrice 3x2.</span><span class="sxs-lookup"><span data-stu-id="38f57-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f57-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38f57-106">Syntax</span></span>



| <span data-ttu-id="38f57-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="38f57-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="38f57-108">dove</span><span class="sxs-lookup"><span data-stu-id="38f57-108">where</span></span>

-   <span data-ttu-id="38f57-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38f57-109">dst is the destination register.</span></span> <span data-ttu-id="38f57-110">Il risultato è un vettore a 2 componenti.</span><span class="sxs-lookup"><span data-stu-id="38f57-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="38f57-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="38f57-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="38f57-112">src1 è un registro di origine che rappresenta una matrice 3x2, che corrisponde al primo di due registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="38f57-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f57-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="38f57-113">Remarks</span></span>



| <span data-ttu-id="38f57-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="38f57-114">Vertex shader versions</span></span> | <span data-ttu-id="38f57-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="38f57-115">1\_1</span></span> | <span data-ttu-id="38f57-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38f57-116">2\_0</span></span> | <span data-ttu-id="38f57-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="38f57-117">2\_x</span></span> | <span data-ttu-id="38f57-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="38f57-118">2\_sw</span></span> | <span data-ttu-id="38f57-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38f57-119">3\_0</span></span> | <span data-ttu-id="38f57-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="38f57-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="38f57-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="38f57-121">m3x2</span></span>                   | <span data-ttu-id="38f57-122">x</span><span class="sxs-lookup"><span data-stu-id="38f57-122">x</span></span>    | <span data-ttu-id="38f57-123">x</span><span class="sxs-lookup"><span data-stu-id="38f57-123">x</span></span>    | <span data-ttu-id="38f57-124">x</span><span class="sxs-lookup"><span data-stu-id="38f57-124">x</span></span>    | <span data-ttu-id="38f57-125">x</span><span class="sxs-lookup"><span data-stu-id="38f57-125">x</span></span>     | <span data-ttu-id="38f57-126">x</span><span class="sxs-lookup"><span data-stu-id="38f57-126">x</span></span>    | <span data-ttu-id="38f57-127">x</span><span class="sxs-lookup"><span data-stu-id="38f57-127">x</span></span>     |



 

<span data-ttu-id="38f57-128">La maschera XY è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38f57-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="38f57-129">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="38f57-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="38f57-130">Le equazioni seguenti illustrano il funzionamento dell'istruzione:</span><span class="sxs-lookup"><span data-stu-id="38f57-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="38f57-131">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="38f57-131">The input vector is in register src0.</span></span> <span data-ttu-id="38f57-132">La matrice di input 3x2 si trova in Register src1 e il successivo registro superiore nello stesso file di registro, come illustrato nella seguente espansione.</span><span class="sxs-lookup"><span data-stu-id="38f57-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="38f57-133">Viene generato un risultato 2D, lasciando inalterati gli altri elementi del registro di destinazione (dest. z e dest. w).</span><span class="sxs-lookup"><span data-stu-id="38f57-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="38f57-134">Questa operazione viene comunemente utilizzata per le trasformazioni 2D.</span><span class="sxs-lookup"><span data-stu-id="38f57-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="38f57-135">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="38f57-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="38f57-136">I modificatori swizzle e negazioni non sono validi per il registro src1.</span><span class="sxs-lookup"><span data-stu-id="38f57-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="38f57-137">Il registro dest e src0, o uno qualsiasi dei registri src1 + i, non può essere lo stesso.</span><span class="sxs-lookup"><span data-stu-id="38f57-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38f57-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38f57-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f57-139">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="38f57-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




