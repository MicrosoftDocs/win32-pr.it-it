---
title: Istruzione switch (Urlmon.h)
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
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477487"
---
# <a name="switch-statement"></a>Istruzione switch

Trasferire il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.


\[*Attributo* \] switch( *Selettore* ) { case 0 : { *StatementBlock*; }   interrompi;   case 1: { *StatementBlock*; }   interrompi;   case n: { *StatementBlock*; }   interrompi;   default: { *StatementBlock*; }   interrompi;



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione. Quando non viene specificato alcun attributo, il compilatore può usare un'opzione hardware o generare una serie **di istruzioni if.**




| Attributo | Descrizione | 
|-----------|-------------|
| rendere bidimensionale | Compilare l'istruzione come una serie <strong>di istruzioni if,</strong> ognuna con l'attributo <strong>flatten.</strong> | 
| ramo | Compilare l'istruzione come una serie di <strong>istruzioni if</strong> ognuna con l'attributo <strong>branch.</strong><blockquote>[!Note]<br />Quando si usa <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0,</a>ogni volta che si usa la creazione dinamica di rami si usano le risorse. Pertanto, se si usa la diramazione dinamica in modo eccessivo quando si usano questi profili come destinazione, è possibile ricevere errori di compilazione.</blockquote><br /> | 
| forcecase | Forzare un'istruzione switch nell'hardware.<blockquote>[!Note]<br />Richiede <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware di livello</a> funzionalità 10_0 o versione successiva.</blockquote><br /> | 
| chiamare | I corpi dei singoli case nel commutatore verranno spostati in subroutine hardware e il commutatore sarà una serie di chiamate di subroutine.<blockquote>[!Note]<br />Richiede <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware di livello</a> funzionalità 10_0 o versione successiva.</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selettore*
</dt> <dd>

Variabile. Le istruzioni case all'interno delle parentesi graffe controllano ognuna questa variabile per verificare se SwitchValue corrisponde al caseValue specifico.

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



Ecco alcuni esempi di utilizzo degli attributi forcecase e call flow control:


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



| Requisito | valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Urlmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Flow Controllo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

