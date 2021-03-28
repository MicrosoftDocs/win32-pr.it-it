---
title: Istruzione while
description: Esegue un blocco di istruzioni fino a quando l'espressione condizionale non riesce.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- Istruzione while HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 190d5474b5e016b41426db67a0c96d98787f79ff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045608"
---
# <a name="while-statement"></a>Istruzione while

Esegue un blocco di istruzioni fino a quando l'espressione condizionale non riesce.



|                                                                  |
|------------------------------------------------------------------|
| \[*Attributo* \] while ( *Conditional* ) { *Block Statement*;} |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.



| Attributo             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll (x)             | Eseguire l'unrolling del ciclo fino a quando non viene arrestata l'esecuzione. Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo può essere eseguito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Usare le istruzioni di controllo di flusso nello shader compilato; non eseguire l'unrolling del ciclo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Riduce il tempo di compilazione ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non eseguirà l'unrolling dei cicli.<br/> Questo attributo ha effetto solo sulle destinazioni del modello dello shader che supportano le istruzioni di [interruzioni](dx-graphics-hlsl-break.md) . Questo attributo è disponibile nel modello shader [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [Modello Shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel [Modello Shader 4](dx-graphics-hlsl-sm4.md) e versioni successive quando il compilatore compila i cicli. Per impostazione predefinita, il compilatore simula i cicli per valutare se è possibile eseguirne il rollback. Se non si desidera che il compilatore esegua l'unrolling dei cicli, utilizzare questo attributo per ridurre il tempo di compilazione.<br/> |
| Consenti \_ \_ condizione UAV | Consente a una condizione di terminazione del ciclo compute shader di essere basata su un UAV letto. Il ciclo non deve contenere intrinseci di sincronizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

[Espressione](dx-graphics-hlsl-expressions.md)condizionale. Se l'espressione restituisce true, viene eseguito il blocco di istruzioni. Il ciclo termina quando l'espressione restituisce false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





