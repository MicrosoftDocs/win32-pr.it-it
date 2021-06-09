---
title: Istruzione while
description: Esegue un blocco di istruzioni fino a quando l'espressione condizionale non ha esito negativo.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- Istruzione while HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826674"
---
# <a name="while-statement"></a><span data-ttu-id="8ed3a-104">Istruzione while</span><span class="sxs-lookup"><span data-stu-id="8ed3a-104">while Statement</span></span>

<span data-ttu-id="8ed3a-105">Esegue un blocco di istruzioni fino a quando l'espressione condizionale non ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="8ed3a-106">\[*Attributo* \] while ( *Conditional* ) { *Statement Block*; }</span><span class="sxs-lookup"><span data-stu-id="8ed3a-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="8ed3a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed3a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="8ed3a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="8ed3a-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="8ed3a-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="8ed3a-110">Attribute</span></span>             | <span data-ttu-id="8ed3a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ed3a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed3a-112">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="8ed3a-112">unroll(x)</span></span>             | <span data-ttu-id="8ed3a-113">Annullare la registrazione del ciclo fino all'arresto dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="8ed3a-114">Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo può essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8ed3a-115">loop</span><span class="sxs-lookup"><span data-stu-id="8ed3a-115">loop</span></span>                  | <span data-ttu-id="8ed3a-116">Usare istruzioni di controllo del flusso nello shader compilato; non annullare la registrazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8ed3a-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="8ed3a-117">fastopt</span></span>               | <span data-ttu-id="8ed3a-118">Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="8ed3a-119">Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="8ed3a-120">Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="8ed3a-121">Questo attributo è disponibile nel modello di shader [rispetto \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [modello shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="8ed3a-122">È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="8ed3a-123">Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="8ed3a-124">Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="8ed3a-125">consenti \_ condizione \_ uav</span><span class="sxs-lookup"><span data-stu-id="8ed3a-125">allow\_uav\_condition</span></span> | <span data-ttu-id="8ed3a-126">Consente a una condizione di terminazione del ciclo compute shader di basarsi su una lettura UAV.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="8ed3a-127">Il ciclo non deve contenere oggetti intrinseci di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8ed3a-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="8ed3a-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="8ed3a-129">Espressione [condizionale](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="8ed3a-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="8ed3a-130">Se l'espressione restituisce true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="8ed3a-131">Il ciclo termina quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="8ed3a-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="8ed3a-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="8ed3a-133">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="8ed3a-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8ed3a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ed3a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed3a-135">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="8ed3a-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





