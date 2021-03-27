---
title: CRS-vs
description: Calcola un prodotto incrociato usando la regola a destra. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352561"
---
# <a name="crs---vs"></a><span data-ttu-id="074b3-104">CRS-vs</span><span class="sxs-lookup"><span data-stu-id="074b3-104">crs - vs</span></span>

<span data-ttu-id="074b3-105">Calcola un prodotto incrociato usando la regola a destra.</span><span class="sxs-lookup"><span data-stu-id="074b3-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="074b3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="074b3-106">Syntax</span></span>



| <span data-ttu-id="074b3-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="074b3-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="074b3-108">dove</span><span class="sxs-lookup"><span data-stu-id="074b3-108">where</span></span>

-   <span data-ttu-id="074b3-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="074b3-109">dst is the destination register.</span></span>
-   <span data-ttu-id="074b3-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="074b3-110">src0 is a source register.</span></span>
-   <span data-ttu-id="074b3-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="074b3-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="074b3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="074b3-112">Remarks</span></span>



| <span data-ttu-id="074b3-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="074b3-113">Vertex shader versions</span></span> | <span data-ttu-id="074b3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="074b3-114">1\_1</span></span> | <span data-ttu-id="074b3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="074b3-115">2\_0</span></span> | <span data-ttu-id="074b3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="074b3-116">2\_x</span></span> | <span data-ttu-id="074b3-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="074b3-117">2\_sw</span></span> | <span data-ttu-id="074b3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="074b3-118">3\_0</span></span> | <span data-ttu-id="074b3-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="074b3-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="074b3-120">CRS</span><span class="sxs-lookup"><span data-stu-id="074b3-120">crs</span></span>                    |      | <span data-ttu-id="074b3-121">x</span><span class="sxs-lookup"><span data-stu-id="074b3-121">x</span></span>    | <span data-ttu-id="074b3-122">x</span><span class="sxs-lookup"><span data-stu-id="074b3-122">x</span></span>    | <span data-ttu-id="074b3-123">x</span><span class="sxs-lookup"><span data-stu-id="074b3-123">x</span></span>     | <span data-ttu-id="074b3-124">x</span><span class="sxs-lookup"><span data-stu-id="074b3-124">x</span></span>    | <span data-ttu-id="074b3-125">x</span><span class="sxs-lookup"><span data-stu-id="074b3-125">x</span></span>     |



 

<span data-ttu-id="074b3-126">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="074b3-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="074b3-127">Alcune restrizioni sull'utilizzo:</span><span class="sxs-lookup"><span data-stu-id="074b3-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="074b3-128">src0 non può essere lo stesso registro di dest.</span><span class="sxs-lookup"><span data-stu-id="074b3-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="074b3-129">src1 non può essere lo stesso registro di dest.</span><span class="sxs-lookup"><span data-stu-id="074b3-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="074b3-130">il valore di src0 non può essere swizzle diverso da quello predefinito swizzle (xyzw).</span><span class="sxs-lookup"><span data-stu-id="074b3-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="074b3-131">il valore di src1 non può essere swizzle diverso da quello predefinito swizzle (xyzw).</span><span class="sxs-lookup"><span data-stu-id="074b3-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="074b3-132">il dest deve avere esattamente una delle sette maschere seguenti:. x \| . y \| . z \| . XY \| . xz \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="074b3-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="074b3-133">il valore di dest deve essere un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="074b3-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="074b3-134">il nome di destinazione non deve corrispondere a src0 o src1</span><span class="sxs-lookup"><span data-stu-id="074b3-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="074b3-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="074b3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="074b3-136">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="074b3-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




