---
title: callnz pred - vs
description: Chiamare se diverso da zero, con un predicato. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predication usa un valore booleano per determinare se di non eseguire l'istruzione.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287025"
---
# <a name="callnz-pred---vs"></a>callnz pred - vs

Chiamare se diverso da zero, con un predicato. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predication usa un valore booleano per determinare se di non eseguire l'istruzione.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

dove:

-   l \# è [un'etichetta e contrassegna](label---vs.md) l'inizio della subroutine da chiamare.
-   \[!\] è un modificatore di negazione facoltativo.
-   p0 è il [registro predicato.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   {x \| y \| z \| w} è lo swizzle di replica richiesto in p0.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz pred            |      |      | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Questa istruzione usa uno slot di istruzioni vertex shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




