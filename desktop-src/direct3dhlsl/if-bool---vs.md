---
title: Se bool-vs
description: Avvia un'if... altrimenti... il blocco endif-vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046058"
---
# <a name="if-bool---vs"></a><span data-ttu-id="80679-103">Se bool-vs</span><span class="sxs-lookup"><span data-stu-id="80679-103">if bool - vs</span></span>

<span data-ttu-id="80679-104">Avvia un'if... [altrimenti](else---vs.md)... il blocco [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="80679-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="80679-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80679-105">Syntax</span></span>



| <span data-ttu-id="80679-106">Se bool</span><span class="sxs-lookup"><span data-stu-id="80679-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="80679-107">dove bool è un numero di registro bool.</span><span class="sxs-lookup"><span data-stu-id="80679-107">where bool is a bool register number.</span></span> <span data-ttu-id="80679-108">Vedere [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="80679-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80679-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="80679-109">Remarks</span></span>



| <span data-ttu-id="80679-110">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="80679-110">Vertex shader versions</span></span> | <span data-ttu-id="80679-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="80679-111">1\_1</span></span> | <span data-ttu-id="80679-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80679-112">2\_0</span></span> | <span data-ttu-id="80679-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="80679-113">2\_x</span></span> | <span data-ttu-id="80679-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="80679-114">2\_sw</span></span> | <span data-ttu-id="80679-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80679-115">3\_0</span></span> | <span data-ttu-id="80679-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="80679-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="80679-117">Se bool</span><span class="sxs-lookup"><span data-stu-id="80679-117">if bool</span></span>                |      | <span data-ttu-id="80679-118">x</span><span class="sxs-lookup"><span data-stu-id="80679-118">x</span></span>    | <span data-ttu-id="80679-119">x</span><span class="sxs-lookup"><span data-stu-id="80679-119">x</span></span>    | <span data-ttu-id="80679-120">x</span><span class="sxs-lookup"><span data-stu-id="80679-120">x</span></span>     | <span data-ttu-id="80679-121">x</span><span class="sxs-lookup"><span data-stu-id="80679-121">x</span></span>    | <span data-ttu-id="80679-122">x</span><span class="sxs-lookup"><span data-stu-id="80679-122">x</span></span>     |



 

<span data-ttu-id="80679-123">Se il registro booleano di origine nell'istruzione If è true, viene eseguito il codice racchiuso dall'istruzione if e l'altro corrispondente.</span><span class="sxs-lookup"><span data-stu-id="80679-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="80679-124">In caso contrario, il codice racchiuso da [else](else---vs.md)... vengono eseguite le istruzioni [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="80679-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="80679-125">Questa istruzione usa uno slot di istruzione.</span><span class="sxs-lookup"><span data-stu-id="80679-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="80679-126">Se i blocchi possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="80679-126">if blocks can be nested.</span></span>

<span data-ttu-id="80679-127">Un blocco If non può risiedere in un blocco di ciclo.</span><span class="sxs-lookup"><span data-stu-id="80679-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="80679-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="80679-128">Example</span></span>

<span data-ttu-id="80679-129">Questa istruzione fornisce il controllo di flusso statico condizionale.</span><span class="sxs-lookup"><span data-stu-id="80679-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="80679-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80679-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80679-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="80679-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="80679-132">else-vs</span><span class="sxs-lookup"><span data-stu-id="80679-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="80679-133">endif-vs</span><span class="sxs-lookup"><span data-stu-id="80679-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




