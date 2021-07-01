---
title: Istruzione switch (Urlmon.h)
description: Trasferire il controllo in un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.
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
ms.openlocfilehash: 4af131ca3a126cd6f1fd54160418bfbe70cc9cce
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119086"
---
# <a name="switch-statement"></a><span data-ttu-id="328c3-104">Istruzione switch</span><span class="sxs-lookup"><span data-stu-id="328c3-104">switch Statement</span></span>

<span data-ttu-id="328c3-105">Trasferire il controllo in un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.</span><span class="sxs-lookup"><span data-stu-id="328c3-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>


<span data-ttu-id="328c3-106">\[*Attributo* \] switch( *Selector* ) { case 0: { *StatementBlock*; }   break;   case 1: { *StatementBlock*; }   break;   case n: { *StatementBlock*; }   break;   default: { *StatementBlock*; }   break;</span><span class="sxs-lookup"><span data-stu-id="328c3-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span>



 

## <a name="parameters"></a><span data-ttu-id="328c3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="328c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328c3-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*</span><span class="sxs-lookup"><span data-stu-id="328c3-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="328c3-109">Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="328c3-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="328c3-110">Quando non viene specificato alcun attributo, il compilatore può usare un'opzione hardware o generare una serie di **istruzioni** if.</span><span class="sxs-lookup"><span data-stu-id="328c3-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="328c3-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="328c3-111">Attribute</span></span></th>
<th><span data-ttu-id="328c3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="328c3-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="328c3-113">rendere bidimensionale</span><span class="sxs-lookup"><span data-stu-id="328c3-113">flatten</span></span></td>
<td><span data-ttu-id="328c3-114">Compilare l'istruzione come una serie di istruzioni <strong>if,</strong> ognuna con <strong>l'attributo flatten.</strong></span><span class="sxs-lookup"><span data-stu-id="328c3-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="328c3-115">ramo</span><span class="sxs-lookup"><span data-stu-id="328c3-115">branch</span></span></td>
<td><span data-ttu-id="328c3-116">Compilare l'istruzione come una serie <strong>di istruzioni if</strong> ognuna con l'attributo <strong>branch.</strong></span><span class="sxs-lookup"><span data-stu-id="328c3-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="328c3-117">Quando si usa <a href="dx-graphics-hlsl-sm2.md">il modello shader 2.x</a> o il modello <a href="dx-graphics-hlsl-sm3.md">shader 3.0,</a>ogni volta che si usa la diramazione dinamica si usano le risorse.</span><span class="sxs-lookup"><span data-stu-id="328c3-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="328c3-118">Pertanto, se si usa la diramazione dinamica in modo eccessivo quando si usano questi profili come destinazione, è possibile ricevere errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="328c3-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="328c3-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="328c3-119">forcecase</span></span></td>
<td><span data-ttu-id="328c3-120">Forzare un'istruzione switch nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="328c3-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="328c3-121">Richiede <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware con livello</a> di funzionalità 10_0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="328c3-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="328c3-122">chiamare</span><span class="sxs-lookup"><span data-stu-id="328c3-122">call</span></span></td>
<td><span data-ttu-id="328c3-123">I corpi dei singoli case nel commutatore verranno spostati in subroutine hardware e il commutatore sarà una serie di chiamate subroutine.</span><span class="sxs-lookup"><span data-stu-id="328c3-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="328c3-124">Richiede <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware con livello</a> di funzionalità 10_0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="328c3-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="328c3-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selettore*</span><span class="sxs-lookup"><span data-stu-id="328c3-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="328c3-126">Variabile.</span><span class="sxs-lookup"><span data-stu-id="328c3-126">A variable.</span></span> <span data-ttu-id="328c3-127">Le istruzioni case all'interno delle parentesi graffe controllano ognuna questa variabile per verificare se SwitchValue corrisponde al caseValue specifico.</span><span class="sxs-lookup"><span data-stu-id="328c3-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="328c3-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*Blocco di istruzioni*</span><span class="sxs-lookup"><span data-stu-id="328c3-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="328c3-129">Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="328c3-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="328c3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="328c3-130">Remarks</span></span>


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



<span data-ttu-id="328c3-131">Equivale a:</span><span class="sxs-lookup"><span data-stu-id="328c3-131">Is equivalent to:</span></span>


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



<span data-ttu-id="328c3-132">Ecco alcuni esempi di utilizzo degli attributi forcecase e call flow control:</span><span class="sxs-lookup"><span data-stu-id="328c3-132">Here are example usages of forcecase and call flow control attributes:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="328c3-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="328c3-133">Requirements</span></span>



| <span data-ttu-id="328c3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="328c3-134">Requirement</span></span> | <span data-ttu-id="328c3-135">Valore</span><span class="sxs-lookup"><span data-stu-id="328c3-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="328c3-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="328c3-136">Header</span></span><br/> | <dl> <span data-ttu-id="328c3-137"><dt>Urlmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="328c3-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328c3-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="328c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328c3-139">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="328c3-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

