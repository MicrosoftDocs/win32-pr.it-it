---
title: DP4-PS
description: Calcola il prodotto del punto a quattro componenti dei registri di origine. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058524"
---
# <a name="dp4---ps"></a><span data-ttu-id="27310-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="27310-104">dp4 - ps</span></span>

<span data-ttu-id="27310-105">Calcola il prodotto del punto a quattro componenti dei registri di origine.</span><span class="sxs-lookup"><span data-stu-id="27310-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="27310-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27310-106">Syntax</span></span>



| <span data-ttu-id="27310-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="27310-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="27310-108">dove</span><span class="sxs-lookup"><span data-stu-id="27310-108">where</span></span>

-   <span data-ttu-id="27310-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27310-109">dst is the destination register.</span></span>
-   <span data-ttu-id="27310-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="27310-110">src0 is a source register.</span></span>
-   <span data-ttu-id="27310-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="27310-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="27310-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="27310-112">Remarks</span></span>



| <span data-ttu-id="27310-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="27310-113">Pixel shader versions</span></span> | <span data-ttu-id="27310-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="27310-114">1\_1</span></span> | <span data-ttu-id="27310-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="27310-115">1\_2</span></span> | <span data-ttu-id="27310-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="27310-116">1\_3</span></span> | <span data-ttu-id="27310-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="27310-117">1\_4</span></span> | <span data-ttu-id="27310-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27310-118">2\_0</span></span> | <span data-ttu-id="27310-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27310-119">2\_x</span></span> | <span data-ttu-id="27310-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="27310-120">2\_sw</span></span> | <span data-ttu-id="27310-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27310-121">3\_0</span></span> | <span data-ttu-id="27310-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="27310-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="27310-123">DP4</span><span class="sxs-lookup"><span data-stu-id="27310-123">dp4</span></span>                   |      | <span data-ttu-id="27310-124">x</span><span class="sxs-lookup"><span data-stu-id="27310-124">x</span></span>    | <span data-ttu-id="27310-125">x</span><span class="sxs-lookup"><span data-stu-id="27310-125">x</span></span>    | <span data-ttu-id="27310-126">x</span><span class="sxs-lookup"><span data-stu-id="27310-126">x</span></span>    | <span data-ttu-id="27310-127">x</span><span class="sxs-lookup"><span data-stu-id="27310-127">x</span></span>    | <span data-ttu-id="27310-128">x</span><span class="sxs-lookup"><span data-stu-id="27310-128">x</span></span>    | <span data-ttu-id="27310-129">x</span><span class="sxs-lookup"><span data-stu-id="27310-129">x</span></span>     | <span data-ttu-id="27310-130">x</span><span class="sxs-lookup"><span data-stu-id="27310-130">x</span></span>    | <span data-ttu-id="27310-131">x</span><span class="sxs-lookup"><span data-stu-id="27310-131">x</span></span>     |



 

<span data-ttu-id="27310-132">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="27310-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="27310-133">Limitazioni per PS \_ 1 \_ 2 e PS \_ 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="27310-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="27310-134">Ogni shader può utilizzare fino a un massimo di quattro istruzioni DP4.</span><span class="sxs-lookup"><span data-stu-id="27310-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="27310-135">Ogni istruzione DP4 viene conteggiata come due istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="27310-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="27310-136">Limitazioni per le \_ versioni 1 X:</span><span class="sxs-lookup"><span data-stu-id="27310-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="27310-137">Questa istruzione non può essere rilasciata perché DP4 viene eseguito sia nella pipeline vettoriale che in quella alfa.</span><span class="sxs-lookup"><span data-stu-id="27310-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27310-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27310-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27310-139">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="27310-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




