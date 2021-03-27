---
title: CRS-PS
description: Calcola un prodotto incrociato usando la regola a destra. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352566"
---
# <a name="crs---ps"></a><span data-ttu-id="667ee-104">CRS-PS</span><span class="sxs-lookup"><span data-stu-id="667ee-104">crs - ps</span></span>

<span data-ttu-id="667ee-105">Calcola un prodotto incrociato usando la regola a destra.</span><span class="sxs-lookup"><span data-stu-id="667ee-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="667ee-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="667ee-106">Syntax</span></span>



| <span data-ttu-id="667ee-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="667ee-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="667ee-108">dove</span><span class="sxs-lookup"><span data-stu-id="667ee-108">where</span></span>

-   <span data-ttu-id="667ee-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="667ee-109">dst is the destination register.</span></span>
-   <span data-ttu-id="667ee-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="667ee-110">src0 is a source register.</span></span>
-   <span data-ttu-id="667ee-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="667ee-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="667ee-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="667ee-112">Remarks</span></span>



| <span data-ttu-id="667ee-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="667ee-113">Pixel shader versions</span></span> | <span data-ttu-id="667ee-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="667ee-114">1\_1</span></span> | <span data-ttu-id="667ee-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="667ee-115">1\_2</span></span> | <span data-ttu-id="667ee-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="667ee-116">1\_3</span></span> | <span data-ttu-id="667ee-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="667ee-117">1\_4</span></span> | <span data-ttu-id="667ee-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="667ee-118">2\_0</span></span> | <span data-ttu-id="667ee-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="667ee-119">2\_x</span></span> | <span data-ttu-id="667ee-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="667ee-120">2\_sw</span></span> | <span data-ttu-id="667ee-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="667ee-121">3\_0</span></span> | <span data-ttu-id="667ee-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="667ee-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="667ee-123">CRS</span><span class="sxs-lookup"><span data-stu-id="667ee-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="667ee-124">x</span><span class="sxs-lookup"><span data-stu-id="667ee-124">x</span></span>    | <span data-ttu-id="667ee-125">x</span><span class="sxs-lookup"><span data-stu-id="667ee-125">x</span></span>    | <span data-ttu-id="667ee-126">x</span><span class="sxs-lookup"><span data-stu-id="667ee-126">x</span></span>     | <span data-ttu-id="667ee-127">x</span><span class="sxs-lookup"><span data-stu-id="667ee-127">x</span></span>    | <span data-ttu-id="667ee-128">x</span><span class="sxs-lookup"><span data-stu-id="667ee-128">x</span></span>     |



 

<span data-ttu-id="667ee-129">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="667ee-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="667ee-130">Alcune restrizioni sull'utilizzo:</span><span class="sxs-lookup"><span data-stu-id="667ee-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="667ee-131">src0 non può essere lo stesso registro di dest.</span><span class="sxs-lookup"><span data-stu-id="667ee-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="667ee-132">src1 non può essere lo stesso registro di dest.</span><span class="sxs-lookup"><span data-stu-id="667ee-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="667ee-133">il valore di src0 non può essere swizzle diverso da quello predefinito swizzle (xyzw).</span><span class="sxs-lookup"><span data-stu-id="667ee-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="667ee-134">il valore di src1 non può essere swizzle diverso da quello predefinito swizzle (xyzw).</span><span class="sxs-lookup"><span data-stu-id="667ee-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="667ee-135">il dest deve avere esattamente una delle sette maschere seguenti:. x \| . y \| . z \| . XY \| . xz \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="667ee-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="667ee-136">il valore di dest deve essere un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="667ee-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="667ee-137">il nome di destinazione non deve corrispondere a src0 o src1</span><span class="sxs-lookup"><span data-stu-id="667ee-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="667ee-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="667ee-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="667ee-139">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="667ee-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




