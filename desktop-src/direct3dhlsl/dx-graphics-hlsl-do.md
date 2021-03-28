---
title: Istruzione do (ocidl. h)
description: Eseguire continuamente una serie di istruzioni fino a quando l'espressione condizionale non riesce.
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
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235007"
---
# <a name="do-statement"></a><span data-ttu-id="f7060-104">Istruzione do</span><span class="sxs-lookup"><span data-stu-id="f7060-104">do Statement</span></span>

<span data-ttu-id="f7060-105">Eseguire continuamente una serie di istruzioni fino a quando l'espressione condizionale non riesce.</span><span class="sxs-lookup"><span data-stu-id="f7060-105">Execute a series of statements continuously until the conditional expression fails.</span></span>



|                                                                     |
|---------------------------------------------------------------------|
| <span data-ttu-id="f7060-106">\[*Attributo* \] do { *Block Statement*;} while ( *condizionale* );</span><span class="sxs-lookup"><span data-stu-id="f7060-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f7060-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7060-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7060-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="f7060-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="f7060-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="f7060-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="f7060-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="f7060-110">Attribute</span></span> | <span data-ttu-id="f7060-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7060-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7060-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="f7060-112">fastopt</span></span>   | <span data-ttu-id="f7060-113">Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive.</span><span class="sxs-lookup"><span data-stu-id="f7060-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="f7060-114">Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.</span><span class="sxs-lookup"><span data-stu-id="f7060-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="f7060-115">Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="f7060-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="f7060-116">Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f7060-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="f7060-117">È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli.</span><span class="sxs-lookup"><span data-stu-id="f7060-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="f7060-118">Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback.</span><span class="sxs-lookup"><span data-stu-id="f7060-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="f7060-119">Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="f7060-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f7060-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="f7060-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="f7060-121">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="f7060-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7060-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="f7060-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="f7060-123">[Espressione](dx-graphics-hlsl-expressions.md)condizionale.</span><span class="sxs-lookup"><span data-stu-id="f7060-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="f7060-124">Il blocco di istruzioni viene eseguito prima della valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="f7060-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="f7060-125">Il ciclo viene terminato quando l'espressione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="f7060-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7060-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7060-126">Requirements</span></span>



| <span data-ttu-id="f7060-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7060-127">Requirement</span></span> | <span data-ttu-id="f7060-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f7060-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7060-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7060-129">Header</span></span><br/> | <dl> <span data-ttu-id="f7060-130"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7060-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7060-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7060-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7060-132">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="f7060-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





