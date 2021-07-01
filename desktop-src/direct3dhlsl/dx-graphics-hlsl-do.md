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
# <a name="do-statement"></a>Istruzione do

Eseguire una serie di istruzioni in modo continuo fino a quando l'espressione condizionale non ha esito negativo.

\[*Attributo* \] do { *Statement Block*; } while( *Conditional* );



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.



| Attributo | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.<br/> Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione. Questo attributo è disponibile nel modello shader [rispetto a \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel modello [shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli. Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione. Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

Espressione [condizionale](dx-graphics-hlsl-expressions.md). Il blocco di istruzioni viene eseguito prima della valutazione dell'espressione. Il ciclo viene terminato quando l'espressione restituisce false.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





