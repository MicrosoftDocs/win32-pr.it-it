---
title: Istruzione if
description: Eseguire in modo condizionale una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Istruzione If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046242"
---
# <a name="if-statement"></a><span data-ttu-id="c40b4-104">Istruzione if</span><span class="sxs-lookup"><span data-stu-id="c40b4-104">if Statement</span></span>

<span data-ttu-id="c40b4-105">Eseguire in modo condizionale una serie di istruzioni, in base alla valutazione dell'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="c40b4-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                               |
|---------------------------------------------------------------|
| <span data-ttu-id="c40b4-106">\[*Attributo* \] if ( *Conditional* ) { *Block Statement*;}</span><span class="sxs-lookup"><span data-stu-id="c40b4-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c40b4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c40b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c40b4-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="c40b4-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="c40b4-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="c40b4-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c40b4-110">Attributo</span><span class="sxs-lookup"><span data-stu-id="c40b4-110">Attribute</span></span></th>
<th><span data-ttu-id="c40b4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c40b4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c40b4-112">ramo</span><span class="sxs-lookup"><span data-stu-id="c40b4-112">branch</span></span></td>
<td><span data-ttu-id="c40b4-113">Valutare solo un lato dell'istruzione if a seconda della condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c40b4-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c40b4-114">Quando si usa il modello di <a href="dx-graphics-hlsl-sm2.md">shader 2. x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader 3,0</a>, ogni volta che si usa la creazione di rami dinamici si utilizzano le risorse.</span><span class="sxs-lookup"><span data-stu-id="c40b4-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="c40b4-115">Quindi, se si usa una diramazione dinamica eccessivamente quando si hanno come destinazione questi profili, è possibile ricevere errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="c40b4-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c40b4-116">rendere bidimensionale</span><span class="sxs-lookup"><span data-stu-id="c40b4-116">flatten</span></span></td>
<td><span data-ttu-id="c40b4-117">Valutare entrambi i lati dell'istruzione if e scegliere tra i due valori risultanti.</span><span class="sxs-lookup"><span data-stu-id="c40b4-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c40b4-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*</span><span class="sxs-lookup"><span data-stu-id="c40b4-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="c40b4-119">[Espressione](dx-graphics-hlsl-expressions.md)condizionale.</span><span class="sxs-lookup"><span data-stu-id="c40b4-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="c40b4-120">L'espressione viene valutata e, se true, viene eseguito il blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="c40b4-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="c40b4-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="c40b4-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="c40b4-122">Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="c40b4-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c40b4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c40b4-123">Remarks</span></span>

<span data-ttu-id="c40b4-124">Quando il compilatore usa il metodo Branch per la compilazione di un'istruzione if, verrà generato codice che valuterà solo un lato dell'istruzione if a seconda della condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c40b4-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="c40b4-125">Ad esempio, nell'istruzione if:</span><span class="sxs-lookup"><span data-stu-id="c40b4-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="c40b4-126">L'istruzione **if** ha un blocco Else implicito, equivalente a x = x.</span><span class="sxs-lookup"><span data-stu-id="c40b4-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="c40b4-127">Poiché è stato indicato al compilatore di usare il metodo Branch con l'attributo Branch precedente, il codice compilato valuterà x ed eseguirà solo il lato che deve essere eseguito. Se x è zero, verrà eseguito il lato **else** e se è diverso da zero, verrà eseguito il lato **then** .</span><span class="sxs-lookup"><span data-stu-id="c40b4-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="c40b4-128">Viceversa, se viene usato l'attributo **Flat** , il codice compilato valuterà entrambi i lati dell'istruzione **if** e sceglierà tra i due valori risultanti usando il valore originale di x.</span><span class="sxs-lookup"><span data-stu-id="c40b4-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="c40b4-129">Di seguito è riportato un esempio di utilizzo dell'attributo Flat:</span><span class="sxs-lookup"><span data-stu-id="c40b4-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="c40b4-130">In alcuni casi, l'utilizzo degli attributi Branch o flat può generare un errore di compilazione.</span><span class="sxs-lookup"><span data-stu-id="c40b4-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="c40b4-131">L'attributo Branch può non riuscire se uno dei lati dell'istruzione if contiene una funzione Gradient, ad esempio [**tex2D**](dx-graphics-hlsl-tex2d.md).</span><span class="sxs-lookup"><span data-stu-id="c40b4-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="c40b4-132">L'attributo flat può non riuscire se entrambi i lati dell'istruzione If contengono un'istruzione di Accodamento del flusso o qualsiasi altra istruzione con effetti collaterali.</span><span class="sxs-lookup"><span data-stu-id="c40b4-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="c40b4-133">Un'istruzione **if** può inoltre utilizzare un blocco else facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c40b4-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="c40b4-134">Se l'espressione **if** è true, il codice nel blocco di istruzioni associato all'istruzione if viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="c40b4-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="c40b4-135">In caso contrario, il blocco di istruzioni associato al blocco else facoltativo viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="c40b4-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c40b4-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c40b4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40b4-137">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="c40b4-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





