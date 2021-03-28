---
title: LogP-vs
description: Precisione parziale LogP ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046093"
---
# <a name="logp---vs"></a><span data-ttu-id="e2123-103">LogP-vs</span><span class="sxs-lookup"><span data-stu-id="e2123-103">logp - vs</span></span>

<span data-ttu-id="e2123-104">Precisione parziale LogP ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="e2123-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2123-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2123-105">Syntax</span></span>



| <span data-ttu-id="e2123-106">LogP DST, src</span><span class="sxs-lookup"><span data-stu-id="e2123-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="e2123-107">dove</span><span class="sxs-lookup"><span data-stu-id="e2123-107">where</span></span>

-   <span data-ttu-id="e2123-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e2123-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e2123-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="e2123-109">src is a source register.</span></span> <span data-ttu-id="e2123-110">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="e2123-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2123-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2123-111">Remarks</span></span>



| <span data-ttu-id="e2123-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="e2123-112">Vertex shader versions</span></span> | <span data-ttu-id="e2123-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="e2123-113">1\_1</span></span> | <span data-ttu-id="e2123-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2123-114">2\_0</span></span> | <span data-ttu-id="e2123-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e2123-115">2\_x</span></span> | <span data-ttu-id="e2123-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e2123-116">2\_sw</span></span> | <span data-ttu-id="e2123-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2123-117">3\_0</span></span> | <span data-ttu-id="e2123-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e2123-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e2123-119">logp</span><span class="sxs-lookup"><span data-stu-id="e2123-119">logp</span></span>                   | <span data-ttu-id="e2123-120">x</span><span class="sxs-lookup"><span data-stu-id="e2123-120">x</span></span>    | <span data-ttu-id="e2123-121">x</span><span class="sxs-lookup"><span data-stu-id="e2123-121">x</span></span>    | <span data-ttu-id="e2123-122">x</span><span class="sxs-lookup"><span data-stu-id="e2123-122">x</span></span>    | <span data-ttu-id="e2123-123">x</span><span class="sxs-lookup"><span data-stu-id="e2123-123">x</span></span>     | <span data-ttu-id="e2123-124">x</span><span class="sxs-lookup"><span data-stu-id="e2123-124">x</span></span>    | <span data-ttu-id="e2123-125">x</span><span class="sxs-lookup"><span data-stu-id="e2123-125">x</span></span>     |



 

<span data-ttu-id="e2123-126">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="e2123-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="e2123-127">Questa istruzione fornisce la precisione parziale logaritmo in base 2, fino a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="e2123-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2123-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2123-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2123-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="e2123-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




