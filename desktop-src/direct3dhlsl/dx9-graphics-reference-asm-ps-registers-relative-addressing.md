---
title: Indirizzamento relativo (informazioni di riferimento su HLSL PS)
description: Per i pixel shader, la sintassi \ \ può essere usata solo in tipi di registro che possono essere relativamente indirizzati in determinati modelli di shader.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405484"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="fdafb-103">Indirizzamento relativo (informazioni di riferimento su HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="fdafb-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="fdafb-104">La \[ \] sintassi può essere usata solo in tipi di registro che possono essere relativamente gestiti in determinati modelli di shader.</span><span class="sxs-lookup"><span data-stu-id="fdafb-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="fdafb-105">Le forme di \[ \] sintassi supportate sono elencate di seguito:</span><span class="sxs-lookup"><span data-stu-id="fdafb-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="fdafb-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="fdafb-106">Where:</span></span>

-   <span data-ttu-id="fdafb-107">"R" indica qualsiasi tipo di registro che può essere relativamente indirizzato.</span><span class="sxs-lookup"><span data-stu-id="fdafb-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="fdafb-108">"A" indica qualsiasi registro che può essere usato come indice per risolvere relativamente altri registri.</span><span class="sxs-lookup"><span data-stu-id="fdafb-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="fdafb-109">n0 - ni, m0 - mj e k sono numeri interi >= 0.</span><span class="sxs-lookup"><span data-stu-id="fdafb-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="fdafb-110">\[\]sintassi</span><span class="sxs-lookup"><span data-stu-id="fdafb-110">\[ \] syntax</span></span>                              | <span data-ttu-id="fdafb-111">Indice effettivo</span><span class="sxs-lookup"><span data-stu-id="fdafb-111">Effective index</span></span>                       | <span data-ttu-id="fdafb-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="fdafb-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="fdafb-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="fdafb-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fdafb-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="fdafb-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="fdafb-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="fdafb-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="fdafb-117">k</span><span class="sxs-lookup"><span data-stu-id="fdafb-117">k</span></span>                                     | <span data-ttu-id="fdafb-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="fdafb-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="fdafb-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-119">R\[ A \]</span></span>                                  | <span data-ttu-id="fdafb-120">Una</span><span class="sxs-lookup"><span data-stu-id="fdafb-120">A</span></span>                                     | <span data-ttu-id="fdafb-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="fdafb-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="fdafb-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fdafb-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="fdafb-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="fdafb-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="fdafb-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fdafb-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="fdafb-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="fdafb-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="fdafb-129">A + k</span><span class="sxs-lookup"><span data-stu-id="fdafb-129">A + k</span></span>                                 | <span data-ttu-id="fdafb-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="fdafb-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="fdafb-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fdafb-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="fdafb-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="fdafb-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="fdafb-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="fdafb-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="fdafb-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="fdafb-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="fdafb-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="fdafb-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="fdafb-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="fdafb-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="fdafb-140">I registri sono disponibili nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fdafb-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="fdafb-141">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="fdafb-141">Register type</span></span>                                                                                   | <span data-ttu-id="fdafb-142">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="fdafb-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="fdafb-143">[contatore di cicli:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL nei registri di input</span><span class="sxs-lookup"><span data-stu-id="fdafb-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="fdafb-144">ps \_ 3 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="fdafb-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="fdafb-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fdafb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdafb-146">Registri</span><span class="sxs-lookup"><span data-stu-id="fdafb-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




