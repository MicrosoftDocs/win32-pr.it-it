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
# <a name="switch-statement"></a>Istruzione switch

Trasferire il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Attributo* \] Switch ( *selector* ) {case 0: { *StatementBlock*;}   interruzione   caso 1: { *StatementBlock*;}   interruzione   caso n: { *StatementBlock*;}   interruzione   impostazione predefinita: { *StatementBlock*;}   interruzione |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione. Se non si specifica alcun attributo, il compilatore può utilizzare un commutire hardware o creare una serie di istruzioni **if** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>rendere bidimensionale</td>
<td>Compilare l'istruzione come una serie di istruzioni <strong>if</strong> , ciascuna con l'attributo <strong>Flat</strong> .</td>
</tr>
<tr class="even">
<td>ramo</td>
<td>Compilare l'istruzione come una serie di istruzioni <strong>if</strong> ognuna con l'attributo <strong>Branch</strong> .
<blockquote>
[!Note]<br />
Quando si usa il modello di <a href="dx-graphics-hlsl-sm2.md">shader 2. x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader 3,0</a>, ogni volta che si usa la creazione di rami dinamici si utilizzano le risorse. Quindi, se si usa una diramazione dinamica eccessivamente quando si hanno come destinazione questi profili, è possibile ricevere errori di compilazione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Forzare un'istruzione switch nell'hardware.
<blockquote>
[!Note]<br />
Richiede l'hardware a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">livello di funzionalità</a> 10_0 o versione successiva.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>chiamare</td>
<td>I corpi dei singoli case nel Commuter verranno spostati in subroutine hardware e l'opzione sarà una serie di chiamate di subroutine.
<blockquote>
[!Note]<br />
Richiede l'hardware a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">livello di funzionalità</a> 10_0 o versione successiva.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selettore*
</dt> <dd>

Variabile. Le istruzioni case racchiuse tra parentesi graffe controllano ciascuna variabile per verificare se il SwitchValue corrisponde al CaseValue specifico.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Commenti


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



Equivale a:


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



Ecco gli esempi di utilizzo di forcecase e degli attributi del controllo del flusso di chiamate:


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

