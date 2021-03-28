---
title: Istruzione for
description: Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- per l'istruzione HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117005"
---
# <a name="for-statement"></a><span data-ttu-id="93842-104">Istruzione for</span><span class="sxs-lookup"><span data-stu-id="93842-104">for Statement</span></span>

<span data-ttu-id="93842-105">Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="93842-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93842-106">\[*Attributo* \] per ( *inizializzatore; Condizionale Iterator* ) { *blocco di istruzioni*;}</span><span class="sxs-lookup"><span data-stu-id="93842-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="93842-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="93842-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93842-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="93842-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="93842-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="93842-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="93842-110">Se non si specifica alcun attributo, il compilatore tenterà innanzitutto di creare una versione con rollup del ciclo e, in caso di esito negativo, oppure se alcune operazioni sarebbero più semplici se il ciclo è stato annullato, verrà eseguito il fallback a una versione non registrata del ciclo.</span><span class="sxs-lookup"><span data-stu-id="93842-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="93842-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="93842-111">Attribute</span></span>             | <span data-ttu-id="93842-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93842-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93842-113">unroll (x)</span><span class="sxs-lookup"><span data-stu-id="93842-113">unroll(x)</span></span>             | <span data-ttu-id="93842-114">Eseguire l'unrolling del ciclo fino a quando non viene arrestata l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="93842-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="93842-115">È possibile specificare facoltativamente il numero massimo di esecuzioni del ciclo.</span><span class="sxs-lookup"><span data-stu-id="93842-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="93842-116">Non compatibile con l'attributo del **\[ ciclo \]** .</span><span class="sxs-lookup"><span data-stu-id="93842-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="93842-117">loop</span><span class="sxs-lookup"><span data-stu-id="93842-117">loop</span></span>                  | <span data-ttu-id="93842-118">Genera codice che usa il controllo di flusso per eseguire ogni iterazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="93842-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="93842-119">Non è compatibile con l'attributo **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="93842-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="93842-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="93842-120">fastopt</span></span>               | <span data-ttu-id="93842-121">Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="93842-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="93842-122">Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.</span><span class="sxs-lookup"><span data-stu-id="93842-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="93842-123">Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="93842-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="93842-124">Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="93842-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="93842-125">È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="93842-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="93842-126">Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback.</span><span class="sxs-lookup"><span data-stu-id="93842-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="93842-127">Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="93842-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="93842-128">Consenti \_ \_ condizione UAV</span><span class="sxs-lookup"><span data-stu-id="93842-128">allow\_uav\_condition</span></span> | <span data-ttu-id="93842-129">Consente a una condizione di terminazione del ciclo compute shader di essere basata su un UAV letto.</span><span class="sxs-lookup"><span data-stu-id="93842-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="93842-130">Il ciclo non deve contenere intrinseci di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="93842-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="93842-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inizializzatore*</span><span class="sxs-lookup"><span data-stu-id="93842-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="93842-132">Valore iniziale del contatore di cicli.</span><span class="sxs-lookup"><span data-stu-id="93842-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="93842-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="93842-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="93842-134">[Espressione](dx-graphics-hlsl-expressions.md)condizionale.</span><span class="sxs-lookup"><span data-stu-id="93842-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="93842-135">Se l'espressione condizionale restituisce true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="93842-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="93842-136">Il ciclo termina quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="93842-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="93842-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iteratore*</span><span class="sxs-lookup"><span data-stu-id="93842-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="93842-138">Aggiornare il valore del contatore di cicli.</span><span class="sxs-lookup"><span data-stu-id="93842-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="93842-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="93842-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="93842-140">Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="93842-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93842-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="93842-141">Remarks</span></span>

<span data-ttu-id="93842-142">Gli attributi **\[ unroll \]** e **\[ loop \]** si escludono a vicenda e generano errori del compilatore quando vengono specificati entrambi.</span><span class="sxs-lookup"><span data-stu-id="93842-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="93842-143">Gli attributi di **\[ \_ \_ condizione \]** **\[ \] fastopt** e Allow UAV vengono ignorati se viene specificato **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="93842-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="93842-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93842-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93842-145">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="93842-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





