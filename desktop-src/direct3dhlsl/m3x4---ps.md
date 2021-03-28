---
title: M3x4-PS
description: Moltiplica un vettore a 3 componenti per una matrice 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981959"
---
# <a name="m3x4---ps"></a><span data-ttu-id="a93dd-104">M3x4-PS</span><span class="sxs-lookup"><span data-stu-id="a93dd-104">m3x4 - ps</span></span>

<span data-ttu-id="a93dd-105">Moltiplica un vettore a 3 componenti per una matrice 3x4.</span><span class="sxs-lookup"><span data-stu-id="a93dd-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93dd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a93dd-106">Syntax</span></span>



| <span data-ttu-id="a93dd-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a93dd-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="a93dd-108">dove</span><span class="sxs-lookup"><span data-stu-id="a93dd-108">where</span></span>

-   <span data-ttu-id="a93dd-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a93dd-109">dst is the destination register.</span></span> <span data-ttu-id="a93dd-110">Result è un vettore a 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="a93dd-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="a93dd-111">src0 è un registro di origine che rappresenta un vettore a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="a93dd-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="a93dd-112">src1 è un registro di origine che rappresenta una matrice 3x4, che corrisponde al primo di 4 registri consecutivi.</span><span class="sxs-lookup"><span data-stu-id="a93dd-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="a93dd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a93dd-113">Remarks</span></span>



| <span data-ttu-id="a93dd-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a93dd-114">Pixel shader versions</span></span> | <span data-ttu-id="a93dd-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="a93dd-115">1\_1</span></span> | <span data-ttu-id="a93dd-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="a93dd-116">1\_2</span></span> | <span data-ttu-id="a93dd-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a93dd-117">1\_3</span></span> | <span data-ttu-id="a93dd-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="a93dd-118">1\_4</span></span> | <span data-ttu-id="a93dd-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a93dd-119">2\_0</span></span> | <span data-ttu-id="a93dd-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a93dd-120">2\_x</span></span> | <span data-ttu-id="a93dd-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a93dd-121">2\_sw</span></span> | <span data-ttu-id="a93dd-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a93dd-122">3\_0</span></span> | <span data-ttu-id="a93dd-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a93dd-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a93dd-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="a93dd-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="a93dd-125">x</span><span class="sxs-lookup"><span data-stu-id="a93dd-125">x</span></span>    | <span data-ttu-id="a93dd-126">x</span><span class="sxs-lookup"><span data-stu-id="a93dd-126">x</span></span>    | <span data-ttu-id="a93dd-127">x</span><span class="sxs-lookup"><span data-stu-id="a93dd-127">x</span></span>     | <span data-ttu-id="a93dd-128">x</span><span class="sxs-lookup"><span data-stu-id="a93dd-128">x</span></span>    | <span data-ttu-id="a93dd-129">x</span><span class="sxs-lookup"><span data-stu-id="a93dd-129">x</span></span>     |



 

<span data-ttu-id="a93dd-130">Per il registro di destinazione è richiesta la maschera xyzw (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a93dd-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="a93dd-131">I modificatori negate e swizzle sono consentiti per src0 ma non per src1.</span><span class="sxs-lookup"><span data-stu-id="a93dd-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="a93dd-132">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="a93dd-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="a93dd-133">Il vettore di input si trova in Register src0.</span><span class="sxs-lookup"><span data-stu-id="a93dd-133">The input vector is in register src0.</span></span> <span data-ttu-id="a93dd-134">La matrice di input 3x4 si trova nel registro src1 e i successivi due registri superiori, come illustrato nell'espansione riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="a93dd-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="a93dd-135">Questa operazione viene in genere usata per trasformare un vettore di posizione in base a una matrice che ha un effetto proiettivo ma non applica alcuna traduzione.</span><span class="sxs-lookup"><span data-stu-id="a93dd-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="a93dd-136">Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a93dd-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="a93dd-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a93dd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93dd-138">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a93dd-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




