---
title: Breakp-vs
description: Suddividere in modo condizionale il ciclo corrente al più vicino EndLoop-vs o endrep-vs. utilizzare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046086"
---
# <a name="breakp---vs"></a><span data-ttu-id="09d33-103">Breakp-vs</span><span class="sxs-lookup"><span data-stu-id="09d33-103">breakp - vs</span></span>

<span data-ttu-id="09d33-104">Suddividere in modo condizionale il ciclo corrente nel [EndLoop-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)più vicino. Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="09d33-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09d33-105">Syntax</span></span>



| <span data-ttu-id="09d33-106">Breakp \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="09d33-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="09d33-107">y</span><span class="sxs-lookup"><span data-stu-id="09d33-107">y\</span></span>|<span data-ttu-id="09d33-108">z</span><span class="sxs-lookup"><span data-stu-id="09d33-108">z\</span></span>|<span data-ttu-id="09d33-109">w</span><span class="sxs-lookup"><span data-stu-id="09d33-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="09d33-110">Dove:</span><span class="sxs-lookup"><span data-stu-id="09d33-110">Where:</span></span>

-   <span data-ttu-id="09d33-111">\[!\] valore booleano facoltativo NOT.</span><span class="sxs-lookup"><span data-stu-id="09d33-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="09d33-112">P0 è il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="09d33-112">p0 is the predicate register.</span></span> <span data-ttu-id="09d33-113">Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="09d33-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="09d33-114">{x \| y \| z \| w} è la replica obbligatoria swizzle su P0.</span><span class="sxs-lookup"><span data-stu-id="09d33-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d33-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="09d33-115">Remarks</span></span>



| <span data-ttu-id="09d33-116">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="09d33-116">Vertex shader versions</span></span> | <span data-ttu-id="09d33-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="09d33-117">1\_1</span></span> | <span data-ttu-id="09d33-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09d33-118">2\_0</span></span> | <span data-ttu-id="09d33-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="09d33-119">2\_x</span></span> | <span data-ttu-id="09d33-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09d33-120">2\_sw</span></span> | <span data-ttu-id="09d33-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09d33-121">3\_0</span></span> | <span data-ttu-id="09d33-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09d33-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="09d33-123">breakp</span><span class="sxs-lookup"><span data-stu-id="09d33-123">breakp</span></span>                 |      |      | <span data-ttu-id="09d33-124">x</span><span class="sxs-lookup"><span data-stu-id="09d33-124">x</span></span>    | <span data-ttu-id="09d33-125">x</span><span class="sxs-lookup"><span data-stu-id="09d33-125">x</span></span>     | <span data-ttu-id="09d33-126">x</span><span class="sxs-lookup"><span data-stu-id="09d33-126">x</span></span>    | <span data-ttu-id="09d33-127">x</span><span class="sxs-lookup"><span data-stu-id="09d33-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="09d33-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09d33-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09d33-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="09d33-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




