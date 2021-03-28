---
title: break_comp-PS
description: Suddividere il ciclo corrente nel EndLoop-PS o endrep-PS più vicino in base a un confronto per componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117201"
---
# <a name="break_comp---ps"></a>Interrompi \_ comp-PS

Suddividere il ciclo corrente nel [EndLoop-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)più vicino in base a un confronto per componente.

## <a name="syntax"></a>Sintassi



| Interrompi \_ comp src0, src1 |
|------------------------|



 

Dove:

-   \_comp è un confronto scalare (o singolo) tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_gt   | Maggiore di          |
    | \_lt   | Minore di             |
    | \_GE   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_EQ   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. La replica swizzle è obbligatoria se si seleziona un singolo componente.
-   src1 è un registro di origine. La replica swizzle è obbligatoria se si seleziona un singolo componente.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Interrompi \_ comp           |      |      |      |      |      | x    | x     | x    | x     |



 

Quando il confronto è true, viene interrotto dal ciclo corrente, come illustrato.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




