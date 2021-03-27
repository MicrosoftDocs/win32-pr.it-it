---
title: MAD-PS
description: Moltiplicare e aggiungere istruzioni. Imposta il registro di destinazione su (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398258"
---
# <a name="mad---ps"></a><span data-ttu-id="34e05-104">MAD-PS</span><span class="sxs-lookup"><span data-stu-id="34e05-104">mad - ps</span></span>

<span data-ttu-id="34e05-105">Moltiplicare e aggiungere istruzioni.</span><span class="sxs-lookup"><span data-stu-id="34e05-105">Multiply and add instruction.</span></span> <span data-ttu-id="34e05-106">Imposta il registro di destinazione su (src0 \* src1) + src2.</span><span class="sxs-lookup"><span data-stu-id="34e05-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e05-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34e05-107">Syntax</span></span>



| <span data-ttu-id="34e05-108">MAD DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="34e05-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="34e05-109">dove</span><span class="sxs-lookup"><span data-stu-id="34e05-109">where</span></span>

-   <span data-ttu-id="34e05-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="34e05-110">dst is the destination register.</span></span>
-   <span data-ttu-id="34e05-111">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="34e05-111">src0 is a source register.</span></span>
-   <span data-ttu-id="34e05-112">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="34e05-112">src1 is a source register.</span></span>
-   <span data-ttu-id="34e05-113">src2 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="34e05-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e05-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="34e05-114">Remarks</span></span>



| <span data-ttu-id="34e05-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="34e05-115">Pixel shader versions</span></span> | <span data-ttu-id="34e05-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="34e05-116">1\_1</span></span> | <span data-ttu-id="34e05-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="34e05-117">1\_2</span></span> | <span data-ttu-id="34e05-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34e05-118">1\_3</span></span> | <span data-ttu-id="34e05-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="34e05-119">1\_4</span></span> | <span data-ttu-id="34e05-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34e05-120">2\_0</span></span> | <span data-ttu-id="34e05-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="34e05-121">2\_x</span></span> | <span data-ttu-id="34e05-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34e05-122">2\_sw</span></span> | <span data-ttu-id="34e05-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34e05-123">3\_0</span></span> | <span data-ttu-id="34e05-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34e05-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="34e05-125">pazzo</span><span class="sxs-lookup"><span data-stu-id="34e05-125">mad</span></span>                   | <span data-ttu-id="34e05-126">x</span><span class="sxs-lookup"><span data-stu-id="34e05-126">x</span></span>    | <span data-ttu-id="34e05-127">x</span><span class="sxs-lookup"><span data-stu-id="34e05-127">x</span></span>    | <span data-ttu-id="34e05-128">x</span><span class="sxs-lookup"><span data-stu-id="34e05-128">x</span></span>    | <span data-ttu-id="34e05-129">x</span><span class="sxs-lookup"><span data-stu-id="34e05-129">x</span></span>    | <span data-ttu-id="34e05-130">x</span><span class="sxs-lookup"><span data-stu-id="34e05-130">x</span></span>    | <span data-ttu-id="34e05-131">x</span><span class="sxs-lookup"><span data-stu-id="34e05-131">x</span></span>    | <span data-ttu-id="34e05-132">x</span><span class="sxs-lookup"><span data-stu-id="34e05-132">x</span></span>     | <span data-ttu-id="34e05-133">x</span><span class="sxs-lookup"><span data-stu-id="34e05-133">x</span></span>    | <span data-ttu-id="34e05-134">x</span><span class="sxs-lookup"><span data-stu-id="34e05-134">x</span></span>     |



 

<span data-ttu-id="34e05-135">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="34e05-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="34e05-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34e05-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34e05-137">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="34e05-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




