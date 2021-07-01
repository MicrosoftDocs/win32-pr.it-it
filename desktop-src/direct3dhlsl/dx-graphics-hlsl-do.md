---
title: Istruzione do (Ocidl.h)
description: Eseguire una serie di istruzioni in modo continuo fino a quando l'espressione condizionale non ha esito negativo.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Istruzione do HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118786"
---
# <a name="do-statement"></a><span data-ttu-id="2da0d-104">Istruzione do</span><span class="sxs-lookup"><span data-stu-id="2da0d-104">do Statement</span></span>

<span data-ttu-id="2da0d-105">Eseguire una serie di istruzioni in modo continuo fino a quando l'espressione condizionale non ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2da0d-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="2da0d-106">\[*Attributo* \] do { *Statement Block*; } while( *Conditional* );</span><span class="sxs-lookup"><span data-stu-id="2da0d-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="2da0d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2da0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da0d-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="2da0d-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="2da0d-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="2da0d-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="2da0d-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="2da0d-110">Attribute</span></span> | <span data-ttu-id="2da0d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2da0d-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da0d-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="2da0d-112">fastopt</span></span>   | <span data-ttu-id="2da0d-113">Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="2da0d-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="2da0d-114">Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.</span><span class="sxs-lookup"><span data-stu-id="2da0d-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="2da0d-115">Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione.</span><span class="sxs-lookup"><span data-stu-id="2da0d-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="2da0d-116">Questo attributo è disponibile nel modello shader [rispetto a \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel modello [shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2da0d-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="2da0d-117">È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="2da0d-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="2da0d-118">Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2da0d-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="2da0d-119">Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2da0d-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2da0d-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="2da0d-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="2da0d-121">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="2da0d-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="2da0d-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="2da0d-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="2da0d-123">Espressione [condizionale](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="2da0d-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="2da0d-124">Il blocco di istruzioni viene eseguito prima della valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="2da0d-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="2da0d-125">Il ciclo viene terminato quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="2da0d-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2da0d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2da0d-126">Requirements</span></span>



| <span data-ttu-id="2da0d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da0d-127">Requirement</span></span> | <span data-ttu-id="2da0d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2da0d-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2da0d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2da0d-129">Header</span></span><br/> | <dl> <span data-ttu-id="2da0d-130"><dt>Ocidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="2da0d-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da0d-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2da0d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da0d-132">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="2da0d-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





