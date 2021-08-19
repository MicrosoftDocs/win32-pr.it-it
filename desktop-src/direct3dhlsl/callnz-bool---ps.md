---
title: callnz bool - ps
description: Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. | callnz bool - ps
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516627"
---
# <a name="callnz-bool---ps"></a>callnz bool - ps

Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

Dove:

-   l \# è [un'etichetta: ps](label---ps.md) contrassegna l'inizio della subroutine da chiamare.
-   \[!\] è un modificatore di negazione facoltativo.
-   b \# identifica un registro [booleano costante.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




