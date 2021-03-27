---
title: Breakp-PS
description: Suddividere in modo condizionale il ciclo corrente nel EndLoop-PS o endrep-PS più vicino. Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398255"
---
# <a name="breakp---ps"></a><span data-ttu-id="90eac-104">Breakp-PS</span><span class="sxs-lookup"><span data-stu-id="90eac-104">breakp - ps</span></span>

<span data-ttu-id="90eac-105">Suddividere in modo condizionale il ciclo corrente nel [EndLoop-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)più vicino.</span><span class="sxs-lookup"><span data-stu-id="90eac-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="90eac-106">Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="90eac-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="90eac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90eac-107">Syntax</span></span>



| <span data-ttu-id="90eac-108">Breakp \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="90eac-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="90eac-109">y</span><span class="sxs-lookup"><span data-stu-id="90eac-109">y\</span></span>|<span data-ttu-id="90eac-110">z</span><span class="sxs-lookup"><span data-stu-id="90eac-110">z\</span></span>|<span data-ttu-id="90eac-111">w</span><span class="sxs-lookup"><span data-stu-id="90eac-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="90eac-112">Dove:</span><span class="sxs-lookup"><span data-stu-id="90eac-112">Where:</span></span>

-   <span data-ttu-id="90eac-113">\[!\] modificatore negazioni facoltativo.</span><span class="sxs-lookup"><span data-stu-id="90eac-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="90eac-114">P0 è il [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="90eac-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="90eac-115">{x \| y \| z \| w} è la replica obbligatoria swizzle su P0.</span><span class="sxs-lookup"><span data-stu-id="90eac-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="90eac-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="90eac-116">Remarks</span></span>



| <span data-ttu-id="90eac-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="90eac-117">Pixel shader versions</span></span> | <span data-ttu-id="90eac-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="90eac-118">1\_1</span></span> | <span data-ttu-id="90eac-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="90eac-119">1\_2</span></span> | <span data-ttu-id="90eac-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="90eac-120">1\_3</span></span> | <span data-ttu-id="90eac-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="90eac-121">1\_4</span></span> | <span data-ttu-id="90eac-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="90eac-122">2\_0</span></span> | <span data-ttu-id="90eac-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="90eac-123">2\_x</span></span> | <span data-ttu-id="90eac-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="90eac-124">2\_sw</span></span> | <span data-ttu-id="90eac-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="90eac-125">3\_0</span></span> | <span data-ttu-id="90eac-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="90eac-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="90eac-127">breakp</span><span class="sxs-lookup"><span data-stu-id="90eac-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="90eac-128">x</span><span class="sxs-lookup"><span data-stu-id="90eac-128">x</span></span>    | <span data-ttu-id="90eac-129">x</span><span class="sxs-lookup"><span data-stu-id="90eac-129">x</span></span>     | <span data-ttu-id="90eac-130">x</span><span class="sxs-lookup"><span data-stu-id="90eac-130">x</span></span>    | <span data-ttu-id="90eac-131">x</span><span class="sxs-lookup"><span data-stu-id="90eac-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="90eac-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90eac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90eac-133">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="90eac-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




