---
title: min-PS
description: Calcola il numero minimo di origini. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981567"
---
# <a name="min---ps"></a><span data-ttu-id="b8ff5-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="b8ff5-104">min - ps</span></span>

<span data-ttu-id="b8ff5-105">Calcola il numero minimo di origini.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ff5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8ff5-106">Syntax</span></span>



| <span data-ttu-id="b8ff5-107">min DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b8ff5-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b8ff5-108">dove</span><span class="sxs-lookup"><span data-stu-id="b8ff5-108">where</span></span>

-   <span data-ttu-id="b8ff5-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b8ff5-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b8ff5-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ff5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8ff5-112">Remarks</span></span>



| <span data-ttu-id="b8ff5-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b8ff5-113">Pixel shader versions</span></span> | <span data-ttu-id="b8ff5-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b8ff5-114">1\_1</span></span> | <span data-ttu-id="b8ff5-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b8ff5-115">1\_2</span></span> | <span data-ttu-id="b8ff5-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b8ff5-116">1\_3</span></span> | <span data-ttu-id="b8ff5-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b8ff5-117">1\_4</span></span> | <span data-ttu-id="b8ff5-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8ff5-118">2\_0</span></span> | <span data-ttu-id="b8ff5-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-119">2\_x</span></span> | <span data-ttu-id="b8ff5-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8ff5-120">2\_sw</span></span> | <span data-ttu-id="b8ff5-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8ff5-121">3\_0</span></span> | <span data-ttu-id="b8ff5-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8ff5-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b8ff5-123">min</span><span class="sxs-lookup"><span data-stu-id="b8ff5-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="b8ff5-124">x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-124">x</span></span>    | <span data-ttu-id="b8ff5-125">x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-125">x</span></span>    | <span data-ttu-id="b8ff5-126">x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-126">x</span></span>     | <span data-ttu-id="b8ff5-127">x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-127">x</span></span>    | <span data-ttu-id="b8ff5-128">x</span><span class="sxs-lookup"><span data-stu-id="b8ff5-128">x</span></span>     |



 

<span data-ttu-id="b8ff5-129">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="b8ff5-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8ff5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8ff5-131">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b8ff5-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




