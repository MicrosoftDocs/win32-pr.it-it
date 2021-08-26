---
title: Istruzione for
description: Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- Istruzione for HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 001683c612aefb56d8257977ce7efe99d162a0919d39c678ee4074128a019a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068191"
---
# <a name="for-statement"></a>Istruzione for

Esegue in modo iterativo una serie di istruzioni, in base alla valutazione dell'espressione condizionale.

\[*Attributo* \] for ( *Inizializzatore; Condizionale; Iterator* ) { *Blocco di istruzioni*; }



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione. Quando non viene specificato alcun attributo, il compilatore tenterà prima di tutto di generare una versione di cui è stato eseguito il roll-roll e, in caso di esito negativo, o se alcune operazioni sarebbero più semplici se il ciclo fosse stato scollegato, verrà eseguito il fall back a una versione di cui non è stata eseguita la registrazione.



| Attributo             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| annullamento della registrazione(x)             | Annullare la registrazione del ciclo fino all'arresto dell'esecuzione. Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo deve essere eseguito. Non compatibile con **\[ l'attributo del \]** ciclo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Generare codice che usa il controllo di flusso per eseguire ogni iterazione del ciclo. Non compatibile con **\[ l'attributo di \] annullamento** della registrazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.<br/> Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione. Questo attributo è disponibile nel modello shader [rispetto a \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel modello [shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli. Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione. Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione. <br/> |
| consenti \_ condizione \_ uav | Consente a una condizione di terminazione del ciclo compute shader di basarsi su una lettura UAV. Il ciclo non deve contenere intrinseci di sincronizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inizializzatore*
</dt> <dd>

Valore iniziale del contatore di cicli.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

Espressione [condizionale](dx-graphics-hlsl-expressions.md). Se l'espressione condizionale restituisce true, viene eseguito il blocco di istruzioni. Il ciclo termina quando l'espressione restituisce false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iteratore*
</dt> <dd>

Aggiornare il valore del contatore del ciclo.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli **\[ attributi \] unroll** **\[ e loop \]** si escludono a vicenda e generano errori del compilatore quando vengono specificati entrambi.

Gli **\[ attributi \] della condizione fastopt** **\[ e allow \_ uav \_ \]** vengono ignorati se **\[ si specifica unroll. \]**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Flow Controllo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





