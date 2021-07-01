---
title: Istruzione for
description: Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- Istruzione for HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119077"
---
# <a name="for-statement"></a><span data-ttu-id="85b10-104">Istruzione for</span><span class="sxs-lookup"><span data-stu-id="85b10-104">for Statement</span></span>

<span data-ttu-id="85b10-105">Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="85b10-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="85b10-106">\[*Attributo* \] for ( *Inizializzatore; Condizionale; Iterator* ) { *Blocco di istruzioni*; }</span><span class="sxs-lookup"><span data-stu-id="85b10-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="85b10-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="85b10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b10-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="85b10-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="85b10-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="85b10-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="85b10-110">Quando non viene specificato alcun attributo, il compilatore tenterà prima di tutto di generare una versione di cui è stato eseguito il roll-roll e, in caso di esito negativo, o se alcune operazioni sarebbero più semplici se il ciclo fosse stato scollegato, verrà eseguito il fall back a una versione di cui non è stata eseguita la registrazione.</span><span class="sxs-lookup"><span data-stu-id="85b10-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="85b10-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="85b10-111">Attribute</span></span>             | <span data-ttu-id="85b10-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85b10-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b10-113">annullamento della registrazione(x)</span><span class="sxs-lookup"><span data-stu-id="85b10-113">unroll(x)</span></span>             | <span data-ttu-id="85b10-114">Annullare la registrazione del ciclo fino a quando non viene interrotta l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="85b10-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="85b10-115">Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="85b10-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="85b10-116">Non compatibile con **\[ l'attributo del \]** ciclo.</span><span class="sxs-lookup"><span data-stu-id="85b10-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="85b10-117">loop</span><span class="sxs-lookup"><span data-stu-id="85b10-117">loop</span></span>                  | <span data-ttu-id="85b10-118">Generare codice che usa il controllo di flusso per eseguire ogni iterazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="85b10-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="85b10-119">Non compatibile con **\[ l'attributo di \] annullamento** della registrazione.</span><span class="sxs-lookup"><span data-stu-id="85b10-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="85b10-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="85b10-120">fastopt</span></span>               | <span data-ttu-id="85b10-121">Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="85b10-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="85b10-122">Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.</span><span class="sxs-lookup"><span data-stu-id="85b10-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="85b10-123">Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione.</span><span class="sxs-lookup"><span data-stu-id="85b10-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="85b10-124">Questo attributo è disponibile nel modello shader [rispetto a \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel modello [shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="85b10-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="85b10-125">È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="85b10-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="85b10-126">Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="85b10-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="85b10-127">Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="85b10-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="85b10-128">consenti \_ condizione \_ uav</span><span class="sxs-lookup"><span data-stu-id="85b10-128">allow\_uav\_condition</span></span> | <span data-ttu-id="85b10-129">Consente a una condizione di terminazione del ciclo compute shader di basarsi su una lettura UAV.</span><span class="sxs-lookup"><span data-stu-id="85b10-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="85b10-130">Il ciclo non deve contenere intrinseci di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="85b10-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="85b10-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inizializzatore*</span><span class="sxs-lookup"><span data-stu-id="85b10-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="85b10-132">Valore iniziale del contatore di cicli.</span><span class="sxs-lookup"><span data-stu-id="85b10-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="85b10-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="85b10-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="85b10-134">Espressione [condizionale](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="85b10-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="85b10-135">Se l'espressione condizionale restituisce true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="85b10-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="85b10-136">Il ciclo termina quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="85b10-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="85b10-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iteratore*</span><span class="sxs-lookup"><span data-stu-id="85b10-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="85b10-138">Aggiornare il valore del contatore del ciclo.</span><span class="sxs-lookup"><span data-stu-id="85b10-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="85b10-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="85b10-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="85b10-140">Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="85b10-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85b10-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="85b10-141">Remarks</span></span>

<span data-ttu-id="85b10-142">Gli **\[ attributi \] unroll** **\[ e loop \]** si escludono a vicenda e generano errori del compilatore quando vengono specificati entrambi.</span><span class="sxs-lookup"><span data-stu-id="85b10-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="85b10-143">Gli **\[ attributi \] della condizione fastopt** **\[ e allow \_ uav \_ \]** vengono ignorati se **\[ si specifica unroll. \]**</span><span class="sxs-lookup"><span data-stu-id="85b10-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="85b10-144">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="85b10-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b10-145">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="85b10-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





