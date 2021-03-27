---
title: Se prede-PS
description: Inizio di un if bool-PS... else-PS... il blocco endif-PS, con la condizione ricavata dal contenuto del registro predicato.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719375"
---
# <a name="if-pred---ps"></a><span data-ttu-id="c89b2-103">Se prede-PS</span><span class="sxs-lookup"><span data-stu-id="c89b2-103">if pred - ps</span></span>

<span data-ttu-id="c89b2-104">Inizio di un [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... il blocco [endif-PS](endif---ps.md) , con la condizione ricavata dal contenuto del registro predicato.</span><span class="sxs-lookup"><span data-stu-id="c89b2-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="c89b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c89b2-105">Syntax</span></span>



| <span data-ttu-id="c89b2-106">Se \[ ! \] prede. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="c89b2-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="c89b2-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="c89b2-107">Where:</span></span>

-   <span data-ttu-id="c89b2-108">\[!\] è un modificatore facoltativo NOT.</span><span class="sxs-lookup"><span data-stu-id="c89b2-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="c89b2-109">Il valore viene modificato nel registro predicato.</span><span class="sxs-lookup"><span data-stu-id="c89b2-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="c89b2-110">prede è il [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c89b2-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="c89b2-111">replicateSwizzle è un singolo componente copiato (o replicato) in tutti i quattro componenti (swizzled).</span><span class="sxs-lookup"><span data-stu-id="c89b2-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="c89b2-112">I componenti validi sono: \[ x, y, z, w \] o \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="c89b2-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="c89b2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c89b2-113">Remarks</span></span>



| <span data-ttu-id="c89b2-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c89b2-114">Pixel shader versions</span></span> | <span data-ttu-id="c89b2-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="c89b2-115">1\_1</span></span> | <span data-ttu-id="c89b2-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="c89b2-116">1\_2</span></span> | <span data-ttu-id="c89b2-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c89b2-117">1\_3</span></span> | <span data-ttu-id="c89b2-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="c89b2-118">1\_4</span></span> | <span data-ttu-id="c89b2-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c89b2-119">2\_0</span></span> | <span data-ttu-id="c89b2-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c89b2-120">2\_x</span></span> | <span data-ttu-id="c89b2-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c89b2-121">2\_sw</span></span> | <span data-ttu-id="c89b2-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c89b2-122">3\_0</span></span> | <span data-ttu-id="c89b2-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c89b2-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c89b2-124">Se \_ prede</span><span class="sxs-lookup"><span data-stu-id="c89b2-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="c89b2-125">x</span><span class="sxs-lookup"><span data-stu-id="c89b2-125">x</span></span>    | <span data-ttu-id="c89b2-126">x</span><span class="sxs-lookup"><span data-stu-id="c89b2-126">x</span></span>     | <span data-ttu-id="c89b2-127">x</span><span class="sxs-lookup"><span data-stu-id="c89b2-127">x</span></span>    | <span data-ttu-id="c89b2-128">x</span><span class="sxs-lookup"><span data-stu-id="c89b2-128">x</span></span>     |



 

<span data-ttu-id="c89b2-129">Questa istruzione viene utilizzata per ignorare un blocco di codice, in base a un canale del registro predicato.</span><span class="sxs-lookup"><span data-stu-id="c89b2-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="c89b2-130">Each se il \_ blocco prede deve terminare con un'istruzione [else-PS](else---ps.md) o [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="c89b2-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="c89b2-131">Tali restrizioni includono:</span><span class="sxs-lookup"><span data-stu-id="c89b2-131">Restrictions include:</span></span>

<span data-ttu-id="c89b2-132">Se i \_ blocchi di predazione possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="c89b2-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="c89b2-133">Viene conteggiata la profondità di nidificazione dinamica totale insieme a [if \_ comp](if-comp---ps.md) Blocks.</span><span class="sxs-lookup"><span data-stu-id="c89b2-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="c89b2-134">Un blocco If prede non può risiedere in \_ un blocco di ciclo, ma deve essere completamente al suo interno o racchiuderlo.</span><span class="sxs-lookup"><span data-stu-id="c89b2-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c89b2-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c89b2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c89b2-136">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c89b2-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




