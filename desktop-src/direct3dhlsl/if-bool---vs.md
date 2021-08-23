---
title: if bool - vs
description: Avvia un'operazione if... Altro... endif - e blocco .
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986531"
---
# <a name="if-bool---vs"></a>if bool - vs

Avvia un'operazione if... [else](else---vs.md)... [endif - rispetto al](endif---vs.md) blocco .

## <a name="syntax"></a>Sintassi



| if bool |
|---------|



 

dove bool è un numero di registro bool. Vedere [Registro booleano costante.](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if bool                |      | x    | x    | x     | x    | x     |



 

Se il registro booleano di origine nell'istruzione if è true, viene eseguito il codice racchiuso tra l'istruzione if e il parametro else corrispondente. In caso contrario, il codice racchiuso tra [...](else---vs.md) [endif : vengono eseguite](endif---vs.md) le istruzioni e . Questa istruzione utilizza uno slot di istruzioni.

se i blocchi possono essere annidati.

Un blocco if non può essere in un blocco di ciclo.

## <a name="example"></a>Esempio

Questa istruzione fornisce il controllo di flusso statico condizionale.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else - vs](else---vs.md)
</dt> <dt>

[endif - vs](endif---vs.md)
</dt> </dl>

 

 




