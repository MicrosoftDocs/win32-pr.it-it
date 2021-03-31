---
title: Indirizzamento relativo (riferimento HLSL VS)
description: La sintassi \ \ può essere utilizzata solo nei tipi di registro che possono essere risolti relativamente in determinati modelli shader.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335676"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="f2f7f-103">Indirizzamento relativo (riferimento HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="f2f7f-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="f2f7f-104">La \[ \] sintassi può essere utilizzata solo nei tipi di registro che possono essere considerati relativamente in determinati modelli shader.</span><span class="sxs-lookup"><span data-stu-id="f2f7f-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="f2f7f-105">I formati di \[ \] sintassi supportati sono elencati di seguito:</span><span class="sxs-lookup"><span data-stu-id="f2f7f-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="f2f7f-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="f2f7f-106">Where:</span></span>

-   <span data-ttu-id="f2f7f-107">"R" indica qualsiasi tipo di registro che può essere considerato relativamente.</span><span class="sxs-lookup"><span data-stu-id="f2f7f-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="f2f7f-108">"A" indica tutti i registri che possono essere usati come indice per indirizzare gli altri registri in modo relativamente diverso.</span><span class="sxs-lookup"><span data-stu-id="f2f7f-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="f2f7f-109">N0-NI, M0-MJ e k sono numeri interi >= 0.</span><span class="sxs-lookup"><span data-stu-id="f2f7f-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="f2f7f-110">\[\]sintassi di</span><span class="sxs-lookup"><span data-stu-id="f2f7f-110">\[ \] syntax</span></span>                              | <span data-ttu-id="f2f7f-111">Indice effettivo</span><span class="sxs-lookup"><span data-stu-id="f2f7f-111">Effective index</span></span>                       | <span data-ttu-id="f2f7f-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="f2f7f-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="f2f7f-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="f2f7f-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f2f7f-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="f2f7f-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="f2f7f-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="f2f7f-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="f2f7f-117">k</span><span class="sxs-lookup"><span data-stu-id="f2f7f-117">k</span></span>                                     | <span data-ttu-id="f2f7f-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="f2f7f-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="f2f7f-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-119">R\[ A \]</span></span>                                  | <span data-ttu-id="f2f7f-120">A</span><span class="sxs-lookup"><span data-stu-id="f2f7f-120">A</span></span>                                     | <span data-ttu-id="f2f7f-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="f2f7f-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="f2f7f-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f2f7f-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="f2f7f-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="f2f7f-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="f2f7f-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f2f7f-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="f2f7f-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="f2f7f-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="f2f7f-129">A + k</span><span class="sxs-lookup"><span data-stu-id="f2f7f-129">A + k</span></span>                                 | <span data-ttu-id="f2f7f-130">C12 \[ al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="f2f7f-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="f2f7f-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f2f7f-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="f2f7f-133">V1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="f2f7f-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="f2f7f-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="f2f7f-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="f2f7f-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="f2f7f-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="f2f7f-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="f2f7f-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="f2f7f-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="f2f7f-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="f2f7f-140">I registri sono disponibili nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2f7f-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="f2f7f-141">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="f2f7f-141">Register type</span></span> | <span data-ttu-id="f2f7f-142">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="f2f7f-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="f2f7f-143">a0</span><span class="sxs-lookup"><span data-stu-id="f2f7f-143">a0</span></span>            | <span data-ttu-id="f2f7f-144">Tutti</span><span class="sxs-lookup"><span data-stu-id="f2f7f-144">All</span></span>                    |
| <span data-ttu-id="f2f7f-145">aL</span><span class="sxs-lookup"><span data-stu-id="f2f7f-145">aL</span></span>            | <span data-ttu-id="f2f7f-146">vs \_ 2 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f2f7f-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="f2f7f-147">cn</span><span class="sxs-lookup"><span data-stu-id="f2f7f-147">cn</span></span>            | <span data-ttu-id="f2f7f-148">vs \_ 1 \_ 1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f2f7f-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="f2f7f-149">on</span><span class="sxs-lookup"><span data-stu-id="f2f7f-149">on</span></span>            | <span data-ttu-id="f2f7f-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2f7f-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="f2f7f-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2f7f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2f7f-152">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="f2f7f-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




