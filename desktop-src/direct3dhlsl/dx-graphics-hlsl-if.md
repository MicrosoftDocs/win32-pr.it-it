---
title: Istruzione if
description: Eseguire in modo condizionale una serie di istruzioni in base alla valutazione dell'espressione condizionale.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Istruzione if HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118956"
---
# <a name="if-statement"></a><span data-ttu-id="9c41a-104">Istruzione if</span><span class="sxs-lookup"><span data-stu-id="9c41a-104">if Statement</span></span>

<span data-ttu-id="9c41a-105">Eseguire in modo condizionale una serie di istruzioni in base alla valutazione dell'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="9c41a-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="9c41a-106">\[*Attributo* \] if ( *condizionale* ) { *Blocco di istruzioni*; }</span><span class="sxs-lookup"><span data-stu-id="9c41a-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="9c41a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c41a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c41a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="9c41a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="9c41a-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="9c41a-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c41a-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="9c41a-110">Attribute</span></span></th>
<th><span data-ttu-id="9c41a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c41a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c41a-112">ramo</span><span class="sxs-lookup"><span data-stu-id="9c41a-112">branch</span></span></td>
<td><span data-ttu-id="9c41a-113">Valutare solo un lato dell'istruzione if a seconda della condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9c41a-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c41a-114">Quando si usa <a href="dx-graphics-hlsl-sm2.md">il modello shader 2.x</a> o il modello <a href="dx-graphics-hlsl-sm3.md">shader 3.0,</a>ogni volta che si usa la diramazione dinamica si usano le risorse.</span><span class="sxs-lookup"><span data-stu-id="9c41a-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="9c41a-115">Pertanto, se si usa la diramazione dinamica in modo eccessivo quando si usano questi profili come destinazione, è possibile ricevere errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="9c41a-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c41a-116">rendere bidimensionale</span><span class="sxs-lookup"><span data-stu-id="9c41a-116">flatten</span></span></td>
<td><span data-ttu-id="9c41a-117">Valutare entrambi i lati dell'istruzione if e scegliere tra i due valori risultanti.</span><span class="sxs-lookup"><span data-stu-id="9c41a-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9c41a-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="9c41a-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="9c41a-119">Espressione [condizionale](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="9c41a-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="9c41a-120">L'espressione viene valutata e, se true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="9c41a-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="9c41a-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="9c41a-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="9c41a-122">Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="9c41a-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c41a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c41a-123">Remarks</span></span>

<span data-ttu-id="9c41a-124">Quando il compilatore usa il metodo branch per compilare un'istruzione if, genererà codice che valuterà solo un lato dell'istruzione if a seconda della condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9c41a-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="9c41a-125">Ad esempio, nell'istruzione if:</span><span class="sxs-lookup"><span data-stu-id="9c41a-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="9c41a-126">**L'istruzione if** ha un blocco else implicito, che equivale a x = x.</span><span class="sxs-lookup"><span data-stu-id="9c41a-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="9c41a-127">Poiché è stato detto al compilatore di usare il metodo branch con l'attributo branch precedente, il codice compilato valuterà x ed eseguirà solo il lato che deve essere eseguito; Se x è zero, verrà eseguito il lato **else** e se è diverso da zero verrà eseguito il **lato then.**</span><span class="sxs-lookup"><span data-stu-id="9c41a-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="9c41a-128">Viceversa, se viene usato l'attributo **flatten,** il codice compilato valuterà entrambi i lati dell'istruzione **if** e sceglierà tra i due valori risultanti usando il valore originale di x.</span><span class="sxs-lookup"><span data-stu-id="9c41a-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="9c41a-129">Di seguito è riportato un esempio di utilizzo dell'attributo flat:</span><span class="sxs-lookup"><span data-stu-id="9c41a-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="9c41a-130">In alcuni casi l'uso del ramo o dell'appiattimento degli attributi può generare un errore di compilazione.</span><span class="sxs-lookup"><span data-stu-id="9c41a-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="9c41a-131">L'attributo branch può avere esito negativo se entrambi i lati dell'istruzione if contengono una funzione di sfumatura, ad esempio [**tex2D.**](dx-graphics-hlsl-tex2d.md)</span><span class="sxs-lookup"><span data-stu-id="9c41a-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="9c41a-132">L'attributo flat può avere esito negativo se entrambi i lati dell'istruzione if contengono un'istruzione di accodamento del flusso o qualsiasi altra istruzione con effetti collaterali.</span><span class="sxs-lookup"><span data-stu-id="9c41a-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="9c41a-133">**Un'istruzione if** può anche usare un blocco else facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9c41a-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="9c41a-134">Se **l'espressione if** è true, viene elaborato il codice nel blocco di istruzioni associato all'istruzione if.</span><span class="sxs-lookup"><span data-stu-id="9c41a-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="9c41a-135">In caso contrario, viene elaborato il blocco di istruzioni associato al blocco else facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9c41a-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c41a-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9c41a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c41a-137">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="9c41a-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





