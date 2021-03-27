---
title: max-PS
description: Calcola il numero massimo di origini. | max-PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982070"
---
# <a name="max---ps"></a><span data-ttu-id="4a1bb-104">max-PS</span><span class="sxs-lookup"><span data-stu-id="4a1bb-104">max - ps</span></span>

<span data-ttu-id="4a1bb-105">Calcola il numero massimo di origini.</span><span class="sxs-lookup"><span data-stu-id="4a1bb-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1bb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a1bb-106">Syntax</span></span>



| <span data-ttu-id="4a1bb-107">Max DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4a1bb-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="4a1bb-108">dove</span><span class="sxs-lookup"><span data-stu-id="4a1bb-108">where</span></span>

-   <span data-ttu-id="4a1bb-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a1bb-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4a1bb-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4a1bb-110">src0 is a source register.</span></span>
-   <span data-ttu-id="4a1bb-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4a1bb-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a1bb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a1bb-112">Remarks</span></span>



| <span data-ttu-id="4a1bb-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="4a1bb-113">Pixel shader versions</span></span> | <span data-ttu-id="4a1bb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4a1bb-114">1\_1</span></span> | <span data-ttu-id="4a1bb-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="4a1bb-115">1\_2</span></span> | <span data-ttu-id="4a1bb-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4a1bb-116">1\_3</span></span> | <span data-ttu-id="4a1bb-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="4a1bb-117">1\_4</span></span> | <span data-ttu-id="4a1bb-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a1bb-118">2\_0</span></span> | <span data-ttu-id="4a1bb-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-119">2\_x</span></span> | <span data-ttu-id="4a1bb-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a1bb-120">2\_sw</span></span> | <span data-ttu-id="4a1bb-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a1bb-121">3\_0</span></span> | <span data-ttu-id="4a1bb-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a1bb-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4a1bb-123">max</span><span class="sxs-lookup"><span data-stu-id="4a1bb-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="4a1bb-124">x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-124">x</span></span>    | <span data-ttu-id="4a1bb-125">x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-125">x</span></span>    | <span data-ttu-id="4a1bb-126">x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-126">x</span></span>     | <span data-ttu-id="4a1bb-127">x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-127">x</span></span>    | <span data-ttu-id="4a1bb-128">x</span><span class="sxs-lookup"><span data-stu-id="4a1bb-128">x</span></span>     |



 

<span data-ttu-id="4a1bb-129">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="4a1bb-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="4a1bb-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a1bb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a1bb-131">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="4a1bb-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




