---
title: Sub-PS
description: Sottrae le origini. | Sub-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761608"
---
# <a name="sub---ps"></a><span data-ttu-id="10f85-104">Sub-PS</span><span class="sxs-lookup"><span data-stu-id="10f85-104">sub - ps</span></span>

<span data-ttu-id="10f85-105">Sottrae le origini.</span><span class="sxs-lookup"><span data-stu-id="10f85-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f85-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10f85-106">Syntax</span></span>



| <span data-ttu-id="10f85-107">Sub DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="10f85-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="10f85-108">dove</span><span class="sxs-lookup"><span data-stu-id="10f85-108">where</span></span>

-   <span data-ttu-id="10f85-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="10f85-109">dst is the destination register.</span></span>
-   <span data-ttu-id="10f85-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="10f85-110">src0 is a source register.</span></span>
-   <span data-ttu-id="10f85-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="10f85-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f85-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="10f85-112">Remarks</span></span>



| <span data-ttu-id="10f85-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="10f85-113">Pixel shader versions</span></span> | <span data-ttu-id="10f85-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="10f85-114">1\_1</span></span> | <span data-ttu-id="10f85-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="10f85-115">1\_2</span></span> | <span data-ttu-id="10f85-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="10f85-116">1\_3</span></span> | <span data-ttu-id="10f85-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="10f85-117">1\_4</span></span> | <span data-ttu-id="10f85-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10f85-118">2\_0</span></span> | <span data-ttu-id="10f85-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="10f85-119">2\_x</span></span> | <span data-ttu-id="10f85-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="10f85-120">2\_sw</span></span> | <span data-ttu-id="10f85-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10f85-121">3\_0</span></span> | <span data-ttu-id="10f85-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="10f85-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="10f85-123">sub</span><span class="sxs-lookup"><span data-stu-id="10f85-123">sub</span></span>                   | <span data-ttu-id="10f85-124">x</span><span class="sxs-lookup"><span data-stu-id="10f85-124">x</span></span>    | <span data-ttu-id="10f85-125">x</span><span class="sxs-lookup"><span data-stu-id="10f85-125">x</span></span>    | <span data-ttu-id="10f85-126">x</span><span class="sxs-lookup"><span data-stu-id="10f85-126">x</span></span>    | <span data-ttu-id="10f85-127">x</span><span class="sxs-lookup"><span data-stu-id="10f85-127">x</span></span>    | <span data-ttu-id="10f85-128">x</span><span class="sxs-lookup"><span data-stu-id="10f85-128">x</span></span>    | <span data-ttu-id="10f85-129">x</span><span class="sxs-lookup"><span data-stu-id="10f85-129">x</span></span>    | <span data-ttu-id="10f85-130">x</span><span class="sxs-lookup"><span data-stu-id="10f85-130">x</span></span>     | <span data-ttu-id="10f85-131">x</span><span class="sxs-lookup"><span data-stu-id="10f85-131">x</span></span>    | <span data-ttu-id="10f85-132">x</span><span class="sxs-lookup"><span data-stu-id="10f85-132">x</span></span>     |



 

<span data-ttu-id="10f85-133">Questa istruzione esegue la sottrazione mostrata in questa formula.</span><span class="sxs-lookup"><span data-stu-id="10f85-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="10f85-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10f85-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f85-135">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="10f85-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




