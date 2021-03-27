---
title: Indirizzamento relativo (riferimenti per HLSL PS)
description: La sintassi \ \ può essere utilizzata solo nei tipi di registro che possono essere risolti relativamente in determinati modelli shader.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719528"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="a6656-103">Indirizzamento relativo (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="a6656-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="a6656-104">La \[ \] sintassi può essere utilizzata solo nei tipi di registro che possono essere considerati relativamente in determinati modelli shader.</span><span class="sxs-lookup"><span data-stu-id="a6656-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="a6656-105">I formati di \[ \] sintassi supportati sono elencati di seguito:</span><span class="sxs-lookup"><span data-stu-id="a6656-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="a6656-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="a6656-106">Where:</span></span>

-   <span data-ttu-id="a6656-107">"R" indica qualsiasi tipo di registro che può essere considerato relativamente.</span><span class="sxs-lookup"><span data-stu-id="a6656-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="a6656-108">"A" indica tutti i registri che possono essere usati come indice per indirizzare gli altri registri in modo relativamente diverso.</span><span class="sxs-lookup"><span data-stu-id="a6656-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="a6656-109">N0-NI, M0-MJ e k sono numeri interi >= 0.</span><span class="sxs-lookup"><span data-stu-id="a6656-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="a6656-110">\[\]sintassi di</span><span class="sxs-lookup"><span data-stu-id="a6656-110">\[ \] syntax</span></span>                              | <span data-ttu-id="a6656-111">Indice effettivo</span><span class="sxs-lookup"><span data-stu-id="a6656-111">Effective index</span></span>                       | <span data-ttu-id="a6656-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a6656-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="a6656-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="a6656-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="a6656-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="a6656-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="a6656-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="a6656-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="a6656-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="a6656-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="a6656-117">k</span><span class="sxs-lookup"><span data-stu-id="a6656-117">k</span></span>                                     | <span data-ttu-id="a6656-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="a6656-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="a6656-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="a6656-119">R\[ A \]</span></span>                                  | <span data-ttu-id="a6656-120">A</span><span class="sxs-lookup"><span data-stu-id="a6656-120">A</span></span>                                     | <span data-ttu-id="a6656-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="a6656-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="a6656-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="a6656-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="a6656-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="a6656-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="a6656-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="a6656-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="a6656-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="a6656-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="a6656-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="a6656-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="a6656-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="a6656-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="a6656-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="a6656-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="a6656-129">A + k</span><span class="sxs-lookup"><span data-stu-id="a6656-129">A + k</span></span>                                 | <span data-ttu-id="a6656-130">C12 \[ al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="a6656-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="a6656-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="a6656-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="a6656-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="a6656-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="a6656-133">V1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="a6656-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="a6656-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="a6656-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="a6656-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="a6656-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="a6656-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="a6656-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="a6656-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="a6656-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="a6656-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="a6656-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="a6656-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="a6656-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="a6656-140">I registri sono disponibili nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6656-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="a6656-141">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="a6656-141">Register type</span></span>                                                                                   | <span data-ttu-id="a6656-142">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a6656-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="a6656-143">[contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md): al nei registri di input</span><span class="sxs-lookup"><span data-stu-id="a6656-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="a6656-144">PS \_ 3 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="a6656-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="a6656-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6656-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6656-146">Registri</span><span class="sxs-lookup"><span data-stu-id="a6656-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




