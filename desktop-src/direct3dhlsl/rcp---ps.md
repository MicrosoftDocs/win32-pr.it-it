---
title: RCP-PS
description: Calcola il reciproco del valore scalare di origine. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981730"
---
# <a name="rcp---ps"></a><span data-ttu-id="b7e68-104">RCP-PS</span><span class="sxs-lookup"><span data-stu-id="b7e68-104">rcp - ps</span></span>

<span data-ttu-id="b7e68-105">Calcola il reciproco del valore scalare di origine.</span><span class="sxs-lookup"><span data-stu-id="b7e68-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e68-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7e68-106">Syntax</span></span>



| <span data-ttu-id="b7e68-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="b7e68-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b7e68-108">dove</span><span class="sxs-lookup"><span data-stu-id="b7e68-108">where</span></span>

-   <span data-ttu-id="b7e68-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b7e68-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b7e68-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b7e68-110">src is a source register.</span></span> <span data-ttu-id="b7e68-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="b7e68-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e68-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7e68-112">Remarks</span></span>



| <span data-ttu-id="b7e68-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b7e68-113">Pixel shader versions</span></span> | <span data-ttu-id="b7e68-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b7e68-114">1\_1</span></span> | <span data-ttu-id="b7e68-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b7e68-115">1\_2</span></span> | <span data-ttu-id="b7e68-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b7e68-116">1\_3</span></span> | <span data-ttu-id="b7e68-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b7e68-117">1\_4</span></span> | <span data-ttu-id="b7e68-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7e68-118">2\_0</span></span> | <span data-ttu-id="b7e68-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b7e68-119">2\_x</span></span> | <span data-ttu-id="b7e68-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b7e68-120">2\_sw</span></span> | <span data-ttu-id="b7e68-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7e68-121">3\_0</span></span> | <span data-ttu-id="b7e68-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b7e68-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b7e68-123">rcp</span><span class="sxs-lookup"><span data-stu-id="b7e68-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="b7e68-124">x</span><span class="sxs-lookup"><span data-stu-id="b7e68-124">x</span></span>    | <span data-ttu-id="b7e68-125">x</span><span class="sxs-lookup"><span data-stu-id="b7e68-125">x</span></span>    | <span data-ttu-id="b7e68-126">x</span><span class="sxs-lookup"><span data-stu-id="b7e68-126">x</span></span>     | <span data-ttu-id="b7e68-127">x</span><span class="sxs-lookup"><span data-stu-id="b7e68-127">x</span></span>    | <span data-ttu-id="b7e68-128">x</span><span class="sxs-lookup"><span data-stu-id="b7e68-128">x</span></span>     |



 

<span data-ttu-id="b7e68-129">L'output deve essere esattamente 1,0 se l'input è esattamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="b7e68-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="b7e68-130">Un'origine di 0,0 restituisce un valore infinito.</span><span class="sxs-lookup"><span data-stu-id="b7e68-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="b7e68-131">Il risultato scalare viene replicato in tutti i canali nella maschera di scrittura di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b7e68-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="b7e68-132">La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 2,0) perché le implementazioni comuni separano mantissa ed esponente.</span><span class="sxs-lookup"><span data-stu-id="b7e68-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7e68-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7e68-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e68-134">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b7e68-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




