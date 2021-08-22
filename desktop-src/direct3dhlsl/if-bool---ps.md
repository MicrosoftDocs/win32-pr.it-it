---
title: if bool - ps
description: Inizio di un blocco if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457511"
---
# <a name="if-bool---ps"></a>if bool - ps

Inizio di un blocco if.

## <a name="syntax"></a>Sintassi



| if bool |
|---------|



 

Dove:

-   bool è un numero di registro bool (booleano). Vedere [Registro booleano costante.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Se il registro booleano di origine nell'istruzione if è true, viene eseguito il codice racchiuso tra l'istruzione if e [l'endif corrispondente - ps](endif---ps.md) o [else - ps.](else---ps.md) In caso contrario, il codice racchiuso tra else - ps... endif: vengono eseguite le istruzioni ps. Questa istruzione utilizza uno slot di istruzioni.

Un blocco if può essere annidato.

Un blocco if non può essere in un blocco di ciclo.

Un blocco if può essere seguito da un blocco di istruzioni e/o da un'istruzione [else - ps](else---ps.md) e/o [endif - ps.](endif---ps.md)

## <a name="example"></a>Esempio

Questa istruzione fornisce il controllo di flusso statico condizionale.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else - ps](else---ps.md)
</dt> <dt>

[endif - ps](endif---ps.md)
</dt> </dl>

 

 




