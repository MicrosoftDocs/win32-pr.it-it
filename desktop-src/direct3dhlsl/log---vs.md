---
title: log-vs
description: ₂ di log con precisione completa (x). | log-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234780"
---
# <a name="log---vs"></a><span data-ttu-id="2fed0-104">log-vs</span><span class="sxs-lookup"><span data-stu-id="2fed0-104">log - vs</span></span>

<span data-ttu-id="2fed0-105">₂ di log con precisione completa (x).</span><span class="sxs-lookup"><span data-stu-id="2fed0-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fed0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fed0-106">Syntax</span></span>



| <span data-ttu-id="2fed0-107">log DST, src</span><span class="sxs-lookup"><span data-stu-id="2fed0-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="2fed0-108">dove</span><span class="sxs-lookup"><span data-stu-id="2fed0-108">where</span></span>

-   <span data-ttu-id="2fed0-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2fed0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="2fed0-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="2fed0-110">src is a source register.</span></span> <span data-ttu-id="2fed0-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="2fed0-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fed0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fed0-112">Remarks</span></span>



| <span data-ttu-id="2fed0-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="2fed0-113">Vertex shader versions</span></span> | <span data-ttu-id="2fed0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="2fed0-114">1\_1</span></span> | <span data-ttu-id="2fed0-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fed0-115">2\_0</span></span> | <span data-ttu-id="2fed0-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2fed0-116">2\_x</span></span> | <span data-ttu-id="2fed0-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2fed0-117">2\_sw</span></span> | <span data-ttu-id="2fed0-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fed0-118">3\_0</span></span> | <span data-ttu-id="2fed0-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2fed0-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2fed0-120">log</span><span class="sxs-lookup"><span data-stu-id="2fed0-120">log</span></span>                    | <span data-ttu-id="2fed0-121">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-121">x</span></span>    | <span data-ttu-id="2fed0-122">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-122">x</span></span>    | <span data-ttu-id="2fed0-123">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-123">x</span></span>    | <span data-ttu-id="2fed0-124">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-124">x</span></span>     | <span data-ttu-id="2fed0-125">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-125">x</span></span>    | <span data-ttu-id="2fed0-126">x</span><span class="sxs-lookup"><span data-stu-id="2fed0-126">x</span></span>     |



 

<span data-ttu-id="2fed0-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="2fed0-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="2fed0-128">Questa istruzione accetta un'origine scalare il cui bit di segno viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2fed0-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="2fed0-129">Il risultato viene replicato in tutti e quattro i canali.</span><span class="sxs-lookup"><span data-stu-id="2fed0-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="2fed0-130">Questa istruzione fornisce 21 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="2fed0-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fed0-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fed0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fed0-132">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="2fed0-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




