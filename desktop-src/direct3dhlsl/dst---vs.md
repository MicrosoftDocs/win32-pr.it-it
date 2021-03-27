---
title: DST-vs
description: Calcola un vettore di distanza. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886091"
---
# <a name="dst---vs"></a><span data-ttu-id="26f3e-104">DST-vs</span><span class="sxs-lookup"><span data-stu-id="26f3e-104">dst - vs</span></span>

<span data-ttu-id="26f3e-105">Calcola un vettore di distanza.</span><span class="sxs-lookup"><span data-stu-id="26f3e-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f3e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26f3e-106">Syntax</span></span>



| <span data-ttu-id="26f3e-107">dest DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="26f3e-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="26f3e-108">dove</span><span class="sxs-lookup"><span data-stu-id="26f3e-108">where</span></span>

-   <span data-ttu-id="26f3e-109">dest è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26f3e-109">dest is the destination register.</span></span>
-   <span data-ttu-id="26f3e-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="26f3e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="26f3e-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="26f3e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f3e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="26f3e-112">Remarks</span></span>



| <span data-ttu-id="26f3e-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="26f3e-113">Vertex shader versions</span></span> | <span data-ttu-id="26f3e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="26f3e-114">1\_1</span></span> | <span data-ttu-id="26f3e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26f3e-115">2\_0</span></span> | <span data-ttu-id="26f3e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="26f3e-116">2\_x</span></span> | <span data-ttu-id="26f3e-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26f3e-117">2\_sw</span></span> | <span data-ttu-id="26f3e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26f3e-118">3\_0</span></span> | <span data-ttu-id="26f3e-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26f3e-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="26f3e-120">DST</span><span class="sxs-lookup"><span data-stu-id="26f3e-120">dst</span></span>                    | <span data-ttu-id="26f3e-121">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-121">x</span></span>    | <span data-ttu-id="26f3e-122">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-122">x</span></span>    | <span data-ttu-id="26f3e-123">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-123">x</span></span>    | <span data-ttu-id="26f3e-124">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-124">x</span></span>     | <span data-ttu-id="26f3e-125">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-125">x</span></span>    | <span data-ttu-id="26f3e-126">x</span><span class="sxs-lookup"><span data-stu-id="26f3e-126">x</span></span>     |



 

<span data-ttu-id="26f3e-127">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="26f3e-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="26f3e-128">Si presuppone che il primo operando di origine (src0) sia il vettore (ignorato, d \* d, d \* d, ignorato) e che il secondo operando di origine (src1) sia il vettore (ignorato, 1/d, ignorato, 1/d).</span><span class="sxs-lookup"><span data-stu-id="26f3e-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="26f3e-129">La destinazione (dest) è il vettore di risultato (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="26f3e-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26f3e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26f3e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f3e-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="26f3e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




