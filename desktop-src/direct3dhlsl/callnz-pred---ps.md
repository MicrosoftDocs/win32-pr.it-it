---
title: callnz pred - ps
description: Chiamare con un predicato, se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predication usa un valore booleano per determinare se di non eseguire l'istruzione.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f56699a4853b7012401529ecfad6fbfb0006e21990a99a2fe5631faebd57674d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983291"
---
# <a name="callnz-pred---ps"></a>callnz pred - ps

Chiamare con un predicato, se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predication usa un valore booleano per determinare se di non eseguire l'istruzione.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

Dove:

-   dove l \# è [un'etichetta, ps](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.
-   \[!\] è un modificatore di negazione facoltativo.
-   p0 è il registro del predicato. Vedere [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} è lo swizzle di replica richiesto in p0.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz pred           |      |      |      |      |      | x    | x     | x    | x     |



 

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

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




