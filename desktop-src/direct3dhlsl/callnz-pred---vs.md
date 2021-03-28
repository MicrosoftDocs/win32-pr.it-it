---
title: callnz Predator-vs
description: Chiamare se non zero, con un predicato. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046084"
---
# <a name="callnz-pred---vs"></a>callnz Predator-vs

Chiamare se non zero, con un predicato. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] P0. x|y|z|w |
|----------------------------------|



 

dove:

-   l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.
-   \[!\] modificatore negazioni facoltativo.
-   P0 è il [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} è la replica obbligatoria swizzle su P0.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| predazione callnz            |      |      | x    | x     | x    | x     |



 

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

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




