---
title: RSQ-PS
description: Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981551"
---
# <a name="rsq---ps"></a><span data-ttu-id="e4d9c-104">RSQ-PS</span><span class="sxs-lookup"><span data-stu-id="e4d9c-104">rsq - ps</span></span>

<span data-ttu-id="e4d9c-105">Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d9c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4d9c-106">Syntax</span></span>



| <span data-ttu-id="e4d9c-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="e4d9c-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e4d9c-108">dove</span><span class="sxs-lookup"><span data-stu-id="e4d9c-108">where</span></span>

-   <span data-ttu-id="e4d9c-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e4d9c-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-110">src is a source register.</span></span> <span data-ttu-id="e4d9c-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="e4d9c-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4d9c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4d9c-112">Remarks</span></span>



| <span data-ttu-id="e4d9c-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e4d9c-113">Pixel shader versions</span></span> | <span data-ttu-id="e4d9c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e4d9c-114">1\_1</span></span> | <span data-ttu-id="e4d9c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e4d9c-115">1\_2</span></span> | <span data-ttu-id="e4d9c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e4d9c-116">1\_3</span></span> | <span data-ttu-id="e4d9c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e4d9c-117">1\_4</span></span> | <span data-ttu-id="e4d9c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4d9c-118">2\_0</span></span> | <span data-ttu-id="e4d9c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-119">2\_x</span></span> | <span data-ttu-id="e4d9c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4d9c-120">2\_sw</span></span> | <span data-ttu-id="e4d9c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4d9c-121">3\_0</span></span> | <span data-ttu-id="e4d9c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4d9c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e4d9c-123">RSQ</span><span class="sxs-lookup"><span data-stu-id="e4d9c-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="e4d9c-124">x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-124">x</span></span>    | <span data-ttu-id="e4d9c-125">x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-125">x</span></span>    | <span data-ttu-id="e4d9c-126">x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-126">x</span></span>     | <span data-ttu-id="e4d9c-127">x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-127">x</span></span>    | <span data-ttu-id="e4d9c-128">x</span><span class="sxs-lookup"><span data-stu-id="e4d9c-128">x</span></span>     |



 

<span data-ttu-id="e4d9c-129">Il valore assoluto viene prelevato prima dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="e4d9c-130">La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 4,0) perché le implementazioni comuni separano mantissa ed esponente.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="e4d9c-131">L'output deve essere esattamente 1,0 se l'input è esattamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="e4d9c-132">Un'origine di 0,0 restituisce un valore infinito.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4d9c-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4d9c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4d9c-134">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e4d9c-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




