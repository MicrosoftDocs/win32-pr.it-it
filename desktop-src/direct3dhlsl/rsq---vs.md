---
title: RSQ-vs
description: Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981799"
---
# <a name="rsq---vs"></a><span data-ttu-id="28080-104">RSQ-vs</span><span class="sxs-lookup"><span data-stu-id="28080-104">rsq - vs</span></span>

<span data-ttu-id="28080-105">Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine.</span><span class="sxs-lookup"><span data-stu-id="28080-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="28080-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28080-106">Syntax</span></span>



| <span data-ttu-id="28080-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="28080-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="28080-108">dove</span><span class="sxs-lookup"><span data-stu-id="28080-108">where</span></span>

-   <span data-ttu-id="28080-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28080-109">dst is the destination register.</span></span>
-   <span data-ttu-id="28080-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="28080-110">src is a source register.</span></span> <span data-ttu-id="28080-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="28080-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="28080-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="28080-112">Remarks</span></span>



| <span data-ttu-id="28080-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="28080-113">Vertex shader versions</span></span> | <span data-ttu-id="28080-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="28080-114">1\_1</span></span> | <span data-ttu-id="28080-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28080-115">2\_0</span></span> | <span data-ttu-id="28080-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28080-116">2\_x</span></span> | <span data-ttu-id="28080-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28080-117">2\_sw</span></span> | <span data-ttu-id="28080-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28080-118">3\_0</span></span> | <span data-ttu-id="28080-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28080-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="28080-120">RSQ</span><span class="sxs-lookup"><span data-stu-id="28080-120">rsq</span></span>                    | <span data-ttu-id="28080-121">x</span><span class="sxs-lookup"><span data-stu-id="28080-121">x</span></span>    | <span data-ttu-id="28080-122">x</span><span class="sxs-lookup"><span data-stu-id="28080-122">x</span></span>    | <span data-ttu-id="28080-123">x</span><span class="sxs-lookup"><span data-stu-id="28080-123">x</span></span>    | <span data-ttu-id="28080-124">x</span><span class="sxs-lookup"><span data-stu-id="28080-124">x</span></span>     | <span data-ttu-id="28080-125">x</span><span class="sxs-lookup"><span data-stu-id="28080-125">x</span></span>    | <span data-ttu-id="28080-126">x</span><span class="sxs-lookup"><span data-stu-id="28080-126">x</span></span>     |



 

<span data-ttu-id="28080-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="28080-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="28080-128">Il valore assoluto viene prelevato prima dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="28080-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="28080-129">La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 4,0) perché le implementazioni comuni separano mantissa ed esponente.</span><span class="sxs-lookup"><span data-stu-id="28080-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="28080-130">Se l'origine non include indici, viene usato il componente x.</span><span class="sxs-lookup"><span data-stu-id="28080-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="28080-131">L'output deve essere esattamente 1,0 se l'input è esattamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="28080-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="28080-132">Un'origine di 0,0 restituisce un valore infinito.</span><span class="sxs-lookup"><span data-stu-id="28080-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28080-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28080-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28080-134">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="28080-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




