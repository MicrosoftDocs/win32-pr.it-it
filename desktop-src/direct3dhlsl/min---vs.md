---
title: min-vs
description: Calcola il numero minimo di origini. | min-vs
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981775"
---
# <a name="min---vs"></a><span data-ttu-id="6b7e9-104">min-vs</span><span class="sxs-lookup"><span data-stu-id="6b7e9-104">min - vs</span></span>

<span data-ttu-id="6b7e9-105">Calcola il numero minimo di origini.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7e9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b7e9-106">Syntax</span></span>



| <span data-ttu-id="6b7e9-107">min DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="6b7e9-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="6b7e9-108">dove</span><span class="sxs-lookup"><span data-stu-id="6b7e9-108">where</span></span>

-   <span data-ttu-id="6b7e9-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="6b7e9-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-110">src0 is a source register.</span></span>
-   <span data-ttu-id="6b7e9-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7e9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b7e9-112">Remarks</span></span>



| <span data-ttu-id="6b7e9-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="6b7e9-113">Vertex shader versions</span></span> | <span data-ttu-id="6b7e9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="6b7e9-114">1\_1</span></span> | <span data-ttu-id="6b7e9-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b7e9-115">2\_0</span></span> | <span data-ttu-id="6b7e9-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-116">2\_x</span></span> | <span data-ttu-id="6b7e9-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6b7e9-117">2\_sw</span></span> | <span data-ttu-id="6b7e9-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b7e9-118">3\_0</span></span> | <span data-ttu-id="6b7e9-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6b7e9-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="6b7e9-120">min</span><span class="sxs-lookup"><span data-stu-id="6b7e9-120">min</span></span>                    | <span data-ttu-id="6b7e9-121">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-121">x</span></span>    | <span data-ttu-id="6b7e9-122">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-122">x</span></span>    | <span data-ttu-id="6b7e9-123">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-123">x</span></span>    | <span data-ttu-id="6b7e9-124">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-124">x</span></span>     | <span data-ttu-id="6b7e9-125">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-125">x</span></span>    | <span data-ttu-id="6b7e9-126">x</span><span class="sxs-lookup"><span data-stu-id="6b7e9-126">x</span></span>     |



 

<span data-ttu-id="6b7e9-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="6b7e9-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="6b7e9-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b7e9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7e9-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="6b7e9-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




