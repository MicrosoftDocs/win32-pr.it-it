---
title: Se bool-vs
description: Avvia un'if... altrimenti... il blocco endif-vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046058"
---
# <a name="if-bool---vs"></a>Se bool-vs

Avvia un'if... [altrimenti](else---vs.md)... il blocco [endif-vs](endif---vs.md) .

## <a name="syntax"></a>Sintassi



| Se bool |
|---------|



 

dove bool è un numero di registro bool. Vedere [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Se bool                |      | x    | x    | x     | x    | x     |



 

Se il registro booleano di origine nell'istruzione If è true, viene eseguito il codice racchiuso dall'istruzione if e l'altro corrispondente. In caso contrario, il codice racchiuso da [else](else---vs.md)... vengono eseguite le istruzioni [endif-vs](endif---vs.md) . Questa istruzione usa uno slot di istruzione.

Se i blocchi possono essere annidati.

Un blocco If non può risiedere in un blocco di ciclo.

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

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else-vs](else---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 




