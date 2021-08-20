---
title: sgn - vs
description: Calcola il segno dell'input.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1a4994c807ff1df99016aad734edf71e5e1ce6efe59fd53a4fb9bb3ee91a4b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671681"
---
# <a name="sgn---vs"></a>sgn - vs

Calcola il segno dell'input.

## <a name="syntax"></a>Sintassi



| sgn dst, src0, src1, src2 |
|---------------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro temporaneo che contiene risultati intermedi. Dopo l'esecuzione, il contenuto non è definito.
-   src2 è un registro temporaneo che contiene risultati intermedi. Dopo l'esecuzione, il contenuto non è definito.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Sgn                    |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 e src2 devono essere [registri](dx9-graphics-reference-asm-vs-registers-temporary.md)temporanei diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




