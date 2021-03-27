---
title: m4x3-PS
description: Moltiplica un vettore a 4 componenti per una matrice 4x3. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981935"
---
# <a name="m4x3---ps"></a><span data-ttu-id="55b8c-104">m4x3-PS</span><span class="sxs-lookup"><span data-stu-id="55b8c-104">m4x3 - ps</span></span>

<span data-ttu-id="55b8c-105">Moltiplica un vettore a 4 componenti per una matrice 4x3.</span><span class="sxs-lookup"><span data-stu-id="55b8c-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b8c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55b8c-106">Syntax</span></span>



| <span data-ttu-id="55b8c-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="55b8c-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="55b8c-108">dove</span><span class="sxs-lookup"><span data-stu-id="55b8c-108">where</span></span>

-   <span data-ttu-id="55b8c-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55b8c-109">dst is the destination register.</span></span> <span data-ttu-id="55b8c-110">Result è un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="55b8c-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="55b8c-111">src0 è un registro di origine che rappresenta un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="55b8c-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="55b8c-112">src1 è un registro di origine che rappresenta una matrice 4x3, che corrisponde al primo di 3 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="55b8c-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b8c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="55b8c-113">Remarks</span></span>



| <span data-ttu-id="55b8c-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="55b8c-114">Pixel shader versions</span></span> | <span data-ttu-id="55b8c-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="55b8c-115">1\_1</span></span> | <span data-ttu-id="55b8c-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="55b8c-116">1\_2</span></span> | <span data-ttu-id="55b8c-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="55b8c-117">1\_3</span></span> | <span data-ttu-id="55b8c-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="55b8c-118">1\_4</span></span> | <span data-ttu-id="55b8c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55b8c-119">2\_0</span></span> | <span data-ttu-id="55b8c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="55b8c-120">2\_x</span></span> | <span data-ttu-id="55b8c-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55b8c-121">2\_sw</span></span> | <span data-ttu-id="55b8c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55b8c-122">3\_0</span></span> | <span data-ttu-id="55b8c-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55b8c-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="55b8c-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="55b8c-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="55b8c-125">x</span><span class="sxs-lookup"><span data-stu-id="55b8c-125">x</span></span>    | <span data-ttu-id="55b8c-126">x</span><span class="sxs-lookup"><span data-stu-id="55b8c-126">x</span></span>    | <span data-ttu-id="55b8c-127">x</span><span class="sxs-lookup"><span data-stu-id="55b8c-127">x</span></span>     | <span data-ttu-id="55b8c-128">x</span><span class="sxs-lookup"><span data-stu-id="55b8c-128">x</span></span>    | <span data-ttu-id="55b8c-129">x</span><span class="sxs-lookup"><span data-stu-id="55b8c-129">x</span></span>     |



 

<span data-ttu-id="55b8c-130">La maschera XYZ è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55b8c-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="55b8c-131">I modificatori negate e swizzle sono consentiti per src0, ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="55b8c-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="55b8c-132">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="55b8c-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="55b8c-133">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="55b8c-133">The input vector is in register src0.</span></span> <span data-ttu-id="55b8c-134">La matrice di input 4x3 si trova nel registro src1 e i successivi due registri superiori, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="55b8c-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="55b8c-135">Viene generato un risultato 3D, lasciando l'altro elemento del registro di destinazione (dest. w) non interessato.</span><span class="sxs-lookup"><span data-stu-id="55b8c-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="55b8c-136">Questa operazione viene in genere usata per trasformare un vettore di posizione in base a una matrice che non ha alcun effetto proiettivo, ad esempio in caso di trasformazioni dello spazio del modello.</span><span class="sxs-lookup"><span data-stu-id="55b8c-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="55b8c-137">Questa istruzione viene implementata come un set di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="55b8c-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="55b8c-138">I modificatori swizzle e negazioni non sono validi per il registro src1.</span><span class="sxs-lookup"><span data-stu-id="55b8c-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="55b8c-139">Il registro DST e src0 non possono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="55b8c-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55b8c-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55b8c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b8c-141">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="55b8c-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




