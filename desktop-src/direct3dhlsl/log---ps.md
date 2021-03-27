---
title: log-PS
description: ₂ di log con precisione completa (x). | log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982016"
---
# <a name="log---ps"></a><span data-ttu-id="abd8d-104">log-PS</span><span class="sxs-lookup"><span data-stu-id="abd8d-104">log - ps</span></span>

<span data-ttu-id="abd8d-105">₂ di log con precisione completa (x).</span><span class="sxs-lookup"><span data-stu-id="abd8d-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="abd8d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abd8d-106">Syntax</span></span>



| <span data-ttu-id="abd8d-107">log DST, src</span><span class="sxs-lookup"><span data-stu-id="abd8d-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="abd8d-108">dove</span><span class="sxs-lookup"><span data-stu-id="abd8d-108">where</span></span>

-   <span data-ttu-id="abd8d-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="abd8d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="abd8d-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="abd8d-110">src is a source register.</span></span> <span data-ttu-id="abd8d-111">Il registro di origine richiede l'uso esplicito di swizzle replicate; ovvero, è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a).</span><span class="sxs-lookup"><span data-stu-id="abd8d-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="abd8d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="abd8d-112">Remarks</span></span>



| <span data-ttu-id="abd8d-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="abd8d-113">Pixel shader versions</span></span> | <span data-ttu-id="abd8d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="abd8d-114">1\_1</span></span> | <span data-ttu-id="abd8d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="abd8d-115">1\_2</span></span> | <span data-ttu-id="abd8d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="abd8d-116">1\_3</span></span> | <span data-ttu-id="abd8d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="abd8d-117">1\_4</span></span> | <span data-ttu-id="abd8d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="abd8d-118">2\_0</span></span> | <span data-ttu-id="abd8d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="abd8d-119">2\_x</span></span> | <span data-ttu-id="abd8d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="abd8d-120">2\_sw</span></span> | <span data-ttu-id="abd8d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="abd8d-121">3\_0</span></span> | <span data-ttu-id="abd8d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="abd8d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="abd8d-123">log</span><span class="sxs-lookup"><span data-stu-id="abd8d-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="abd8d-124">x</span><span class="sxs-lookup"><span data-stu-id="abd8d-124">x</span></span>    | <span data-ttu-id="abd8d-125">x</span><span class="sxs-lookup"><span data-stu-id="abd8d-125">x</span></span>    | <span data-ttu-id="abd8d-126">x</span><span class="sxs-lookup"><span data-stu-id="abd8d-126">x</span></span>     | <span data-ttu-id="abd8d-127">x</span><span class="sxs-lookup"><span data-stu-id="abd8d-127">x</span></span>    | <span data-ttu-id="abd8d-128">x</span><span class="sxs-lookup"><span data-stu-id="abd8d-128">x</span></span>     |



 

<span data-ttu-id="abd8d-129">Il frammento di codice seguente mostra le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="abd8d-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="abd8d-130">Questa istruzione accetta un'origine scalare il cui bit di segno viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="abd8d-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="abd8d-131">Il risultato viene replicato in tutti e quattro i canali.</span><span class="sxs-lookup"><span data-stu-id="abd8d-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abd8d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abd8d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abd8d-133">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="abd8d-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




