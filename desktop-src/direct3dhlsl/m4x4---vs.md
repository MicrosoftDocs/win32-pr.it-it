---
title: M4x4-vs
description: Moltiplica un vettore a 4 componenti per una matrice 4x4. | M4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234694"
---
# <a name="m4x4---vs"></a><span data-ttu-id="13487-104">M4x4-vs</span><span class="sxs-lookup"><span data-stu-id="13487-104">m4x4 - vs</span></span>

<span data-ttu-id="13487-105">Moltiplica un vettore a 4 componenti per una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="13487-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="13487-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13487-106">Syntax</span></span>



| <span data-ttu-id="13487-107">M4x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="13487-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="13487-108">dove</span><span class="sxs-lookup"><span data-stu-id="13487-108">where</span></span>

-   <span data-ttu-id="13487-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="13487-109">dst is the destination register.</span></span> <span data-ttu-id="13487-110">Result è un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="13487-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="13487-111">src0 è un registro di origine che rappresenta un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="13487-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="13487-112">src1 è un registro di origine che rappresenta una matrice 4x4, che corrisponde al primo di 4 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="13487-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="13487-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="13487-113">Remarks</span></span>



| <span data-ttu-id="13487-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="13487-114">Vertex shader versions</span></span> | <span data-ttu-id="13487-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="13487-115">1\_1</span></span> | <span data-ttu-id="13487-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13487-116">2\_0</span></span> | <span data-ttu-id="13487-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="13487-117">2\_x</span></span> | <span data-ttu-id="13487-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="13487-118">2\_sw</span></span> | <span data-ttu-id="13487-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13487-119">3\_0</span></span> | <span data-ttu-id="13487-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="13487-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="13487-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="13487-121">m4x4</span></span>                   | <span data-ttu-id="13487-122">x</span><span class="sxs-lookup"><span data-stu-id="13487-122">x</span></span>    | <span data-ttu-id="13487-123">x</span><span class="sxs-lookup"><span data-stu-id="13487-123">x</span></span>    | <span data-ttu-id="13487-124">x</span><span class="sxs-lookup"><span data-stu-id="13487-124">x</span></span>    | <span data-ttu-id="13487-125">x</span><span class="sxs-lookup"><span data-stu-id="13487-125">x</span></span>     | <span data-ttu-id="13487-126">x</span><span class="sxs-lookup"><span data-stu-id="13487-126">x</span></span>    | <span data-ttu-id="13487-127">x</span><span class="sxs-lookup"><span data-stu-id="13487-127">x</span></span>     |



 

<span data-ttu-id="13487-128">Per il registro di destinazione è richiesta la maschera xyzw (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="13487-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="13487-129">I modificatori negate e swizzle sono consentiti per src0, ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="13487-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="13487-130">I modificatori swizzle e negazioni non sono validi per il registro src0.</span><span class="sxs-lookup"><span data-stu-id="13487-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="13487-131">I registri dest e src0 non possono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="13487-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="13487-132">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="13487-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="13487-133">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="13487-133">The input vector is in register src0.</span></span> <span data-ttu-id="13487-134">La matrice di input 4x4 è in Register src1 e i successivi tre registri superiori, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="13487-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="13487-135">Questa operazione viene in genere usata per trasformare una posizione in base a una matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="13487-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="13487-136">Questa istruzione viene implementata come una serie di prodotti dot, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="13487-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="13487-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13487-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13487-138">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="13487-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




