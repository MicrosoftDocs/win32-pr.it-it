---
title: M3X3-PS
description: Moltiplica un vettore a 3 componenti per una matrice 3x3. | M3X3-PS
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ac72acd2133c8b34393bdd1ab7de8aec1df4db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981911"
---
# <a name="m3x3---ps"></a><span data-ttu-id="3ea22-104">M3X3-PS</span><span class="sxs-lookup"><span data-stu-id="3ea22-104">m3x3 - ps</span></span>

<span data-ttu-id="3ea22-105">Moltiplica un vettore a 3 componenti per una matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="3ea22-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea22-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ea22-106">Syntax</span></span>



| <span data-ttu-id="3ea22-107">M3X3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3ea22-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="3ea22-108">dove</span><span class="sxs-lookup"><span data-stu-id="3ea22-108">where</span></span>

-   <span data-ttu-id="3ea22-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3ea22-109">dst is the destination register.</span></span> <span data-ttu-id="3ea22-110">Result è un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="3ea22-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="3ea22-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="3ea22-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="3ea22-112">src1 è un registro di origine che rappresenta una matrice 3x3, che corrisponde al primo di 3 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="3ea22-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ea22-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ea22-113">Remarks</span></span>



| <span data-ttu-id="3ea22-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3ea22-114">Pixel shader versions</span></span> | <span data-ttu-id="3ea22-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="3ea22-115">1\_1</span></span> | <span data-ttu-id="3ea22-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="3ea22-116">1\_2</span></span> | <span data-ttu-id="3ea22-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3ea22-117">1\_3</span></span> | <span data-ttu-id="3ea22-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="3ea22-118">1\_4</span></span> | <span data-ttu-id="3ea22-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3ea22-119">2\_0</span></span> | <span data-ttu-id="3ea22-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3ea22-120">2\_x</span></span> | <span data-ttu-id="3ea22-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3ea22-121">2\_sw</span></span> | <span data-ttu-id="3ea22-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3ea22-122">3\_0</span></span> | <span data-ttu-id="3ea22-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3ea22-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3ea22-124">m3x3</span><span class="sxs-lookup"><span data-stu-id="3ea22-124">m3x3</span></span>                  |      |      |      |      | <span data-ttu-id="3ea22-125">x</span><span class="sxs-lookup"><span data-stu-id="3ea22-125">x</span></span>    | <span data-ttu-id="3ea22-126">x</span><span class="sxs-lookup"><span data-stu-id="3ea22-126">x</span></span>    | <span data-ttu-id="3ea22-127">x</span><span class="sxs-lookup"><span data-stu-id="3ea22-127">x</span></span>     | <span data-ttu-id="3ea22-128">x</span><span class="sxs-lookup"><span data-stu-id="3ea22-128">x</span></span>    | <span data-ttu-id="3ea22-129">x</span><span class="sxs-lookup"><span data-stu-id="3ea22-129">x</span></span>     |



 

<span data-ttu-id="3ea22-130">La maschera XYZ è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3ea22-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="3ea22-131">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="3ea22-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="3ea22-132">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="3ea22-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="3ea22-133">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="3ea22-133">The input vector is in register src0.</span></span> <span data-ttu-id="3ea22-134">La matrice di input 3x3 si trova in Register src1 e i successivi due registri successivi, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="3ea22-134">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="3ea22-135">Viene generato un risultato 3D, lasciando l'altro elemento del registro di destinazione (dest. w) non interessato.</span><span class="sxs-lookup"><span data-stu-id="3ea22-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="3ea22-136">Questa operazione viene in genere usata per trasformare i vettori normali durante i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="3ea22-136">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="3ea22-137">Questa istruzione viene implementata come un set di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3ea22-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="3ea22-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ea22-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea22-139">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3ea22-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




