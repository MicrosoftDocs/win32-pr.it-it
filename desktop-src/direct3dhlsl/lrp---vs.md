---
title: LRP-vs
description: Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995568"
---
# <a name="lrp---vs"></a><span data-ttu-id="58baa-104">LRP-vs</span><span class="sxs-lookup"><span data-stu-id="58baa-104">lrp - vs</span></span>

<span data-ttu-id="58baa-105">Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine.</span><span class="sxs-lookup"><span data-stu-id="58baa-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="58baa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58baa-106">Syntax</span></span>



| <span data-ttu-id="58baa-107">LRP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="58baa-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="58baa-108">dove</span><span class="sxs-lookup"><span data-stu-id="58baa-108">where</span></span>

-   <span data-ttu-id="58baa-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58baa-109">dst is the destination register.</span></span>
-   <span data-ttu-id="58baa-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="58baa-110">src0 is a source register.</span></span>
-   <span data-ttu-id="58baa-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="58baa-111">src1 is a source register.</span></span>
-   <span data-ttu-id="58baa-112">src2 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="58baa-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="58baa-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58baa-113">Remarks</span></span>



| <span data-ttu-id="58baa-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="58baa-114">Vertex shader versions</span></span> | <span data-ttu-id="58baa-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="58baa-115">1\_1</span></span> | <span data-ttu-id="58baa-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58baa-116">2\_0</span></span> | <span data-ttu-id="58baa-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="58baa-117">2\_x</span></span> | <span data-ttu-id="58baa-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58baa-118">2\_sw</span></span> | <span data-ttu-id="58baa-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58baa-119">3\_0</span></span> | <span data-ttu-id="58baa-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58baa-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="58baa-121">LRP</span><span class="sxs-lookup"><span data-stu-id="58baa-121">lrp</span></span>                    |      | <span data-ttu-id="58baa-122">x</span><span class="sxs-lookup"><span data-stu-id="58baa-122">x</span></span>    | <span data-ttu-id="58baa-123">x</span><span class="sxs-lookup"><span data-stu-id="58baa-123">x</span></span>    | <span data-ttu-id="58baa-124">x</span><span class="sxs-lookup"><span data-stu-id="58baa-124">x</span></span>     | <span data-ttu-id="58baa-125">x</span><span class="sxs-lookup"><span data-stu-id="58baa-125">x</span></span>    | <span data-ttu-id="58baa-126">x</span><span class="sxs-lookup"><span data-stu-id="58baa-126">x</span></span>     |



 

<span data-ttu-id="58baa-127">Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="58baa-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="58baa-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58baa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58baa-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="58baa-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




