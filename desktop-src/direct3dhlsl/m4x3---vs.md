---
title: m4x3-vs
description: Moltiplica un vettore a 4 componenti per una matrice 4x3. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981303"
---
# <a name="m4x3---vs"></a><span data-ttu-id="60897-104">m4x3-vs</span><span class="sxs-lookup"><span data-stu-id="60897-104">m4x3 - vs</span></span>

<span data-ttu-id="60897-105">Moltiplica un vettore a 4 componenti per una matrice 4x3.</span><span class="sxs-lookup"><span data-stu-id="60897-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="60897-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60897-106">Syntax</span></span>



| <span data-ttu-id="60897-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="60897-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="60897-108">dove</span><span class="sxs-lookup"><span data-stu-id="60897-108">where</span></span>

-   <span data-ttu-id="60897-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="60897-109">dst is the destination register.</span></span> <span data-ttu-id="60897-110">Result è un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="60897-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="60897-111">src0 è un registro di origine che rappresenta un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="60897-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="60897-112">src1 è un registro di origine che rappresenta una matrice 4x3, che corrisponde al primo di 3 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="60897-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="60897-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="60897-113">Remarks</span></span>



| <span data-ttu-id="60897-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="60897-114">Vertex shader versions</span></span> | <span data-ttu-id="60897-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="60897-115">1\_1</span></span> | <span data-ttu-id="60897-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60897-116">2\_0</span></span> | <span data-ttu-id="60897-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="60897-117">2\_x</span></span> | <span data-ttu-id="60897-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="60897-118">2\_sw</span></span> | <span data-ttu-id="60897-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60897-119">3\_0</span></span> | <span data-ttu-id="60897-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="60897-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="60897-121">m4x3</span><span class="sxs-lookup"><span data-stu-id="60897-121">m4x3</span></span>                   | <span data-ttu-id="60897-122">x</span><span class="sxs-lookup"><span data-stu-id="60897-122">x</span></span>    | <span data-ttu-id="60897-123">x</span><span class="sxs-lookup"><span data-stu-id="60897-123">x</span></span>    | <span data-ttu-id="60897-124">x</span><span class="sxs-lookup"><span data-stu-id="60897-124">x</span></span>    | <span data-ttu-id="60897-125">x</span><span class="sxs-lookup"><span data-stu-id="60897-125">x</span></span>     | <span data-ttu-id="60897-126">x</span><span class="sxs-lookup"><span data-stu-id="60897-126">x</span></span>    | <span data-ttu-id="60897-127">x</span><span class="sxs-lookup"><span data-stu-id="60897-127">x</span></span>     |



 

<span data-ttu-id="60897-128">La maschera XYZ è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="60897-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="60897-129">I modificatori negate e swizzle sono consentiti per src0, ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="60897-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="60897-130">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="60897-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



<span data-ttu-id="60897-131">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="60897-131">The input vector is in register src0.</span></span> <span data-ttu-id="60897-132">La matrice di input 4x3 si trova nel registro src1 e i successivi due registri superiori, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="60897-132">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="60897-133">Viene generato un risultato 3D, lasciando l'altro elemento del registro di destinazione (dest. w) non interessato.</span><span class="sxs-lookup"><span data-stu-id="60897-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="60897-134">Questa operazione viene in genere usata per trasformare un vettore di posizione in base a una matrice che non ha alcun effetto proiettivo, ad esempio in caso di trasformazioni dello spazio del modello.</span><span class="sxs-lookup"><span data-stu-id="60897-134">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="60897-135">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="60897-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="60897-136">I modificatori swizzle e negazioni non sono validi per il registro src1.</span><span class="sxs-lookup"><span data-stu-id="60897-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="60897-137">Il registro DST e src0 non possono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="60897-137">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60897-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60897-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60897-139">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="60897-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




