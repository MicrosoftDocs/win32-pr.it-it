---
title: ABS-PS
description: Calcola il valore assoluto. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352156"
---
# <a name="abs---ps"></a><span data-ttu-id="643ab-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="643ab-104">abs - ps</span></span>

<span data-ttu-id="643ab-105">Calcola il valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="643ab-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="643ab-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="643ab-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="643ab-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="643ab-107">abs dst, src</span></span> |



 

<span data-ttu-id="643ab-108">dove</span><span class="sxs-lookup"><span data-stu-id="643ab-108">where</span></span>

-   <span data-ttu-id="643ab-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="643ab-109">dst is the destination register.</span></span>
-   <span data-ttu-id="643ab-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="643ab-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="643ab-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="643ab-111">Remarks</span></span>



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="643ab-112">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="643ab-112">Pixel shader versions</span></span> | <span data-ttu-id="643ab-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="643ab-113">1\_1</span></span> | <span data-ttu-id="643ab-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="643ab-114">1\_2</span></span> | <span data-ttu-id="643ab-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="643ab-115">1\_3</span></span> | <span data-ttu-id="643ab-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="643ab-116">1\_4</span></span> | <span data-ttu-id="643ab-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="643ab-117">2\_0</span></span> | <span data-ttu-id="643ab-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="643ab-118">2\_x</span></span> | <span data-ttu-id="643ab-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="643ab-119">2\_sw</span></span> | <span data-ttu-id="643ab-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="643ab-120">3\_0</span></span> | <span data-ttu-id="643ab-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="643ab-121">3\_sw</span></span> |
| <span data-ttu-id="643ab-122">abs</span><span class="sxs-lookup"><span data-stu-id="643ab-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="643ab-123">x</span><span class="sxs-lookup"><span data-stu-id="643ab-123">x</span></span>    | <span data-ttu-id="643ab-124">x</span><span class="sxs-lookup"><span data-stu-id="643ab-124">x</span></span>    | <span data-ttu-id="643ab-125">x</span><span class="sxs-lookup"><span data-stu-id="643ab-125">x</span></span>     | <span data-ttu-id="643ab-126">x</span><span class="sxs-lookup"><span data-stu-id="643ab-126">x</span></span>    | <span data-ttu-id="643ab-127">x</span><span class="sxs-lookup"><span data-stu-id="643ab-127">x</span></span>     |



 

<span data-ttu-id="643ab-128">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="643ab-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="643ab-129">Informazioni istruzioni</span><span class="sxs-lookup"><span data-stu-id="643ab-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="643ab-130">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="643ab-130">Minimum operating system</span></span> | <span data-ttu-id="643ab-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="643ab-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="643ab-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="643ab-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="643ab-133">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="643ab-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




