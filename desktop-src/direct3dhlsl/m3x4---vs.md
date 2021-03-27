---
title: M3x4-vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981306"
---
# <a name="m3x4---vs"></a><span data-ttu-id="951f3-104">M3x4-vs</span><span class="sxs-lookup"><span data-stu-id="951f3-104">m3x4 - vs</span></span>

<span data-ttu-id="951f3-105">Moltiplica un vettore a 3 componenti per una matrice 3x4.</span><span class="sxs-lookup"><span data-stu-id="951f3-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="951f3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="951f3-106">Syntax</span></span>



| <span data-ttu-id="951f3-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="951f3-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="951f3-108">dove</span><span class="sxs-lookup"><span data-stu-id="951f3-108">where</span></span>

-   <span data-ttu-id="951f3-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="951f3-109">dst is the destination register.</span></span> <span data-ttu-id="951f3-110">Result è un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="951f3-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="951f3-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="951f3-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="951f3-112">src1 è un registro di origine che rappresenta una matrice 3x4, che corrisponde al primo di 4 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="951f3-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="951f3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="951f3-113">Remarks</span></span>



| <span data-ttu-id="951f3-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="951f3-114">Vertex shader versions</span></span> | <span data-ttu-id="951f3-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="951f3-115">1\_1</span></span> | <span data-ttu-id="951f3-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="951f3-116">2\_0</span></span> | <span data-ttu-id="951f3-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="951f3-117">2\_x</span></span> | <span data-ttu-id="951f3-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="951f3-118">2\_sw</span></span> | <span data-ttu-id="951f3-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="951f3-119">3\_0</span></span> | <span data-ttu-id="951f3-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="951f3-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="951f3-121">m3x4</span><span class="sxs-lookup"><span data-stu-id="951f3-121">m3x4</span></span>                   | <span data-ttu-id="951f3-122">x</span><span class="sxs-lookup"><span data-stu-id="951f3-122">x</span></span>    | <span data-ttu-id="951f3-123">x</span><span class="sxs-lookup"><span data-stu-id="951f3-123">x</span></span>    | <span data-ttu-id="951f3-124">x</span><span class="sxs-lookup"><span data-stu-id="951f3-124">x</span></span>    | <span data-ttu-id="951f3-125">x</span><span class="sxs-lookup"><span data-stu-id="951f3-125">x</span></span>     | <span data-ttu-id="951f3-126">x</span><span class="sxs-lookup"><span data-stu-id="951f3-126">x</span></span>    | <span data-ttu-id="951f3-127">x</span><span class="sxs-lookup"><span data-stu-id="951f3-127">x</span></span>     |



 

<span data-ttu-id="951f3-128">Per il registro di destinazione è richiesta la maschera xyzw (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="951f3-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="951f3-129">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="951f3-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="951f3-130">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="951f3-130">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



<span data-ttu-id="951f3-131">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="951f3-131">The input vector is in register src0.</span></span> <span data-ttu-id="951f3-132">La matrice di input 3x4 è in Register src1 e i successivi tre registri superiori, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="951f3-132">The input 3x4 matrix is in register src1 and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="951f3-133">Questa operazione viene in genere usata per trasformare un vettore di posizione in base a una matrice che ha un effetto proiettivo ma non applica alcuna traduzione.</span><span class="sxs-lookup"><span data-stu-id="951f3-133">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="951f3-134">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="951f3-134">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="951f3-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="951f3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="951f3-136">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="951f3-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




