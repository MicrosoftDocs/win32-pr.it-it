---
title: callnz prede-PS
description: Chiamare con un predicato, se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956071"
---
# <a name="callnz-pred---ps"></a>callnz prede-PS

Chiamare con un predicato, se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] P0. x|y|z|w |
|----------------------------------|



 

Dove:

-   dove l \# è un' [etichetta-PS](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.
-   \[!\] modificatore negazioni facoltativo.
-   P0 è il registro predicato. Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} è la replica obbligatoria swizzle su P0.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| predazione callnz           |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




