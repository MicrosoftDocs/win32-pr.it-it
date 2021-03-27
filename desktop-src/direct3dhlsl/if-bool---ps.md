---
title: Se bool-PS
description: Inizio di un blocco If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719354"
---
# <a name="if-bool---ps"></a><span data-ttu-id="2bf5f-103">Se bool-PS</span><span class="sxs-lookup"><span data-stu-id="2bf5f-103">if bool - ps</span></span>

<span data-ttu-id="2bf5f-104">Inizio di un blocco If.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bf5f-105">Syntax</span></span>



| <span data-ttu-id="2bf5f-106">Se bool</span><span class="sxs-lookup"><span data-stu-id="2bf5f-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="2bf5f-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="2bf5f-107">Where:</span></span>

-   <span data-ttu-id="2bf5f-108">bool è un numero di registro bool (Boolean).</span><span class="sxs-lookup"><span data-stu-id="2bf5f-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="2bf5f-109">Vedere [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="2bf5f-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf5f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bf5f-110">Remarks</span></span>



| <span data-ttu-id="2bf5f-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="2bf5f-111">Pixel shader versions</span></span> | <span data-ttu-id="2bf5f-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2bf5f-112">1\_1</span></span> | <span data-ttu-id="2bf5f-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2bf5f-113">1\_2</span></span> | <span data-ttu-id="2bf5f-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2bf5f-114">1\_3</span></span> | <span data-ttu-id="2bf5f-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2bf5f-115">1\_4</span></span> | <span data-ttu-id="2bf5f-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2bf5f-116">2\_0</span></span> | <span data-ttu-id="2bf5f-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2bf5f-117">2\_x</span></span> | <span data-ttu-id="2bf5f-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2bf5f-118">2\_sw</span></span> | <span data-ttu-id="2bf5f-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2bf5f-119">3\_0</span></span> | <span data-ttu-id="2bf5f-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2bf5f-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2bf5f-121">Se bool</span><span class="sxs-lookup"><span data-stu-id="2bf5f-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="2bf5f-122">x</span><span class="sxs-lookup"><span data-stu-id="2bf5f-122">x</span></span>    | <span data-ttu-id="2bf5f-123">x</span><span class="sxs-lookup"><span data-stu-id="2bf5f-123">x</span></span>     | <span data-ttu-id="2bf5f-124">x</span><span class="sxs-lookup"><span data-stu-id="2bf5f-124">x</span></span>    | <span data-ttu-id="2bf5f-125">x</span><span class="sxs-lookup"><span data-stu-id="2bf5f-125">x</span></span>     |



 

<span data-ttu-id="2bf5f-126">Se il registro booleano di origine nell'istruzione If è true, viene eseguito il codice racchiuso dall'istruzione if e il corrispondente [endif-PS](endif---ps.md) o [else-PS](else---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf5f-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="2bf5f-127">In caso contrario, il codice racchiuso da Else-PS... vengono eseguite le istruzioni endif-PS.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="2bf5f-128">Questa istruzione usa uno slot di istruzione.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="2bf5f-129">Un blocco if può essere annidato.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-129">An if block can be nested.</span></span>

<span data-ttu-id="2bf5f-130">Un blocco If non può risiedere in un blocco di ciclo.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="2bf5f-131">Un blocco if può essere seguito da un blocco di istruzioni e/o da un'istruzione [else-PS](else---ps.md) e/o da un'istruzione [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf5f-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="2bf5f-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="2bf5f-132">Example</span></span>

<span data-ttu-id="2bf5f-133">Questa istruzione fornisce il controllo di flusso statico condizionale.</span><span class="sxs-lookup"><span data-stu-id="2bf5f-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="2bf5f-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bf5f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bf5f-135">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="2bf5f-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="2bf5f-136">else-PS</span><span class="sxs-lookup"><span data-stu-id="2bf5f-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="2bf5f-137">endif-PS</span><span class="sxs-lookup"><span data-stu-id="2bf5f-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




