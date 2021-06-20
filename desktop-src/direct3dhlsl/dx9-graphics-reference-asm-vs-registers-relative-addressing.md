---
title: Indirizzamento relativo (informazioni di riferimento su HLSL VS)
description: Per i vertex shader, la sintassi \ \ può essere usata solo nei tipi di registro che possono essere relativamente indirizzati in determinati modelli shader.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406694"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="26f50-103">Indirizzamento relativo (informazioni di riferimento su HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="26f50-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="26f50-104">La \[ \] sintassi può essere usata solo nei tipi di registro che possono essere relativamente indirizzati in determinati modelli shader.</span><span class="sxs-lookup"><span data-stu-id="26f50-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="26f50-105">Le forme di \[ \] sintassi supportate sono elencate di seguito:</span><span class="sxs-lookup"><span data-stu-id="26f50-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="26f50-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="26f50-106">Where:</span></span>

-   <span data-ttu-id="26f50-107">"R" indica qualsiasi tipo di registro che può essere relativamente indirizzato.</span><span class="sxs-lookup"><span data-stu-id="26f50-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="26f50-108">"A" indica qualsiasi registro che può essere usato come indice per risolvere relativamente altri registri.</span><span class="sxs-lookup"><span data-stu-id="26f50-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="26f50-109">n0 - ni, m0 - mj e k sono numeri interi >= 0.</span><span class="sxs-lookup"><span data-stu-id="26f50-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="26f50-110">\[\]sintassi</span><span class="sxs-lookup"><span data-stu-id="26f50-110">\[ \] syntax</span></span>                              | <span data-ttu-id="26f50-111">Indice effettivo</span><span class="sxs-lookup"><span data-stu-id="26f50-111">Effective index</span></span>                       | <span data-ttu-id="26f50-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="26f50-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="26f50-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="26f50-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="26f50-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="26f50-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="26f50-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="26f50-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="26f50-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="26f50-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="26f50-117">k</span><span class="sxs-lookup"><span data-stu-id="26f50-117">k</span></span>                                     | <span data-ttu-id="26f50-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="26f50-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="26f50-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="26f50-119">R\[ A \]</span></span>                                  | <span data-ttu-id="26f50-120">Una</span><span class="sxs-lookup"><span data-stu-id="26f50-120">A</span></span>                                     | <span data-ttu-id="26f50-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="26f50-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="26f50-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="26f50-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="26f50-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="26f50-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="26f50-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="26f50-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="26f50-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="26f50-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="26f50-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="26f50-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="26f50-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="26f50-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="26f50-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="26f50-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="26f50-129">A + k</span><span class="sxs-lookup"><span data-stu-id="26f50-129">A + k</span></span>                                 | <span data-ttu-id="26f50-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="26f50-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="26f50-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="26f50-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="26f50-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="26f50-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="26f50-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="26f50-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="26f50-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="26f50-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="26f50-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="26f50-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="26f50-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="26f50-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="26f50-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="26f50-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="26f50-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="26f50-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="26f50-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="26f50-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="26f50-140">I registri sono disponibili nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="26f50-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="26f50-141">Tipo di registrazione</span><span class="sxs-lookup"><span data-stu-id="26f50-141">Register type</span></span> | <span data-ttu-id="26f50-142">Versioni di Vertex Shader</span><span class="sxs-lookup"><span data-stu-id="26f50-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="26f50-143">a0</span><span class="sxs-lookup"><span data-stu-id="26f50-143">a0</span></span>            | <span data-ttu-id="26f50-144">Tutti</span><span class="sxs-lookup"><span data-stu-id="26f50-144">All</span></span>                    |
| <span data-ttu-id="26f50-145">aL</span><span class="sxs-lookup"><span data-stu-id="26f50-145">aL</span></span>            | <span data-ttu-id="26f50-146">vs \_ 2 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="26f50-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="26f50-147">cn</span><span class="sxs-lookup"><span data-stu-id="26f50-147">cn</span></span>            | <span data-ttu-id="26f50-148">vs \_ 1 \_ 1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="26f50-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="26f50-149">on</span><span class="sxs-lookup"><span data-stu-id="26f50-149">on</span></span>            | <span data-ttu-id="26f50-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26f50-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="26f50-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26f50-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f50-152">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="26f50-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




