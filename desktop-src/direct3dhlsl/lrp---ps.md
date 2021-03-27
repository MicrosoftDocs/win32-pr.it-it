---
title: LRP-PS
description: Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058568"
---
# <a name="lrp---ps"></a><span data-ttu-id="7fc0d-104">LRP-PS</span><span class="sxs-lookup"><span data-stu-id="7fc0d-104">lrp - ps</span></span>

<span data-ttu-id="7fc0d-105">Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc0d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fc0d-106">Syntax</span></span>



| <span data-ttu-id="7fc0d-107">LRP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="7fc0d-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="7fc0d-108">dove</span><span class="sxs-lookup"><span data-stu-id="7fc0d-108">where</span></span>

-   <span data-ttu-id="7fc0d-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7fc0d-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="7fc0d-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-111">src1 is a source register.</span></span>
-   <span data-ttu-id="7fc0d-112">src2 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fc0d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fc0d-113">Remarks</span></span>



| <span data-ttu-id="7fc0d-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="7fc0d-114">Pixel shader versions</span></span> | <span data-ttu-id="7fc0d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7fc0d-115">1\_1</span></span> | <span data-ttu-id="7fc0d-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="7fc0d-116">1\_2</span></span> | <span data-ttu-id="7fc0d-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7fc0d-117">1\_3</span></span> | <span data-ttu-id="7fc0d-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="7fc0d-118">1\_4</span></span> | <span data-ttu-id="7fc0d-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7fc0d-119">2\_0</span></span> | <span data-ttu-id="7fc0d-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-120">2\_x</span></span> | <span data-ttu-id="7fc0d-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7fc0d-121">2\_sw</span></span> | <span data-ttu-id="7fc0d-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7fc0d-122">3\_0</span></span> | <span data-ttu-id="7fc0d-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7fc0d-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7fc0d-124">LRP</span><span class="sxs-lookup"><span data-stu-id="7fc0d-124">lrp</span></span>                   | <span data-ttu-id="7fc0d-125">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-125">x</span></span>    | <span data-ttu-id="7fc0d-126">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-126">x</span></span>    | <span data-ttu-id="7fc0d-127">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-127">x</span></span>    | <span data-ttu-id="7fc0d-128">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-128">x</span></span>    | <span data-ttu-id="7fc0d-129">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-129">x</span></span>    | <span data-ttu-id="7fc0d-130">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-130">x</span></span>    | <span data-ttu-id="7fc0d-131">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-131">x</span></span>     | <span data-ttu-id="7fc0d-132">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-132">x</span></span>    | <span data-ttu-id="7fc0d-133">x</span><span class="sxs-lookup"><span data-stu-id="7fc0d-133">x</span></span>     |



 

<span data-ttu-id="7fc0d-134">Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="7fc0d-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fc0d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc0d-136">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="7fc0d-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




