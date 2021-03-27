---
title: break_comp-vs
description: Suddividere in modo condizionale il ciclo corrente nel EndLoop-vs o endrep-vs più vicino.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857778"
---
# <a name="break_comp---vs"></a>Interrompi \_ comp-vs

Suddividere in modo condizionale il ciclo corrente nel [EndLoop-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)più vicino.

## <a name="syntax"></a>Sintassi



| Interrompi \_ comp src0, src1 |
|------------------------|



 

Dove:

-   \_comp è un confronto tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_gt   | Maggiore di          |
    | \_lt   | Minore di             |
    | \_GE   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_EQ   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. Per selezionare un singolo componente è necessario replicare Swizzle.
-   src1 è un registro di origine. Per selezionare un singolo componente è necessario replicare Swizzle.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Interrompi \_ comp            |      |      | x    | x     | x    | x     |



 

Quando il confronto è true, viene interrotto dal ciclo corrente, come illustrato.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




