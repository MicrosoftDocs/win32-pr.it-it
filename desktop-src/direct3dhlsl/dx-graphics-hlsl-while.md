---
title: Istruzione while
description: Esegue un blocco di istruzioni fino a quando l'espressione condizionale non riesce.
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
ms.openlocfilehash: 190d5474b5e016b41426db67a0c96d98787f79ff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045608"
---
# <a name="while-statement"></a><span data-ttu-id="51134-104">Istruzione while</span><span class="sxs-lookup"><span data-stu-id="51134-104">while Statement</span></span>

<span data-ttu-id="51134-105">Esegue un blocco di istruzioni fino a quando l'espressione condizionale non riesce.</span><span class="sxs-lookup"><span data-stu-id="51134-105">Executes a statement block until the conditional expression fails.</span></span>



|                                                                  |
|------------------------------------------------------------------|
| <span data-ttu-id="51134-106">\[*Attributo* \] while ( *Conditional* ) { *Block Statement*;}</span><span class="sxs-lookup"><span data-stu-id="51134-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="51134-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="51134-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51134-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="51134-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="51134-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="51134-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="51134-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="51134-110">Attribute</span></span>             | <span data-ttu-id="51134-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51134-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51134-112">unroll (x)</span><span class="sxs-lookup"><span data-stu-id="51134-112">unroll(x)</span></span>             | <span data-ttu-id="51134-113">Eseguire l'unrolling del ciclo fino a quando non viene arrestata l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="51134-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="51134-114">Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo può essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="51134-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51134-115">loop</span><span class="sxs-lookup"><span data-stu-id="51134-115">loop</span></span>                  | <span data-ttu-id="51134-116">Usare le istruzioni di controllo di flusso nello shader compilato; non eseguire l'unrolling del ciclo.</span><span class="sxs-lookup"><span data-stu-id="51134-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="51134-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="51134-117">fastopt</span></span>               | <span data-ttu-id="51134-118">Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="51134-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="51134-119">Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.</span><span class="sxs-lookup"><span data-stu-id="51134-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="51134-120">Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="51134-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="51134-121">Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="51134-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="51134-122">È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="51134-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="51134-123">Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback.</span><span class="sxs-lookup"><span data-stu-id="51134-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="51134-124">Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="51134-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="51134-125">Consenti \_ \_ condizione UAV</span><span class="sxs-lookup"><span data-stu-id="51134-125">allow\_uav\_condition</span></span> | <span data-ttu-id="51134-126">Consente a una condizione di terminazione del ciclo compute shader di essere basata su un UAV letto.</span><span class="sxs-lookup"><span data-stu-id="51134-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="51134-127">Il ciclo non deve contenere intrinseci di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="51134-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="51134-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="51134-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="51134-129">[Espressione](dx-graphics-hlsl-expressions.md)condizionale.</span><span class="sxs-lookup"><span data-stu-id="51134-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="51134-130">Se l'espressione restituisce true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="51134-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="51134-131">Il ciclo termina quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="51134-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="51134-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="51134-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="51134-133">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="51134-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="51134-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51134-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51134-135">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="51134-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





