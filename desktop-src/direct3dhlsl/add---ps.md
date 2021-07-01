---
title: add - ps
description: Aggiunge due vettori. | add - ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130090"
---
# <a name="add---ps"></a><span data-ttu-id="6c906-104">add - ps</span><span class="sxs-lookup"><span data-stu-id="6c906-104">add - ps</span></span>

<span data-ttu-id="6c906-105">Aggiunge due vettori.</span><span class="sxs-lookup"><span data-stu-id="6c906-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c906-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c906-106">Syntax</span></span>



| <span data-ttu-id="6c906-107">add dst, src0, src1</span><span class="sxs-lookup"><span data-stu-id="6c906-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="6c906-108">dove</span><span class="sxs-lookup"><span data-stu-id="6c906-108">where</span></span>

-   <span data-ttu-id="6c906-109">dst è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6c906-109">dst is the destination register.</span></span>
-   <span data-ttu-id="6c906-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6c906-110">src0 is a source register.</span></span>
-   <span data-ttu-id="6c906-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6c906-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c906-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c906-112">Remarks</span></span>



| <span data-ttu-id="6c906-113">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="6c906-113">Pixel shader versions</span></span> | <span data-ttu-id="6c906-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="6c906-114">1\_1</span></span> | <span data-ttu-id="6c906-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="6c906-115">1\_2</span></span> | <span data-ttu-id="6c906-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6c906-116">1\_3</span></span> | <span data-ttu-id="6c906-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="6c906-117">1\_4</span></span> | <span data-ttu-id="6c906-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6c906-118">2\_0</span></span> | <span data-ttu-id="6c906-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6c906-119">2\_x</span></span> | <span data-ttu-id="6c906-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6c906-120">2\_sw</span></span> | <span data-ttu-id="6c906-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6c906-121">3\_0</span></span> | <span data-ttu-id="6c906-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6c906-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6c906-123">add</span><span class="sxs-lookup"><span data-stu-id="6c906-123">add</span></span>                   | <span data-ttu-id="6c906-124">x</span><span class="sxs-lookup"><span data-stu-id="6c906-124">x</span></span>    | <span data-ttu-id="6c906-125">x</span><span class="sxs-lookup"><span data-stu-id="6c906-125">x</span></span>    | <span data-ttu-id="6c906-126">x</span><span class="sxs-lookup"><span data-stu-id="6c906-126">x</span></span>    | <span data-ttu-id="6c906-127">x</span><span class="sxs-lookup"><span data-stu-id="6c906-127">x</span></span>    | <span data-ttu-id="6c906-128">x</span><span class="sxs-lookup"><span data-stu-id="6c906-128">x</span></span>    | <span data-ttu-id="6c906-129">x</span><span class="sxs-lookup"><span data-stu-id="6c906-129">x</span></span>    | <span data-ttu-id="6c906-130">x</span><span class="sxs-lookup"><span data-stu-id="6c906-130">x</span></span>     | <span data-ttu-id="6c906-131">x</span><span class="sxs-lookup"><span data-stu-id="6c906-131">x</span></span>    | <span data-ttu-id="6c906-132">x</span><span class="sxs-lookup"><span data-stu-id="6c906-132">x</span></span>     |



 

<span data-ttu-id="6c906-133">Il frammento di codice seguente illustra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="6c906-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="6c906-134">Informazioni sulle istruzioni</span><span class="sxs-lookup"><span data-stu-id="6c906-134">Instruction Information</span></span>



|   <span data-ttu-id="6c906-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c906-135">Requirement</span></span>                       | <span data-ttu-id="6c906-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6c906-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="6c906-137">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="6c906-137">Minimum operating system</span></span> | <span data-ttu-id="6c906-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6c906-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6c906-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c906-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c906-140">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="6c906-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




