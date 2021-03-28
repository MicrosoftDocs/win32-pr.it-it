---
title: RCP-vs
description: Calcola il reciproco del valore scalare di origine. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982010"
---
# <a name="rcp---vs"></a><span data-ttu-id="2ef30-104">RCP-vs</span><span class="sxs-lookup"><span data-stu-id="2ef30-104">rcp - vs</span></span>

<span data-ttu-id="2ef30-105">Calcola il reciproco del valore scalare di origine.</span><span class="sxs-lookup"><span data-stu-id="2ef30-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef30-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ef30-106">Syntax</span></span>



| <span data-ttu-id="2ef30-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="2ef30-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="2ef30-108">dove</span><span class="sxs-lookup"><span data-stu-id="2ef30-108">where</span></span>

-   <span data-ttu-id="2ef30-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ef30-109">dst is the destination register.</span></span>
-   <span data-ttu-id="2ef30-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="2ef30-110">src is a source register.</span></span> <span data-ttu-id="2ef30-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="2ef30-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef30-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ef30-112">Remarks</span></span>



| <span data-ttu-id="2ef30-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="2ef30-113">Vertex shader versions</span></span> | <span data-ttu-id="2ef30-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="2ef30-114">1\_1</span></span> | <span data-ttu-id="2ef30-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2ef30-115">2\_0</span></span> | <span data-ttu-id="2ef30-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2ef30-116">2\_x</span></span> | <span data-ttu-id="2ef30-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2ef30-117">2\_sw</span></span> | <span data-ttu-id="2ef30-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2ef30-118">3\_0</span></span> | <span data-ttu-id="2ef30-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2ef30-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2ef30-120">rcp</span><span class="sxs-lookup"><span data-stu-id="2ef30-120">rcp</span></span>                    | <span data-ttu-id="2ef30-121">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-121">x</span></span>    | <span data-ttu-id="2ef30-122">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-122">x</span></span>    | <span data-ttu-id="2ef30-123">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-123">x</span></span>    | <span data-ttu-id="2ef30-124">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-124">x</span></span>     | <span data-ttu-id="2ef30-125">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-125">x</span></span>    | <span data-ttu-id="2ef30-126">x</span><span class="sxs-lookup"><span data-stu-id="2ef30-126">x</span></span>     |



 

<span data-ttu-id="2ef30-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="2ef30-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="2ef30-128">L'output deve essere esattamente 1,0 se l'input è esattamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="2ef30-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="2ef30-129">Un'origine di 0,0 restituisce un valore infinito.</span><span class="sxs-lookup"><span data-stu-id="2ef30-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="2ef30-130">La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 2,0) perché le implementazioni comuni separano mantissa ed esponente.</span><span class="sxs-lookup"><span data-stu-id="2ef30-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="2ef30-131">Se l'origine non contiene pedici, viene usato il componente x.</span><span class="sxs-lookup"><span data-stu-id="2ef30-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ef30-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ef30-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef30-133">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="2ef30-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




