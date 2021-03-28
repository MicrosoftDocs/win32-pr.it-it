---
title: Istruzione switch (Urlmon. h)
description: Trasferire il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Istruzione switch HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761921"
---
# <a name="switch-statement"></a><span data-ttu-id="b4ac7-104">Istruzione switch</span><span class="sxs-lookup"><span data-stu-id="b4ac7-104">switch Statement</span></span>

<span data-ttu-id="b4ac7-105">Trasferire il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ac7-106">\[*Attributo* \] Switch ( *selector* ) {case 0: { *StatementBlock*;}   interruzione   caso 1: { *StatementBlock*;}   interruzione   caso n: { *StatementBlock*;}   interruzione   impostazione predefinita: { *StatementBlock*;}   interruzione</span><span class="sxs-lookup"><span data-stu-id="b4ac7-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="b4ac7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4ac7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ac7-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="b4ac7-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac7-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="b4ac7-110">Se non si specifica alcun attributo, il compilatore può utilizzare un commutire hardware o creare una serie di istruzioni **if** .</span><span class="sxs-lookup"><span data-stu-id="b4ac7-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4ac7-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="b4ac7-111">Attribute</span></span></th>
<th><span data-ttu-id="b4ac7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4ac7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4ac7-113">rendere bidimensionale</span><span class="sxs-lookup"><span data-stu-id="b4ac7-113">flatten</span></span></td>
<td><span data-ttu-id="b4ac7-114">Compilare l'istruzione come una serie di istruzioni <strong>if</strong> , ciascuna con l'attributo <strong>Flat</strong> .</span><span class="sxs-lookup"><span data-stu-id="b4ac7-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4ac7-115">ramo</span><span class="sxs-lookup"><span data-stu-id="b4ac7-115">branch</span></span></td>
<td><span data-ttu-id="b4ac7-116">Compilare l'istruzione come una serie di istruzioni <strong>if</strong> ognuna con l'attributo <strong>Branch</strong> .</span><span class="sxs-lookup"><span data-stu-id="b4ac7-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4ac7-117">Quando si usa il modello di <a href="dx-graphics-hlsl-sm2.md">shader 2. x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader 3,0</a>, ogni volta che si usa la creazione di rami dinamici si utilizzano le risorse.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="b4ac7-118">Quindi, se si usa una diramazione dinamica eccessivamente quando si hanno come destinazione questi profili, è possibile ricevere errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4ac7-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="b4ac7-119">forcecase</span></span></td>
<td><span data-ttu-id="b4ac7-120">Forzare un'istruzione switch nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4ac7-121">Richiede l'hardware a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">livello di funzionalità</a> 10_0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4ac7-122">chiamare</span><span class="sxs-lookup"><span data-stu-id="b4ac7-122">call</span></span></td>
<td><span data-ttu-id="b4ac7-123">I corpi dei singoli case nel Commuter verranno spostati in subroutine hardware e l'opzione sarà una serie di chiamate di subroutine.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4ac7-124">Richiede l'hardware a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">livello di funzionalità</a> 10_0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="b4ac7-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selettore*</span><span class="sxs-lookup"><span data-stu-id="b4ac7-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac7-126">Variabile.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-126">A variable.</span></span> <span data-ttu-id="b4ac7-127">Le istruzioni case racchiuse tra parentesi graffe controllano ciascuna variabile per verificare se il SwitchValue corrisponde al CaseValue specifico.</span><span class="sxs-lookup"><span data-stu-id="b4ac7-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="b4ac7-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="b4ac7-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="b4ac7-129">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="b4ac7-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4ac7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4ac7-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="b4ac7-131">Equivale a:</span><span class="sxs-lookup"><span data-stu-id="b4ac7-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="b4ac7-132">Ecco gli esempi di utilizzo di forcecase e degli attributi del controllo del flusso di chiamate:</span><span class="sxs-lookup"><span data-stu-id="b4ac7-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="b4ac7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4ac7-133">Requirements</span></span>



| <span data-ttu-id="b4ac7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4ac7-134">Requirement</span></span> | <span data-ttu-id="b4ac7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b4ac7-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ac7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4ac7-136">Header</span></span><br/> | <dl> <span data-ttu-id="b4ac7-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ac7-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ac7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4ac7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ac7-139">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="b4ac7-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

