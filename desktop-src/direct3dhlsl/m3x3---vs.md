---
title: M3X3-vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x3. | M3X3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401899"
---
# <a name="m3x3---vs"></a><span data-ttu-id="4f044-104">M3X3-vs</span><span class="sxs-lookup"><span data-stu-id="4f044-104">m3x3 - vs</span></span>

<span data-ttu-id="4f044-105">Moltiplica un vettore a 3 componenti per una matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="4f044-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f044-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f044-106">Syntax</span></span>



| <span data-ttu-id="4f044-107">M3X3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4f044-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="4f044-108">dove</span><span class="sxs-lookup"><span data-stu-id="4f044-108">where</span></span>

-   <span data-ttu-id="4f044-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4f044-109">dst is the destination register.</span></span> <span data-ttu-id="4f044-110">Result è un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="4f044-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="4f044-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="4f044-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="4f044-112">src1 è un registro di origine che rappresenta una matrice 3x3, che corrisponde al primo di 3 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="4f044-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f044-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f044-113">Remarks</span></span>



| <span data-ttu-id="4f044-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4f044-114">Vertex shader versions</span></span> | <span data-ttu-id="4f044-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="4f044-115">1\_1</span></span> | <span data-ttu-id="4f044-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f044-116">2\_0</span></span> | <span data-ttu-id="4f044-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4f044-117">2\_x</span></span> | <span data-ttu-id="4f044-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f044-118">2\_sw</span></span> | <span data-ttu-id="4f044-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f044-119">3\_0</span></span> | <span data-ttu-id="4f044-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4f044-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4f044-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="4f044-121">m3x3</span></span>                   | <span data-ttu-id="4f044-122">x</span><span class="sxs-lookup"><span data-stu-id="4f044-122">x</span></span>    | <span data-ttu-id="4f044-123">x</span><span class="sxs-lookup"><span data-stu-id="4f044-123">x</span></span>    | <span data-ttu-id="4f044-124">x</span><span class="sxs-lookup"><span data-stu-id="4f044-124">x</span></span>    | <span data-ttu-id="4f044-125">x</span><span class="sxs-lookup"><span data-stu-id="4f044-125">x</span></span>     | <span data-ttu-id="4f044-126">x</span><span class="sxs-lookup"><span data-stu-id="4f044-126">x</span></span>    | <span data-ttu-id="4f044-127">x</span><span class="sxs-lookup"><span data-stu-id="4f044-127">x</span></span>     |



 

<span data-ttu-id="4f044-128">La maschera XYZ è obbligatoria per il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4f044-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="4f044-129">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="4f044-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="4f044-130">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="4f044-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="4f044-131">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="4f044-131">The input vector is in register src0.</span></span> <span data-ttu-id="4f044-132">La matrice di input 3x3 si trova in Register src1 e i successivi due registri successivi, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f044-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="4f044-133">Viene generato un risultato 3D, lasciando l'altro elemento del registro di destinazione (dest. w) non interessato.</span><span class="sxs-lookup"><span data-stu-id="4f044-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="4f044-134">Questa operazione viene in genere usata per trasformare i vettori normali durante i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="4f044-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="4f044-135">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f044-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="4f044-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f044-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f044-137">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4f044-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




