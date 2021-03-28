---
title: Se prede-vs
description: Inizio di un'se prede-vs... else-vs... endif-vs blocco, con la condizione ricavata dal contenuto del registro predicato.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335476"
---
# <a name="if-pred---vs"></a><span data-ttu-id="824af-103">Se prede-vs</span><span class="sxs-lookup"><span data-stu-id="824af-103">if pred - vs</span></span>

<span data-ttu-id="824af-104">Inizio di un'se prede-vs... [else-vs](else---vs.md)... [endif-vs](endif---vs.md) blocco, con la condizione ricavata dal contenuto del registro predicato.</span><span class="sxs-lookup"><span data-stu-id="824af-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="824af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="824af-105">Syntax</span></span>



| <span data-ttu-id="824af-106">Se \[ ! \] prede. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="824af-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="824af-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="824af-107">Where:</span></span>

-   <span data-ttu-id="824af-108">\[!\] un modificatore facoltativo NOT.</span><span class="sxs-lookup"><span data-stu-id="824af-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="824af-109">Il valore viene modificato nel registro predicato.</span><span class="sxs-lookup"><span data-stu-id="824af-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="824af-110">prede è il registro predicato, P0.</span><span class="sxs-lookup"><span data-stu-id="824af-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="824af-111">Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="824af-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="824af-112">replicateSwizzle è un singolo componente copiato (o replicato) in tutti i quattro componenti (swizzled).</span><span class="sxs-lookup"><span data-stu-id="824af-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="824af-113">I componenti validi sono: x, y, z, w o r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="824af-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="824af-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="824af-114">Remarks</span></span>



| <span data-ttu-id="824af-115">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="824af-115">Vertex shader versions</span></span> | <span data-ttu-id="824af-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="824af-116">1\_1</span></span> | <span data-ttu-id="824af-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="824af-117">2\_0</span></span> | <span data-ttu-id="824af-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="824af-118">2\_x</span></span> | <span data-ttu-id="824af-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="824af-119">2\_sw</span></span> | <span data-ttu-id="824af-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="824af-120">3\_0</span></span> | <span data-ttu-id="824af-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="824af-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="824af-122">Se prede</span><span class="sxs-lookup"><span data-stu-id="824af-122">if pred</span></span>                |      |      | <span data-ttu-id="824af-123">x</span><span class="sxs-lookup"><span data-stu-id="824af-123">x</span></span>    | <span data-ttu-id="824af-124">x</span><span class="sxs-lookup"><span data-stu-id="824af-124">x</span></span>     | <span data-ttu-id="824af-125">x</span><span class="sxs-lookup"><span data-stu-id="824af-125">x</span></span>    | <span data-ttu-id="824af-126">x</span><span class="sxs-lookup"><span data-stu-id="824af-126">x</span></span>     |



 

<span data-ttu-id="824af-127">Questa istruzione viene utilizzata per ignorare un blocco di codice, in base a un canale del registro predicato.</span><span class="sxs-lookup"><span data-stu-id="824af-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="824af-128">Each se il \_ blocco prede deve terminare con un'istruzione else o endif.</span><span class="sxs-lookup"><span data-stu-id="824af-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="824af-129">Tali restrizioni includono:</span><span class="sxs-lookup"><span data-stu-id="824af-129">Restrictions include:</span></span>

<span data-ttu-id="824af-130">Se i \_ blocchi di predazione possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="824af-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="824af-131">Viene conteggiata la profondità di nidificazione dinamica totale insieme a [if \_ comp](if-comp---vs.md) Blocks.</span><span class="sxs-lookup"><span data-stu-id="824af-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="824af-132">Un blocco If prede non può risiedere in \_ un blocco di ciclo, deve trovarsi completamente al suo interno o racchiuderlo tra loro.</span><span class="sxs-lookup"><span data-stu-id="824af-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="824af-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="824af-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="824af-134">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="824af-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




