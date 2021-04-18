---
title: callnz bool-vs
description: Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995762"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.

## <a name="syntax"></a>Sintassi



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

dove:

-   dove l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.
-   \[!\] è il modificatore booleano NOT facoltativo.
-   b \# identifica un [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| bool callnz            |      | x    | x    | x     | x    | x     |



 

Questa istruzione esegue le operazioni seguenti:


```
if (specified boolean register is not zero)
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

 

 




