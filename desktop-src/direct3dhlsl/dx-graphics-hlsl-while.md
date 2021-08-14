---
title: Istruzione while
description: Esegue un blocco di istruzioni fino a quando l'espressione condizionale non ha esito negativo.
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
ms.openlocfilehash: a4e9ae7dc0d8280c9b9823d77dcfe5968243a1ddebdaf78e76b03651ee465034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983161"
---
# <a name="while-statement"></a>Istruzione while

Esegue un blocco di istruzioni fino a quando l'espressione condizionale non ha esito negativo.

\[*Attributo* \] while ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.



| Attributo             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Annullare la registrazione del ciclo fino all'arresto dell'esecuzione. Facoltativamente, è possibile specificare il numero massimo di volte in cui il ciclo può essere eseguito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Usare istruzioni di controllo del flusso nello shader compilato. non annullare la registrazione del ciclo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Riduce il tempo di compilazione, ma produce ottimizzazioni meno aggressive. Se si usa questo attributo, il compilatore non annulla la registrazione dei cicli.<br/> Questo attributo influisce solo sulle destinazioni del modello shader che supportano [le istruzioni di](dx-graphics-hlsl-break.md) interruzione. Questo attributo è disponibile nel modello di shader [rispetto \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e nel [modello shader 3](dx-graphics-hlsl-sm3.md) e versioni successive. È particolarmente utile nel modello [shader 4 e](dx-graphics-hlsl-sm4.md) versioni successive quando il compilatore compila i cicli. Il compilatore simula i cicli per impostazione predefinita per valutare se è possibile annullarne la registrazione. Se non si vuole che il compilatore srotoli i cicli, usare questo attributo per ridurre il tempo di compilazione.<br/> |
| consenti \_ condizione \_ uav | Consente a una condizione di terminazione del ciclo compute shader di basarsi su una lettura UAV. Il ciclo non deve contenere oggetti intrinseci di sincronizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

Espressione [condizionale](dx-graphics-hlsl-expressions.md). Se l'espressione restituisce true, viene eseguito il blocco di istruzioni. Il ciclo termina quando l'espressione restituisce false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Flow Controllo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





