---
title: Istruzione for
description: Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- per l'istruzione HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117005"
---
# <a name="for-statement"></a>Istruzione for

Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*Attributo* \] per ( *inizializzatore; Condizionale Iterator* ) { *blocco di istruzioni*;} |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione. Se non si specifica alcun attributo, il compilatore tenterà innanzitutto di creare una versione con rollup del ciclo e, in caso di esito negativo, oppure se alcune operazioni sarebbero più semplici se il ciclo è stato annullato, verrà eseguito il fallback a una versione non registrata del ciclo.



| Attributo             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll (x)             | Eseguire l'unrolling del ciclo fino a quando non viene arrestata l'esecuzione. È possibile specificare facoltativamente il numero massimo di esecuzioni del ciclo. Non compatibile con l'attributo del **\[ ciclo \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Genera codice che usa il controllo di flusso per eseguire ogni iterazione del ciclo. Non è compatibile con l'attributo **\[ unroll \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.<br/> Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) . Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli. Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback. Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione. <br/> |
| Consenti \_ \_ condizione UAV | Consente a una condizione di terminazione del ciclo compute shader di essere basata su un UAV letto. Il ciclo non deve contenere intrinseci di sincronizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inizializzatore*
</dt> <dd>

Valore iniziale del contatore di cicli.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

[Espressione](dx-graphics-hlsl-expressions.md)condizionale. Se l'espressione condizionale restituisce true, viene eseguito il blocco di istruzioni. Il ciclo termina quando l'espressione restituisce false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iteratore*
</dt> <dd>

Aggiornare il valore del contatore di cicli.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli attributi **\[ unroll \]** e **\[ loop \]** si escludono a vicenda e generano errori del compilatore quando vengono specificati entrambi.

Gli attributi di **\[ \_ \_ condizione \]** **\[ \] fastopt** e Allow UAV vengono ignorati se viene specificato **\[ unroll \]** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





