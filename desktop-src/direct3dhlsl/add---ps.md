---
title: Add-PS
description: Aggiunge due vettori. | Add-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981122"
---
# <a name="add---ps"></a><span data-ttu-id="01397-104">Add-PS</span><span class="sxs-lookup"><span data-stu-id="01397-104">add - ps</span></span>

<span data-ttu-id="01397-105">Aggiunge due vettori.</span><span class="sxs-lookup"><span data-stu-id="01397-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="01397-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01397-106">Syntax</span></span>



| <span data-ttu-id="01397-107">aggiungere DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="01397-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="01397-108">dove</span><span class="sxs-lookup"><span data-stu-id="01397-108">where</span></span>

-   <span data-ttu-id="01397-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01397-109">dst is the destination register.</span></span>
-   <span data-ttu-id="01397-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="01397-110">src0 is a source register.</span></span>
-   <span data-ttu-id="01397-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="01397-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="01397-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="01397-112">Remarks</span></span>



| <span data-ttu-id="01397-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="01397-113">Pixel shader versions</span></span> | <span data-ttu-id="01397-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="01397-114">1\_1</span></span> | <span data-ttu-id="01397-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="01397-115">1\_2</span></span> | <span data-ttu-id="01397-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="01397-116">1\_3</span></span> | <span data-ttu-id="01397-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="01397-117">1\_4</span></span> | <span data-ttu-id="01397-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01397-118">2\_0</span></span> | <span data-ttu-id="01397-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="01397-119">2\_x</span></span> | <span data-ttu-id="01397-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01397-120">2\_sw</span></span> | <span data-ttu-id="01397-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01397-121">3\_0</span></span> | <span data-ttu-id="01397-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01397-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="01397-123">add</span><span class="sxs-lookup"><span data-stu-id="01397-123">add</span></span>                   | <span data-ttu-id="01397-124">x</span><span class="sxs-lookup"><span data-stu-id="01397-124">x</span></span>    | <span data-ttu-id="01397-125">x</span><span class="sxs-lookup"><span data-stu-id="01397-125">x</span></span>    | <span data-ttu-id="01397-126">x</span><span class="sxs-lookup"><span data-stu-id="01397-126">x</span></span>    | <span data-ttu-id="01397-127">x</span><span class="sxs-lookup"><span data-stu-id="01397-127">x</span></span>    | <span data-ttu-id="01397-128">x</span><span class="sxs-lookup"><span data-stu-id="01397-128">x</span></span>    | <span data-ttu-id="01397-129">x</span><span class="sxs-lookup"><span data-stu-id="01397-129">x</span></span>    | <span data-ttu-id="01397-130">x</span><span class="sxs-lookup"><span data-stu-id="01397-130">x</span></span>     | <span data-ttu-id="01397-131">x</span><span class="sxs-lookup"><span data-stu-id="01397-131">x</span></span>    | <span data-ttu-id="01397-132">x</span><span class="sxs-lookup"><span data-stu-id="01397-132">x</span></span>     |



 

<span data-ttu-id="01397-133">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="01397-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="01397-134">Informazioni istruzioni</span><span class="sxs-lookup"><span data-stu-id="01397-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="01397-135">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="01397-135">Minimum operating system</span></span> | <span data-ttu-id="01397-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="01397-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01397-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01397-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01397-138">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="01397-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




