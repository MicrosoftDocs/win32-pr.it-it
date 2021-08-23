---
title: break_comp - vs
description: Interrompere in modo condizionale il ciclo corrente all'endloop più vicino , rispetto a endrep o endrep, rispetto a
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a02bf34844918255086b318d9a13feeabbd6e75bdecca03684adaba70b420626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626561"
---
# <a name="break_comp---vs"></a>break \_ comp - vs

Interrompere in modo condizionale il ciclo corrente [all'endloop più](endloop---vs.md) vicino , rispetto a [endrep o endrep, rispetto a](endrep---vs.md).

## <a name="syntax"></a>Sintassi



| break \_ comp src0, src1 |
|------------------------|



 

Dove:

-   \_comp è un confronto tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_Gt   | Maggiore di          |
    | \_Tenente   | Minore di             |
    | \_Ge   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_Eq   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. Replicare lo swizzle è necessario per selezionare un singolo componente.
-   src1 è un registro di origine. Replicare lo swizzle è necessario per selezionare un singolo componente.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| interrompere \_ la compilazione            |      |      | x    | x     | x    | x     |



 

Quando il confronto è true, esce dal ciclo corrente, come illustrato.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




