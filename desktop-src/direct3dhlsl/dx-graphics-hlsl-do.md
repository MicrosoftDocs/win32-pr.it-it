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
# <a name="do-statement"></a>Istruzione do

Eseguire continuamente una serie di istruzioni fino a quando l'espressione condizionale non riesce.



|                                                                     |
|---------------------------------------------------------------------|
| \[*Attributo* \] do { *Block Statement*;} while ( *condizionale* ); |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.



| Attributo | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.<br/> Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) . Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli. Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback. Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

[Espressione](dx-graphics-hlsl-expressions.md)condizionale. Il blocco di istruzioni viene eseguito prima della valutazione dell'espressione. Il ciclo viene terminato quando l'espressione restituisce false.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





